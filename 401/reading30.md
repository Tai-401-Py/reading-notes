# [What a way to REACT](https://reactjs.org/docs)

## [Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)

- Inline If with Logical && Operator: You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator. It can be handy for conditionally including an element:
        
              {unreadMessages.length > 0 &&
        <h2>
          You have {unreadMessages.length} unread messages.
        </h2>
        }

- Conditional turnary operator: `if ? this:that`
- Preventing Component from Rendering: In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return `null` instead of its render output.        

## [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)\

- Keys Must Only Be Unique Among Siblings

## Containment

Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.

We recommend that such components use the special children prop to pass children elements directly into their output:

        function FancyBorder(props) {
        return (
            <div className={'FancyBorder FancyBorder-' + props.color}>
            {props.children}
            </div>
        );
        }