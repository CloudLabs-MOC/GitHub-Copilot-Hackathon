# Desafío 1: Primeros Pasos con GitHub Copilot

### Tiempo Estimado: 45 minutos

## Introducción

Como desarrollador de software en **Contoso Ltd.**, una empresa líder en desarrollo de software, tiene la tarea de investigar e implementar herramientas y tecnologías innovadoras para mejorar el proceso de codificación y la productividad de la compañía. La empresa está particularmente interesada en soluciones que puedan mejorar la eficiencia del código, agilizar el proceso de desarrollo y mejorar la colaboración entre sus equipos distribuidos globalmente.

**Contoso Ltd.** ha identificado **GitHub Copilot**, un asistente de programación impulsado por IA, como una posible solución y lo ha inscrito a usted en una serie de desafíos para explorar y comprender sus capacidades. Su misión es comenzar a utilizar **GitHub Copilot**, configurarlo en su entorno de programación, explorar sus características y usarlo para generar código y hacer sugerencias. **GitHub Copilot** es un innovador asistente de programación con tecnología de IA que se integra perfectamente en **Visual Studio Code** y está diseñado para mejorar su experiencia de codificación. Aprovechando los algoritmos de machine learning, Copilot ayuda a los desarrolladores en la creación de código sugiriendo de forma inteligente finalizaciones y generando fragmentos de código contextualmente relevantes.

Imagine que tiene que abordar un complejo proyecto de programación y se encuentra con problemas que exigen una atención meticulosa a los detalles. **GitHub Copilot** se convierte en su aliado en la programación, ofreciéndole sugerencias útiles y funciones de autocompletado adaptadas al contexto de codificación. Esto no solo mejora la eficiencia de la programación, sino que también sirve como una valiosa herramienta de aprendizaje, ya que proporciona una comprensión más profunda de las estructuras y los patrones de codificación.

Experimentará con **GitHub Copilot** en varios escenarios de programación, como la creación de una calculadora basada en Python/JavaScript y una aplicación que obtiene datos meteorológicos usando APIs. También aprovechará GitHub Copilot para refactorizar fragmentos de código determinados y para depurar código intencionadamente defectuoso, lo que le permitirá comprender el proceso de mejora del código y la depuración eficaz. Además, explorará la integración de **GitHub Copilot** con GitHub Codespaces, una característica que amplía el potencial colaborativo de su entorno de programación. Esto le permitirá comprender cómo Copilot puede ser utilizado en un ambiente de codificación colaborativo, permitiendo a los equipos trabajar sin problemas en proyectos independientemente de los límites geográficos.

En esta serie de desafíos, se sumergirá en las capacidades de **GitHub Copilot**, comenzando por la configuración y la exploración de sus funciones. Desde la programación colaborativa con GitHub Codespaces hasta la experimentación con las sugerencias de Copilot y la creación de código para varias tareas, se embarcará en un viaje para aprovechar todo el potencial de este revolucionario asistente de programación. Al finalizar este desafío, su objetivo será demostrar cómo se puede usar **GitHub Copilot** eficazmente para aumentar la productividad de la codificación, mejorar la calidad del código y optimizar el proceso de desarrollo de software en **Contoso Ltd**.

## Requisitos previos

Asegúrese de que dispone de lo siguiente del ambiente integrado proporcionado por CloudLabs:

