# TaskFlow

TaskFlow is a small task-management dashboard built with React, TypeScript, and Vite. It displays tasks and their owners, with controls to organize and update the list.

## Features

- View total, completed, and pending task counts.
- Filter tasks by completion status and search by title.
- Filter the task list by owner.
- Add tasks, assign them to a user, mark them complete or pending, edit titles, and delete tasks.
- Retry loading tasks or users if the network request fails.
- Responsive layout for smaller screens.

## Getting started

### Requirements

- Node.js and npm
- An internet connection to load the initial task and user data

### Install and run

```bash
npm install
npm run dev
```

Open the local URL printed by Vite in your browser.

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server. |
| `npm run build` | Type-check the project and create a production build in `dist/`. |
| `npm run preview` | Preview the production build locally. |
| `npm run lint` | Run ESLint. |

## Data and persistence

The app loads up to 50 tasks from the [JSONPlaceholder Todos API](https://jsonplaceholder.typicode.com/todos?_limit=50) and user names from the [JSONPlaceholder Users API](https://jsonplaceholder.typicode.com/users). Adding, editing, completing, and deleting tasks updates the in-memory list in the browser; those changes are not saved to the API or persisted after a page reload.

## Project structure

```text
src/
  components/       Reusable task, filter, search, summary, and statistics UI
  App.tsx           App state, data loading, filtering, and task operations
  api.ts            JSONPlaceholder requests
  index.css         Application styles
  main.tsx          React entry point
  types.ts          Task, user, and filter types
```
