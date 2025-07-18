# Desafío 3: Implementar la Aplicación en Azure

### Tiempo Estimado: 60 Minutos

## Introducción

En el desafío anterior, desarrolló con éxito una **Aplicación CRUD MyMvcApp** completamente funcional, desarrollada principalmente con la ayuda de **GitHub Copilot**, y también obtuvo información valiosa sobre cómo la IA se puede integrar perfectamente en el flujo de trabajo de desarrollo.

Como desarrollador de software en **Contoso Ltd.**, una empresa líder en desarrollo de software, tiene la tarea de explorar tecnologías y herramientas innovadoras que puedan mejorar el proceso de desarrollo de software y la gestión de la infraestructura de la empresa. **Contoso Ltd.** reconoce el potencial de la Infraestructura como Código (IaC) en la gestión y el aprovisionamiento de sus recursos informáticos y está particularmente interesado en las plantillas de Azure Resource Manager (ARM) para implementar aplicaciones en Azure.

En este desafío, utilizará **GitHub Copilot** para agilizar el desarrollo de una plantilla **Azure Resource Manager (ARM)** para desplegar la **Aplicación MyMvcApp CRUD** completamente funcional que desarrolló anteriormente. Las plantillas ARM son archivos de Infraestructura como Código (IaC) que se utilizan para implementar y administrar recursos en Azure. Aprovechando las capacidades de generación de código de Copilot, acelerará la creación de una plantilla ARM para desplegar una aplicación en Azure. Además de esto, también automatizará los procesos de construcción y prueba de su código. Creará un pipeline de GitHub Actions, con la ayuda de GitHub Copilot para generar los scripts necesarios. Para documentar los conocimientos y la información adquiridos en este ejercicio, utilizará **GitHub Copilot** para generar una documentación completa y precisa para este desafío. Esta documentación servirá como guía para crear la plantilla ARM, configurar el pipeline de GitHub Actions e implementar la **Aplicación MyMvcApp CRUD** completamente funcional en Azure.

Al completar este desafío, su objetivo es demostrar a Contoso Ltd. cómo **GitHub Copilot** puede agilizar el desarrollo de plantillas ARM, automatizar los procesos de construcción y prueba con GitHub Actions y generar documentación detallada. Esto resaltará aún más el valor de la integración de la IA en el flujo de trabajo de desarrollo, tras el desarrollo exitoso de la aplicación de la Base de Datos de Contactos en el desafío anterior.

## Requisitos previos

Asegúrese de que dispone de lo siguiente del ambiente integrado proporcionado por CloudLabs:

