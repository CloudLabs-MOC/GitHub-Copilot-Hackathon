# Challenge 02: Develop an App with GitHub Copilot

### Estimated Duration: 90 Minutes
  
## Introduction  

At **Contoso Ltd.**, a leading software development company, you, as a **software developer**, are given the task of exploring the capabilities of **GitHub Copilot**, an AI-powered coding assistant, and leveraging them in the company's software development process. The company believes that integrating AI into the development process can significantly enhance the efficiency and productivity of the development teams.

As part of this mission, you are assigned to develop a CRUD application named **MyMvcApp** using **GitHub Copilot**. The aim of this challenge is to understand the potential of AI in software development and to familiarize you with GitHub Copilot's capabilities. With the assistance of GitHub Copilot, you are expected to generate the necessary code, guided by the comments provided in the file. You will utilize GitHub Copilot at every stage of the development process, from generating code for empty methods to building essential features and testing the application thoroughly.

Throughout the challenge, you'll leverage Copilot's ability to understand context and provide relevant code suggestions. By engaging with Copilot Chat, you'll enhance collaboration and receive insightful coding recommendations, further enriching your coding experience.

By the end of this challenge, your goal is to have a fully functional **MyMvcApp CRUD Application**, developed mainly with the assistance of **GitHub Copilot**. Upon completion, you'll have not only developed a feature-rich application but also gained valuable insights into how AI can be seamlessly integrated into the development workflow. This hands-on experience with GitHub Copilot will empower you to explore its vast capabilities and unlock its potential in various development scenarios. This will demonstrate the potential of AI in software development and provide valuable insights into its practical implementation at **Contoso Ltd**.
  
## Prerequisites

Make sure you have the following from the CloudLabs-provided integrated environment:

- Basic understanding of the C# programming language
- GitHub account

## Creating a new GitHub Repository

1. Navigate to the already signed-in **GitHub homepage** and then click **Import repository**.

   ![](../../media/new/home.png)

1. Enter the following GitHub repository for the source URL to be imported:

   - `https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Database-Application`

   ![](../../media/new/github-import-repo.png)

1. Enter the following details while creating a new repository:

   - **Owner:** Select **Cloudlabs-Enterprises (1)**

   - **Repository name:** Enter the name **github-copilot-hack-<inject key="Deployment-id"  enableCopy="false"/> (2)**

   - **Visibility:** Choose **Internal (3)**.
   
   - Then click **Begin import (4)**.
  
     ![](../../media/new/github-begin-import.png)

1. After a few moments, the newly created repository will be ready for use.

   ![](../../media/new/github-import-new-repo.png)

## Setting up Visual Studio Code

1. Open a new Visual Studio Code window, under **Start**, click on the **Clone Git Repository...**.

   ![](../../media/new/7.png)

1. **Paste (1)** the **URL** that you had copied earlier in the search bar at the top of the **Visual Studio Code** and select **Clone from URL (2)** option.

   ![](../../media/new/clone-repo-url.png)

1. Choose the default folder to clone your GitHub repository locally and click **Select as Repository Destination**. 

   ![](../../media/new/select-folder.png)

1. If prompted with **Connect to GitHub** pop-up, click on **Sign in with your browser** under GitHub Sign in.

   ![](../../media/new/11.png)

1. Now, in the browser, click on **Authorize git-ecosystem**.

   ![](../../media/new/12.png)

1. Once you are logged in, you will get **Authentication Succeeded** message. You can now switch to IDE VS Code. 

   ![](../../media/new/13.png)

1. On VS Code, you will find a pop-up for confirmation **Would you like to open the repository?**, click on **Open**.

   ![](../../media/new/14.png)

1. Now you will see another screen, **Do you trust the authors of the files in this folder?**. Select the checkbox (1) **Trust the authors** and then click on **Yes, I trust the authors** (2). 

   ![](../../media/new/15.png)

1. Navigate to **Extentions** and ensure **Nuget Gallery** and **C# Dev Kit** extensions are installed.

