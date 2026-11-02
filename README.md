# ShelfSpace Pro — React Edition

A React + Vite edition of ShelfSpace Pro, a campus resource discovery, borrowing, booking and operations dashboard. The existing interactive experience is preserved while React owns the application mount point. The current feature logic is kept in a compatibility module so the UI can be migrated into smaller React components incrementally.

## Tech stack

- React and React DOM
- Vite development server and production build
- HTML5 and CSS3
- JavaScript with browser LocalStorage
- Lucide React dependency included for future component-level icon usage

## Requirements

- Node.js 20.19+ or 22.12+ recommended
- npm (installed with Node.js)
- VS Code (recommended)

## Setup on Windows

1. Download and extract `ShelfSpace_Pro_React_Hackathon.zip`.
2. Open the extracted `ShelfSpace_React` folder in VS Code.
3. Open Terminal → New Terminal.
4. Check Node and npm:

   ```bash
   node -v
   npm -v
   ```

5. Install dependencies:

   ```bash
   npm install
   ```

6. Start the development server:

   ```bash
   npm run dev
   ```

7. Open the Local URL printed by Vite, normally `http://localhost:5173`.
8. To stop the server, press `Ctrl + C` in the terminal.

## Production build

```bash
npm run build
npm run preview
```

Vite writes the production-ready site to the `dist` folder. Use `npm run preview` to test that build locally.

## Project structure

```text
ShelfSpace_React/
├── index.html
├── package.json
├── README.md
└── src/
    ├── main.jsx
    ├── App.jsx
    ├── legacy.html
    ├── legacy.css
    └── legacy.js
```

## Current modules

- Student overview dashboard
- Resource catalog, search, filters, sorting and favourites
- Borrowing, returns, renewals and waitlists
- Room and equipment slot booking with overlap checks
- Activity timeline and notifications
- Study planner and Pomodoro focus timer
- Local catalog-aware resource assistant
- Support request form
- Admin inventory, member directory and analytics
- CSV import/export, command palette and theme toggle

## Important prototype notes

This is a front-end hackathon prototype. Demo data is stored in the browser's LocalStorage. It does not provide production authentication, shared multi-user data, server-side authorization, cloud sync, real AI, or server-enforced booking locks. Those capabilities require a backend and database before real campus deployment.

## React migration note

React currently mounts the application shell and owns the rendered app root. The previous DOM-driven feature module is loaded after the markup is mounted to preserve all working prototype interactions. For a production-grade React architecture, migrate each screen and its state into React components and hooks, then remove the compatibility module.
