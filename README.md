# 📝 TO-DO-LIST

> A simple, interactive task manager that helps you organize your daily tasks, track progress, and stay productive—all directly in your browser.

![HTML5](https://img.shields.io/badge/HTML5-Markup-orange?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-Styling-blue?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-yellow?logo=javascript&logoColor=black)
![Storage](https://img.shields.io/badge/Storage-localStorage-green)
![Build](https://img.shields.io/badge/build-no_build_step-lightgrey)
![License](https://img.shields.io/badge/license-not_specified-lightgrey)

## 📌 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [How It Works](#-how-it-works)
- [Tech Stack](#-tech-stack)
- [Project Scope and Objectives](#-project-scope-and-objectives)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation and Setup](#-installation-and-setup)
- [Usage Guide](#-usage-guide)
- [Data Storage](#-data-storage)
- [Limitations and Future Enhancements](#-limitations-and-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

## 🚀 Overview

### Why?

Keeping track of daily tasks can become difficult without a simple way to record responsibilities, identify pending work, and monitor completed activities. This project addresses that need with a lightweight task management interface that runs directly in a web browser.

### What?

**TO-DO-LIST** is a browser-based task management application that lets users create and manage tasks through an interactive interface. Task information is saved in the browser's local storage, allowing tasks to remain available across page reloads in the same browser.

### How?

The application uses standard web technologies without a backend server or application framework.

1. **User interaction:** Users enter tasks and interact with task controls through the HTML interface.
2. **Application logic:** JavaScript handles task creation, editing, deletion, completion status, and filtering.
3. **Data persistence:** Task objects are serialized as JSON and stored in browser `localStorage`.
4. **Interface rendering:** The application renders the task list and updates its presentation according to the selected filter and task status.

### To Whom?

This project is suitable for:

- Individuals who want a simple daily task tracker.
- Beginners learning HTML, CSS, JavaScript, and DOM manipulation.
- Students practicing browser-based application development.
- Developers exploring client-side state management and browser storage.

## ✨ Features

- **Add Tasks:** Create a task by entering its name and pressing Enter.
- **Edit Tasks:** Update an existing task without creating a duplicate.
- **Delete Tasks:** Remove individual tasks using the task actions menu.
- **Track Completion:** Mark tasks as completed or pending with a checkbox.
- **Filter Tasks:** View all tasks, pending tasks, or completed tasks.
- **Clear All Tasks:** Remove all saved tasks with a single action.
- **Persistent Storage:** Save task names and completion statuses in browser `localStorage`.
- **Interactive Interface:** Use task menus, status indicators, and an organized task list.

## 🏗️ How It Works

The application follows a simple client-side architecture.

```text
             User
              |
              v
       index.html
       User Interface
              |
              v
          script.js
       Task Management
              |
       +------+------+
       |             |
       v             v
  Task Filtering   Task Actions
       |          Add / Edit /
       |          Delete / Complete
       +------+------+
              |
              v
       Browser localStorage
         "todo-list"
              |
              v
      JSON Task Data
```

### Task Data Model

Each task is represented by an object containing its name and status.

```javascript
{
  name: "Complete project documentation",
  status: "pending"
}
```

The `status` property supports two values:

- `pending` — the task is not yet completed.
- `completed` — the task has been marked as complete.

The application stores the collection of tasks as a JSON array in browser storage.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Defines the application structure and task controls |
| CSS3 | Styles the interface, layout, and task states |
| JavaScript (ES6+) | Implements task management and interactive behavior |
| Browser DOM API | Connects user interactions to application logic |
| Browser `localStorage` | Persists tasks between page reloads |
| Unicons | Provides interface icons through an external stylesheet |

### Technology Badges

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

The application does not require React, Node.js, a database server, or a package manager to run in its current form.

## 🎯 Project Scope and Objectives

### Objectives

- Provide an accessible, straightforward task management interface.
- Support the complete basic task lifecycle: creation, editing, completion, and deletion.
- Separate completed and pending tasks through filtering.
- Persist task information locally without requiring an account or remote service.
- Demonstrate practical JavaScript DOM manipulation and event handling.

### In Scope

- Client-side task management.
- Task status tracking.
- Filtering by completion status.
- Local browser storage.
- A styled web interface with interactive controls.

### Out of Scope

The current implementation does not provide:

- User accounts or authentication.
- Cloud synchronization across devices.
- A backend API or remote database.
- Due dates, reminders, or task priorities.
- Collaborative task management.
- Server-side storage or multi-user access.

## 📂 Project Structure

```text
TO-DO-LIST/
├── index.html       # HTML structure and interface
├── style.css        # Application styling and layout
├── script.js        # Task logic and localStorage integration
├── bars-icon.svg    # SVG icon used in the task input area
└── README.md        # Project documentation
```

### Key Files

| File | Responsibility |
|---|---|
| `index.html` | Defines the task input, filter controls, Clear All button, and task list |
| `style.css` | Defines the visual presentation and layout |
| `script.js` | Implements task operations, filtering, and persistence |
| `bars-icon.svg` | Supplies an interface icon |

The HTML also references the Unicons stylesheet hosted externally by Iconscout.

## 💻 Prerequisites

The application has minimal setup requirements.

- A modern web browser such as Chrome, Firefox, Edge, or Safari.
- Git, if you want to clone the repository.
- Python 3 or another static HTTP server, optionally, to serve the files locally.

**Node.js, npm, Docker, and a database are not required** for the current implementation.

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/pratikabhang/TO-DO-LIST.git
```

### 2. Navigate to the Project Directory

```bash
cd TO-DO-LIST
```

### 3. Run the Application

**Option A: Open directly in your browser**

Open `index.html` in your preferred browser.

**Option B: Use a local HTTP server**

If Python 3 is installed, run:

```bash
python -m http.server 8000
```

On systems where Python is available as `python3`, use:

```bash
python3 -m http.server 8000
```

Then open:

[http://localhost:8000](http://localhost:8000)

Press `Ctrl+C` in the terminal to stop the server.

### 4. Start Managing Tasks

Enter a task in the input field and press Enter. Use the task controls to edit, delete, or mark it as completed.

No dependency installation, compilation, or environment variable configuration is needed.

## 📖 Usage Guide

### Add a Task

1. Open the application.
2. Click the input field labeled **Add a new task**.
3. Enter a task name.
4. Press Enter to save it.

Example task names:

- Complete an assignment
- Review project documentation
- Prepare for a meeting

Empty or whitespace-only task entries are ignored.

### Edit a Task

1. Open the task's actions menu using the ellipsis icon.
2. Select **Edit**.
3. Update the text in the input field.
4. Press Enter to save the changes.

### Mark a Task as Completed

Select the checkbox next to a task to mark it as completed. Uncheck it to return the task to the pending state.

### Filter Tasks

Use the filter controls to change which tasks are displayed.

| Filter | Description |
|---|---|
| **All** | Displays every saved task |
| **Pending** | Displays tasks that are not completed |
| **Completed** | Displays tasks marked as completed |

### Delete a Task

Open the task's actions menu and select **Delete** to remove that task.

### Clear All Tasks

Select **Clear All** to remove all tasks from the current task list. This operation updates the saved data in local storage.

## 💾 Data Storage

The application uses the browser's built-in `localStorage` API rather than a remote database.

### Storage Key

```text
todo-list
```

### Example Stored Value

The following illustrates how multiple tasks may be represented in storage:

```json
[
  {
    "name": "Complete project documentation",
    "status": "completed"
  },
  {
    "name": "Review pull requests",
    "status": "pending"
  }
]
```

### Persistence Behavior

- Tasks are serialized to JSON before being saved.
- Task names and completion statuses are stored locally.
- Existing tasks are loaded when the application initializes.
- Changes remain available after refreshing the page in the same browser profile.
- Clearing browser site data or local storage can remove saved tasks.

**Privacy note:** Task data is stored in the current browser's local storage. It is not synchronized between browsers or devices by this implementation.

## 🔮 Limitations and Future Enhancements

Potential improvements include:

- Add task due dates, priorities, and categories.
- Add drag-and-drop task ordering.
- Improve keyboard accessibility and screen-reader support.
- Add confirmation before deleting all tasks.
- Introduce automated tests for task operations.
- Improve input validation and safe rendering of user-provided task names.
- Add import and export functionality.
- Add optional cloud synchronization and authentication.
- Replace the external icon stylesheet with locally bundled assets.

These are proposed enhancements, not claims about existing functionality.

## 🤝 Contributing

Contributions, bug reports, and suggestions are welcome.

### Contribution Workflow

1. Fork the repository.
2. Clone your fork:

   ```bash
   git clone https://github.com/<your-username>/TO-DO-LIST.git
   cd TO-DO-LIST
   ```

3. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. Make your changes to the relevant HTML, CSS, or JavaScript files.
5. Test the application in a browser, including task creation, editing, deletion, filtering, and persistence.
6. Commit your changes:

   ```bash
   git add .
   git commit -m "Add: describe your change"
   ```

7. Push your branch:

   ```bash
   git push origin feature/your-feature-name
   ```

8. Open a pull request against the original repository.

### Contribution Guidelines

- Keep changes focused and easy to review.
- Preserve existing functionality unless a change is intentional.
- Test changes in a modern browser.
- Document new features and behavioral changes.
- Avoid introducing unnecessary dependencies.

## 📄 License

No `LICENSE` file is listed in the current repository root. Therefore, the project's license has not been verified.

Before distributing or reusing this project, add an appropriate license file and update this section accordingly.

## 👤 Author

**Pratik Abhang**

- GitHub: [@pratikabhang](https://github.com/pratikabhang)
- Repository: [TO-DO-LIST](https://github.com/pratikabhang/TO-DO-LIST)

---

⭐ If you find this project useful, consider starring the repository.

**Built with HTML, CSS, and JavaScript.**
