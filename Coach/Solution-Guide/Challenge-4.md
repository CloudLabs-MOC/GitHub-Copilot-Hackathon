# Desafío 4: Usando el Espacio de Trabajo y la Referencia de Archivos de GitHub Copilot - Guía de Soluciones

>**Nota:** Los resultados producidos por **GitHub Copilot** para esta tarea en particular pueden no coincidir exactamente con los suyos. Esta discrepancia se produce porque **GitHub Copilot** es una herramienta impulsada por IA que puede generar resultados variables de vez en cuando.

### Tarea 1: Utilizar GitHub Copilot Workspace

En esta tarea, utilizarás GitHub Copilot Workspace para mejorar la eficiencia de la programación al proporcionar sugerencias de código contextualmente relevantes.

1. Abra su proyecto en VS Code, donde inició sesión con los detalles de la cuenta de GitHub proporcionados por CloudLabs.

    ![](../../media/vscode-launch.png)

1. En el panel izquierdo, seleccione el ícono **Chat**. Aparecerá la ventana de chat de bienvenida de **GitHub Copilot**.

    ![](../../media/file1.png)

1. En el cuadro de texto, ingrese **@** **(1)** y seleccione **workspace (2)** para comenzar a trabajar con el agente **GitHub Copilot Workspace**.

    ![](../../media/file2.png)

1. Ahora, puede proporcionar sus propios prompts y seleccionar **Submit** para obtener la respuesta. Para comenzar, puede preguntarle a **GitHub Copilot Chat** cómo iniciar su proyecto actual proporcionando este prompt: `How do I start the current project?`. Cuando envíe su prompt, Copilot analizará automáticamente los archivos y directorios del espacio de trabajo actual, divididos en fragmentos de pasos:

    1. Escanea los nombres de los archivos o directorios para comprender cuáles de ellos son potencialmente relevantes para dar una respuesta.
    
    1. Lee el contenido de los archivos. A veces, todo el archivo, a veces, solo partes de ellos (debido a los límites de memoria del token).
    
    1. Crea un contexto a partir de todo lo que ha podido recopilar.
    
    1. Comienza a responder, combinando el contexto del prompt con el que pudo obtener.

    ![](../../media/file3.png)

1. **GitHub Copilot** le proporcionará una explicación paso a paso de cómo ejecutar su proyecto. Puede seguir los mismos pasos y verificar que su proyecto ejecute correctamente.

    ![](../../media/file4.png)

1. Además de eso, también puede ejecutar el comando `Tell me the current workspace structure.` sin la ayuda del **agente Workspace** y comparar los resultados.

    ![](../../media/file5.png)

    La salida proporcionada es extremadamente abstracta y, al final, le indica que no puede darle la solución exacta y genera solo una solución genérica.

1. Después de esto, puede probar el prompt usando la función **Workspace** y obtener información completa sobre su proyecto de trabajo actual mediante el siguiente prompt: `@workspace Tell me about the current workspace structure.`

    ![](../../media/file6.png)

    Analice el resultado generado y compruebe que la estructura se ajusta a la estructura real de su proyecto.

1. También puede probar los siguientes prompts de ejemplo, proporcionar sus propios prompts según su curiosidad y requisitos, y verificar el resultado:

    ```
    @workspace Create a new lazy-loaded page with the path “/faq.”
    ```
    ```
    @workspace How can I add a new route to my ASP.NET MVC application?
    ```
    ```
    @workspace How can I handle form submissions in ASP.NET MVC?
    ```
    
### Tarea 2: Utilizar GitHub Copilot Workspace para Crear un Nuevo Espacio de Trabajo de Aplicación

