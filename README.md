# Task Management App:  [Live Link](https://taskmanager-dusky-delta.vercel.app/)
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

### Install Dependencies
2. Install the project dependencies: Using npm:
   ```bash
   npm install
### Running the App Locally
3. To start the app locally, run:
   ```bash
    npm run dev
4. Open your browser and navigate to http://localhost:3000 to see the application in action.   

## How It Works
- **Adding Tasks:** Enter a task name, select a priority (Top, Middle, or Low), and pick a deadline. Click the Add Task button to save the task.
- **Editing Tasks:** You can edit an existing task by clicking the Edit button, modifying the task details, and clicking Add Task again to update it.
- **Marking Tasks as Done:** Once a task is completed, you can click the Mark Done button to move it to the completed tasks list.
- **Deleting Tasks:** You can delete any task by clicking the Delete button next to it.
- **Search and Filter:** Use the search bar to find tasks by name, and use the priority filter to see tasks of a particular priority level.


## Persistent Data with localStorage
- The app uses localStorage to store task data, so even after refreshing the page, the tasks remain available.
- The state of tasks is saved and retrieved from localStorage using React’s useEffect hook.
- Client-Side Rendering
- Since localStorage is only available in the browser, the app uses the useEffect hook to handle data fetching and saving after the component has mounted. This ensures it works seamlessly with Next.js's server-side rendering (SSR).


## Future Improvements
- **Authentication:** Add user authentication to support multiple users.
- **API Integration:** Use a backend database for task management instead of localStorage.
- **Notifications:** Add reminders and deadline alerts.
- **Mobile Optimization:** Enhance UI for better mobile responsiveness.


## Contributing

**We welcome contributions to enhance this project! Here's how you can contribute:**

### Fork the Repository

- Click on the **Fork** button at the top-right corner of the repository.

### Clone Your Fork

1. Clone the forked repository:
   ```bash
   git clone https://github.com/your-username/task-management-app.git
   cd task-management-app

    
### Create a Feature Branch

2. Create a new branch for your feature:
   ```bash
   git checkout -b feature/your-feature-name

### Commit and Push

3. Commit your changes and push them to your forked repository:
   ```bash
   git add .
   git commit -m "Describe your changes"
   git push origin feature/your-feature-name

### Open a Pull Request

4. Go to the **original repository** and open a pull request from your feature branch.

---

### Thank You! 😊

Thank you for exploring and contributing to the **Task Management App**!


---

# [Answer to Technical Questions](https://github.com/Manas-Pathak/taskmanager/blob/main/Answers%20to%20technical%20questions.md)

