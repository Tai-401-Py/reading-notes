
# INTRODUCTORY HTML AND JAVASCRIPT

---

## HTML

### Introduction

---

Reading notes depot 01. Notes on HTML and Javascript

HTML is the core language of the internet, it is the building blocks of the internet. 

- Browsers
  - Used to read HTML and display content on a monitor.
  - Often updated on the regular to support new code and features
    - Not everyone runs the latest software versions.

- Web Servers
  - Host the information to be read from.
  - Often times webpages outsourced to a web hosting platform who has their own servers.

- Devices
  - More people access the internet with various devices, as such it is important to rembember when designing a webpage.

- What you see
  - Browser interprets HTML and CSS to create visual content.
  - Most sites use Javascript and Flash [^1] to display extra content and give more functionality and interactivity to a page.

### Structure

---

Many web pages are set up to act like documents you would normally encounter in physical form. Structure is important in assisting the user identify and retreive the information they want.

- Structuring a word document
  - The use of headings and sub-headings help a user identify importance of information.
  - Each heading and sub-heading is usually expanded upon 

- Structuring web pages
  - In order to display content on web pages you must use HTML.
    - HTML is made up of **Elements** 
      - Elements consist of an opening `<..>` and closing tag `</..>`
      - Each elements content tells the browser what to do with the content between opening and closing tags.
    - **Tags** are containers that tell you what to do with the information contained between opening and closing `<p>`.
    - **Attributes** provide informationcabout the content of the tag. [^2]
      - Appear on the opening tag and consist of a *name* and a *value* seperated by an `=` sign  

- Coding in a content management system [^3]
  - Working within a larger hosting site, such as a blog or e-commerce site, even social media. You use content managment systems.
  - Useful to keep content consistant across numerous page with many users.
  - Has an advantage that even users without HTML knowledge can create content online.
  - Some allow more advanced users to alter templates.

NOTE: You can use a view source command by right clicking on most web pages to view content and code.

### Extra Markup

---

Because of several different itterations of HTML every webpage should start with a `<!DOCTYPE ()>` declaration to tell the browser which version to use.

Adding comments to HTML can be done with `<!--comment text-->`. This content will not be displayed to the viewer, they are important because when you come back to review the code later you will be able to better understand what you did. It is also helpful if someone else ever needs to look at it. 

Comments are often used on a  long page to indicate where certain sections start and stop. they are also useful for commenting out certain sections of code. 

**id** attributes are very helpful in identifying and styling specific sections of code. 

- Used to help identify and style an element differently than other content
- They can be used in JavaScript to interact with specific elements. 
- Are a global attribute and can be used on any element


**class** attribute can be added like the **id** attribute, to any element. 

- Should be used to group similar content


**block elements** will always appear to start a new line in the browser window

**inline elements** will always appear to continue using the same line as thier neigboring elements.

`<div>` Elements allow you to group a set of elements together in one block-level block

- Often paired with the **id** attribute for styling
- Can make it easire to navigate codes

`<span>` Elements are an inline equivalent of a `<div>` element.

- Contain a section of text where no other suitable element to differentiate from surrounding text
- Used to contain inline elements
- Used to finely control styling of inline elements

`<iframe>` element is like a little cutout window that can be used to view another webpage. 

- Short for "inline frame"
- must have **src, height, width** attributes
- Other attributes of an `<iframe>`
  - **scrolling** - not supported in HTML5
    - 3 values  **yes, no, auto**
  - **frameborder**
    - uses binary values **1 yes, 0 no**
  - **seamless**

`<meta>` elements live in the `<head>` element

- Contain info about webpage
- Fulfills a number of purposes
  - Telling search engines about page
  - Who created the page
  - Can also be used to make a page expire after a certain time
- attributes of a `<meta>` element
  - description : usually about a max of 155 char. Displayed in search engine results
  - keywords: used for indexing by search engines [^4]
  - robots: indicate yes or no for search engines to add. 
    - noindex to keep site off of search engines
    - nofollow can be used to add page but no linked pages
- http-equiv is also used in pairs with the following
  - author: defines author
  - pragma: prevents browser caching
  - expires: used to indicate when the page should expire note date must be specified as ex. below
    - "Fri. 04 Apr 2014 23:59:59 GMT"

Escape Characters are used to replace some of the reserved characters by HTML code such as the angled brackets.

### HTML 5 Layout

---

- Traditional layouts use `<div>` elements to group together related content using class or id attributes to indicate rols.
- modern layouts use some new elements such as `<header>` and `<nav>` in order to group content
  - these elemnts are significant due to search engine indexing and thier content replaces the keyword `<meta>` attribute.
  - screen readers also use this content in order to help navigate.

 `<header>` and `<footer>` elements

 - Used to contain differnet sections at the top and bottom of page

 `<nav>` element

 - Used to contain navigation elements


 `<article>` element

 - used to contain primary content on a site

 `<aside>` element

