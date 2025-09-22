# Challenge 2: Develop an App with GitHub Copilot - Solution Guide

## Task 1: Develop an App

In this task you will be creating and testing a Contact Database MVC application using GitHub Copilot in Visual Studio. It involves forking and cloning a repository, configuring extensions, generating controller methods with Copilot, and running the application. Finally, CRUD operations create, read, update, and delete are tested to ensure proper functionality.

### Login to GitHub

1. Login to [GitHub](https://github.com/login) with the CloudLabs provided GitHub account. Ensure that you are logged in to the correct GitHub account provided for this lab session.

### Fork the Repository

1. Navigate to the provided GitHub repository link: [MyMvcApp-Contact-Databse-Application](https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application.git).

   ![](../../media/Repo-info.png)

1. **Fork** the repository into the CloudLabs-provided GitHub account.

   ![](../../media/Fork-repo.png)

### Open Visual Studio Code and Clone the Repository

1. Open the File Explorer and create a folder named **GitHub Copilot** in **C:\Users\azureuser**. 

1. Launch Visual Studio and click on **Clone Repository**.

   ![](../../media/CloneRepo.png)

1. In the search bar, enter the **Git Repository URL** and click Enter.

   ![](../../media/CloneURL.png)

1. Select the **GitHub Copilot** folder in **C:\Users\azureuser** as the repository destination and click **Slect as Repository Destination**.

   ![](../../media/Folder.png)

1. The window will look like this.

   ![](../../media/Cloned-rep.png)

### Setting Up Visual Studio Code

1. Navigate to **Extensions**. 

   ![](../../media/Extension.png)

1. Install **Nuget Gallery** and **C# Dev Kit**

   - Click on the extension on the left-hand side
   - Search for NuGet Gallery and C# Dev Kit
   - Click on **Install**, and post this; the extensions should be installed.

      ![](../../media/NuGet.png) 
   
      ![](../../media/CAPP.png)

### Implement Methods using GitHub Copilot
 
1. Navigate to the **UserController.cs** file within the **Controllers** folder.

   ![](../../media/ABC.png)

#### Scenario 1
 
1. Use GitHub Copilot to generate code for each empty method in the `UserController.cs` file. To generate code for each empty method using GitHub Copilot, select or highlight the lines of the empty method, and then right-click on the highlighted lines to open the context menu.
 
   ![](../../media/Ex1.png)
 
1. From the context menu, choose the **Generate Code (1)** option and click on **Fix (2)**.
 
   ![](../../media/fix2.png)
 
1. GitHub Copilot will generate a code suggestion based on the context of the method. Review the suggestion provided by GitHub Copilot, and you can choose to **Accept** or **Discard** the suggestion based on its relevance to your requirements.
 
   ![](../../media/Exxxx4.png)
 
#### Scenario 2
 
1. Use GitHub Copilot to generate code for each empty method in the `UserController.cs` file. To generate code for each empty method using GitHub Copilot, select or highlight the lines of the empty method, and then right-click on the highlighted lines to open the context menu.

   ![](../../media/Ex1.png)
 
1. From the context menu, choose the **Open Inline chat**.
   
   ![](../../media/inline.png)
     
1. GitHub Copilot will generate a code suggestion based on the context of the method. Review the suggestion provided by GitHub Copilot, and you can choose to **Accept** or **Discard** the suggestion based on its relevance to your requirements.
 
   ![](../../media/accept.png)
 
#### Scenario 3
 
1. Use GitHub Copilot to generate code for each empty method in the `UserController.cs` file. To generate code for each empty method using GitHub Copilot.
 
1. Open GitHub Copilot chat and ask Copilot to **Generate the code for UserController.cs file**.

   ![](../../media/result.png)
 
1. Copy the code and replace it in the `UserController.cs` file.
 
1. Following these steps will allow you to efficiently utilize GitHub Copilot to generate code for each empty method in the `UserController.cs` file.

### Run and test the Application

1. Locate the app file **MyMvcApp.csproj** and right click **Open in Integreted Terminal**.

   ![](../../media/OpenTerminal.png)

1. Run the command below to run the application on the local host. 

    ```
    dotnet run
    ```

1. A successful run will look like this.

   ![](../../media/Coderun.png)

1. Once the code runs and the build is successful, you can navigate to the **URL** for the app.
  
   ![](../../media/apprun.png)

### Create a New Contact

1. In the opened web browser, locate the **Create New** button and click on it.

   ![](../../media/crud1.7.png)

1. Fill in the required fields for **Name (1)** and **Email (2)** in the form provided. Click on the **Create (3)** button to submit the form and create a new contact.

   ![](../../media/crud1.8.png)

### Edit a Contact

1. After creating a contact, return to the homepage.

1. Find the contact you created in the list and locate the **Edit** button associated with it and click on it.

   ![](../../media/crud1.9.png)

1. Modify the existing details (Name or Email) as desired. Save the changes by clicking on the **Save** button.

   ![](../../media/crud1.10.png)

### Verify Details of a Contact

1. Once again, return to the homepage.

1. Locate the contact whose details you want to verify. Click on the **Details** button associated with that contact.

   ![](../../media/crud1.11.png)

1. Verify that the displayed details match the information you entered earlier.

   ![](../../media/crud1.12.png)

### Delete a Contact

1. From the homepage, find the contact you wish to delete.

1. Click on the **Delete** button associated with that contact.

   ![](../../media/crud1.13.png)

1. A confirmation dialog will appear asking if you're sure you want to delete the contact. Click on **Delete**.

   ![](../../media/crud1.14.png)

1. Ensure that the contact is removed from the list after deletion.

   ![](../../media/crud1.15.png)

By following these steps meticulously, you can thoroughly test the CRUD (Create, Read, Update, Delete) functionalities of the application and ensure its proper functioning.

# Task 2: Generate Unit Test Cases

This task involves generating and running unit test cases for the Contact Database MVC application. You create a new xUnit test project, add necessary packages and references, and rename the test file. Using GitHub Copilot, you generate test cases for UserController.cs, execute them with dotnet test, and validate results.

1. Run the commands below in the command prompt to create a new folder named **MyMvcApp.Tests** in **C:\Users\azureuser\GitHub Copilot** for generating unit test cases.

   ```
   cd C:\Users\azureuser\GitHub Copilot
   ```

   ```
   dotnet new xunit -n MyMvcApp.Tests
   ```

1. In your Visual Studio Code, locate the **MyMvcApp.Tests** folder in the Solution Explorer, right click and select **Open in integrated terminal**. Run the command below in the terminal to add the dotnet package.

   ```
   dotnet add package Microsoft.CodeDom.Providers.DotNetCompilerPlatform
   ```

1. Locate the **MyMvcApp.Tests** folder in the Solution Explorer and rename the **UnitTest1.cs** file to **UserControllerTests.cs**.
  
   ![](../../media/Newfile.png)

1. Run the below command in the terminal to add your **MyMvcApp.csproj** project as a reference to generate unit test cases for `UserController.cs`.

   ```
   dotnet add reference ../MyMvcApp-Contact-Database-Application\MyMvcApp.csproj
   ```

   ![](../../media/prom.png)

1. In the **Github Copilot chat** window, ask the GitHub Copilot to `Generate test cases to UserControllerTests for the MyMvcApp.csproj app by using xunit`.

   ![](../../media/Genetest.png)

1. Copy the code generated by Copilot in the **UserControllerTests.cs** file, which will be similar to the code below.

   ```
    using Xunit;
    using Microsoft.AspNetCore.Mvc;
    using MyMvcApp.Controllers;
    using MyMvcApp.Models;
    using System.Collections.Generic;
    using System.Linq;

     namespace MyApp.Tests
      {
         public class UserControllerTests
      {
         private UserController _controller;
 
         public UserControllerTests()
         {
             // Initialize UserController with an empty list for each test
             UserController.userlist = new List<User>();
             _controller = new UserController();
         }

         [Fact]
         public void Index_ReturnsViewResult_WithAListOfUsers()
         {
             // Arrange
             UserController.userlist.Add(new User { Id = 1, Name = "Test User 1", Email = "test1@example.com" });
             UserController.userlist.Add(new User { Id = 2, Name = "Test User 2", Email = "test2@example.com" });

             // Act
             var result = _controller.Index();

             // Assert
             var viewResult = Assert.IsType<ViewResult>(result);
             var model = Assert.IsAssignableFrom<IEnumerable<User>>(viewResult.Model);
             Assert.Equal(2, model.Count());
         }

         [Fact]
         public void Details_WithUnexistingId_ReturnsNotFound()
         {
             // Act
             var result = _controller.Details(99);

             // Assert
             Assert.IsType<NotFoundResult>(result);
         }

         [Fact]
         public void Details_WithExistingId_ReturnsViewResult()
         {
             // Arrange
             UserController.userlist.Add(new User { Id = 1, Name = "Test User", Email = "test@example.com" });

             // Act
             var result = _controller.Details(1);

             // Assert
             var viewResult = Assert.IsType<ViewResult>(result);
             var model = Assert.IsType<User>(viewResult.Model);
             Assert.Equal(1, model.Id);
         }

         [Fact]
         public void Create_PostValidUser_RedirectsToIndex()
         {
             // Arrange
             var user = new User { Id = 1, Name = "New User", Email = "new@example.com" };
 
             // Act
             var result = _controller.Create(user);

             // Assert
             var redirectToActionResult = Assert.IsType<RedirectToActionResult>(result);
             Assert.Equal("Index", redirectToActionResult.ActionName);
             Assert.Single(UserController.userlist);
         }

         [Fact]
        
         public void Create_PostInvalidUser_ReturnsViewWithModel()
         {
             // Arrange
             _controller.ModelState.AddModelError("Name", "Required");

             // Act
             var result = _controller.Create(new User());

             // Assert
             var viewResult = Assert.IsType<ViewResult>(result);
             Assert.False(viewResult.ViewData.ModelState.IsValid);
         }
       }
    }
   ```

   ![](../../media/Testfilegene.png)
    
1. Right-click on the current project **MyMvcApp.Tests**, then select **Open in the Integrated terminal**.

   ![](../../media/Opengene.png)

1. Run the command below in the terminal to fetch the unit test results.

   ```
   dotnet test
   ```

   ![](../../media/RunGene.png)

# Task 3: Develop and Test Features

This task focuses on enhancing the Contact Database application by implementing a search feature with GitHub Copilot. You update the UserController.cs and Index.cshtml files to enable search functionality, run the application, and test the feature. This demonstrates Copilot’s usefulness in adding new, user-friendly features efficiently.

### Utilize GitHub Copilot Chat for Feature Development:
  
1. Open the GitHub Copilot chat window by slecting the **Toggle chat (1)** drop-down and select **Open chat (2)** to open the GitHub Copilot Chat window.

      ![](../../media/togchat.png)

### Ask GitHub Copilot Chat for Feature Implementation:
   
1. Initiate a conversation with GitHub Copilot Chat by asking, **How can we add a search feature/functionality to our application?**

   ![](../../media/function.png)

1. Based on the response generated by GitHub Copilot, proceed with implementing the suggested code.

   >**Note:** The generated code made vary from the screenshots provided.

1. In this case, GitHub Copilot suggested adding a new method to accept a search string as a parameter and filter the user list based on the search string before passing it to the view.

   ![](../../media/Copilotanswer.png)

1. Copy and paste the provided code snippet into the `UserController.cs` file within the appropriate action method, typically the `Index` method. In this code, if a searchString is provided, the user list is filtered to only include users whose names contain the searchString. If no searchString is provided, all users are returned.

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

   ![](../../media/Addsearch.png)

1. GitHub Copilot also suggested modifying the `Index.cshtml` file located in the path **Views\User\Index.cshtml** to include a form for the search string.

1. Copy and paste the provided code snippet found in the Copilot chat into the `Index.cshtml` file. This form sends a GET request to the Index action method, passing the search string as a query string parameter.

   ```
   @using (Html.BeginForm("Index", "User", FormMethod.Get))
   {
      <p>
       Find by name: @Html.TextBox("searchString") 
       <input type="submit" value="Search" />
      </p>
    }
   ```

   ![](../../media/Indexcode.png)

### Save Changes and Run the Application:

1. Save both the `UserController.cs` and `Index.cshtml` files after making the necessary changes.

1. Run the application by clicking on Terminal and by the command **dotnet run**. This action starts the application on **localhost** in a web browser.

   ![](../../media/runsearch.png)

### Test the Search Functionality:

1. Add a couple of contact entries to the application by clicking on the **Create New** button and filling in the **Name** and **Email** fields.

   ![](../../media/crud4.6.png)

1. Once contacts are added, test the search functionality by typing a contact name in the search field that was previously added. Click on the **Search** button to execute the search.

   ![](../../media/crud4.07.png)

1. If the feature was implemented properly, you should be able to see the searched contact in the results.

   ![](../../media/crud4.8.png)

By following these steps, you can effectively utilize GitHub Copilot to implement and test new features in your application, enhancing its functionality and usability.

## Conclusion  
In this challenge, you've managed to develop a fully functional Contact Database application predominantly with the assistance of GitHub Copilot, demonstrating its practical usefulness in a real-world software development scenario.
You've successfully navigated through the development process, from generating code for empty methods in the UserController.cs file to building essential features for the application. You've utilized GitHub Copilot to understand your context and provide relevant code suggestions, enhancing your coding experience.

The engagement with Copilot Chat has enriched your collaboration and provided insightful coding recommendations, showcasing how AI can be seamlessly integrated into the development workflow. The test cases generated with GitHub Copilot's assistance have ensured the robustness and reliability of your application. Your achievements in this challenge have demonstrated the potential of AI in software development and provided valuable insights into its practical implementation. You've shown that with the right tools, such as GitHub Copilot, the development process can be made more efficient and productive.

### Click on Next >> to proceed with the next challenge.

   ![](../../media/next-page.png)
