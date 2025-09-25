# Desafío 2: Desarrollar una Aplicación con GitHub Copilot

### Tiempo Estimado: 60 minutos

## Introducción

En **Contoso Ltd.**, una empresa líder en desarrollo de software, usted, como **desarrollador de software**, tiene la tarea de explorar las capacidades de **GitHub Copilot**, un asistente de programación impulsado por IA, y aprovecharlas en el proceso de desarrollo de software de la compañía. La empresa cree que la integración de la IA en el proceso de desarrollo puede mejorar significativamente la eficiencia y la productividad de los equipos de desarrollo.

Como parte de esta misión, se le asigna desarrollar una aplicación CRUD llamada **MyMvcApp** utilizando **GitHub Copilot**. El objetivo de este desafío es comprender el potencial de la IA en el desarrollo de software y familiarizarse con las capacidades de GitHub Copilot. Con la ayuda de GitHub Copilot, se espera que genere el código necesario, guiándose por los comentarios proporcionados en el archivo. Utilizará GitHub Copilot en todas las fases del proceso de desarrollo, desde la generación de código para métodos vacíos hasta la creación de funciones esenciales y la prueba exhaustiva de la aplicación.

A lo largo del desafío, aprovechará la capacidad de Copilot para entender el contexto y brindar sugerencias de código relevantes. Al interactuar con Copilot Chat, mejorará la colaboración y recibirá recomendaciones de codificación útiles, lo que enriquecerá aún más su experiencia de programación.

Al finalizar este desafío, su objetivo es tener una **Aplicación CRUD MyMvcApp** completamente funcional, desarrollada principalmente con la ayuda de **GitHub Copilot**. Al finalizar, no solo habrá desarrollado una aplicación con muchas funciones, sino que también habrá obtenido valiosos conocimientos sobre cómo la IA se puede integrar sin problemas en el flujo de trabajo de desarrollo. Esta experiencia práctica con GitHub Copilot le permitirá explorar sus amplias capacidades y desbloquear su potencial en diversos escenarios de desarrollo. Esto demostrará el potencial de la IA en el desarrollo de software y brindará información valiosa sobre su implementación práctica en **Contoso Ltd**.
  
## Requisitos previos

Asegúrese de que dispone de lo siguiente del ambiente integrado proporcionado por CloudLabs:

- Conocimientos básicos del lenguaje de programación C#.
- Cuenta de GitHub.
- Cree una carpeta denominada **GitHub Copilot** en **C:\Users\azureuser**.
- Ejecute los siguientes comandos en el símbolo del sistema para crear una nueva carpeta llamada **MyMvcApp.Tests** en **C:\Users\azureuser\GitHub Copilot** para generar casos de pruebas unitarias.

  ```
  cd "C:\Users\azureuser\GitHub Copilot"
  ```
  ```
  dotnet new xunit -n MyMvcApp.Tests
  ```

## Configurando Visual Studio Code

1. Inicie sesión en Visual Studio Code con sus credenciales de Usuario de GitHub desde la pestaña **Ambiente > Credenciales de GitHub**.

2. Navegue hasta el siguiente enlace de GitHub y bifurque (haga fork) el repositorio en la cuenta de GitHub proporcionada por CloudLabs.

   ```
   https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application
   ```

   > **Nota:** Ya ha hecho fork del repositorio de GitHub proporcionado en el Desafío 01.
   
3. Clone el repositorio bifurcado en Visual Studio Code con la cuenta de GitHub proporcionada por CloudLabs.

4. En Visual Studio Code, busque la carpeta **MyMvcApp.Tests** en el Explorador de soluciones, haga clic derecho y seleccione **Abrir en terminal integrado**. Ejecute el siguiente comando en la terminal para agregar el paquete dotnet.

      ```
      dotnet add package Microsoft.CodeDom.Providers.DotNetCompilerPlatform
      ```

