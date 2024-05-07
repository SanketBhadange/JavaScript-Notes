# 1. Modifying Element Content:

textContent: Sets or gets the text content of an element, including text and child elements.

Syntax: element.textContent = "New content" (sets) const content = element.textContent; (gets)
innerText: Similar to textContent but excludes script and style elements (less common).

innerHTML: Sets or gets the HTML content of an element, including all child elements.

Syntax: element.innerHTML = "<p>Modified content</p>" (sets) const html = element.innerHTML; (gets)
Example:

```HTML
<p id="message">Original message</p>
```
```JavaScript
const messageElement = document.getElementById("message");
messageElement.textContent = "This is the updated message"; // Change text content
// OR
messageElement.innerHTML = "<b>Bold message</b>"; // Change HTML content (including formatting)
```

# 2. Modifying Element Attributes:

setAttribute(attributeName, attributeValue): Sets the specified attribute on an element.
getAttribute(attributeName): Gets the value of the specified attribute.
removeAttribute(attributeName): Removes the specified attribute from an element.
Example:

```HTML
<img id="profile-pic" src="default.png" alt="Profile picture">
```
```JavaScript
const profilePic = document.getElementById("profile-pic");
profilePic.setAttribute("src", "new_profile_pic.jpg"); // Update image source
const altText = profilePic.getAttribute("alt"); // Get alt text
profilePic.removeAttribute("alt"); // Remove alt attribute (if needed)
```

# 3. Modifying Element Styles:

style: Accesses the inline style object of an element. You can set individual style properties directly (e.g., element.style.color = "red").
Example:

```HTML
<h2 id="heading">This is a heading</h2>
```
```JavaScript
const heading = document.getElementById("heading");
heading.style.color = "blue";
heading.style.fontSize = "2em"; // Set multiple styles
```

# 4. Adding and Removing Elements:

createElement(tagName): Creates a new HTML element with the specified tag name.
appendChild(childElement): Appends a child element to the end of an element's child node list.
removeChild(childElement): Removes a child element from the element.
Example:

```HTML
<ul id="todo-list"></ul>
```

```JavaScript
const todoList = document.getElementById("todo-list");

const newTodo = document.createElement("li");
newTodo.textContent = "New todo item";

todoList.appendChild(newTodo); // Add the new item to the list

// To remove an item (assuming you have a reference to it):
todoList.removeChild(itemToRemove);
```

# 5. Event Listeners:

addEventListener(eventName, eventHandlerFunction): Attaches an event listener to an element. The eventName specifies the event type (like "click", "mouseover"), and the eventHandlerFunction is the code to execute when the event occurs.
Example:

```HTML
<button id="my-button">Click me</button>
```

```JavaScript
const button = document.getElementById("my-button");

button.addEventListener("click", function() {
  alert("Button clicked!");
});
```
