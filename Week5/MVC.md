# Intro to MVC
## Description
- What does MVC stand for?
- Why use MVC?
- When should MVC be used?
- What are the steps to creating an MVC project?
- What role does the Model play?
- What role does the View play?
- What role does the Controller play?
- What is Razor?

### What is MVC?
- MVC is a way we can design our web applications. Web applications are most website you visit that have interactivity. Things such as a login, the ability to save information, a page that changes depending on your settings of different factors. Those are all good signs of a web application.(We'll dig more into the definition later.)
- There are many different ways to design web applications. But as we build larger and larger applications we need a better way to manage them. Without MVC we might be left hundreds of unique files to edit and manage to get the functionality we like.
- MVC takes a large application and splits it into three distinct parts. The **M**odel, the **V**iew, and the **C**ontroller. This is where we get our acronym MVC from. Each of the three parts as a specific purpose, there isn't much overlap so it allows our applications to be segmented my purpose.
- Separating out application into distinct parts does a few things. First it allows us to simply our code. Rather than looking everywhere it allows us to look in part that matches the functionality we're looking for. Next it allows us to reuse our code. Instead of writing unique code for each part, we can write more generalized and reuse the code where appropriate. Often times at large organizations a separate team may be responsible for the Model, the view, and the controller.
- Now lets look at what each one of these parts does in detail.


### Model
- The model handles all of the data and contains business logic.
  - For example, the classes you create for your application (with attributes and methods) belong in the model.
- The *Model* represents what is being displayed. If you check your email via Gmail (or a similar web client), the {content} of your emails represents the model.

### View
- The *View* is how the model is shown to the user. The interface you're looking at when you're checking Facebook, including its styling (fonts, borders, etc) represent the view. Different people checking their Facebook will see the same interface, but different content. Their feeds are unique. Different people will see the *same* view but *different* models.
- This is the front end of the application where HTML, CSS, JavaScript languages belong.

### Controller
- The controller is responsible for controlling the flow of the program.
  - The controller controls the interactions between the models and views. It's the "intermediary" in between the model and view.
- The *Controller* is the glue that holds the two together. When you want to create or delete an email in your email client, you're sending a message to the controller. It is responsible for updating the model (creating or deleting the email), then refreshing the view (showing you what you see on the screen).


## Show It
- Let's walk through [creating an ASP.NET MVC Web Application](https://docs.google.com/presentation/d/1yqn9NZOcxetfKugCa_jkCg2vbTnDQMY14IVDMBR9mqA/edit?usp=sharing)
- Take a moment to let students explore what's in each of the folders.
- App_Start Folder
  - Here you will find config files. Let's look specifically at the `RouteConfig.cs` file. Double click on it to open it.
  - You will define the routes and those routes will map URLs to a specific controller action.
  - An action is just a method on the controller. 
  - It can also pick parameters out of that URL and pass them as parameters into the method.
  - This route that is defined in the application is the default route. 
  - When you see a URL arrive in the form of (something)/(something)/(something), then the first piece is the controller name, second piece is the action name, and the third piece is an ID parameter.
  - Let's see what happens when you change `defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }` from Index to About, like so: `defaults: new { controller = "Home", action = "About", id = UrlParameter.Optional }`
    - The new default route is the About page instead of the Index page. Have students save and run the app to see for themselves.
    - Now have students on their own change the homepage/default route back to the Index page.
- Content Folder
  - The content folder holds the Bootstrap files as well as the Site.css file.
- Controllers Folder
  - The controllers folder holds all of the MVC controllers. Let's look at the `HomeController.cs`.
  - Notice it has methods that return the view for each of the pages of our application.
- Models Folder
  - The models folder has all of the classes for the data or business logic of the application.
  - Ask the students where they think the Account and Identity classes came from?
- Views Folder
  - Inside the Views folder, you will find a subfolder for each of the Controllers (Home, Account, Manage) plus a Shared folder.
  - Let's first look at `Index.cshtml` and then run the page. See what it is rendered in the browser. There is body content, but also a navbar.
  - Have the students delete everything in the `Index.cshtml` except for the first few lines that include:
  ```
  @{
    ViewBag.Title = "Home Page";
  }
  ```
  - Now have the students save and run the app. Notice what's left. Have students explore and try to figure out where the navbar is coming from.
  - Now, have students open the Shared Folder inside Views. Double-click on `_Layout.cshtml` 
  - The Layout page is like a template. It holds all of the other information, such as the Head section, Navbar, and Footer that we want to be applied to all views. 
  - Look for `@RenderBody()` on the Layout page.
  - `RenderBody()` is where the content of each of the Views, such as Index or About is placed with respect to the Layout page.   
- Scripts Folder
  - This folder holds all of the JavaScript and jQuery files.
  
  ## Show It
### Razor
- Razor isn't an entirely new language, it simply means "we're executing this C# in the view to create some additional HTML". If we think about a social media site, this is how each user has a separate feed based on the users or topics they follow.

- A section of razor code is started with an `@` symbol. You can think of this as a _switch_ that causes the rest of the line. For example: 
```csharp
@Html.DisplayFor(modelItem => item.Details)
```

- If an `@` symbol is placed in front of curly brace, the section between the opening and closing closing curly brace will all be razor. This allows us to have multiple lines of razor. For example: 
```csharp
@{
    ViewBag.Title = "Index";
}
```

- We can also use razor to call methods. Most commonly you'll see razor used to called HTML helper methods, we'll cover these in more detail later as well. These are methods that can make web programming a lot more convenient. You can place an `@` in front of a method call and everything up util the end of the method will be razor. This allows us to insert razor in our HTML. For example, the following Razor method will produce HTML that will populate the href attribute of a link: 
```csharp
   <a href="@Url.Action("ToggleDone", new {id = item.ItemID})">
``` 

### MVC In-Class Projects

[Suggestion Box](https://docs.google.com/presentation/d/1FX787R7R9UrSFlbf6RnrRObsaqW_5yXV1TiFsycxEWY/edit?usp=sharing)

[Migrations Walkthrough](https://docs.google.com/presentation/d/14Mf60EoUVF5ple2oUwMZKpspd2Bk8QFbJXazMCHWQcg/edit?usp=sharing)
