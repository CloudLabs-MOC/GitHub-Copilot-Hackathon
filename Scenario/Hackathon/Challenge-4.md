# Challenge 04: Using GitHub Copilot workspace and file reference

### Estimated Duration: 90 Minutes

## Introduction

As a software developer at **Contoso Ltd.**, a leading software development company, you are always looking for ways to enhance your coding efficiency and the overall quality of your code. After successfully exploring the basic features of **GitHub Copilot** and using it to develop and deploy an application to Azure, you now turn your focus to some of the advanced features of this AI-powered coding assistant.

In this challenge, you are specifically tasked with exploring and utilizing the three key features of the **GitHub Copilot**: the **workspace** and the **file reference**. Understanding and utilizing these features can significantly boost your productivity and efficiency in coding by providing more accurate, context-aware code suggestions.

- **GitHub Copilot Workspace:** **GitHub Copilot Workspace** is an advanced feature of **GitHub Copilot**, an AI-powered code completion tool. The workspace in GitHub Copilot refers to the current working directory where your code files reside.

   When you're coding, **GitHub Copilot** utilizes the information in your workspace to generate contextually relevant code suggestions. This means that it takes into account the specifics of your current project, such as the code files, libraries, and dependencies that are present in your workspace, to provide you with the most suitable code completions. This feature makes **GitHub Copilot** an intelligent coding assistant that not only understands the syntax and language semantics but also the context of your project, which results in more accurate and helpful code suggestions.
   By effectively using the **Workspace** feature, developers can improve their coding efficiency, reduce errors, and create higher-quality code.

- **File referencing in GitHub Copilot:** **File referencing in GitHub Copilot** refers to the AI's ability to understand and interpret the context of your project by considering the information in other files within your workspace.

   When you're working on a specific file in your codebase, **GitHub Copilot** can take into account the information, functions, classes, or variables defined in other files of your project. This means it doesn't just provide suggestions based on the current file you're working on; it can also reference other files to give you more accurate and relevant code completions. This feature is particularly useful when you're working on large projects where code is spread across multiple files. GitHub Copilot's ability to reference other files allows it to better understand the bigger picture of your project, resulting in more context-aware suggestions. This can significantly improve your coding efficiency and the overall quality of your code.

Whether you are a seasoned developer looking to enhance your coding efficiency or a beginner seeking to improve your coding skills, this lab will provide valuable insights into how **GitHub Copilot** can be a powerful tool in your coding journey. By the end of this challenge, you aim to demonstrate to **Contoso Ltd.** how these advanced features of **GitHub Copilot** can significantly enhance coding efficiency and the overall quality of code, further reinforcing the benefits of integrating AI into the development workflow. Let's get started!

## Prerequisites

Make sure you have the following from the CloudLabs-provided integrated environment:

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) installed in VS Code.

## Challenge Objectives:

1. **Utilize the GitHub Copilot Workspace in the existing Contact Database Application:**

   - Understand and explore how the Workspace feature works.

   - Use the same VS Code window which was created in Challenge 01 for the [CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application](https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application) GitHub repository.

   - Give some prompts to the workspace agent in your VS Code workspace and review its outputs, like asking relevant things related to your current workspace, generating new functionality, identifying issues in any file, and more.
     
     >**Hint:** Use **@workspace**, **@vscode** and **@terminal** file references for the prompts.

2. **Utilize the GitHub Copilot Workspace to create a new React app named Expense Tracker:**

   - Create a new folder named **DemoApp** in **C:/Users/azureuser**

   - Launch a new Visual Studio Code window and open the **DemoApp** folder inside the VS Code.

   - Create the fundamental workspace structure from scratch using the **GitHub Copilot Workspace** feature in `C:/Users/azureuser/DemoApp`.
     
     >**Hint:** Ask Copilot to create a workspace for a new Expense Tracker React application with all the necessary files and code.

   - Develop the individual components required in the Expense Tracker app outline using **GitHub Copilot's** transformative capabilities.
     
     >**Hint:** Use **@workspace** file reference to add functionality to all the files.

   - Debug all the possible errors coming out while running the Expense tracker app using the GitHub Copilot Workspace.

   - Run the application on your local system on port **3000** successfully. The application should be similar to the below example:

     > **Hint:** Use @workspace reference in GitHub Copilot chat window on how to run the app (expense tracker).

      ![](../../media/app-working.png)

      <validation step="76e12adb-fdce-4aea-a013-b0f721a72995" />

      <validation step="2458065d-db29-4909-a6a8-6be48c96d04b" />

   >**Note:** Provide the GitHub Username parameter in the **github-cloudlabsuser-XXXX** format while validating the task.


3. **Utilize the capabilities of file referencing:**

      - Understand how GitHub Copilot references files in your documents and how it helps with code flow.

      - Provide some prompts that require GitHub Copilot to reference multiple files in your multi-file project and analyze the references properly, i.e., provide such prompts that describe the uses of the **index.js** file in the **Expense Tracker** application you built earlier.

      - Provide such a prompt using file references that integrate the **Date** field in the **ExpenseForm** document in your **Expense Tracker Application** and display it in the **ExpenseItem**, and then you will be able to sort the expenses by date in the **ExpenseList** component.

      The output should be similar to what is given below:

      ![](../../media/app-working-date.png)

## Success Criteria:

- Make sure you understand the functioning of the GitHub Copilot Workspace and File Referencing.

- Make sure you successfully provided the relevant prompts to test the working of the workspace agent and file referencing.

- Verify that the Expense tracker application is running properly.

- Verify the outputs generated by your prompts and their accuracy.

- Verify that the date component is added to your application and working properly.

## Additional Resources:

- Refer [here](https://githubnext.com/projects/copilot-workspace/) for more information.

## Conclusion

In this challenge, you have gained a deeper understanding of how **Github Copilot Workspace and File Referencing** function and how they can enhance your coding process. By effectively using these features, you can significantly improve your coding efficiency and the overall quality of your code. Whether you're a seasoned developer or a beginner, these insights will surely be valuable in your coding journey.

### Now, click on Next from the lower right corner to move on to the next challenge.

   ![](../../media/next-page.png)



