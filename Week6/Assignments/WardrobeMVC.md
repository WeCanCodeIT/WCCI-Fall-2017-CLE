# Wardrobe MVC
## Due: Due: Monday November 6 2017 at 9:30am
### - [Submission Link](https://docs.google.com/forms/d/e/1FAIpQLScUEvl_ZgH_OgBu0zbg_WIvB6zBSkkXh7wfxqjv4LwLdBDxLg/viewform)

## Overview
Create a web application for managing the contents of your wardrobe. The app will allow you to add, edit, view, and delete items in your closet.

## Skills Required
- Database First MVC

## Tasks
- [ ] Organization of clothing by type
  - [ ] Tops
  - [ ] Bottoms
  - [ ] Shoes
  - [ ] Accessories
- [ ] Model(s) must include the following properties
  - [ ] ID
  - [ ] Name
  - [ ] Photo
  - [ ] Type
  - [ ] Color
  - [ ] Season
  - [ ] Occasion
- [ ] Controllers
  - [ ] For each model
- [ ] Views
  - [ ] Customize layout for index & details pages to properly show the properties for the following:
    - [ ] Tops
    - [ ] Bottoms
    - [ ] Shoes
    - [ ] Accessories
  - [ ] Photo properly included where appropriate (index/detail)
  - [ ] Homepage should be updated for your app
- [ ] Bootstrap/CSS
  - [ ] Updated navbar
  - [ ] Thumbnails
  - [ ] At least 1 other Bootstrap component of your choice
  - [ ] Responsive layout (using Bootstrap grid)
  - [ ] Customize styling for all index and details pages
- [ ] Generate a SQL script for database (schema and data)

## Details
Design an app that will let you manage the contents of your closet. It should support several different types of clothing stored in your database:

- Tops
- Bottoms
- Shoes
- Accessories

Whether or not you store these as separate tables or a single table is up to you. You will need to have views that allow the user to focus on clothing by type, so keep that in mind when making your decision.

Each item of clothing will need to have the following properties kept with it:
- ID
- Name
- Photo
- Type
- Color
- Season
- Occasion

You need to determine the appropriate columns/constraints to use for all fields.

You should customize all of your views to develop the best user experience you can manage. Show photos when appropriate, but don't have them get in the way. Use Bootstrap effectively to make the app responsive for both desktops and mobile devices. Add your own styles to make it a little less "bootstrappy".

### Stretch Tasks
A natural progression of this app is to support the creation of outfits - a collection of coordinating tops/bottoms/shoes/accessories. Build this into your model, and create views for working with outfits.

Ultimately, your views should be integrated, so you can see all the pictures of each item per outfit.

## Hints
As usual, start with the model, and spend some time considering how many tables to create and how they will be related.

Use the scaffolded controller views to get going and put some data in your app, and then start to work on the index view(s) and making them look nice.

Always target MVP - and once you get there, figure out what the next MVP is!

Use dropdowns when you want to limit a user's possible choices. There's an HTML element that lets you do this!

For the photo, you should use an `nvarchar` column type, and put all photos in the `Content` folder of your project. Save a relative URL of the form `~/Content/myphoto.jpg`, and use that as the `src` of an `<img>` tag in your view file in the following format:
```
@Url.Content(Model.Photo)
```
Don't forget to add your .gitignore!!!
