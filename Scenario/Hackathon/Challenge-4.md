# Challenge 4: Using GitHub Copilot workspace and file reference

### Estimated Time: 60 minutes

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

> **Note**: Prerequisites are already set up in the CloudLabs-provided environment. If you're using your personal computer or laptop, please make sure that all necessary prerequisites are installed to complete this hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) installed in VS Code.

## Challenge Objectives:

1. **Utilize the GitHub Copilot Workspace in the existing Contact Database Application:**

   - Understand and explore how the Workspace feature works.

   - Give some prompts to the workspace agent in your VS Code workspace and review its outputs, like asking relevant things related to your current workspace, generating new functionality, identifying issues in any file, and more.

2. **Utilize the GitHub Copilot Workspace to create a new React app named Expense Tracker:**

   - Create the fundamental workspace structure from scratch using the **GitHub Copilot Workspace** feature in `C:/users/azureuser/DemoApp`.

   - Develop the individual components required in the Expense Tracker app outline using **GitHub Copilot's** transformative capabilities.

   - Debug all the possible errors coming out while running the Expense tracker app using the GitHub Copilot Workspace.

   - Run the application on your local system successfully. The application should be similar to the below example:

      ![](../../media/app-working.png)

   <validation step="76e12adb-fdce-4aea-a013-b0f721a72995" />

   <validation step="2458065d-db29-4909-a6a8-6be48c96d04b" />

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

### Challenge Validation
 
1. After completing the challenge, you need to visit the **Lab Validation (1)** tab and click on the **VALIDATE (2)** button under Actions to perform the validation steps. Verify that you have met the success criteria of the challenge. 
 
    ![azure](../../media/validate01.png)
 
1. If the validation status displays **SUCCESS** for all the validation steps, **congratulations!** This means that you have completed the challenge.
 
     ![azure](../../media/validate02.png)
   
1. If the validation status displays **FAIL**, **don't worry!** This could mean that you did not perform the challenge correctly.
 
     ![azure](../../media/validate03.png)
 
1. Hover your mouse over the **`i`** **(1)** icon to see the error message and determine the root cause of the failure. Based on the error message, revisit the challenge as necessary, and redo the validation by clicking on the **VALIDATE (3)** button again.
   
     ![azure](../../media/validate04.png)
   
1. If you are still having trouble, you can reach out to the support team via `labs-support@spektrasystems.com` for further assistance. The support team is available to help you troubleshoot and resolve any technical issues or validation issues that may arise while the lab environment is live.

## Conclusion

In this challenge, you have gained a deeper understanding of how **Github Copilot Workspace and File Referencing** function and how they can enhance your coding process. By effectively using these features, you can significantly improve your coding efficiency and the overall quality of your code. Whether you're a seasoned developer or a beginner, these insights will surely be valuable in your coding journey.
