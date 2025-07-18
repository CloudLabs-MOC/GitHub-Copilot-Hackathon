# Desafío 2: Desarrollar una Aplicación con GitHub Copilot - Guía de Soluciones

## Tarea 1: Desarrollar una Aplicación

### Iniciar sesión en GitHub

1. Inicie sesión en [GitHub](https://github.com/login) con la cuenta de GitHub proporcionada por CloudLabs. Asegúrese de haber iniciado sesión en la cuenta de GitHub correcta proporcionada para esta sesión de laboratorio.

### Bifurcar (Hacer fork) el Repositorio

1. Navegue hasta el enlace del repositorio de GitHub proporcionado: [MyMvcApp-Contact-Database-Application](https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application.git).

    ![](../../media/Repo-info.png)

1. Bifurque (haga fork) el repositorio en la cuenta de GitHub proporcionada por CloudLabs.

    ![](../../media/Fork-repo.png)

### Abrir Visual Studio y Clonar el Repositorio

1. Inicie Visual Studio y haga clic en ""Clonar el repositorio Git".

   ![](../../media/Clone-Git-repo.png)

1. Ingrese la URL del Repositorio Git y haga presione Enter

    ![](../../media/URL-Repo.png)

1. La ventana se verá así.

    ![](../../media/Cloned-rep.png)


### Configurar Visual Studio 2022

1. En Visual Studio, navegue y haga clic en la opción **GitHub Copilot** ubicada en la parte superior derecha y seleccione **Instalar Copilot**.

2. En el panel Instalador de Visual Studio, asegúrese de que **GitHub Copilot** esté seleccionado y haga clic en **Instalar**. Esto cerrará la aplicación Visual Studio.

3. Espere a que la extensión GitHub Copilot se descargue por completo (esto puede tardar unos minutos) y cierre el panel del Instalador de Visual Studio.

  > **Nota:** Ignore el mensaje de error 'Couldn't install Microsoft.Net.4.8.1.FullRedist', esto no afectará los desafíos.

4. Vuelva a iniciar Visual Studio y verifique que GitHub Copilot esté activo. Ahora se puede utilizar la ventana GitHub Copilot Chat.

5. Una vez que se haya clonado el repositorio, busque y abra el archivo `MyMvcApp.sln` desde el Explorador de Soluciones.

  ![](../../media/MyMvcApp_ss.png)

6. Vaya a Extensiones 

  ![](../../media/Extension.png)

7. Instale **Nuget Gallery** y **C# Dev Kit**

  ![](../../media/NuGet.png)  ![](../../media/CAPP.png)

8. Ejecute el siguiente comando en la consola.

    ```
    Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r
    ```

    ![](../../media/crud5.6.png)

### Implementar Métodos usando GitHub Copilot

1. Navegue hasta el archivo `UserController.cs` dentro de la carpeta `Controllers`.

    ![](../../media/crud2.7.png)

2. Utilice GitHub Copilot para generar código para cada método vacío en el archivo `UserController.cs`. Para generar código para cada método vacío con GitHub Copilot, seleccione o resalte las líneas del método vacío y luego haga clic derecho en las líneas resaltadas para abrir el menú contextual.

    ![](../../media/crud1.2.png)
    ![](../../media/crud1.3.png)

3. En el menú contextual, seleccione la opción "Preguntar a Copilot". En el cuadro de mensaje, escriba "Fill in the Index method".

    ![](../../media/crud1.4.png)

4. GitHub Copilot generará una sugerencia de código basada en el contexto del método. Revise la sugerencia proporcionada por GitHub Copilot y podrá elegir aceptarla o descartarla según su relevancia para sus requisitos.

    ![](../../media/crud1.5.png)

5. Repita este proceso para cada método vacío en el archivo UserController.cs hasta que se hayan implementado todos los métodos.

6. Siguiendo estos pasos, podrá utilizar eficientemente GitHub Copilot para generar código para cada método vacío en el archivo UserController.cs.

### Ejecutar y probar la Aplicación

1. Localice el botón IIS Express (un botón de reproducción verde) en la barra de herramientas y haga clic en él. Esta acción inicia la aplicación en localhost en un navegador web.

    ![](../../media/crud1.6.png)

2. Una vez que ejecute la aplicación en un navegador web local a través de IIS Express, aparecerán un par de ventanas emergentes que permitirán que la aplicación se ejecute con un certificado autofirmado que IIS Express ha generado.

    ![](../../media/ssl-yes.png)

    ![](../../media/ssl-yes01.png)

### Crear un Nuevo Contacto

1. En el navegador web abierto, localice el botón "Create New" y haga clic en él.

    ![](../../media/crud1.7.png)

2. Complete los campos obligatorios de Name y Email en el formulario proporcionado. Haga clic en el botón "Create" para enviar el formulario y crear un nuevo contacto.

    ![](../../media/crud1.8.png)

### Editar un Contacto

1. Después de crear un contacto, vuelva a la página de inicio.

2. Busque el contacto que creó en la lista y localice el botón "Edit" asociado a él. Haga clic en el botón "Edit".

    ![](../../media/crud1.9.png)

3. Modifique los detalles existentes (Name o Email) como desee. Guarde los cambios haciendo clic en el botón "Save".

    ![](../../media/crud1.10.png)

### Verificar los Detalles de un Contacto

1. Una vez más, vuelva a la página de inicio.

2. Localice el contacto cuyos datos desea verificar. Haga clic en el botón "Details" asociado a ese contacto.

    ![](../../media/crud1.11.png)

3. Compruebe que los detalles que se muestran coincidan con la información que introdujo anteriormente.

    ![](../../media/crud1.12.png)

### Eliminar un Contacto

1. Desde la página de inicio, busque el contacto que desea eliminar.

2. Haga clic en el botón "Delete" asociado a ese contacto.

    ![](../../media/crud1.13.png)

3. Aparecerá un cuadro de diálogo de confirmación que le preguntará si está seguro de que desea eliminar el contacto. Confirme la acción.

    ![](../../media/crud1.14.png)

4. Asegúrese de que el contacto se remueva de la lista después de la eliminación.

    ![](../../media/crud1.15.png)

Siguiendo estos pasos meticulosamente, podrá probar a fondo las funcionalidades CRUD (Crear, Leer, Actualizar, Borrar) de la aplicación y garantizar su correcto funcionamiento.

# Tarea 2: Generar Casos de Pruebas Unitarias

1. Para generar casos de pruebas unitarias, necesitamos agregar un nuevo proyecto. En el explorador de soluciones, haga clic derecho en la Solución.

    ![](../../media/crud3.1.png)

2. Haga clic en Agregar y luego en Nuevo Proyecto.

    ![](../../media/crud3.2.png)

3. Ahora busque Unit Test (Prueba Unitaria) en el cuadro de búsqueda, seleccione Unit Test Project (.NET Framework) (Proyecto de Prueba Unitaria) y luego haga clic en Siguiente.

    ![](../../media/crud3.3.png)

4. Nombre al proyecto como Usercontrollertest y luego haga clic en Crear.

    ![](../../media/crud3.4.png)

5. Cambie el nombre del archivo UnitTest1.cs a UserControllerTests.cs.

6. Ahora, pidamos a Github Copilot Chat que genere casos de prueba. Haga clic en la opción "Ver" en el panel superior de Visual Studio. En las opciones, seleccione "Chat de GitHub Copilot" para abrir la ventana de GitHub Copilot Chat.

    ![](../../media/crud3.5.png)

7. Abra el archivo UserController.cs y seleccione/resalte todo el código que contiene.

    ![](../../media/crud3.6.png)

8. Una vez que se haya resaltado todo el código, en Github Copilot Chat, proporcione un prompt como "generate unit test cases for usercontroller.cs"

    ![](../../media/crud3.7.png)

9. Github Copilot comenzará a generar casos de prueba unitaria para usercontroller.cs.

    ![](../../media/crud3.8.png)

10. Ahora copie el código proporcionado por Github Copilot haciendo clic en el ícono de copiar.

    ![](../../media/crud3.9.png)

11. Elimine el código existente y pegue el código que copiamos en el archivo.

    ![](../../media/crud3.10.png)

12. Ahora agreguemos referencias al proyecto. Localice las Referencias para UserControllertest y luego haga clic derecho sobre ellas. Luego haga clic en Agregar referencia.

    ![](../../media/crud3.11.png)

13. Ahora, en Proyectos, marque la casilla de verificación y luego haga clic en Aceptar.

    ![](../../media/crud3.12.png)

14. Ahora, solucionemos los problemas del archivo colocando el cursor sobre TestFixture y luego haciendo clic en las funciones Preguntar a Copilot (1) o Acciones rápidas y refactorizaciones... (2).
  
    ![](../../media/ask-copilot.png)

    ![](../../media/quick-actions.png)

15. Haga clic en "Instalar paquete NUnit" y luego en "Buscar e instalar la última versión".

    ![](../../media/crud3.14.png)

16. De manera similar, pase el cursor sobre controller.Index(), haga clic en Mostrar posibles correcciones y, a continuación, haga clic en "Instalar paquete 'Microsoft.ASPNet.Mvc'" y luego en "Usar la versión local '5.2.7'"

    ![](../../media/crud3.15.png)

17. Nuevamente, para RouteValues pase el cursor por encima y luego haga clic en Mostrar posibles correcciones, y luego haga clic en Agregar referencia.

    ![](../../media/crud3.16.png)

18. De nueva cuenta, para Assert, pase el cursor por encima y haga clic en Mostrar posibles correcciones y luego en using Assert.

    ![](../../media/crud3.17.png)

19. Después de resolver todos los problemas en el archivo, haga clic en la opción Prueba (Test) en el panel superior de Visual Studio. Luego haga clic en Explorador de pruebas.

    ![](../../media/crud3.18.png)

20. En el Explorador de pruebas, haga clic en el botón Ejecutar Todo para ejecutar los casos de prueba.

    ![](../../media/crud3.19.png)

21. Verifique que se hayan aprobado todos los casos de prueba.

    ![](../../media/crud3.20.png)

# Tarea 3: Desarrollar y Probar funciones

### Utilizar GitHub Copilot Chat para el Desarrollo de Funciones:
  
1. clic en la opción "Ver" en el panel superior de Visual Studio. De las opciones, seleccione "Chat de GitHub Copilot" para abrir la ventana de GitHub Copilot Chat.
  
        ![](../../media/crud3.5.png)

### Solicitar a GitHub Copilot Chat la Implementación de Funciones:
   
1. Inicie una conversación con GitHub Copilot Chat preguntando "How can we add a search feature/functionality to our application?"

        ![](../../media/crud4.1.png)

2. Según la respuesta generada por GitHub Copilot, proceda a implementar el código sugerido.
  
3. En este caso, GitHub Copilot sugirió agregar un nuevo método para aceptar una cadena de búsqueda como parámetro y filtrar la lista de usuarios según la cadena de búsqueda antes de pasarla a la vista.

        ![](../../media/crud4.2.png)
  
4. Copie y pegue el fragmento de código proporcionado en el archivo `UserController.cs` dentro del método de acción apropiado, generalmente el método `Index`. En este código, si se proporciona una cadena de búsqueda (searchString), la lista de usuarios se filtra para incluir solo los usuarios cuyos nombres contienen la cadena de búsqueda. Si no se proporciona ninguna cadena de búsqueda, se devuelven todos los usuarios.

        ```
        // GET: User
        public ActionResult Index(string searchString)
        {
            var users = from u in userlist
                        select u;
            if (!String.IsNullOrEmpty(searchString))
            {
                users = users.Where(s => s.Name.Contains(searchString));
            }
            return View(users.ToList());
        }
        ```

        ![](../../media/crud4.3.png)

5. GitHub Copilot también sugirió modificar el archivo `Index.cshtml` ubicado en la ruta **Views\User\Index.cshtml** a fin de incluir un formulario para la cadena de búsqueda.

        ![](../../media/crud4.4.png)

6. Copie y pegue el fragmento de código proporcionado en el archivo `Index.cshtml`. Este formulario envía una solicitud GET al método de acción Index, pasando la cadena de búsqueda como un parámetro de cadena de consulta.

        ```
        @using (Html.BeginForm("Index", "User", FormMethod.Get))
        {
            <p>
                Find by name: @Html.TextBox("searchString") 
                <input type="submit" value="Search" />
            </p>
        }
        ```

        ![](../../media/crud4.5.png)

### Guardar los Cambios y Ejecutar la Aplicación:

1. Guarde los archivos `UserController.cs` e `Index.cshtml` después de realizar los cambios necesarios.

2. Ejecute la aplicación haciendo clic en el botón IIS Express. Esta acción inicia la aplicación en localhost en un navegador web.

        ![](../../media/crud1.6.png)

### Probar la Función de Búsqueda:

1. Agregue un par de entradas de contacto a la aplicación haciendo clic en el botón "Create New" y rellenando los campos Name y Email.

        ![](../../media/crud4.6.png)

2. Una vez que añadidos los contactos, pruebe la funcionalidad de búsqueda escribiendo el nombre de un contacto en el campo de búsqueda previamente añadido. Haga clic en el botón "Search" para ejecutar la búsqueda.

        ![](../../media/crud4.7.png)

3. Si la función se ha implementado correctamente, debería poder ver el contacto buscado en los resultados.

        ![](../../media/crud4.8.png)

Siguiendo estos pasos, puede utilizar GitHub Copilot de manera efectiva para implementar y probar nuevas características en su aplicación, mejorando su funcionalidad y usabilidad.

# Tarea 4: Generar Mensajes de Confirmación (Commit)

La nueva función Generated Commit Message utiliza GitHub Copilot AI para describir los cambios de código. Esto hace que escribir mensajes de confirmación descriptivos y útiles sea tan fácil como hacer clic en un botón y luego agregar una explicación.

1. Localice Cambios de GIT y haga clic en él.

    ![](../../media/crud5.1.png)

2. Use el nuevo ícono de lápiz brillante “Add AI Generated Commit Message” en la ventana Cambios de GIT para generar una sugerencia.

    ![](../../media/crud5.2.png)

3. GitHub Copilot analizará los cambios en los archivos de su confirmación, los resumirá y luego describirá cada cambio. Luego puede “Insert AI Suggestion” o “Discard”. Haga clic en Commit All.

    ![](../../media/crud5.3.png)

4. Una vez confirmado localmente, haga clic en Push para insertar los cambios en el repositorio.

    ![](../../media/crud5.4.png)

## Conclusión
En este desafío, has logrado desarrollar una aplicación de base de datos de contactos completamente funcional, principalmente con la ayuda de GitHub Copilot, demostrando su utilidad práctica en un escenario real de desarrollo de software.
Has completado con éxito el proceso de desarrollo, desde la generación de código para métodos vacíos en el archivo UserController.cs hasta la creación de funciones esenciales para la aplicación. Has utilizado GitHub Copilot para comprender tu contexto y proporcionar sugerencias de código relevantes, mejorando tu experiencia de programación.

La interacción con Copilot Chat ha enriquecido tu colaboración y proporcionado recomendaciones de programación útiles, mostrando cómo la IA puede integrarse perfectamente en el flujo de trabajo de desarrollo. Los casos de prueba generados con la ayuda de GitHub Copilot han garantizado la robustez y fiabilidad de tu aplicación. Tus logros en este desafío han demostrado el potencial de la IA en el desarrollo de software y han proporcionado información valiosa para su implementación práctica. Has demostrado que con las herramientas adecuadas, como GitHub Copilot, el proceso de desarrollo puede ser más eficiente y productivo.

### Haga clic en Siguiente >> para continuar con el próximo desafío.

![](../../media/next-page.png)
