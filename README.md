# reactInterviewQuestions

# Q - 1 Why React Called Single page application?
- A Single Page Application is a web application or website that interacts with the web browser by dynamically rewriting the current web page with new data from the web server, instead of the default method of the browser loading entire new pages.
- A single-page application is an application that loads a single HTML page and all the necessary assets (such as JavaScript and CSS) required for the application to run.
- This means that the URL of your website will not change completely (page will not reload), instead it will keep getting content and rewriting the DOM with it instead of loading a new page.
- Any interactions with the page or subsequent pages do not require a round trip to the server which means the page is not reloaded.

# Q - 2 What are synthetic events in react?
- it is cross browser wrapper that wrap arounds the browser's native events
- to avoid creating multiple implementations for multiple methods for multiple browsers, creating common names for all events across browsers. 
- e.preventDefault() prevents all the default behavior by the browser.
  ```e.preventDefault()```
- e.stopPropagation() prevents the call to the parent component whenever a child component gets called.
- Here ‘e’ is a synthetic event, a cross-browser object. It is made with a wrapper around the actual event of the browser. 

# Q - 3 How React Works?
- React works on Virtual DOM.
- When a state changes in a component, it runs a diffing algorithm. This identifies that what has been changed in the virtual DOM. 
- The next step is reconciliation which updates the DOM with diff result. 
- HTML DOM has a tree structure shape that is allowed by the structure of HTML document. DOM trees are big due to the size of large apps. Nowadays, we are looking more towards dynamic apps (Single page applications) so it is important to change the DOM tree constantly a lot. This is a real performance and pain in development. 
- Virtual DOM is lightweight, and it’s detached from browser-specific implementation details.
- Virtual DOM is not developed by React, but it uses it and provides it for free.  
- ReactElement lives inside the virtual DOM. It makes the basic node here. ReactElements are rendered into the “real” DOM once you define the elements. 
- Once a state is changed in React diff algorithm identifies what has been changed. Then DOM gets updated with the result of diff. Virtual DOM is faster than the regular DOM. 




