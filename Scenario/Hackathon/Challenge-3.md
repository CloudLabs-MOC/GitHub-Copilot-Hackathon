# Challenge 03: Deploy the App to Azure

### Estimated Duration: 90 Minutes

## Introduction

In the previous challenge, you successfully developed a fully functional **MyMvcApp CRUD Application**, developed mainly with the assistance of **GitHub Copilot**, and also gained valuable insights into how AI can be seamlessly integrated into the development workflow.

As a software developer at **Contoso Ltd.**, a leading software development company, you are tasked with exploring innovative technologies and tools that can enhance the company's software development process and infrastructure management. **Contoso Ltd.** recognizes the potential of Infrastructure as Code (IaC) in managing and provisioning its computing resources and is particularly interested in Azure Resource Manager (ARM) templates for deploying applications to Azure.

In this challenge, you will utilize **GitHub Copilot** to streamline the development of an **Azure Resource Manager (ARM)** template to deploy the fully functional **MyMvcApp CRUD Application** that you developed earlier. ARM templates are Infrastructure as Code (IaC) files used to deploy and manage resources in Azure. By leveraging Copilot's code generation capabilities, you'll expedite the creation of an ARM template for deploying an application to Azure. In addition to this, you will also automate the build and testing processes of your code. You will create a GitHub Actions pipeline, with GitHub Copilot assisting in generating the necessary scripts. To document the knowledge and insights gained from this exercise, you will use **GitHub Copilot** to generate comprehensive and accurate documentation for this challenge. This documentation will serve as a guide for creating the ARM template, setting up the GitHub Actions pipeline, and deploying the fully functional **MyMvcApp CRUD Application** to Azure.

By completing this challenge, you aim to demonstrate to Contoso Ltd. how **GitHub Copilot** can streamline the development of ARM templates, automate build and testing processes with GitHub Actions, and generate insightful documentation. This will further highlight the value of integrating AI into the development workflow, following the successful development of the Contact Database application in the previous challenge.

## Prerequisites

Make sure you have the following from the CloudLabs-provided integrated environment:

> **Note**: Prerequisites are already set up in the CloudLabs provided environment. If you're using your personal computer or laptop, please make sure that all necessary prerequisites are installed to complete this hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) installed in VS Code.
- Make sure to deploy the web app in the existing resource group named **GitHub-Copilot-Challenges**.

## Accessing Azure Portal

1. To access the Azure portal, open a private/incognito window in your browser and navigate to **[Azure Portal](https://portal.azure.com)**.

1. On the **Sign in to Microsoft Azure** tab, you will see a login screen. Enter the following email/username and then click on **Next**. 

   * Email/Username: <inject key="AzureAdUserEmail"></inject>

1. Now enter the following password and click on **Sign in**.

   * Password: <inject key="AzureAdUserPassword"></inject>

1. If you see the pop-up **Stay Signed in?** click **No**.

1. If a **Welcome to Microsoft Azure** pop-up window appears, click **Cancel** to skip the tour.

1. Now you will see the Azure Portal Dashboard. Click on **Resource groups** from the navigate panel to see the resource groups.

1. Confirm you have a resource group **GitHub-Copilot-Challenges** present. You need to use the **GitHub-Copilot-Challenges** resource group throughout this challenge.

## Challenge Objectives:

1. **Develop an ARM template to deploy an app to Azure:**

   - Use GitHub Copilot to assist you in generating the initial structure of an ARM template for deploying the **MyMvcApp CRUD Application** to Azure.

   - Define the necessary Azure resources in the ARM template, that is, a **Web App** present in **Azure App Services** required to deploy your application.

   - Save the ARM template and parameters files as **deploy.json** and **deploy.parameters.json**. Deploy the ARM template to Azure in **Github-Copilot-Challenges** resource group.

2. **Generate a new GitHub repository secret and GitHub action workflow:**

      - Once the App Service deploys successfully, navigate to the App Service and **download the publish profile** from the **Overview** page, as you will need it to create the GitHub repository secret for workflow deployment authentication.
      
      - Navigate to your **github-copilot-hack-<inject key="Deployment-id"  enableCopy="false"/>** GitHub repository and add a **New repository secret** from repository **Settings → Secrets and variables → Actions → Repository Secrets**.
  
        - Name: **AZURE_WEBAPP_PUBLISH_PROFILE**
        - Secret Value: Paste the complete Azure App Service publish profile XML content downloaded from the Azure portal.
        
      - Download and save the below `deploy-webapp.yml` worflow file and save it in the **`.github/workflows/deploy-webapp.yml`** path within your **github-copilot-hack-<inject key="Deployment-id"  enableCopy="false"/>** GitHub repository.
  
        - Workflow file: https://experienceazure.blob.core.windows.net/templates/github-copilot-hackathon-new/deploy-webapp.yml
       
      - Update the `deploy-webapp.yml` worflow file with the following input values:
  
        - webAppName: **<YOUR_APP_SEVICE_NAME>**
        - resourceGroupName: **Github-Copilot-Challenges**

3. **Get the app working on Azure:**

      - Verify that the GitHub Actions pipeline build has succeeded and the app is working as expected through the Web App.
        
         ![](../../media/challenge3-web-app-001.png)

      - Verify that the deployed resources match the specifications outlined in your ARM template and that the application is working from the Azure Web App's **Default Domain**.

4. **Generate documentation with Copilot for the app:**

      - Use GitHub Copilot Chat to assist you in generating detailed and accurate documentation specifically for this challenge.

      - Create an MD file in your **MyMvcApp-Contact-Database-Application** GitHub repository as a **README.md** file on the **master** branch. This will act as a guide in creating an ARM template to deploy the app and the GitHub actions pipeline workflow file.

## Success Criteria:

- Verify that the web app from Azure App Services containing your application code is present in Azure.
- Verify that the Github action pipeline was created successfully.
- Verify that the **MyMvcApp CRUD Application** is deployed successfully on Azure and test the functionality.
- Verify that the documentation was created successfully.

## Additional Resources:

- If you encounter any challenges or have questions, refer to the [GitHub Copilot Documentation](https://github.com/github/copilot-docs) for guidance.

## Conclusion

In this challenge,  you've demonstrated how AI can significantly aid in the development and deployment of applications, specifically through the use of GitHub Copilot. Not only did you develop a fully functional Contact Database application in the previous challenge, but you also effectively deployed it to Azure using an ARM template generated with the help of GitHub Copilot. You've utilized GitHub Copilot to streamline the creation of the ARM template, which is a powerful example of Infrastructure as Code (IaC), and also automated the build and testing process of your code by creating a GitHub Actions pipeline, with GitHub Copilot assisting in generating the necessary scripts. Furthermore, you've produced comprehensive and accurate documentation for this challenge, serving as a valuable guide for future projects.

Through this challenge, you've showcased to Contoso Ltd. the potential of integrating AI into the development workflow. You've demonstrated how GitHub Copilot can aid in not only the development of applications but also in the deployment and management of infrastructure, thus highlighting its versatility and value. By successfully deploying the Contact Database application to Azure and verifying its functionality, you've provided a tangible demonstration of the benefits of AI in software development.

## Now, click on Next >> from the lower right corner to move on to the next challenge.

![](../../media/next-page.png)
