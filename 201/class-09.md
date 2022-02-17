# Class 09 Reading Forms and Events

---

## Forms

Form controls

- Adding Text
  - Text input
  - Password Input
  - Text Area
    - multi line
- Making Choices
  - Radio Buttons
  - Check Boxes
  - Drop-down
- Submitting Forms
  - Submit Buttons
  - Image Buttons
  - File Uploading

### Form Structure

- `<form>` - Every form requires an `action="` attribute. 
  - Forms can be sent using two methods
    - Get
      - The values are added to the end of the url specified by the action attribute
      - Ideal for short forms or retreiving dayta from a web server. 
    - Post
      - Values are sent in http headers
      - Allows user to upload
      - is very long
      - contains sensitive info
      - ADDS INFORMATION FROM A DATABASE

- Inputs
  - `<input>` 
    - `type="text"` - designates single line text input
      - `name=""` - Identifies each form for a server
      - `maxlength=""` - Sets max char length for form.
    - `type="password"` - self explanitory
  - `<textarea>` = multi-line input
    - `col="" and rows=""` - sets size - but now done through CSS
  - `type="radio"` - allows users to pick from some options.
    - `name=""` - assigns groupings
    - `checked="checked"` - preselects a default (only one per grouping please)
  - `type="checkbox"` - Similar to radio but mulitple can be selected.
  - `<select>` - AKA dropdown.
    - `<option>` - used to add options to a dropdown grouping.
  - `type="submit"`- Used to send forms 
    - Can use image for submit button
  - `<label>` - can add labels to seletors. 
- `<fieldset>` - can group multiple inputs together.
- `required="required"` attribute for making sure a form is submitted with info (typically done on the JS side)

## Lists, Tables, Forms 

## Formatting forms

- They are objects like everything else, you can use flex,grid or other methods to style them in thier own container.
- Cursors also have several styles which you can trigger on hover or action. 

## EVENTS

- When an event occours it is fired or raised
- events trigger scripts.

- How to use to trigger
  - Select the element nodes you want the script to respond to by querying the DOM
  - Indicate the even on the selected nodes will trigger the response ( Bind the event to the node)
  - State the code you'd like to run on event.
- Binding an element
  - HTML EVENT HANDLER
    - Outdated but know what they look like
  - TRAD. DOM HANDLER
    - `element.onevent = functionName;` - no parenthesis after functionname
  - LVL 2 DOM EVENT LISTENERS
    - They are the favored way of handling events. 
    - `element.addEventListener('event', functionName, [boolean]);`