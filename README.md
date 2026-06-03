# 🌿 Landscaping Project Manager

A lightweight, single-file web app for managing landscaping projects — track tasks, materials, costs, and completion progress across multiple jobs, all from your browser with no installation required.

---

## Features

- **Multiple projects** — create as many project cards as you need, each with its own name, task list, and cost summary
- **Per-task fields** — each task row holds a task description, item/material, and cost
- **Done tracking** — check off tasks as they're completed; a progress bar shows how many are done per project
- **Estimated total** — costs are summed automatically per project as you type
- **Dark mode** — toggle between light and dark themes with a single button; preference is saved across sessions
- **Persistent storage** — all projects and the dark mode preference are saved to `localStorage`, so your data survives page refreshes
- **Responsive layout** — works on desktop and mobile (≤480px breakpoint)
- **Accessible** — done checkboxes include descriptive `aria-label` attributes for screen readers
- **Zero dependencies** — plain HTML, CSS, and vanilla JavaScript; no build step, no frameworks, no server required

---

## How to run

Because the app is a single HTML file with no server-side code, you can open it directly in any modern browser.

### Option 1 — Open the file directly

1. Download or clone this repository
2. Double-click `landscaping-todo.html`, or drag it into a browser window

That's it. The app runs entirely in the browser.

### Option 2 — Serve locally (optional)

If your browser restricts `file://` access, serve the file with any static server:

```bash
# Python 3
python3 -m http.server 8080

# Node.js (npx, no install needed)
npx serve .
```

Then open `http://localhost:8080/landscaping-todo.html` in your browser.

### Option 3 — GitHub Pages

1. Fork or push the repo to GitHub
2. Go to **Settings → Pages**
3. Set the source to the `main` branch, root folder
4. GitHub will publish the app at `https://<your-username>.github.io/<repo-name>/landscaping-todo.html`

---

## Usage

| Action | How |
|---|---|
| Add a project | Click **+ New Project** |
| Name a project | Type in the green header field |
| Add a task | Click **+ Add Task** inside a project card |
| Fill in task details | Type in the Task, Item/Material, and Cost fields |
| Mark a task done | Check the checkbox on the left of a task row |
| Delete a task | Click the **✕** button at the end of a task row |
| Delete a project | Click the **✕** button in the project header |
| Toggle dark mode | Click **🌙 Dark** / **☀️ Light** in the top-right of the header |

---

## Data storage

All data is stored in the browser's `localStorage` under the key `lp_projects`. No data is sent to any server. Clearing browser storage will reset the app.

---

## Browser support

Any modern browser with CSS custom property and `localStorage` support — Chrome, Firefox, Safari, and Edge are all supported.
