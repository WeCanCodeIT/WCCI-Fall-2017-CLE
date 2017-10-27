# MVC Review Site Project
## Due: Monday October 30 2017 at 9:30am
### - [Submission Link](https://docs.google.com/forms/d/e/1FAIpQLScUEvl_ZgH_OgBu0zbg_WIvB6zBSkkXh7wfxqjv4LwLdBDxLg/viewform)

## Overview
For this project you will be developing an MVC application that uses multiple models and foreign keys to model a relationship. You have the choice to develop either a Technology Review site or a Travel Review site.

## Skills Required
- Intro to MVC
- Code First Model Design

## Tasks
- [ ] Create the following models
  - [ ] Review
  - [ ] Category
  - Note: Your Review model should have properties to properly represent all the fields you feel need to be represented in a review. This may include:
    - [ ] ID
    - [ ] Title
    - [ ] Content
    - [ ] Publish Date
    - [ ] Etc
- [ ] Content Requirements
  - [ ] Homepage (AKA Index.html inside your Home folder in Views)
    - Include a title for your website and a brief description. You can use lorem ipsum.
  - [ ] Reviews Index
    - Display all reviews.  Experiment with different ways of presenting the reviews. Follow the examples provided in class to customize your view. Do not use the default table layout.
  - [ ] Reviews Details
    - Attempt to make the Details View look like an Article or Card on a review site like Yelp. Customize styling so it is not default detail-list (dl, dt, dd) layout in the Details View.
- [ ] Styling requirements (For the Review views ONLY. Do not style the Category views)
  - [ ] Homepage
  - [ ] Reviews Index
  - [ ] Reviews Details
    - Note: Use what we’ve learned regarding CSS and Bootstrap to style the pages to your liking. Pages should no longer look like basic Bootstrap. Do not worry about styling the Create, Edit and Delete views initially. 
- [ ] Bootstrap Requirements
  - [ ] Navbar
    - User should be able to navigate to the Reviews Index and Categories Index from the homepage
  - [ ] Row(s)
  - [ ] Columns
- [ ] Recommended: Populate Categories table and Reviews table
  - Recommended: Three categories
  - Recommended: Five reviews
  - *NOTE*: Your categories and reviews will not be committed to Github because we have not yet introduced you to how to transfer database data to Github. Create these categories and reviews to practice, but be aware that the Education Team will be creating their own categories and reviews in your project in order to grade it.
- [ ] Documentation
  - [ ] Program should be commented throughout explaining the code
## Details
You should have at least two models and a foreign key relationship. Review the [Bookshelf](https://docs.google.com/a/wecancodeit.org/presentation/d/1C9v9Upx7NWePFbh5kO06GSQnuxdyeJwFVAWsTKHzgdw/edit?usp=sharing) for an example of a foreign key relationship. You should be able to view the styled home page, navigate to the reviews index, click a review and view a styled detail page.

RECOMMENDED: After your app is created populate the Categories table with at least 3 categories, and your Reviews table with at least 5 mock reviews. Feel free to fill them out Lorem Ipsum.

## Stretch Tasks
  - [ ] Add Unique images for each review
  - [ ] Style the Edit, Create, and Delete pages
  
## Hints
 - If you want to clean up your Reviews Index page, use CSS and Bootstrap to hide some of the fields, but show them in Details.   
   - So maybe you have a Title and an Author field that displays on the Index, but on the Details view you display a Title, Author, Review, and Score. Be creative!
 - Do not do *ANY* styling until you have a working application, including a working foreign key relationship!! Best practice is to include styling after you are sure that everything works.
 - This project may seem significantly more difficult than what we've done in class this week, but it is not. It does have more "moving parts", but it is actually not anything more than what you have seen thus far. Don't overthink it!