> **Nota**: Los requisitos previos ya están configurados en el ambiente proporcionado por CloudLabs. Si está utilizando su computadora personal o portátil, asegúrese de que todos los requisitos previos necesarios estén instalados para completar este hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [Cuenta de GitHub](https://github.com/)
- [Extensión GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) instalada en VS Code.
- Asegúrese de implementar la aplicación web en el grupo de recursos existente denominado **GitHub-Copilot-Challenges**.

## Accediendo al Portal de Azure

1. Para acceder al portal de Azure, abra una ventana privada o de incógnito en su navegador y navegue hasta **[Portal de Azure](https://portal.azure.com)**.

1. En la pestaña **Iniciar sesión en Microsoft Azure**, verá una pantalla de inicio de sesión. Ingrese el siguiente correo electrónico o nombre de usuario y, a continuación, haga clic en **Siguiente**. 

   * Correo Electrónico/Nombre de Usuario: <inject key="AzureAdUserEmail"></inject>
        
1. Ahora ingrese la siguiente contraseña y haga clic en **Iniciar sesión**.
   * Contraseña: <inject key="AzureAdUserPassword"></inject>

1. **Omita** el registro de MFA si aparece la ventana emergente al iniciar sesión en el portal de Azure.

1. Si ve la ventana emergente **¿Quiere mantener la sesión iniciada?**, haga clic en No.

1. Si ve la ventana emergente **¡Tiene recomendaciones gratuitas de Azure Advisor!**, cierre la ventana para continuar con el laboratorio.

1. Si aparece una ventana emergente **Bienvenido a Microsoft Azure**, haga clic en **Cancelar** para omitir la visita guiada.
   
1. Ahora verá el Panel del Portal de Azure. Haga clic en **Grupos de recursos** en el panel Navegar para ver los grupos de recursos.
  
1. Confirme que tiene un grupo de recursos **GitHub-Copilot-Challenges** presente, como se muestra en la siguiente captura de pantalla. Debe usar el grupo de recursos **GitHub-Copilot-Challenges** a lo largo de este desafío.

## Objetivos del Desafío:

1. **Desarrollar una plantilla ARM para implementar una aplicación en Azure:**

      - Utilice GitHub Copilot para generar la estructura inicial de una plantilla ARM para desplegar la **Aplicación CRUD MyMvcApp** en Azure.

      - Defina los recursos de Azure necesarios en la plantilla ARM, es decir, una **Aplicación web** presente en **Azure App Services** necesaria para implementar la aplicación.

      - Guarde la plantilla ARM y los archivos de parámetros en el repositorio de GitHub de la **Aplicación CRUD MyMvcApp** como **deploy.json** y **deploy.parameters.json** en la rama **master**.

   <validation step="93dbb711-57a3-462c-8ffe-699f1208865e" />

2. **Generar un flujo de trabajo de GitHub Actions mediante el Centro de Implementación desde la Aplicación Web en el portal de Azure:**

      - Implemente y construya el código del flujo de trabajo desde el **Centro de Implementación** de su Aplicación Web para el repositorio fuente de GitHub **MyMvcApp-Contact-Database-Application** para iniciar la canalización del flujo de trabajo a fin de desplegar su Aplicación Web en Azure.
       
         >**Nota:** build fallará debido a una ruta no definida en el archivo YAML del flujo de trabajo.

      - Especifique la ruta como **D:\a\MyMvcApp-Contact-Databse-Application\MyMvcApp-Contact-Databse-Application\bin\Release\net8.0\MyMvcApp** para los pasos **dotnet publish** y **Upload artifact for deployment job** en su archivo de flujo de trabajo.

   <validation step="019351e9-84ff-4623-a26c-66afe706bf66" />

3. **Conseguir que la aplicación funcione en Azure:**

      - Verifique que el pipeline de construcción de GitHub Actions se haya realizado correctamente y que la aplicación esté funcionando como se esperaba a través de la Aplicación Web.

     ![](../../media/challenge3-web-app-001.png)

      - Verifique que los recursos implementados coincidan con las especificaciones descritas en su plantilla ARM y que la aplicación esté funcionando desde el **Dominio predeterminado** de la Aplicación Web de Azure.

4. **Generar documentación con Copilot para la aplicación:**

      - Utilice GitHub Copilot para ayudarle a generar documentación detallada y precisa específicamente para este desafío.

      - Cree un archivo **README.md** en su repositorio de GitHub **MyMvcApp-Contact-Database-Application** en la rama **master**. Esto servirá de guía para crear una plantilla ARM para implementar la aplicación y el archivo de flujo de trabajo del pipeline de GitHub Actions.

## Criterios de Éxito:

- Compruebe que la aplicación web de Azure App Services que contiene el código de su aplicación esté presente en Azure.
- Verifique que el pipeline de GitHub Actions se haya creado correctamente.
- Verifique que la **Aplicación CRUD MyMvcApp** se haya implementado correctamente en Azure y pruebe la funcionalidad.
- Compruebe que la documentación se haya creado correctamente.

## Recursos Adicionales:

- Consulte [aquí](https://learn.microsoft.com/en-us/azure/developer/github/deploy-to-azure) para obtener ayuda adicional.
- Si encuentra algún problema o tiene alguna pregunta, consulte la [Documentación de GitHub Copilot](https://github.com/github/copilot-docs) para obtener orientación.

### Validación del Desafío

Proporcione el parámetro de Nombre de Usuario de GitHub en el formato **github-cloudlabsuser-XXXX** para el paso de validación **Validate GitHub directory**.

## ConclusiÓn

En este desafío, ha demostrado cómo la IA puede ayudar significativamente en el desarrollo y la implementación de aplicaciones, específicamente mediante el uso de GitHub Copilot. No solo ha desarrollado una aplicación de Base de Datos de Contactos completamente funcional en el desafío anterior, sino que también la ha desplegado de manera efectiva en Azure utilizando una plantilla ARM generada con la ayuda de GitHub Copilot. Ha utilizado GitHub Copilot para agilizar la creación de la plantilla ARM, que es un poderoso ejemplo de Infraestructura como código (IaC), y también ha automatizado el proceso de construcción y prueba de su código mediante la creación de un pipeline de GitHub Actions, con la ayuda de GitHub Copilot para generar los scripts necesarios. Además, ha elaborado una documentación completa y precisa para este desafío, la cual le servirá de valiosa guía para proyectos futuros.

A través de este desafío, ha mostrado a Contoso Ltd. el potencial de integrar la IA en el flujo de trabajo de desarrollo. Ha demostrado cómo GitHub Copilot puede ayudar no solo en el desarrollo de aplicaciones, sino también en la implementación y administración de la infraestructura, destacando así su versatilidad y valor. Al desplegar con éxito la aplicación de la Base de Datos de Contactos en Azure y verificar su funcionalidad, ha proporcionado una demostración tangible de los beneficios de la IA en el desarrollo de software.

### Haga clic en Siguiente >> para continuar con el próximo desafío.

![](../../media/next-page-spanish.png)
