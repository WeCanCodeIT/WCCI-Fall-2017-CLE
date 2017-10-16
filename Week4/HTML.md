## Topics
#### What is HTML & CSS?
- Structure & Syntax
- What role does HTML play in web development?
- What role does CSS play in web development?
- Internal Vs. External Vs. Inline Styling
- Classes & IDs

## Topics
- What is HTML and what is it used for?
- What is the syntax used?
- How do you setup an HTML document?
- Attributes
- Comments

#### Common HTML Elements
- Headings
- Paragraphs
- Links
- Images
- Lists
- Tables
- Div
- Form
  - Input
  - Button
  - Option
  - Textarea

#### Common HTML5 Elements
- Header
- Footer
- Section
- Nav

## Description
- HTML stands for HyperText Markup Language
- What's the difference between a markup language and a programming language?
- HTML is like the bones of the website
  - It's what allows us to add content to our webpages, such as text, images, videos, and links
- The syntax for HTML relies on the use of tags
- Tags are how we tell the browser what type of element or content we are adding to the webpage

- Let's look at tags more closely through the setup of an HTML file:

```html
<!doctype html>
<html>
<head>
  <title>

  </title>

</head>
<body>


</body>
</html>
```

- The tags we use to setup our HTML file are `!doctype html`, `html`, `head`, `title`, and `body`
- Excluding `<!doctype html>`, notice how there are 2 of each tag, one without a slash and one with the slash.
  - The tag, which is from angle bracket to angle bracket, that does NOT have a slash is called the opening or starting tag
  - The tag that DOES have the slash is called the closing or ending tag
  - From opening tag to closing tag is called the element
- Most tags require an opening and closing tag, but some, such as `<!doctype html>` only have one tag.
- Anything we want to be viewable on our webpage, must be added inside the `<body>`

#### Headings
- Let's add headings to our page:

```html
<h1>Hello World</h1>
<h2>Hello World</h2>
<h3>Hello World</h3>
<h4>Hello World</h4>
<h5>Hello World</h5>
<h6>Hello World</h6>
```

- `<h1>` elements are especially important because they improve SEO value.

#### Paragraphs
- Unlike headings, there is only one type of paragraph.

```html
<p>This is a paragraph</p>
```

- If you have a large block of text inside your paragraph tags, and you want there to breaks to make it appear as seperate paragraphs, you have 2 options:
  - Option 1: Place each paragraph within its own set of paragraph tags
  
  ```html
  <p>This is the first paragraph</p>
  <p>This is the second paragraph</p>
  ```
  
  - Option 2: This is not used as commonly, but you can also create a line break:
  
  ```html
  <p>
    This is the first paragraph.<br/>
    This is the second paragraph.
  </p>
  ```

#### Links
- Links will introduce us to something called an attribute
- Attributes are included in the opening tag of elements and gives more information to the browser about how the element should function.

```html
<a href="http://wwww.wecancodeit.org">Click Here</a>
```

- The tag is the `a` and it stands for anchor
- The attribute used with links is the `href` attribute and it tells the browser to what webpage it should take the user when the link is clicked
- `Click Here` is the innerHTML of the element. It is the text that will actually show up as the link.
- Note that all attributes follow the same syntax:
  - It starts with the name of the attribute (in this case it's `href`)
  - Followed by a `=` and a set of quotation marks (`" "`)
  - Inside the quotations marks will be the value that is appropriate to the attribute type (in this case, its the link address)
  
#### Images
- Images also have a required attribute called `src`
- The `src` attribute tells the browser where to get the image from (where the image is located)
- Images can be located on the internet (i.e. Google Images) or it can be located as a local file within your site
- Create an `images` folder to your solution and add an image inside the folder
- Now let's add the image to the webpage:
```html
<img src="images/profilepic.png" />
```
## Resources
- [W3Schools](https://www.w3schools.com/html/default.asp)
- [HTML Tutorial](https://tutorialehtml.com/en/html-tutorial-complete-html-guide/)
- [Tutorials Point](https://www.tutorialspoint.com/html/html_pdf_version.htm)

