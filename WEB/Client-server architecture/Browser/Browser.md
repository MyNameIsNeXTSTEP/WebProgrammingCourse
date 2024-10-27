**HTML DOM**, **CSSOM**, **Browser Rendering & Layout**, **Network**, and **Browser Dev Tools**

### 1. **HTML DOM (Document Object Model)**

**1.1 What is the DOM?**

- **Definition**: The DOM represents an HTML document as a tree of objects (nodes). Each element in the HTML becomes a node in the DOM, allowing JavaScript to interact with the structure and content of the webpage.
- **Node Types**: The primary node types are Element nodes, Text nodes, and Comment nodes. Each node can have children (other nodes nested inside them).

**Key Points**:

- The DOM is **not** HTML—it’s a representation of the page’s structure after the browser parses the HTML.
- You can use JavaScript to add, remove, and manipulate elements on the page dynamically.

**Resources**:
- [MDN - DOM Overview](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

**1.2 DOM Manipulation**

- **Selectors**: Access elements using methods like `getElementById`, `querySelector`, and `querySelectorAll`. These are crucial for identifying which elements to manipulate.
    
- **Modifying Elements**:
    
    - Use `createElement` to create new elements programmatically.
    - Methods like `appendChild` and `removeChild` let you add or remove elements from the DOM.
    - `innerHTML` allows changing the content of an element as HTML, while `textContent` changes plain text.
- **Event Listeners**: JavaScript can attach events (e.g., clicks, keypresses) to elements using `addEventListener`. It's essential to understand event propagation (bubbling vs. capturing).
    

**Key Points**:

- Direct manipulation of the DOM can be costly in terms of performance, especially if done frequently. It’s good to batch updates to minimize reflows.
- Avoid using `innerHTML` for security reasons (XSS attacks).

**Resources**:
- [MDN - DOM Methods](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/DOM_Events)

---

### 2. **CSSOM (CSS Object Model)**

**2.1 What is the CSSOM?**

- **Definition**: The CSSOM is the counterpart to the DOM for CSS. It’s a tree-like structure that the browser builds to apply CSS rules to HTML elements.
- **Interaction with DOM**: The DOM and CSSOM combine to create the render tree, which the browser uses to display the page.

**Key Points**:

- CSSOM is essential for understanding how styles are applied and how modifying CSS can affect performance (since it can trigger layout recalculations).
- Avoid **direct DOM/CSSOM manipulations** that force reflows or repaints.

**Resources**:
- [MDN - CSS Object Model](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model)

**2.2 Styling Elements via JavaScript**

- You can change the styles of elements programmatically using `element.style`. For complex stylesheets, the `getComputedStyle` method lets you see the current styles applied to an element.
- The `classList` API is useful for adding/removing/toggling CSS classes dynamically, e.g., `element.classList.add('active')`.

**Key Points**:

- Prefer manipulating classes (with `classList`) instead of inline styles for better performance and separation of concerns.

**Resources**:
- [MDN - Manipulating CSS with JavaScript](https://developer.mozilla.org/en-US/docs/Web/API/ElementCSSInlineStyle/style)

---

### 3. **Browser Rendering & Layout**

**3.1 Rendering Pipeline Overview**

- **Steps**:
    1. **Parsing HTML/CSS**: The browser parses HTML into the DOM and CSS into the CSSOM.
    2. **Render Tree**: The browser combines the DOM and CSSOM to create the render tree.
    3. **Layout**: The browser calculates the position of elements based on the render tree.
    4. **Painting**: The browser fills in pixels for visual elements.
    5. **Compositing**: The browser layers elements and applies effects (like animations).

**Key Points**:

- Recalculating the layout (reflow) is costly, especially if it happens frequently (e.g., with animations or frequent DOM manipulations).

**Resources**:

- Google Developers - Critical Rendering Path
- CSS Tricks - How Browsers Render Pages

**3.2 Reflow and Repaint**

- **Reflow**: When the browser has to recalculate positions of elements (e.g., resizing a window, adding content).
- **Repaint**: When visual changes happen without affecting layout (e.g., changing a color).

**Key Points**:

- Minimize reflows by batching DOM changes.
- `position: absolute/fixed` can reduce layout recalculations since the element is taken out of the normal flow.

**Resources**:
- [Google Developers - Rendering Performance](https://web.dev/articles/rendering-performance)
- [Google Developers - Catching issues of rendering performance](https://developer.chrome.com/docs/devtools/rendering/performance?hl=ru)
- [MDN - Reflow and Repaint](https://developer.mozilla.org/en-US/docs/Web/Performance/Reflow)

---

### 4. **Network (Browser Networking & HTTP)**

**4.1 How Browsers Fetch Resources**

- Browsers send HTTP requests to fetch resources (HTML, CSS, JavaScript, images).
- **Connection lifecycle**: DNS lookup → TCP handshake → SSL/TLS (if secure).

**Key Points**:

- Understanding **HTTP status codes** (e.g., `200 OK`, `404 Not Found`, `500 Server Error`) is critical for troubleshooting resource loading issues.

**Resources**:

- [MDN - HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
- [MDN - How Browsers Work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
- [Chrome Developers - Inside look of modern web browser](https://developer.chrome.com/blog/inside-browser-part3?hl=ru)

**4.2 Performance Optimization**

- **Critical resources** (CSS, JavaScript) block rendering; defer or asynchronously load non-essential resources to avoid blocking the rendering pipeline.
- Use caching strategies (like setting cache headers) to improve performance for repeat visits.

**Key Points**:

- Always use `async` or `defer` attributes for loading JavaScript to prevent render blocking.
- Minimize the number of requests by bundling files and using image sprites.

**Resources**:
- [Google dev article - Critical Rendering path](https://web.dev/articles/critical-rendering-path)
- [MDN - Critical Rendering path and optimizing](https://developer.mozilla.org/en-US/docs/Web/Performance/Critical_rendering_path)
- [MDN - Asynchronous Script Loading](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)

---

### 5. **Browser Developer Tools**

**5.1 Inspecting and Manipulating the DOM**

- The **Elements** tab in browser dev tools allows inspecting the DOM, modifying elements, and viewing styles.
- Real-time changes can help debug layout issues or test changes without refreshing the page.

**Key Points**:

- Chrome’s **Styles** pane shows CSS applied to an element, including inherited styles and overridden rules.

**Resources**:

- [MDN - Browser Developer Tools Overview](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_browser_developer_tools)

**5.2 JavaScript Debugging**

- The **Sources** panel lets you set breakpoints in JavaScript and step through the code to inspect variables and the call stack.
- You can also pause on exceptions, making it easier to debug errors.

**Key Points**:

- Use the **Console** to execute JavaScript and inspect variables or elements in real time.

**5.3 Network Performance**

- The **Network** tab helps you inspect the HTTP requests being made, view response headers, and monitor the performance of network requests.

**Key Points**:

- Waterfall charts show how long each resource took to load and can reveal bottlenecks like slow server response times.

**Overall resources**:

- [Google Developers - Dev tools](https://developer.chrome.com/docs/devtools?hl=ru)