Github Copilot Workspace no solo puede proporcionar instrucciones, respuestas o fragmentos de código detallados sobre las consultas que le envíe, sino que también puede crear el espacio de trabajo completo de una aplicación desde cero. Aquí, creará una nueva aplicación sencilla de React llamada **Expense Tracker** para realizar un seguimiento de los gastos de los usuarios y también modificarlos (editarlos) o eliminarlos, todo con la ayuda de **GitHub Copilot Workspace**. Depurará la aplicación utilizando esta función y verificará que la aplicación se ejecute correctamente en su entorno local. Para crear la aplicación `Expense Tracker` utilizando **GitHub Copilot workspace**, siga los pasos mostrados a continuación:

1. Abra una nueva ventana en **VS Code** eligiendo **Archivo** en la barra superior y luego seleccionando **Nueva Ventana**.

    ![](../../media/new-window.png)

1. Ahora, seleccione **Abrir carpeta** en la página **Bienvenida**, busque la carpeta DemoApp y haga doble clic para abrirla en VS Code.

    ![](../../media/vscode-open-folder.png)

1. En el panel izquierdo, seleccione el ícono **Chat**. Aparecerá la ventana de chat de bienvenida de **Github Copilot**.

    ![](../../media/vscode-copilot-chat.png)

1. En el cuadro de texto, ingrese **@ (1)** y seleccione **workspace (2)** para comenzar a trabajar con el agente **Github Copilot Workspace**.

    ![](../../media/@workspace.png)

1. Proporcione el prompt, `Create a workspace for the Expense Tracker React application with all the necessary files and code.` En el cuadro de prueba, seleccione **Submit** para generar el espacio de trabajo completo de su aplicación Expense Tracker React, junto con un par de archivos de componentes.

    ![](../../media/expense-tracker-workspace.png)

    >**Nota:** La versión actual de **Github Copilot Workspace** le permite crear el espacio de trabajo automáticamente con toda la estructura de archivos, solo haga clic en **Create Workspace**.

1. Ahora, cree el espacio de trabajo para su aplicación **Expense Tracker** creando los archivos y carpetas necesarios. Para ello, selecciona **Explorador** en el panel izquierdo y elija los íconos de archivo o carpeta adecuados para crear un nuevo archivo o carpeta según la estructura del espacio de trabajo de su aplicación.

    ![](../../media/vscode-explorer.png)

1. La estructura del espacio de trabajo para su aplicación **Expense Tracker** sería similar a esta, según el resultado generado por **GitHub Copilot Workspace**:

    ![](../../media/created-workspace.png)

1. Ahora, genere el código para todos los componentes necesarios de su aplicación proporcionando los prompts pertinentes a **GitHub Copilot** en la sección **Chat**. Por ejemplo, para crear código para el componente **ExpenseForm.js** de su aplicación, escriba `@workspace. How can I add functionality to the ExpenseForm component to handle user input and save expenses?` y seleccione **Submit**.

    **GitHub Copilot** le proporcionará el código relacionado con el componente al que se hace referencia.

    ![](../../media/expense-form.png)

1. Seleccione el ícono **Copiar** para copiar el código y pegarlo en el componente **ExpenseForm.js** relacionado. Guarde el archivo.

    ![](../../media/expense-form-completed.png)

    >**Nota:** Lea bien la salida generada por **Copilot** y asegúrese de instalar todos los paquetes necesarios si Copilot se lo solicita, antes de ejecutar su aplicación.

1. Haga lo mismo con todos los componentes necesarios de sus aplicaciones sugeridas por **GitHub Copilot Workspace** en **GitHub Copilot Chat** y complete todos los componentes.

1. Asegúrese de utilizar **GitHub Copilot Workspace** en caso de que se produzcan errores en cualquiera de los componentes de su aplicación. Supongamos que aparece un problema en el archivo **app.js** de su aplicación. En ese caso, puede proporcionar un prompt similar al que se muestra para saber el motivo del error y utilizar las funciones avanzadas de **GitHub Copilot Workspace** para corregir el error: `@workspace. Fix the issue in the app.js file.`

    >**Nota:** Asegúrese de utilizar el comando **@workspace** en el cuadro de chat para utilizar la función de workspace de modo que pueda analizar todos los archivos y directorios del espacio de trabajo de su aplicación y ofrecerle la mejor resolución para el error que no entre en conflicto con ningún otro componente.

