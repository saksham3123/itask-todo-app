# iTask - Todo List App

A simple, clean todo app built with **React** and **Tailwind CSS**. Add, edit, delete, and complete tasks, and your list is saved in the browser so it's still there after a refresh.

## Features

- Add new todos
- Edit existing todos
- Delete todos
- Mark todos as completed (shown with a strikethrough)
- Toggle "Show Finished" to hide or show completed todos
- Todos persist across page reloads using `localStorage`
- Responsive layout

## Tech Stack

- [React](https://react.dev/) (with Vite)
- [Tailwind CSS](https://tailwindcss.com/)
- [React Icons](https://react-icons.github.io/react-icons/)
- [uuid](https://www.npmjs.com/package/uuid) for unique todo IDs

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- npm

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/<your-repo-name>.git

# Go into the project folder
cd <your-repo-name>

# Install dependencies
npm install

# Start the development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for production

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/
│   └── Navbar.jsx    # Top navigation bar
├── App.jsx           # Main app: todo state, handlers, and UI
├── index.css         # Tailwind import
└── main.jsx          # App entry point
```

## How It Works

- Todos are stored in React state as objects: `{ id, todo, isCompleted }`.
- The initial state is loaded from `localStorage` when the app starts.
- A `useEffect` saves the list to `localStorage` whenever it changes, so the saved data is always up to date.
- State is updated immutably using `map` and `filter`.

## Future Improvements

- Add a todo by pressing Enter
- Backend and database for syncing across devices
- Due dates and categories
- Dark mode

## License

This project is open source and available under the [MIT License](LICENSE).
