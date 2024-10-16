# What I Learned Today

## 1. Event Handling in Forms
- **e.preventDefault()**: I learned how this method stops the form from doing its default action (which refreshes the page) and lets us control what happens when we submit the form with JavaScript.
- **Event Listener for Submit**: We added a listener to the form so when we submit it, a function runs. This way, we can handle input data without reloading the page.

## 2. DOM Manipulation
- **Creating Elements Dynamically**: I learned how to create HTML elements (like `<li>` for tasks and delete buttons) directly using JavaScript.
- **Appending Child Elements**: After creating elements, I add them to the page with `appendChild()`.

## 3. Local Storage
- **Storing Data**: I now know how to store tasks in localStorage using `localStorage.setItem()` as strings.
- **Retrieving Data**: I use `localStorage.getItem()` to get tasks back from localStorage (stored as JSON strings).
- **Parsing/Serializing Data**: I convert arrays into strings using `JSON.stringify()` for storage, and back into arrays using `JSON.parse()` when retrieving them.
- **Persistent Storage**: Tasks are stored so they stay even if the page reloads.

## 4. Array Operations with Spread Operator
- **Merging Arrays**: I learned how the spread operator (`...`) helps me combine old tasks from localStorage with the new task into one array.
- **Immutable Update**: By using the spread operator, I make sure the original array isn’t changed; instead, I create a new array each time I add a task.

## 5. Deleting Elements and Event Delegation
- **Deleting Tasks**: I learned how to handle clicks on delete buttons with event delegation, so when I click the delete button, it removes the task from both the page and localStorage.
- **Removing from Local Storage**: When I delete a task, I filter it out from the array, and then save the updated list back to localStorage.

## 6. Flexbox for UI Layout
- **Right-aligning Buttons**: I used the flexbox layout to align elements. Specifically, the delete button goes to the right side of the task text by using `justify-content: space-between`.

## 7. Using window.onload for Initialization
- **Loading Data on Page Load**: I learned how `window.onload` runs a function that gets tasks from localStorage and shows them on the page when it loads.

---

## Summary:
Today, I worked on:
- Handling form submissions without reloading the page.
- Creating and adding DOM elements with JavaScript.
- Storing, retrieving, and updating tasks in localStorage.
- Combining old and new tasks using the spread operator.
- Deleting tasks and making sure they’re removed from both the page and localStorage.
- Using flexbox to control layout, especially for aligning buttons.
- Making tasks stay on the page even after reloads, thanks to localStorage.

This stuff helps build interactive, data-driven websites and apps.