1. Obtendrá un resultado similar a este:

    ![](../../media/error-fix.png)

    Revise la respuesta y resuelva los errores siguiendo los pasos que en ella se indican.

1. Ahora, cuando se hayan corregido todos los errores, puede preguntarle a Copilot cómo ejecutar su aplicación indicando `@workspace. How can I run this app?` y enviándola.

    Siga los pasos que le indica y ejecute su aplicación.

    ![](../../media/run-app.png)

1. También puede comprobar si todos los requisitos previos necesarios para ejecutar su aplicación **Expense Tracker** ya están instalados proporcionando a Copilot el prompt `@workspace. What are the prerequisites I should install to run this app?`

    ![](../../media/app-prerequisites.png)

    Revise detenidamente la respuesta generada por **GitHub Copilot** usando su función de espacio de trabajo y asegúrese de que todos estos requisitos previos estén instalados. Si no es así, instálelos siguiendo los pasos mencionados en su respuesta.

1. Ejecute la aplicación y se abrirá en su navegador **Edge** tal como se muestra a continuación:

    ![](../../media/app-working.png)

### Tarea 3: Utilizar las Capacidades de Referencia de Archivos

**Referencia de Archivos en GitHub Copilot** se refiere a la capacidad de la IA de comprender e interpretar el contexto de su proyecto al considerar la información en otros archivos dentro de su espacio de trabajo.

Cuando trabaja en un archivo específico en su base de código, **GitHub Copilot** puede tener en cuenta la información, las funciones, las clases o las variables definidas en otros archivos de su proyecto. Esto significa que no solo proporciona sugerencias basadas en el archivo actual en el que está trabajando, sino que también puede hacer referencia a otros archivos para brindarle complementos de código más precisos y relevantes. Esta característica es particularmente útil cuando trabaja en proyectos grandes donde el código está repartido en varios archivos. La capacidad de **GitHub Copilot** de hacer referencia a otros archivos le permite comprender mejor el panorama general de su proyecto, lo que se traduce en sugerencias más sensibles al contexto. Esto puede mejorar significativamente su eficiencia de programación y la calidad general de su código.

En esta tarea, utilizará la función de **Referencia de Archivos de GitHub Copilot** para mejorar la eficiencia de la codificación proporcionando sugerencias de código contextualmente relevantes. Para utilizar la función de referencia de archivos, siga los pasos que se indican a continuación:

1. Abra su proyecto Expense Tracker en **VS Code**, donde inició sesión con los detalles de la cuenta de GitHub proporcionados por CloudLabs.

    ![](../../media/vscode-launch.png)

1. En el panel izquierdo, seleccione el ícono **Chat**. Aparecerá la ventana de chat de bienvenida de **GitHub Copilot**.

    ![](../../media/vscode-copilot-chat.png)

1. En el cuadro de texto, ingrese **@ (1)** y seleccione **Workspace (2)** para activar el agente **GitHub Copilot Workspace**. Necesita que este agente analice todo su espacio de trabajo para que pueda proporcionar respuestas precisas y los bloques de código relacionados haciendo referencia a los archivos correctos.

    ![](../../media/@workspace.png)

