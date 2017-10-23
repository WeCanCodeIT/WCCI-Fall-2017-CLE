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
