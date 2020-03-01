# Intro to HTML and JavaScript

## It is important too keep in mind the different ways that people access the Web:
- **Browsers**
- **Web Servers**
- **Devices**
- **Screen Readers**

## How the web works, in 4 basic steps:
1. You connect to the web, via an *ISP* (Internet Service Provider).  Then you type in the web address or domain name that you wish to visit.
1. Your computer then contacts a network of servers called a *DNS* (Domain Name System).  The DNS acts like a phone book, relaying the *IP address* of the site you want to connect to, back to your computer (every device on the internet has their own unique IP address, and it works similar to a phone number).
1. The unique IP address the was returned to your computer via the DNS, then allows your computer to contact the *web server that hosts the website you want to visit.  A web server is a computer that is always connected to the web and is set up to send requested web pages to the users.
1. The web server sends the web page you requested back to your web browser.

## HTML- Hyper Text Markup Language

### Structure- HTML describes the structure of page.
### HTML pages are text documents, that hold all of the content to be displayed on your web pages.
- HTML code is made up characters that live inside of angled brackets. These are called **elements**, which *generally* consist of 2 **tags**, an opening and closing (the closing tag has an extra forward slash that signals the end of the element).  **Tags** act as containers, and tell you about the information that lies between them.
- **Attributes** tell additional information about the content of the elements.  The consist of a *name* and a *value* (value of an attribute should be in between double quotes) separated by an equal sign.  The majority of attributes can only be usd for certain elements, and generally their values are pre-defined.
- **Head and Body** are 2 main elements that make up your HTML document.
  - **Head** contains information about the page.  Generally will contain the **title** element, the title will be displayed in the top of the browser window (above the URL bar).
  - **Body** contains all of the content that will be displayed on your main browser window.
-  You can use *view source* or *source* which is contained in the *View* menu within your browser to see how other sites are built.

### Extra Markup
- **DOCTYPE**- There are a number of iterations of HTML, with HTML5 being the newest.  The DOCTYPE should *always* be declared on the first line of your HTML page. This is what it would look like \<!DOCTYPE html>.
- **Comments** in HTML- These would look like this \<!-- comment here -->.  The comment with in the tag will not be shown on the web page, but can be viewed within the source code.  It is a good idea to use comments so that when you revisit the code at a later point you will be able to better understand the code (also helps others who may be viewing your code).  Can also be used to prevent code from being displayed in the browser.  Also on long pages will help to indicate where sections start and end, or with notes explaining the code.
- **ID and Class** attributes allow you to identify particular elements.
  - **ID** Attributes- used to uniquely identify an element from other elements on the page.  They should be unique, meaning only assign an id attribute to one element.  Has a higher specificity or importance than a class attribute, so if both are applied with conflicting styles to an element, the id attribute will always be applied.  Known as a **global** attribute,because it can be used on any element.
  - **Class** Attributes- Allow you to target multiple elements to be different from other elements on the page, and can use multiple within the same element separated by a space.
- **Block** Elements- These elements will always appear to start on a new line.  Examples of these are \<h1>, \<p>, \<ul>, and \<li>.
- **Inline** Elements- These are elements that appear to continue on the same line as their neighboring elements. Examples of these are \<a>, \<b>, \<em>, and \<img>.
- Grouping Text and Elements in a Box- the \<div> element allows you to group a set of elements together inn one block level box.  Adding and id element helps to style with CSS.  Generally good practice to add a comment after the div end tag to highlight that the div element is complete (because the div element generally contains multiple elements).
- Grouping Text and Elements inline- the \<span> element is similar to the div element. The difference being that it allows you to either contain a section of text when there is not a more suitable element to differentiate it from the surrounding text.  Or it contains a number of inline elements.  Generally used to to control the appearance of the content with CSS.
- **Iframes** are like windows that are cut into your web page and allow other pages to be displayed.  A good example is when you embed navigation (Google Maps) into your page.  Requires 3 attributes: *scr* or the URL of the page your are displaying, *height* and *width* which will set the size of the frame in pixels.
- Information About Your Pages- \<meta> allows you to supply all kinds of information about your page.  The meta tag lives inside of the head element and is an empty element, meaning it does not require an end tag.  The most common attributes are the name and content attributes, which are generally used together.  
- Escape Characters-  These are used to include special characters in your web page. Examples of these characters are the ampersand, copyright symbol, register trademark, quotes (single and double), less than or greater than signs, etc.