1. Ahora, puede utilizar el siguiente prompt para entender cómo funciona la función de referencia de archivos en **GitHub Copilot**. Puede proporcionar con precisión la respuesta para el archivo al que hace referencia: `What is the purpose of the index.js file in my project?`

    **GitHub Copilot** hará referencia a la información, funciones, clases o variables definidas en el archivo sobre el que ha hecho la pregunta y le proporcionará una explicación detallada de lo que hay en **index.js**. No solo la explicación, también le proporcionará el código relacionado acompañado de la respuesta, a la que se hace referencia en el archivo proporcionado.

    **GitHub Copilot** también hace referencia automáticamente a los archivos adicionales de su proyecto que pueden ser necesarios para ofrecerle la mejor respuesta. Para obtener información sobre esos archivos, seleccione **Used n references** (donde **n** es el número total de archivos a los que se hace referencia en su proyecto actual) presente al inicio de la respuesta y observe todos los archivos a los que **GitHub Copilot** hizo referencia para proporcionarle la respuesta.

    ![](../../media/files-referred-2.png)

    Algunos prompts adicionales que puede proporcionar para comprender la función de referencia de archivos son:

    ```
    @workspace What does the ExpenseList.js file do in my application?
    ```
    ```
    @workspace What is the purpose of the app.js file in my project?
    ```
    ```
    @workspace How can I change the CSS for my application?
    ```
    
#### **Agregar una nueva característica en la aplicación mediante la Referencia de Archivo:**

En esta tarea, utilizará la capacidad de referencia de archivo para integrar una nueva característica en su aplicación **Expense Tracker**. Incluirá un campo **Date** en el documento **ExpenseForm** y lo mostrará en **ExpenseItem**, y luego podrá ordenar los gastos por fecha en el componente **ExpenseList**.

Para ello, siga los pasos a continuación:

1. Abra su proyecto en VS Code, donde inició sesión con los detalles de la cuenta de GitHub proporcionada por CloudLabs.

    ![](../../media/vscode-launch.png)

1. En el panel izquierdo, seleccione el ícono **Chat**. Aparecerá la ventana de chat de bienvenida de **GitHub Copilot**.

    ![](../../media/vscode-copilot-chat.png)

1. En el cuadro de texto, ingrese **@ (1)** y seleccione **workspace (2)** para activar el agente **GitHub Copilot Workspace**. Necesita que este agente analice todo su espacio de trabajo para que pueda proporcionar respuestas precisas y los bloques de código relacionados haciendo referencia a los archivos correctos.

    ![](../../media/@workspace.png)

1. Ahora, proporcione este prompt para incluir un nuevo campo **Date** en los componentes y permitir que los usuarios ordenen sus gastos en consecuencia: `How can I modify the ExpenseForm component to include a date field, display this date in the ExpenseItem component, and sort the expenses by date in the ExpenseList component?`

1. La función **GitHub Copilot** hará referencia a los archivos que solicite en los prompts, además de analizar todo su espacio de trabajo y brindarle la mejor respuesta posible. Le proporcionará los fragmentos de código que puede añadir a los componentes **ExpenseForm**, **ExpenseItem** y **ExpenseList** según corresponda. También puede ver los archivos a los que hizo referencia mientras le proporcionaba la respuesta seleccionando **Used n references** (donde n es la cantidad de archivos a los que se hizo referencia) presente al inicio de la respuesta.

    ![](../../media/files-referred.png)

1. Puede revisar la respuesta, realizar los cambios sugeridos por **GitHub Copilot** usando su función de referencia de archivos y editar los componentes como se indica en la respuesta.

1. Ejecute la aplicación y compruebe que el componente **Date** se ha añadido y que funciona correctamente.

    ![](../../media/app-working-date.png)

### Conclusión

En este desafío, ha adquirido una comprensión más profunda de cómo funcionan Github Copilot Workspace y File Referencing y cómo pueden mejorar su proceso de codificación. Al utilizar estas funciones de forma eficaz, puede mejorar significativamente la eficiencia de su codificación y la calidad general de su código. Ya sea que sea un desarrollador experimentado o un principiante, estos conocimientos seguramente serán valiosos en su viaje a la codificación.

### Ahora, haga clic en Siguiente en la esquina inferior derecha para pasar al siguiente desafío.

   ![](../../media/next-page.png)