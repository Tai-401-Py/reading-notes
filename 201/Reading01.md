
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

### Process and Design

[^1]: Flash is an outdated program that has since been discontinued from modern use. Some older sites may still use it, though older browsers are needed to read as most modern browsers will not display flash programs due to security risks. 
[^2]: HTML5 allows you to use uppercase attribute names and leave off quotation marks but is not reccomended. It is best practice to use all lowercase and always put value in quotes.
[^3]: Personal note - Content management system is a cool idea and would like to know more about creation of one.
[^4]: In practice no longer has any effect on how your site is indexed