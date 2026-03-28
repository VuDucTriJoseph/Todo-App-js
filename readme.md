# Todo App

A simple, responsive todo-list web app built with vanilla HTML, CSS, and JavaScript.

## ✅ Features

- Add tasks by typing in the input and pressing Enter or clicking the add button
- Mark tasks complete/incomplete with custom styled checkboxes
- Delete individual tasks
- Clear all completed tasks with one button
- Filter tasks:
  - All
  - Active
  - Completed
- Persist tasks in `localStorage` so data survives page refresh
- Dynamic item counter (“x items left")
- Friendly empty state view when no tasks exist
- Display current date (weekday, month, day)

## 🧩 Project structure

- `index.html` — app markup, layout, icon font include
- `style.css` — UI styles, responsive cards, states, transitions
- `script.js` — core todo logic, app state, event handlers, rendering
- `readme.md` — project documentation

## 🚀 Usage

1. Open `index.html` in a browser.
2. Add tasks in the input field.
3. Toggle checkbox to mark complete/incomplete.
4. Click the `x` icon to delete a task.
5. Use filter buttons to view all/active/completed items.
6. Click “Clear completed" to remove finished tasks.

## 💾 Persistence

- Todos are saved to browser `localStorage` under key `todos`.
- Data loads automatically on page load.

## 🛠️ How it works (script overview)

- `todos` array is the app state with each todo `{ id, text, completed }`
- `addTodo(text)` validates input, updates state, saves, and rerenders
- `toggleTodo(id)`, `deleteTodo(id)`, `clearCompleted()` mutate state then save/render
- `filterTodos(currentFilter)` determines visible list
- `renderTodos()` builds list DOM from filtered todos
- `updateItemsCount()` and `checkEmptyState()` keep footer UI accurate

## 📌 Notes

- Input trimming prevents empty tasks.
- Task IDs use `Date.now()`.
- Styles include state classes for checked and completed tasks.

## 🛠️ Optional improvements

- Edit task text inline
- Drag-and-drop ordering
- Undo last deletion
- Add due dates and priority labels
- Sync across devices via backend API

---

Made for learning frontend essentials with no frameworks.