### HTML5 Layout
HTML5 allows you set up your web page easier, by eliminating the need for so may \<div>.  Structure is as follows:
![Example of HTML](https://lh3.googleusercontent.com/proxy/EV7jlGdSLrRk6imDE4QpUFzMCdar_V3Zic6n41QsbIaPH5s8z9QFxj6QXjhGS6fDql1UjzlbglnxuVPIBB37PxkksCfxUSuh2Z6LEu0Rc6I)
- **Headers and Footers** \<header>\<footer>-  Header can be used various ways, but commonly it is used to hold the title, some navigation, and possibly a logo.  The footer often share info about the site (author, :copyright: date, privacy policies, etc.), it may also contain contact info or the sites connected social media, and also may have links to move around the page.
- **Navigation** \<nav>- This allows you to block together common themed links to important information.  Generally you will see it as a unordered list \<ul>, with \<a href=""> with in the list items \<li>
- **Articles** \<article>-  a container for info within a site that can stand alone as an independent piece of content.  Ideal for things like articles and blogs, which would sit within thier own \<article>.  Can nest articles within articles.
- **Asides** \<aside>- If used within an article, can contain info that is related to or supports that article.  If it is outside of an \<article>, it is a container for content of that entire page.
- **Sections** \<section>- groups related content together.  has a class attribute.
- **Heading Group** \<hgroup>-  is used to group together a set of 1 or more \<h1> elements.
- **Figures** \<figure> \<figcaption>- used to contain any content that is referenced from the main flow of an article.  Can be used for images, videos, graphs, diagrams, code samples, or just text that supports the main body.  The \<figcaption> should be a description of the content of the \<figure>.
- **Sectioning Elements** \<div>-  use when there is not specific sectioning element.
- **Linking around block-level elements** \<a>- this allows you block together child elements, and turn the entire content into a link.

### Process and Design
  - Who is the site for?-  Need to have a target audience.  - Need to understand who that is. Are you targeting individuals of companies?-
  - Why people will visit your website.  What aer their key **motivations** and specific **goals**.
  - What are the visitors to your site trying to achieve?  The key tasks and motivations, you wont be able to address every reason.
  - What information do visitors need?  You want them to be able to find the information quickly and effectively.  Are they familiar with your subject area/ brand, products/ services/ info?  What are your most important features that you offer?  Why are you special or what differentiates you?  FAQ are effective.
  - How often are people visiting your site?  How often people are visiting your site lets you know how often your site should be updated.  Focus on certain sections of your site where there is more traffic and keep that up to date.
  - **Site Maps**- A way of organizing your site to optimize flow for the users.  Separates information into sections or pages.
    - **Card Sorting**- involve putting each piece of info on a card and then grouping like info together.  Each group will relate to a page.
  Once the info is grouped into different sections you can the turn it into a diagram, which is your **site map**.  It is important to reflect the customers understanding of the subject.
  - **Wireframes**-  is a simple sketch of key info that need to go on each page of a site. This includes key elements such as : logo, prim. navigation, headings, main bodies of text, user logins, etc.  Ensures key info is not left out.  focuses just on content, creating a visual hierarchy to indicate the most important details.  Good to do before building a site to get the customers approval that all needs are met.  See page 463 for sources to do sketch on comp.
- Getting the message across with the use of design.
  - Content
  - Prioritizing- visual hierarchy * see below for description.
  - Organizing- grouping into blocks or chunks.  With similarity or consistency, very effective from a visual sense.  Headings, Proximity, Closure, Continuance, White Space, Color, Borders are ways this can be achieved.
- **Visual hierarchy**- The order to which eyes perceive what they see.  Most web users do not read entire pages.  Achieved through visual contrast.  Images offer a very attractive draw.
  - Size
  - Color 
  - Style
- Designing of Navigation- tells people where to go, but also what your site is about and how it is organized.
  - Concise
  - Clear
  - Selective
  - Context
  - Interactive
  - Consistent

## Intro to JavaScript
- **JAVASCRIPT** makes web pages more interactive by accessing and modifying content and markup used in web pages while it is being viewed in the browser.  It can make a page feel interactive by responding to what the user does.  JavaScript does this multiple ways:
1. *Access* to content- you can select any element, attribute or text from an HTML page.
1. *Modify* Content- you can add elements, attributes and text to the page, or just remove them.
1. *Program* rules- you can specify step for the browser to follow, which will allow it to access or change the content of your web page.
1. *React* to events- You specify a **script** to run when a specific event occurs.
- Examples of JavaScript in the browser are:
  - Slideshows
  - Forms
  - Reload part of a page
  - Filtering data
 
### **Script**- 
- Scripts are a series of instructions, similar to a recipe, handbook or manual, that the computer follows step-by-step to complete a desired task.  The browser may use different parts of the script depending on the interactions of the user.  Scripts can run different sections of the code dependant on the situation around them.
- **To write a script you need to first state your goal and then list the tasks that you need to be completed in order to achieve it.** 
  - It is just a series of short instructions, each of which is performed to solve a problem at hand.  **A computer doesn't learn how to perform tasks, It needs to follow instructions *every time* it performs the task.**  Must give enough detail to perform the task as if every time was its first time.
  - Start with the big picture of what you want to achieve, and then break that down to smaller tasks:
  1. Define the goal-  what is it that you want to achieve?
  1. Design the script- Define tasks that need to be performed, then list the steps required for each task.  You can use a *Flowchart* to work out how the tasks fit together, it shows the paths between each step.
  1. Code each step- Each step then needs to be written in a language a computer can understand, a code language
    - **Vocabulary**- words the computer will understand
    - **Syntax**- How to put words together to create instructions computers can follow.
  - **Programmatic** approach to problem-solving.  Computers follow a series of instructions, one after another.  Needs to be precise and detailed for the computer to properly achieve the goal you set out to achieve.  They can not learn or fill in the blanks.

### Computers create models of the world using data.
- **Objects** (Things)- physical things in the world are seen as an object.  Each object is made up of 3 things properties, events and methods, together they help to create a working model of that object.
  - **Properties** or characteristics-  Tells us abut the object. Each property has a *name* and a *value*
  - **Events**- Programmers choose which event the computer will respond to.  When a specific action occurs it can trigger a specific section of code to run.  Events can trigger methods.
  - **Methods**- The code for a method can contain lots of instructions that together make up one single task.  They can retrieve or update the values of an object' properties, and perform a task based on that information.
- How a browser sees a web page.
  1. Receives the web page as HTML code.
  1. Creates a model of the page and stores it in memory.  Each element creates its own *node* which is a kind of object.
  1. Uses a rendering engine to show the page on a screen.

### JAVASCRIPT is the behavior layer, or interactive layer of a  website.
- It si best to keep it in its own file (with a .js extension), just as you would with HTML and CSS, respectively.  
- It include buttons, dropdowns, media players, etc.
- It is added last and enhances the usability of the page or the experience of interacting with the site.  The site can work even if the JS does not, where as  without HTML \(the content layer) and CSS \(the presentation layer), your  site would not function.  The interaction between these 3 is called **progressive *enhancement**.  
- The HTML \<script> element is used in your HTML page to tell the browser to load the JavaScript file.