## Challenge Objectives  

1. **Develop an app:** 

      - You will be creating a CRUD application named **MyMvcApp**, a C# application, with the help of **Github Copilot**, which will let the users save the contact details of people as per requirements and also carry out the basic functions like editing their details, deleting their profiles, and so on. You will be provided with the skeleton of the application already, but you will need to build the functionalities inside the **UserController.cs** file by yourself. Your task is to complete these methods by utilizing GitHub Copilot to generate the necessary code, guided by the comments provided in the file.

      - Use GitHub Copilot Agent mode to understand your context and provide relevant code suggestions.

      - Test the application thoroughly and ensure all functionalities work as expected.
  
        ![](../../media/challenge3-mymvcapp-localhost.png)

2. **Generate unit test case scripts and validate them**:

      - Run the below commands in command prompt to create a new folder named **MyMvcApp.Tests** in the parent directory for generating unit test cases.
        
        ```
        dotnet new xunit -n MyMvcApp.Tests
        ```

      - In your Visual Studio Code, locate the **MyMvcApp.Tests** folder in the Solution Explorer, right click and select **Open in integrated terminal**. Run the below command in the terminal to add the dotnet package.

        ```
        dotnet add package Microsoft.CodeDom.Providers.DotNetCompilerPlatform
        ```

      - Rename the **UnitTest1.cs** file to **UserControllerTests.cs** after creating the **MyMvcApp.Test** folder.
  
      - Run the below command in the terminal to add your **MyMvcApp.csproj** project as a reference to generate unit test cases for `UserController.cs`.

      - For each of the features in the **MyMvcApp** you built inside the **UserController.cs** file, generate unit test cases for the **UserControllerTests.cs** file by using **xunit** by utilizing **Github Copilot**.
  
        ```
        Generate test cases to UserControllerTests for the MyMvcApp.csproj app by using xunit
        ```

      - Run the required scripts generated by the **Github Copilot** and verify that all the unit test cases have passed.
  
        ```
        dotnet test
        ```

2. **Develop and test features:** 

      - Once the methods are completed, the next step is to develop and add a search feature/functionality to the application and test out this feature thoroughly.
        
      - Utilize GitHub Copilot to generate code snippets for building the search feature.

      - Test the application and make sure that the search functionality is working as expected.
  
        ![](../../media/challenge3-mymvcapp-search.png)

3. **Use GitHub Copilot at each stage of the challenge:** 

      - Use GitHub Copilot to assist in writing meaningful commit messages that clearly describe the changes made.

      - Throughout the development process, engage with Copilot Chat to enhance collaboration and receive insightful coding recommendations.
  
## Success Criteria  

- Verify that the methods in the `UserController.cs` file are completed successfully using GitHub Copilot.
- Verify that all the test cases generated by Copilot have passed.  
- Verify that the developed search feature is working as expected.    
- Make sure to successfully utilize GitHub Copilot to write commit messages.

## Additional Resources:

- Refer to the [GitHub Copilot Documentation](https://github.com/github/copilot-docs) for any clarifications or guidance during the challenge.
  
## Conclusion  

In this challenge, you've managed to develop a fully functional Contact Database application predominantly with the assistance of GitHub Copilot, demonstrating its practical usefulness in a real-world software development scenario.

You've successfully navigated through the development process, from generating code for empty methods in the UserController.cs file to building essential features for the application. You've utilized GitHub Copilot to understand your context and provide relevant code suggestions, enhancing your coding experience.

The engagement with Copilot Chat has enriched your collaboration and provided insightful coding recommendations, showcasing how AI can be seamlessly integrated into the development workflow. The test cases generated with GitHub Copilot's assistance have ensured the robustness and reliability of your application. Your achievements in this challenge have demonstrated the potential of AI in software development and provided valuable insights into its practical implementation. You've shown that with the right tools, such as GitHub Copilot, the development process can be made more efficient and productive.
  
## Now, click on Next >> from the lower right corner to move on to the next challenge.

![](../../media/next-page.png)