- Two uses depending on in or out of an `<article>` element
  - inside it is used for information related but not essential to overall meaning
    - outside it is for content related to entire page

`<section>` element

- groups related content together
  - each element typically has their own **class** attribute to identify content
  - may contain several `<article>` tags 
  - should not be used as a wrapper for whole page unless the page onl has one distinct piece of content. Though still best left to the `<div>` element

`<hgroup>` element

- Groups headings together so they are treated as one object
  - contriversial, as some devs do not like it and prefer to use `<p>` tags with an attribute indicating a subheading
  
`<figure>` `<figcaption>` element

- Should only be used when content simply references the element and not for something integral to page flow,

`<a>` element

- now can be used with a closing tag to turn an entire block-level element into a link. [^5]

Helping older browsers understand

- Older browsers will treat new elements like inline elements
  - You can help by including a line on css which states new elements should be rendered as a block
    - `header, section, footer, aside, nav, article, figcaption { display: block;}`
  - You can also use an HTML shiv by way of JavaScript for versions older than IE9 which is available through google.

### Process and Design

---

Desgining a site is one of the most important aspects, and should be catered to your audience. Not yourself or site owner.

- Consider that it is unrealistic to be able to cater a site to everyone. 
- Narrow down your target audience to a sample size.
- Create some fictional characters and their demographics and think about how they would use the site. To influence color and details.

Why are people coming to your site?

- Content and design should be influenced by the goals of your users. 
  - what are underlying motivations for users to visit
  - what is the goal of your visitor
    - these two are triggers for coming to the site
- Make use of your fictional demographics and create key tasks and motivations.

What your visitors need

- It is important to know what info your target audience needs to acheive thier goals quickly and effectively
  - Prioritize key info down to non-essential fluff
  - Ensuring content is what your visitors are looking for will make the site more relevant to them
  - Once they have determined relevancy then you can try and add the flulff and promote other items as well.
- Questions to ask
  - Are visitors familiar with brand/subject of site
  - Do they need background info on service.product
  - What are the most important features of what you're offering
  - What makes you different from competitors
  - Once people have acheived goal is there any extra info they need/can use
- How often do people visit the site
  - How often do you need to update site?
    - How frequently is the subject matter updated
    - How often do people return to your site for information and how can you make it more effective
    - Who is coming back, or is this a need once sort of info.

Site mapping

- Important to map out and group pages by content.
  - think more about how the public would use, not just yourself.
    - what makes sense to you may not make sense to the public.
- Wireframes
  - Rough layout sketch of where everything should go. 
  - When presenting most clients care about looks and may only raise issues about functionality once built
- visual hierarchy
  - items of high contrast like images usually processed first
- Similarity
  - we have a tendancy to group like visual things together
- Navigation
  - Should be clear, concise, and selective
    - Avoid crowding and group as much as you can
    - Lets user know where they are
    - Should be interactive
    - Should be consistent across all pages

## JavaScript

---

JavaScript is used to make pages more interactive and accessible.

- Access content on page
- Modify the content of a page
- Program rules or instructions the browser can follow
- React to events triggered by user

### What is a script and how do I create one?

---

A script is a series of instructions that computer follows to achieve a goal.

To write a script you first need to state your goal then list the tasks that need to be accomplished to acheive it. Every goal is just a larger one that needs to be broken down into smaller ones to achieve it. 

Writing a script is like writing a manual on how to do basic things one step at a time. Computers do not reactively learn, and can only do as thier told so must be given detailed enough instructions on how to perform the task correctly as if it was thier first time, every time.

1. Design your goal

  - Define the task you want to accomplish

2. Design the script

  - Split the goal intp a series of tasks
  - Write down individual steps to complete each task

3. Code Each Step

  - Write the instructions in a language the computer will understand

Computers think programatically they follow instructions one after another so you must think as such in order to acheive your goal. 

Flowcharts can be helpful in defining and designing a script.



[^1]: Flash is an outdated program that has since been discontinued from modern use. Some older sites may still use it, though older browsers are needed to read as most modern browsers will not display flash programs due to security risks. 
[^2]: HTML5 allows you to use uppercase attribute names and leave off quotation marks but is not reccomended. It is best practice to use all lowercase and always put value in quotes.
[^3]: Personal note - Content management system is a cool idea and would like to know more about creation of one.
[^4]: In practice no longer has any effect on how your site is indexed
[^5] Not really new but was seen as improper usage in previous versions of HTML.