## Objetivos del Desafío
1. **Desarrollar una aplicación:** 

      - Creará una aplicación CRUD llamada **MyMvcApp**, una aplicación C#, con la ayuda de **Github Copilot**, que permitirá a los usuarios guardar los datos de contacto de las personas de acuerdo a los requisitos y también llevar a cabo funciones básicas, tales como editar sus datos, eliminar sus perfiles, etc. Se le proporcionará el esqueleto de la aplicación, pero deberá crear las funcionalidades dentro del archivo **UserController.cs** por su cuenta. Su tarea es completar estos métodos utilizando GitHub Copilot para generar el código necesario, guiado por los comentarios proporcionados en el archivo.

      - Explore la capacidad de Copilot para comprender su contexto y proporcionar sugerencias de código relevantes.
        >**Sugerencia:** Utilice las funciones Iniciar en el Editor, Corregir esto y Chat de GitHub Copilot de GitHub Copilot para desarrollar el código necesario

      - Pruebe la aplicación a fondo y asegúrese de que todas las funcionalidades funcionen como se espera.
  
        ![](../../media/challenge3-mymvcapp-localhost.png)

   <validation step="daaa3f6f-00f1-437a-8f35-01b59fb2da41" />

   <validation step="c7f107a0-97a2-4442-9cef-b14297fd5b7a" />

2. **Generar scripts de casos de pruebas unitarias y valídelos**:

      - Para cada una de las características de **MyMvcApp** que creó dentro del archivo **UserController.cs**, genere casos de pruebas unitarias para el archivo **UserControllerTests.cs** usando **xunit** mediante **Github Copilot**.
        >**Sugerencia:** Cambie el nombre del archivo **UnitTest1.cs** a **UserControllerTests.cs** después de crear la carpeta **MyMvcApp.Test**.

      - Ejecute los scripts requeridos generados por **Github Copilot** y compruebe que todos los casos de pruebas unitarias hayan pasado.

3. **Desarrollar y probar características:** 

      - Una vez que completados los métodos, el siguiente paso es desarrollar y agregar una característica/funcionalidad de búsqueda en la aplicación y probar esta función a fondo.
        
      - Utilice GitHub Copilot para generar fragmentos de código para construir la función de búsqueda.

      - Pruebe la aplicación y asegúrese de que la función de búsqueda funciona como se espera.
  
        ![](../../media/challenge3-mymvcapp-search.png)

4. **Usar GitHub Copilot en cada etapa del desafío:**

      - Utilice GitHub Copilot para ayudar a escribir mensajes de confirmación significativos que describan claramente los cambios realizados.

      - A lo largo del proceso de desarrollo, interactúe con Copilot Chat para mejorar la colaboración y recibir recomendaciones de codificación útiles y perspicaces.
  
## Criterios de Éxito

- Verifique que los métodos en el archivo `UserController.cs` se completen correctamente usando GitHub Copilot.
- Compruebe que todos los casos de prueba generados por Copilot hayan pasado.
- Verifique que la función de búsqueda desarrollada esté funcionando como se esperaba.
- Asegúrese de utilizar correctamente GitHub Copilot para escribir mensajes de confirmación.

## Recursos Adicionales:

- Consulte la [documentación de GitHub Copilot](https://github.com/github/copilot-docs) para cualquier aclaración u orientación durante el desafío.
  
### Validación del Desafío

Proporcione el parámetro de Nombre de Usuario de GitHub en el formato **github-cloudlabsuser-XXXX** para el paso de validación **Validate the cloned Repo**.

## Conclusión  
En este desafío, ha conseguido desarrollar una aplicación de Base de Datos de Contactos completamente funcional principalmente con la ayuda de GitHub Copilot, demostrando su utilidad práctica en un escenario de desarrollo de software del mundo real.
Ha navegado con éxito a través del proceso de desarrollo, desde la generación de código para métodos vacíos en el archivo UserController.cs hasta la construcción de características esenciales para la aplicación. Ha utilizado GitHub Copilot para comprender su contexto y brindar sugerencias de código relevantes, mejorando su experiencia de programación.

La interacción con Copilot Chat ha enriquecido su colaboración y ha proporcionado recomendaciones de codificación útiles, mostrando cómo la IA puede integrarse perfectamente en el flujo de trabajo de desarrollo. Los casos de prueba generados con la ayuda de GitHub Copilot han garantizado la solidez y fiabilidad de su aplicación. Sus logros en este desafío han demostrado el potencial de la IA en el desarrollo de software y han proporcionado información valiosa sobre su implementación práctica. Ha demostrado que con las herramientas adecuadas, como GitHub Copilot, el proceso de desarrollo se puede volver más eficiente y productivo.
  
### Haga clic en **Siguiente** en la esquina inferior derecha para embarcarse en su viaje al laboratorio.

![](../../media/new-github-copilot-hack-spn-06.png)
