# Desafío 4: Usando el espacio de trabajo y la referencia de archivos de GitHub Copilot

### Tiempo Estimado: 60 Minutos

## Introducción

Como desarrollador de software en **Contoso Ltd.**, una empresa líder en desarrollo de software, siempre está buscando formas de mejorar su eficiencia de codificación y la calidad general de su código. Después de explorar con éxito las características básicas de **GitHub Copilot** y usarlo para desarrollar e implementar una aplicación en Azure, ahora se centra en algunas de las características avanzadas de este asistente de programación impulsado por IA.

En este desafío, se le asigna específicamente la tarea de explorar y utilizar las tres características clave de **GitHub Copilot**: el **espacio de trabajo** y la **referencia a archivo**. La comprensión y utilización de estas características puede aumentar significativamente su productividad y eficiencia en la programación al proporcionar sugerencias de código más precisas y contextualizadas.

- **GitHub Copilot Workspace:** **GitHub Copilot Workspace** es una característica avanzada de **GitHub Copilot**, una herramienta de completado de código impulsada por IA. El espacio de trabajo en GitHub Copilot se refiere al directorio de trabajo actual donde residen sus archivos de código.

   Cuando está programando, **GitHub Copilot** utiliza la información en su espacio de trabajo para generar sugerencias de código contextualmente relevantes. Esto significa que tiene en cuenta los detalles de su proyecto actual, tales como los archivos de código, las bibliotecas y las dependencias que están presentes en su espacio de trabajo, a fin de proporcionarle las terminaciones de código más adecuadas. Esta característica convierte a **GitHub Copilot** en un asistente de programación inteligente que no solo entiende la sintaxis y la semántica del lenguaje, sino también el contexto de su proyecto, lo que se traduce en sugerencias de código más precisas y útiles.
   Mediante el uso eficaz de la característica **Workspace**, los desarrolladores pueden mejorar su eficiencia de codificación, reducir errores y crear código de mayor calidad.

- **Referencias a archivos en GitHub Copilot:** La **referencia a archivos en GitHub Copilot** se refiere a la capacidad de la IA de comprender e interpretar el contexto de su proyecto teniendo en cuenta la información en otros archivos dentro de su espacio de trabajo.

   Cuando está trabajando en un archivo específico de su base de código, **GitHub Copilot** puede tener en cuenta la información, las funciones, las clases o las variables definidas en otros archivos de su proyecto. Esto significa que no solo proporciona sugerencias basadas en el archivo actual en el que se encuentra trabajando, sino que también puede hacer referencia a otros archivos para brindarle complementos de código más precisos y relevantes. Esta función es particularmente útil cuando trabaja en proyectos grandes en los que el código se distribuye en varios archivos. La capacidad de GitHub Copilot de hacer referencia a otros archivos le permite comprender mejor el panorama general de su proyecto, lo que se traduce en sugerencias más contextualizadas. Esto puede mejorar significativamente su eficiencia de codificación y la calidad general de su código.

Tanto si es un desarrollador experimentado que busca mejorar su eficiencia de codificación o un principiante que busca mejorar sus habilidades de programación, este laboratorio le proporcionará información valiosa sobre cómo **GitHub Copilot** puede ser una herramienta poderosa en su viaje de programación. Al final de este desafío, su objetivo es demostrar a **Contoso Ltd.** cómo estas características avanzadas de **GitHub Copilot** pueden mejorar significativamente la eficiencia de codificación y la calidad general del código, reforzando aún más los beneficios de integrar la IA en el flujo de trabajo de desarrollo. ¡Comencemos!

## Requisitos previos

Asegúrese de que dispone de lo siguiente del ambiente integrado proporcionado por CloudLabs:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Cuenta de GitHub](https://github.com/)
- [Extensión GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) instalada en VS Code.
- Cree una nueva carpeta denominada **DemoApp** en **C:/Users/azureuser**.

## Objetivos del Desafío:

1. **Utilizar GitHub Copilot Workspace en la aplicación de Base de Datos de Contactos existente:**

   - Entienda y explore cómo funciona la función Workspace.

   - Proporcione algunos prompts al agente workspace en su espacio de trabajo de VS Code y revise sus salidas, como preguntar cosas relevantes relacionadas con su espacio de trabajo actual, generar nuevas funcionalidades, identificar problemas en cualquier archivo y más.
     >**Sugerencia:** Use las referencias de archivo **@workspace**, **@vscode** y **@terminal** para los prompts.

2. **Utilizar GitHub Copilot Workspace para crear una nueva aplicación React llamada Expense Tracker:**

   - Cree la estructura fundamental del espacio de trabajo desde cero usando la característica **GitHub Copilot Workspace** en `C:/Users/azureuser/DemoApp`.
     >**Sugerencia:** Solicite a Copilot que cree un espacio de trabajo para una nueva aplicación React llamada Expense Tracker con todos los archivos y el código necesarios.

   - Desarrolle los componentes individuales necesarios en el esquema de la aplicación Expense Tracker utilizando las capacidades de transformación de **GitHub Copilot**.
     >**Sugerencia:** Utilice la referencia de archivo **@workspace** para agregar funcionalidad a todos los archivos.

   - Depure todos los posibles errores que surjan al ejecutar la aplicación Expense Tracker utilizando GitHub Copilot Workspace.

   - Ejecute la aplicación en su sistema local correctamente. La aplicación debería ser similar al siguiente ejemplo:

      ![](../../media/app-working.png)

   <validation step="76e12adb-fdce-4aea-a013-b0f721a72995" />

   <validation step="2458065d-db29-4909-a6a8-6be48c96d04b" />

3. **Utilizar las capacidades de referencia de archivos:**

      - Entienda cómo GitHub Copilot hace referencia a los archivos en sus documentos y cómo ayuda con el flujo de código.

      - Proporcione algunos prompts que requieran que GitHub Copilot haga referencia a múltiples archivos en su proyecto de varios archivos y analice las referencias correctamente, es decir, proporcione prompts que describan los usos del archivo **index.js** en la aplicación **Expense Tracker** que construyó con anterioridad.

      - Proporcione dicho prompt utilizando referencias de archivos que integren el campo **Date** en el documento **ExpenseForm** en su **Aplicación Expense Tracker** y lo muestren en **ExpenseItem**, y entonces podrá ordenar los gastos por fecha en el componente **ExpenseList**.

      El resultado debería ser similar al que se muestra a continuación:

      ![](../../media/app-working-date.png)

## Criterios de Éxito:

- Asegúrese de que comprende el funcionamiento de GitHub Copilot Workspace y la referencia de archivos.

- Asegúrese de haber proporcionado correctamente los prompts pertinentes para probar el funcionamiento del agente del espacio de trabajo y la referencia de archivos.

- Compruebe que la aplicación Expense Tracker se esté ejecutando correctamente.

- Verifique las salidas generadas por sus prompts y su precisión.

- Verifique que el componente de fecha se haya agregado a su aplicación y esté funcionando correctamente.

## Recursos Adicionales:

- Consulte [aquí](https://githubnext.com/projects/copilot-workspace/) para obtener más información.

## Conclusión

En este desafío, ha adquirido una comprensión más profunda de cómo funcionan **Github Copilot Workspace y Referencias a Archivos** y cómo pueden mejorar su proceso de programación. Mediante el uso eficaz de estas características, puede mejorar significativamente su eficiencia de codificación y la calidad general de su código. Tanto si es un desarrollador experimentado como un principiante, estos conocimientos seguramente serán de gran utilidad en su proceso de programación.

### Haga clic en Siguiente >> para continuar con el próximo desafío.

![](../../media/next-page-spanish.png)
