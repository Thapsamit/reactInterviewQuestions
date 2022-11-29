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

# Q - 3 What is Reconcilition?
- Reconciliation is the process through which React updates the Browser DOM.
- the working of the Reconciliation process are:
  - Virtual DOM  
  - Diffing Algorithm
  
- Browser does the following tasks:
  - Creates a DOM (Document Object Model) represented by a tree structure.
  - Renders any new data to the DOM even if data is similar to previous ones.  
- This rendering by Browser has a sequence of steps and is rather costly in nature. The concept of Virtual DOM used by React makes rendering much faster.

- Virtual DOM: React renders JSX components to the Browser DOM, but keeps a copy of the actual DOM to itself. This copy is the Virtual DOM. We can think of it as the twin brother of the real or Browser DOM. The following actions take place in React:

- React stores a copy of Browser DOM which is called Virtual DOM.
- When we make changes or add data, React creates a new Virtual DOM and compares it with the previous one.
- Comparison is done by Diffing Algorithm. The cool fact is all these comparisons take place in the memory and nothing is yet changed in the Browser.
- After comparing, React goes ahead and creates a new Virtual DOM having the changes. It is to note that as many as 200,000 virtual DOM nodes can be produced in a second.
- Then it updates the Browser DOM with the least number of changes possible without rendering the entire DOM again. 


# Q - 4 Different Lifecycle component and its method?
- lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component’s existence.
- **Initialization:** This is the stage where the component is constructed with the given Props and default state. This is done in the constructor of a Component Class.
- **Initialization:** This is the stage where the component is constructed with the given Props and default state. This is done in the constructor of a Component Class.
- **Mounting:** Mounting is the stage of rendering the JSX returned by the render method itself.
- **Updating:** Updating is the stage when the state of a component is updated and the application is repainted.
- **Unmounting:** As the name suggests Unmounting is the final step of the component lifecycle where the component is removed from the page.
- **Mounting Methodss:-**
  - componentWillMount():- This function is invoked right before the component is mounted on the DOM i.e. this function gets invoked once before the render() function is executed for the first time.
  - componentDidMount():- Similarly as the previous one this function is invoked right after the component is mounted on the DOM i.e. this function gets invoked once after the render() function is executed for the first time
  
- **Update Methods:-**
  - **componentWillReceiveProps() Function:** This is a Props exclusive Function and is independent of States. This function is invoked before a mounted component gets its props reassigned. The function is passed the new set of Props which may or may not be identical to the original Props. 
  - **shouldComponentUpdate():- By default, every state or props update re-render the page but this may not always be the desired outcome, sometimes it is desired that updating the page will not be repainted. The shouldComponentUpdate() Function fulfills the requirement by letting React know whether the component’s output will be affected by the update or not.
  - **componentWillUpdate() Function:** As the name clearly suggests, this function is invoked before the component is rerendered i.e. this function gets invoked once before the render() function is executed after the updation of State or Props.
  - **componentDidUpdate() Function:** Similarly this function is invoked after the component is rerendered i.e. this function gets invoked once after the render() function is executed after the updation of State or Props.
 
 - **Unmount**:- 
  - componentWillUnmount() Function: This function is invoked before the component is finally unmounted from the DOM i.e. this function gets invoked once before the component is removed from the page and this denotes the end of the lifecycle.
  
  
# Q - 5 Difference between props vs propTypes


# Q - 6 All About Hooks
- Hooks are functions that let you “hook into” React state and lifecycle features from function components. such as useState.
- You’ve likely performed data fetching, subscriptions, or manually changing the DOM from React components before. We call these operations “side effects” (or “effects” for short) because they can affect other components and can’t be done during rendering.
- useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount
- In order to customize our Hook to render only when the component mounts, we can send a second argument to useEffect. By passing useEffect an empty array ([]) as the second argument, React knows to only call useEffect when the component mounts.









