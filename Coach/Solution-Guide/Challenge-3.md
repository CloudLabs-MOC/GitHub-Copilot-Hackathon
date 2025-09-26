# Desafío 3: Implementar la Aplicación en Azure - Guía de Soluciones

## Accediendo al Portal de Azure

1. Para acceder al portal de Azure, abra una ventana privada o de incógnito en su navegador y navegue hasta **[Portal de Azure](https://portal.azure.com)**.

1. En la pestaña **Iniciar sesión en Microsoft Azure**, verá una pantalla de inicio de sesión. Ingrese el siguiente correo electrónico o nombre de usuario y luego haga clic en **Siguiente**.
   * Correo electrónico/Nombre de usuario: <inject key="AzureAdUserEmail"></inject>
        
1. Ahora ingrese la siguiente contraseña y haga clic en **Iniciar sesión**.
   * Contraseña: <inject key="AzureAdUserPassword"></inject>
     
1. Si ve la ventana emergente **¿Desea permanecer conectado?**, haga clic en No.

1. Si ve la ventana emergente **¡Tiene recomendaciones gratuitas de Azure Advisor!**, cierre la ventana para continuar con el laboratorio.

1. Si aparece una ventana emergente **Bienvenido a Microsoft Azure**, haga clic en **Cancelar** para omitir el recorrido.
   
1. Ahora verá el Panel de Azure Portal. Haga clic en **Grupos de recursos** en el panel Navegar para ver los grupos de recursos.
  
1. Confirme que tiene un grupo de recursos **GitHub-Copilot-Challenges** presente, tal como se muestra en la siguiente captura de pantalla. Debe usar el grupo de recursos **GitHub-Copilot-Challenges** a lo largo de este desafío.

## Tarea 1: Desarrollar una Plantilla ARM para implementar una aplicación en Azure

En esta tarea, generará una plantilla ARM para desplegar una aplicación web en Azure mediante Azure App Services y definirá los recursos necesarios.

1. En la ventana GitHub Copilot Chat, pida a GitHub Copilot que genere una plantilla ARM para implementar una aplicación web con los recursos necesarios definidos (plan de precios básico/gratuito, autenticación básica habilitada y configuración de GitHub Actions deshabilitada).

   ![](../../media/challenge3-generate-arm.png)

1. GitHub Copilot generará una plantilla ARM básica (que podría no ser precisa). Copie y pegue la plantilla ARM en un nuevo archivo llamado **deploy.json** y utilice GitHub Copilot Suggestions y Chat para refactorizar la plantilla según sus especificaciones. Su plantilla ARM debe parecerse a la que se muestra a continuación, con los recursos y las especificaciones.

   ```
   {
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "subscriptionId": {
            "type": "String"
        },
        "resourceGroupName": {
            "type": "String"
        },
        "name": {
            "type": "String"
        },
        "location": {
            "type": "String"
        },
        "hostingPlanName": {
            "type": "String"
        }
    },
    "variables": {},
    "resources": [
        {
            "type": "Microsoft.Web/sites",
            "apiVersion": "2018-11-01",
            "name": "[parameters('name')]",
            "location": "[parameters('location')]",
            "dependsOn": [
                "[concat('Microsoft.Web/serverfarms/', parameters('hostingPlanName'))]"
            ],
            "tags": {},
            "properties": {
                "name": "[parameters('name')]",
                "siteConfig": {
                    "appSettings": [],
                    "metadata": [
                        {
                            "name": "CURRENT_STACK",
                            "value": "dotnet"
                        }
                    ],
                    "phpVersion": "OFF",
                    "netFrameworkVersion": "v8.0",
                    "alwaysOn": false,
                    "ftpsState": "FtpsOnly"
                },
                "serverFarmId": "[concat('/subscriptions/', parameters('subscriptionId'),'/resourcegroups/', parameters('resourceGroupName'), '/providers/Microsoft.Web/serverfarms/', parameters('hostingPlanName'))]",
                "clientAffinityEnabled": true,
                "virtualNetworkSubnetId": null,
                "httpsOnly": true,
                "publicNetworkAccess": "Enabled"
            },
            "resources": [
                {
                    "type": "Microsoft.Web/sites/basicPublishingCredentialsPolicies",
                    "apiVersion": "2022-09-01",
                    "name": "[concat(parameters('name'), '/scm')]",
                    "dependsOn": [
                        "[resourceId('Microsoft.Web/Sites', parameters('name'))]"
                    ],
                    "properties": {
                        "allow": true
                    }
                },
                {
                    "type": "Microsoft.Web/sites/basicPublishingCredentialsPolicies",
                    "apiVersion": "2022-09-01",
                    "name": "[concat(parameters('name'), '/ftp')]",
                    "dependsOn": [
                        "[resourceId('Microsoft.Web/Sites', parameters('name'))]"
                    ],
                    "properties": {
                        "allow": true
                    }
                }
            ]
        },
        {
            "type": "Microsoft.Web/serverfarms",
            "apiVersion": "2018-11-01",
            "name": "[parameters('hostingPlanName')]",
            "location": "[parameters('location')]",
            "dependsOn": [],
            "tags": {},
            "sku": {
                "Tier": "Basic",
                "Name": "B1"
            },
            "kind": "",
            "properties": {
                "name": "[parameters('hostingPlanName')]",
                "workerSize": "0",
                "workerSizeId": "0",
                "numberOfWorkers": "1",
                "zoneRedundant": false
            }
         }
      ] 
   }
   ```

1. En VS Code, cree un nuevo archivo **deploy.parameters.json** para definir los parámetros de su archivo *deploy.json*.

   ```
   {
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "subscriptionId": {
            "type": "String"
        },
        "resourceGroupName": {
            "type": "String"
        },
        "name": {
            "type": "String"
        },
        "location": {
            "type": "String"
        },
        "hostingPlanName": {
            "type": "String"
        }
     }
   }
   ```

1. En el portal de Azure, busque el servicio **Implementar una plantilla personalizada (Deploy a custom template)**. Utilizará este servicio de Azure para implementar su plantilla ARM personalizada.

   ![](../../media/challenge3-azure-custom.png)

1. En la pestaña Implementación personalizada, haga clic en **Crear su propia plantilla en el editor**.

   ![](../../media/challenge3-custom-deploy.png)

1. En la pestaña Editar plantilla, elimine la plantilla ARM de esqueleto existente, copie y pegue la plantilla ARM recién generada con GitHub Copilot y haga clic en **Guardar**.

   ![](../../media/challenge3-custom-deploy-save.png)

1. Ingrese las especificaciones para desplegar su aplicación web. Asegúrese de implementar la aplicación web en el grupo de recursos existente llamado **GitHub-Copilot-Challenges**.

1. Una vez que haya especificado todos los parámetros, haga clic en **Revisar + crear** y, luego, en **Crear**.

1. Espere a que la implementación se realice correctamente y compruebe que los recursos App Service Plan y Web App Service existan en el grupo de recursos.

   ![](../../media/challenge3-custom-deploy-verify.png)

## Tarea 2: Generar Flujo de Trabajo de GitHub Actions mediante el Centro de Implementación desde la Aplicación Web en el Portal de Azure

En esta tarea, generará un pipeline de flujo de trabajo de GitHub Actions mediante el Centro de Implementación desde la Aplicación Web en el portal de Azure.

1. Navegue hasta su recurso de servicio de aplicación web y, en la configuración de **Implementación (1)**, seleccione **Centro de Implementación (2)**.

   ![](../../media/challenge3-deployment-center.png)

1. Especifique las siguientes configuraciones para generar un archivo YAML de flujo de trabajo de GitHub Action y haga clic en **Guardar** (8):

   * **Origen**: GitHub (1)
   * **Sesión iniciada como**: Su Cuenta de GitHub (2)
   * **Organización**: Su Organización de GitHub ()3
   * **Repositorio**: Su Repositorio de Github  (**MyMvcApp-Contact-Database-Application**) (4)
   * **Rama**: Su Rama de Repositorio de GitHub Repository (5)
   * **Pila del entorno en tiempo de ejecución**: .NET
   * **Versión**: v8.0 (6)
   * **Tipo de autenticación**: Autenticación básica (7)
  
   ![](../../media/challenge3-deployment-center-01.png)

   ![](../../media/challenge3-deployment-center-02.png)

    >**Nota:** Si ve Autorizar, haga clic en Iniciar sesión como

    - Enter the Github credentials **Username or email, Password** and click on **Sign in**.

    - Enter the verification code sent to the github user credentials from the outlook and click on **Verify**.

    - Click on **Authorize AzureAppService**.

1. También puede ver la configuración de su flujo de trabajo haciendo clic en el botón **Archivo de versión preliminar**.

1. Navegue hasta su repositorio de GitHub y, en la pestaña **Actions**, notará que el trabajo build ha comenzado para su aplicación web.

   ![](../../media/challenge3-github-build.png)

1. El flujo de trabajo fallará con el error **build** que indica que el proceso se completó con exit code 1 debido al problema de ruta no definida en su archivo YAML de flujo de trabajo.

   ![](../../media/challenge3-github-build-fail.png)

   ![](../../media/challenge3-github-build-fail-error.png)

1. Ahora naveguemos hasta el archivo YAML del flujo de trabajo editando el archivo y definiendo las rutas para los pasos **dotnet publish** y **Upload artifact for deployment job**.

   ![](../../media/challenge3-github-workflow-edit.png)

1. Ubique los pasos **dotnet publish** y **Upload artifact for deployment job** en su archivo de flujo de trabajo y reemplace las rutas **${{env.DOTNET_ROOT}}/myapp** con **D:\a\MyMvcApp-Contact-Databse-Application\MyMvcApp-Contact-Databse-Application\bin\Release\net8.0\MyMvcApp** y haga clic en **Commit changes**.

   ![](../../media/challenge3-github-workflow-edit-01.png)

   ![](../../media/challenge3-github-workflow-edit-02.png)

1. Vuelva a la pestaña **Actions**, notará que el trabajo build se ha reiniciado para su aplicación web después de definir las rutas. Espere a que build en el flujo de trabajo se complete con éxito.

   ![](../../media/challenge3-github-build-succeed.png)

## Tarea 3: Conseguir que la aplicación funcione en Azure

En esta tarea, verificará que el build pipeline de GitHub Actions se haya completado con éxito, que se haya creado el archivo de flujo de trabajo y que su aplicación web esté funcionando como se espera en Azure.

1. En la configuración de Actions de su repositorio de GitHub, verifique que el pipeline build de ambos trabajos se haya completado con éxito **(1)**.

   ![](../../media/challenge3-github-build-verify.png)

1. Verifique que su aplicación web esté funcionando como se espera navegando a la aplicación web **(2)** en una pestaña diferente.

   ![](../../media/challenge3-web-app-001.png)

1. Además, compruebe que su archivo de flujo de trabajo se haya creado en un nuevo directorio **.github/workflows**.

   ![](../../media/challenge3-github-workflows.png)

1. El archivo de flujo de trabajo de GitHub tendrá el siguiente formato:

   ```
   # Docs for the Azure Web Apps Deploy action: https://github.com/Azure/webapps-deploy
   # More GitHub Actions for Azure: https://github.com/Azure/actions

   name: Build and deploy ASP.Net Core app to Azure Web App - mymvcapp-webapp949348

   on:
     push:
       branches:
         - main
     workflow_dispatch:

   jobs:
     build:
       runs-on: windows-latest

       steps:
         - uses: actions/checkout@v4

         - name: Set up .NET Core
           uses: actions/setup-dotnet@v4
           with:
             dotnet-version: '8.x'

         - name: Build with dotnet
           run: dotnet build --configuration Release

         - name: dotnet publish
           run: dotnet publish -c Release -o D:\a\MyMvcApp-Contact-Databse-Application\MyMvcApp-Contact-Databse-Application\bin\Release\net8.0\MyMvcApp

         - name: Upload artifact for deployment job
           uses: actions/upload-artifact@v4
           with:
             name: .net-app
             path: D:\a\MyMvcApp-Contact-Databse-Application\MyMvcApp-Contact-Databse-Application\bin\Release\net8.0\MyMvcApp

     deploy:
       runs-on: windows-latest
       needs: build
       environment:
         name: 'Production'
         url: ${{ steps.deploy-to-webapp.outputs.webapp-url }}
    
       steps:
         - name: Download artifact from build job
           uses: actions/download-artifact@v4
           with:
             name: .net-app
      
         - name: Deploy to Azure Web App
           id: deploy-to-webapp
           uses: azure/webapps-deploy@v3
           with:
             app-name: 'mymvcapp-webapp949348'
             slot-name: 'Production'
             package: .
             publish-profile: ${{ secrets.AZUREAPPSERVICE_PUBLISHPROFILE_EA47AEBAC2C64100A420A4304676DAF5 }}
   ```

1. También puede verificar el funcionamiento de su aplicación web navegando al portal de Azure, App Service, en la configuración de Información general y haciendo clic en **Dominio predeterminado**.

   ![](../../media/challenge3-default-domain.png)

## Tarea 4: Generar Documentación con Copilot para la Aplicación

En esta tarea, utilizará GitHub Copilot para generar documentación específica para este desafío, que incluirá la plantilla ARM y el archivo de flujo de trabajo de GitHub Actions para desplegar la aplicación web en Azure.

1. En su ventana GitHub Copilot Chat, solicite a GitHub Copilot que genere documentación que especifique la implementación de la plantilla ARM y el archivo de flujo de trabajo de GitHub Actions para implementar la aplicación web en Azure para su espacio de trabajo.

   * @workspace genera documentación que incluirá el proceso de implementación de la plantilla ARM y el archivo de flujo de trabajo de GitHub Actions en el directorio .github/workflows para desplegar la aplicación web en Azure.

1. Notará que GitHub Copilot genera una breve documentación sobre la implementación de la plantilla ARM de su espacio de trabajo en Azure, así como sobre el funcionamiento del archivo de flujo de trabajo y de algunos archivos de configuración.

   ```
   # Deployment of Web Application to Azure
   This document outlines the process of deploying the web application to Azure using ARM templates and GitHub Actions.

   ## ARM Template Deployment
   ARM templates are defined in deploy.json and deploy.parameters.json files.

   ### ARM Template File - deploy.json

   This file contains the Azure Resource Manager (ARM) template which describes the resources that are needed for the application.

   ### Parameters File - deploy.parameters.json

   This file contains the values for the parameters that are used in the ARM template.

   ### To deploy the ARM template, you can use the Azure CLI with the following command:

   az deployment group create --name ExampleDeployment --resource-group ExampleGroup --template-file ./deploy.json --parameters ./deploy.parameters.json

   ## GitHub Actions Workflow
   The GitHub Actions workflow is defined in the .github/workflows directory.

   #### Workflow File - .github/workflows/workflow.yml

   This file contains the GitHub Actions workflow that automates the deployment process. It is triggered on a push to the main branch and it runs the Azure CLI command to deploy the ARM template.

   In this workflow, replace ExampleDeployment and ExampleGroup with your actual deployment name and resource group name. Also, make sure to store your Azure credentials as a secret in your GitHub repository.

   ## Web Configuration
   The web application's configuration is defined in the Web.config, Web.Debug.config, and Web.Release.config files.

   ### Web Configuration File - Web.config

   This file contains the main configuration for the web application.

   ### Debug Configuration File - Web.Debug.config

   This file contains the configuration for the web application when it is in debug mode.

   ### Release Configuration File - Web.Release.config

   This file contains the configuration for the web application when it is in release mode.
   ```

   ![](../../media/challenge3-copilot-doc-generate.png)

## Conclusión

En este desafío, demostró cómo la IA puede ayudar significativamente en el desarrollo y la implementación de aplicaciones, específicamente mediante el uso de GitHub Copilot. No solo desarrolló una aplicación de base de datos de contactos completamente funcional en el desafío anterior, sino que también la implementó de manera efectiva en Azure utilizando una plantilla ARM generada con la ayuda de GitHub Copilot. Ha utilizado GitHub Copilot para agilizar la creación de la plantilla ARM, que es un poderoso ejemplo de infraestructura como código (IaC), y también ha automatizado el proceso de compilación y prueba de su código mediante la creación de una canalización de GitHub Actions, con GitHub Copilot ayudando a generar los scripts necesarios. Además, ha producido documentación completa y precisa para este desafío, que sirve como una guía valiosa para proyectos futuros.

A través de este desafío, le mostró a Contoso Ltd. el potencial de integrar la IA en el flujo de trabajo de desarrollo. Ha demostrado cómo GitHub Copilot puede ayudar no solo al desarrollo de aplicaciones sino también a la implementación y administración de infraestructura, destacando así su versatilidad y valor. Al implementar con éxito la aplicación Contact Database en Azure y verificar su funcionalidad, proporcionó una demostración tangible de los beneficios de la IA en el desarrollo de software.

## Ahora, haga clic en Siguiente en la esquina inferior derecha para pasar al siguiente desafío.

![](../../media/spnext.png)
