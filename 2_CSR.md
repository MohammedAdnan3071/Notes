# Client Side Rendering 

Client Side Rendering (CSR) is a modern technique used in web development where the rendering of a webpage is performed in the browser using Js. 
Instead of the Server sending a full rendered HTML page to the client

Good Example of CSR is React 

![Client side Rendering](image.png)

let us see a react project in action 
1. Initialize a react project
 npm create vite@latest
 2. Add dependencies
   npm i 
3. Start the project 
    npm run build 
4. Serve the project 
    cd dist/
    serve

open the network tab and notice how the intial HTML file does not have any content
![network tab csr explanation](image-1.png)

This means that the Js runs and actually populates / renders the contents on the page

React (or CSR) make your life as a developer easy. You write components, Js renders them to the DOM.

Downsides?
1. Not SEO optimized
2. User sees a flash before the page renders
3. Waterfalling problem 
![waterfalling problem ](image-2.png)