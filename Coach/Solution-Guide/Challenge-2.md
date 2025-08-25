# Challenge 02: Develop an App with GitHub Copilot - Solution Guide

## Task 1: Develop an App

### Login to GitHub

- Login to [GitHub](https://github.com/login) with the CloudLabs provided GitHub account. Ensure that you are logged in to the correct GitHub account provided for this lab session.

### Fork the Repository

- Navigate to the provided GitHub repository link: [MyMvcApp-Contact-Databse-Application](https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application.git).

    ![](../../media/Repo-info.png)

- Fork the repository into the CloudLabs-provided GitHub account.

    ![](../../media/Fork-repo.png)

### Open Visual Studio and Clone the Repository

- Launch Visual Studio and click on "Clone Git repository".

   ![](../../media/Clone-Git-repo.png)

- Enter the Git Repository URL and click Enter

    ![](../../media/URL-Repo.png)

- The window will look like this.

    ![](../../media/Cloned-rep.png)


### Setting Up Visual Studio 2022

- In the Visual Studio, navigate and click on the **GitHub Copilot** option located at the top right and select **Install Copilot**.

    >**Note:** If **GitHub Copilot** forlder is not availble then create a new.

- In the Visual Studio Installer pane, make sure that the **GitHub Copilot** is selected and click **Install**. This will close the Visual Studio application.

- Wait for the GitHub Copilot extension to download completely (this might take a few minutes) and close the Visual Studio Installer pane.

  > **Note:** Ignore the error message 'Couldn't install Microsoft.Net.4.8.1.FullRedist', this won't affect the challenges.

- Re-launch the Visual Studio and verify that the GitHub Copilot is active. The GitHub Copilot Chat window can now be utlized.

- Once the repository is cloned, locate and open the `MyMvcApp.sln` file from the Solution Explorer.

  ![](../../media/MyMvcApp_ss.png)

- Navigate to Extentions 

  ![](../../media/Extension.png)

- Install **Nuget Gallery** and **C# Dev Kit**

  - Click on extensions on the left hand side.
  - Search for Nueget Gallery and C# Dev Kit
  - Click on install.

- Run the below command on the console.

    ```
    Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r
    ```

    ![](../../media/crud5.6.png)

### Implement Methods using GitHub Copilot

- Navigate to the `UserController.cs` file within the `Controllers` folder.

    ![](../../media/crud2.7.png)

- Use GitHub Copilot to generate code for each empty method in the `UserController.cs` file. To generate code for each empty method using GitHub Copilot, Select or highlight the lines of the empty method, and then right-click on the highlighted lines to open the context menu. 

    ![](../../media/crud1.2.png)
    ![](../../media/crud1.3.png)

- From the context menu, choose the "Ask Copilot" option. In the prompt box, type "Fill in the Index method"

    ![](../../media/crud1.4.png)

- GitHub Copilot will generate a code suggestion based on the context of the method. Review the suggestion provided by GitHub Copilot, and you can choose to accept or discard the suggestion based on its relevance to your requirements.

    ![](../../media/crud1.5.png)

- Repeat this process for each empty method in the UserController.cs file until all methods are implemented.

- Following these steps will allow you to efficiently utilize GitHub Copilot to generate code for each empty method in the UserController.cs file.

### Run and test the Application

- Locate the IIS Express button (a green play button) in the toolbar and click on it. This action starts the application on localhost in a web browser.

    ![](../../media/crud1.6.png)

- Once you run the application in a local web browser through IIS Express, then a couple of pop-ups will appear which will allow the application to run with a self-signed certificate that the IIS Express has generated.

    ![](../../media/ssl-yes.png)

    ![](../../media/ssl-yes01.png)

### Create a New Contact

- In the opened web browser, locate the "Create New" button and click on it.

    ![](../../media/crud1.7.png)

- Fill in the required fields for Name and Email in the form provided. Click on the "Create" button to submit the form and create a new contact.

    ![](../../media/crud1.8.png)

### Edit a Contact

- After creating a contact, return to the homepage.

- Find the contact you created in the list and locate the "Edit" button associated with it. Click on the "Edit" button.

    ![](../../media/crud1.9.png)

- Modify the existing details (Name or Email) as desired. Save the changes by clicking on the "Save" button.

    ![](../../media/crud1.10.png)

### Verify Details of a Contact

- Once again, return to the homepage.

- Locate the contact whose details you want to verify. Click on the "Details" button associated with that contact.

    ![](../../media/crud1.11.png)

- Verify that the displayed details match the information you entered earlier.

    ![](../../media/crud1.12.png)

### Delete a Contact

- From the homepage, find the contact you wish to delete.

- Click on the "Delete" button associated with that contact.

    ![](../../media/crud1.13.png)

- A confirmation dialog will appear asking if you're sure you want to delete the contact. Confirm the action.

    ![](../../media/crud1.14.png)

- Ensure that the contact is removed from the list after deletion.

    ![](../../media/crud1.15.png)

By following these steps meticulously, you can thoroughly test the CRUD (Create, Read, Update, Delete) functionalities of the application and ensure its proper functioning.

# Task 2: Generate Unit Test Cases

- To generate unit test cases, we need to add a new project. In the Solution Explorer, right-click on the Solution.

    ![](../../media/crud3.1.png)

- Click on Add, and then click on New Project.

    ![](../../media/crud3.2.png)

- Now search for Unit test in the search box, select the Unit Test Project (.Net Framework) and then click on Next.

    ![](../../media/crud3.3.png)

- Name the project Usercontrollertest and then click on Create.

    ![](../../media/crud3.4.png)

- Rename the UnitTest1.cs file to UserControllerTests.cs.

- Now let's ask Github Copilot Chat to generate test cases. Click on the "View" option on the top panel of Visual Studio. From the options, select "GitHub Copilot Chat" to open the GitHub Copilot Chat window.

    ![](../../media/crud3.5.png)

- Open the UserController.cs file and select/highlight the entire code in it.

    ![](../../media/crud3.6.png)

- Once the entire code is highlighted, in the Github Copilot Chat, provide a prompt as "generate unit test cases for usercontroller.cs"

    ![](../../media/crud3.7.png)

- Github Copilot will start generating unit test cases for the usercontroller.cs.

    ![](../../media/crud3.8.png)

- Now, copy the code provided by Github Copilot by clicking on the copy icon.

    ![](../../media/crud3.9.png)

- Remove the existing code and paste the code that we copied into the file.

    ![](../../media/crud3.10.png)

- Let us now add references to the project. Locate the References for UserControllertest and then right-click on it. Then click on Add Reference.

    ![](../../media/crud3.11.png)

- Now in the Projects, check the check box, and then click on OK.

    ![](../../media/crud3.12.png)

- Now let's fix the issues in the file by hovering the cursor at the Test Fixture and then clicking on either Ask Copilot (1) or Quick Actions and Refactoring... (2) features.
  
    ![](../../media/ask-copilot.png)

    ![](../../media/quick-actions.png)

- Click on "Install package NUnit" and then click on "Find and install latest version".

    ![](../../media/crud3.14.png)

- Similarly, hover the cursor on the controller.Index() click on Show potential fixes, and then click on "Install package 'Microsoft.ASPNet.Mvc'" and then click on "Use Local version '5.2.7'"

    ![](../../media/crud3.15.png)

- Again, for the RouteValues, hover the cursor and then click on show potential fixes, and then click on Add reference.

    ![](../../media/crud3.16.png)

- Again, for the Assert, hover the cursor and then click on show potential fixes and then click on ussing Assert.

    ![](../../media/crud3.17.png)

- After resolving all the issues in the file, you click on the Test option on the top panel of Visual Studio. Then click on Test Explorer. 

    ![](../../media/crud3.18.png)

- In the Test Explorer, click on the Run All button to run the test cases.

    ![](../../media/crud3.19.png)

- Verify that all the test cases have passed.

    ![](../../media/crud3.20.png)

# Task 3: Develop and Test Features

### Utilize GitHub Copilot Chat for Feature Development:
  
   - Click on the "View" option on the top panel of Visual Studio. From the options, select "GitHub Copilot Chat" to open the GitHub Copilot Chat window.
  
        ![](../../media/crud3.5.png)

### Ask GitHub Copilot Chat for Feature Implementation:
   
   - Initiate a conversation with GitHub Copilot Chat by asking, "How can we add a search feature/functionality to our application?"

        ![](../../media/crud4.1.png)

   - Based on the response generated by GitHub Copilot, proceed with implementing the suggested code.
  
   - In this case, GitHub Copilot suggested adding a new method to accept a search string as a parameter and filter the user list based on the search string before passing it to the view.

        ![](../../media/crud4.2.png)
  
   - Copy and paste the provided code snippet into the `UserController.cs` file within the appropriate action method, typically the `Index` method. In this code, if a searchString is provided, the user list is filtered to only include users whose names contain the searchString. If no searchString is provided, all users are returned.

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

   - GitHub Copilot also suggested modifying the `Index.cshtml` file located in the path **Views\User\Index.cshtml** to include a form for the search string.

        ![](../../media/crud4.4.png)

   - Copy and paste the provided code snippet into the `Index.cshtml` file. This form sends a GET request to the Index action method, passing the search string as a query string parameter.

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

### Save Changes and Run the Application:

   - Save both the `UserController.cs` and `Index.cshtml` files after making the necessary changes.

   - Run the application by clicking on the IIS Express button. This action starts the application on localhost in a web browser.

        ![](../../media/crud1.6.png)

### Test the Search Functionality:

   - Add a couple of contact entries to the application by clicking on the "Create New" button and filling in the Name and Email fields.

        ![](../../media/crud4.6.png)

   - Once contacts are added, test the search functionality by typing a contact name in the search field that was previously added. Click on the "Search" button to execute the search.

        ![](../../media/crud4.7.png)

   - If the feature was implemented properly, you should be able to see the searched contact in the results.

        ![](../../media/crud4.8.png)

By following these steps, you can effectively utilize GitHub Copilot to implement and test new features in your application, enhancing its functionality and usability.

# Task 4: Generating Commit Messages

The new Generated Commit Message feature uses GitHub Copilot AI to describe your code changes.  This makes writing descriptive and helpful commit messages as easy as clicking a button, and then adding your explanation.

- Locate the Git Changes and click on it.

    ![](../../media/crud5.1.png)

- Use the new “Add AI Generated Commit Message” sparkle pen icon in the Git Changes window to generate a suggestion.

    ![](../../media/crud5.2.png)

- GitHub Copilot will look at the file changes in your commit, summarize them, and then describe each change. You can then “Insert AI Suggestion” or “Discard.” Click on Commit All.

    ![](../../media/crud5.3.png)

- Once it is committed locally, click on Push to push the changes into the repository.

    ![](../../media/crud5.4.png)

Now, click on Next from the lower right corner to move on to the next challenge.

![](../../media/next-page.png)
