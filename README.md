# Task Management App

A simple **Task Management** application built with **Next.js** to manage tasks with priority, deadlines, and completion status. This app allows users to add, edit, delete, mark tasks as completed, and filter them based on search and priority. It uses **localStorage** to persist tasks data across page reloads.

## Features

- **Add Tasks**: Users can add tasks with a name, priority, and deadline.
- **Edit Tasks**: Users can edit existing tasks.
- **Delete Tasks**: Users can delete tasks from the list.
- **Mark Tasks as Completed**: Users can mark tasks as done and move them to the completed list.
- **Search and Filter**: Users can search for tasks by name and filter by priority.
- **Persistent Data**: Tasks and completed tasks are saved in `localStorage`, so data persists even after a page refresh.

## Technologies Used

- **Next.js**: Framework for React-based applications.
- **React**: For building the user interface and managing component state.
- **CSS Modules**: Scoped CSS styling for individual components.
- **localStorage**: For saving task data persistently across page reloads.
  
## Installation & Setup

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v14.x or higher)
- **npm** (node package manager) or **yarn** (alternative package manager)

### Clone the Repository

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/task-management-app.git
   cd task-management-app