> **Nota**: Los requisitos previos ya están configurados en el ambiente proporcionado por CloudLabs. Si está utilizando su computadora personal o portátil, asegúrese de que todos los requisitos previos necesarios estén instalados para completar este hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [Cuenta de GitHub](https://github.com/)
- Los módulos de Python y NodeJs están instalados en su Lab-VM en el directorio **C:\Program Files**.

## Iniciar sesión en GitHub

1. En el escritorio de LABVM, busque **Microsoft Edge** **(1)**, haga clic en el navegador **Microsoft Edge** **(2)**.

   ![](../../media/Edge.png)

1. Navegue a la página de inicio de sesión de GitHub usando la URL que se proporciona a continuación:
   ```
   https://github.com/login
   ```
   
1. En la pestaña **Sign in to GitHub**, verá la pantalla de inicio de sesión. En esa pantalla, ingrese el siguiente **correo electrónico** **(1)** y **contraseña** **(2)**. Luego, haga clic en **Sign in** **(3)**.

   >**Nota**: Para obtener las credenciales de GitHub, diríjase a la pestaña **Detalles del Ambiente** y haga clic en la opción **Credenciales de GitHub** para ver los pares clave-valor de **GitHub UserEmail** y **GitHub Password**. Puede usar los botones de copia que se encuentran debajo de la columna de acciones para que los valores se copien al instante. Como alternativa, se sugiere copiar los valores en un bloc de notas para facilitar el acceso.
   
   ![](../../media/github-login.png)
          
1. A continuación, para obtener el código de autenticación, inicie sesión en Outlook (https://outlook.office365.com/mail/) con las credenciales de Git dentro de la pestaña Ambiente del paso anterior. Una vez que haya iniciado sesión en Outlook, busque el correo electrónico reciente que contiene el código de verificación. Ingresa el código de verificación y haga clic en **Verify**.

   >**Nota:** El correo electrónico que contiene el código de verificación a veces puede colarse en las carpetas de archivo/spam dentro de Outlook.

   ![](../../media/authgit.png)

## Objetivos del Desafío:

1. **Configurar GitHub Copilot en VS Code:**
      - Instale la extensión GitHub Copilot desde VS Code Marketplace.
      - Configure los ajustes de la extensión que se adapten a sus preferencias.

   <validation step="afc73673-26ad-4c49-b013-4632e09d8634" />

2. **Iniciar sesión con una cuenta de GitHub:**
      - Inicie sesión en GitHub dentro de Visual Studio Code con las credenciales de GitHub proporcionadas. Puede encontrar estas credenciales en la pestaña **Ambiente > Credenciales de GitHub**.
      - En la página de inicio de sesión de GitHub, ingrese sus credenciales de GitHub y haga clic en **Sign in**.
      - Para verificar el inicio de sesión de su cuenta de GitHub, inicie sesión en **Outlook** en la Máquina Virtual del Laboratorio a través de una ventana privada (https://outlook.office365.com/mail/) con sus credenciales de GitHub, busque el correo electrónico que contiene el código de verificación y seleccione **Verify**.
      - Haga clic en Authorize Visual-Studio-Code para proporcionar permisos adicionales a GitHub para VS Code.

3. **Usar GitHub Codespaces con Copilot:**
      - Crea un Codespace para tu repositorio de GitHub. Vaya al repositorio **https://github.com/CloudLabsAI-Azure/Code-Generation-Refactoring** y bifurque este repositorio en la cuenta de GitHub proporcionada por CloudLabs para crear un nuevo espacio de código.
      - Clona el repositorio de GitHub anterior en tu código VS.
      - Comprenda cómo se puede utilizar Copilot en un entorno de programación colaborativa.
      - Utilice GitHub Codespaces para enviar/confirmar los archivos locales de VS Code a GitHub en los próximos desafíos.

4. **Prueba de Función de Copilot:**   
   - Crear un Nuevo Archivo Python:
     - Abre Visual Studio Code y crea un nuevo archivo llamado hello.py.
   - Utilizando GitHub Copilot:
     - Presiona Ctrl + I para solicitar sugerencias de código a GitHub Copilot.
     - En la ventana mini de Copilot, escribe:
     - "Generar un programa básico de Hola Mundo en Python."
     - Revisa el código generado, que debería verse así:
     ```
     print("Hello, World!")
     ```
     - Haz clic en Aceptar para insertar el código en tu archivo.
     >**Sugerencia:** Accede a la ventana de Sugerencias de GitHub Copilot presionando Ctrl + Enter en Visual Studio Code.

5. **Generar Código con Copilot y Copilot Chat:**
      - Cree código basado en Python/JS para construir una calculadora.
         - Utilice GitHub Copilot para generar código Python o JavaScript que cree una calculadora básica.
         - Una vez que haya escrito el código, guarde el archivo como ***calculator.py*** si usa Python, o ***calculator.js*** si usa JavaScript, y envíelo a su bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring** repositorio GitHub.
         - Experimente con diferentes operaciones matemáticas e interacciones de usuario.
      - Cree una aplicación basada en Python/JS para obtener datos meteorológicos de las APIs de OpenWeatherMap.
         - Regístrese en el sitio web de OpenWeatherMap (https://openweathermap.org/).
         - Aproveche Copilot para generar código Python/JS que interactúe con las APIs meteorológicas para recuperar datos del clima.
         - Guarde este archivo como ***weather_script.py*** para Python o ***weather_script.js*** para JavaScript y envíelo a su repositorio bifurcado de GitHub **CloudLabsAI-Azure/Code-Generation-Refactoring**.

   <validation step="b5244888-2b42-4686-b326-465182a86561" />

6. **Refactorizar y Depurar Código:**
      - Refactorice el código `sum_elements.py` de su repositorio GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring** usando Copilot, entendiendo el proceso de mejora del código.
        >**Sugerencia:** Utilice la función **Refactor** de GitHub Copilot.

      - Depure el código `card_draw.py` de manera efectiva desde su repositorio GitHub bifurcado **CloudLabsAI-Azure/Code-Generation-Refactoring** con la ayuda de Copilot, abordando y solucionando problemas identificados. 
        >**Sugerencia:** Utilice la función **Reparar** de GitHub Copilot.

7. **Explorar las Características de GitHub Copilot:**
      - Experimente con Copilot en varios escenarios de codificación.
      - Utilice las sugerencias de Copilot para acelerar su proceso de escritura de código.
        >**Sugerencia:** Acceda a la ventana GitHub Copilot Suggestions con el atajo **Ctrl+Enter** en VS Code.

## Criterios de Éxito:

- Compruebe que GitHub Copilot se haya instalado y configurado correctamente en Visual Studio Code y que se haya iniciado sesión.
- Explore con éxito la integración de GitHub Codespaces y comprenda sus funciones de colaboración.
- Pruebe con éxito Copilot en escenarios de programación, experimentando sus capacidades de generación de código.
- Verifique que el código Python/JS para una calculadora y una aplicación para obtener datos meteorológicos con Copilot se hayan creado y ejecutado correctamente.
- Verifique que el fragmento de código elegido se haya refactorizado correctamente, mejorando la legibilidad y la calidad general.
- Compruebe que un fragmento de código con errores intencionales se haya corregido correctamente utilizando las sugerencias de Copilot.

## Recursos Adicionales:

- [Documentación de GitHub Copilot](https://github.com/github/copilot-docs)
- [Documentación de GitHub Codespaces](https://docs.github.com/en/codespaces)

### Conclusión

En este desafío, ha configurado con éxito GitHub Copilot en Visual Studio Code, ha configurado los ajustes de la extensión y ha iniciado sesión con su cuenta de GitHub. También ha logrado crear código Python/JS para una calculadora y una aplicación para obtener datos meteorológicos de las APIs de OpenWeatherMap. Además, ha perfeccionado sus habilidades de programación refactorizando fragmentos de código y depurando con la ayuda de Copilot.

### Haga clic en **Siguiente** en la esquina inferior derecha para embarcarse en su viaje al laboratorio.

![](../../media/new-github-copilot-hack-spn-06.png)
