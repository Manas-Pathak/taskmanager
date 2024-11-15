# Answers to Technical Questions:

### 1. How long did you spend on the coding test?

I spent around **4-5 hours** on the coding test. This time was primarily spent on understanding the requirements, implementing the core features of the task management app (such as adding, editing, and deleting tasks), and ensuring the persistence of data using `localStorage`. The additional time was spent on testing the application, refining the UI, and ensuring responsiveness.

---

### 2. What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.

The most useful feature added to **React (the primary language used in Next.js)** in its latest version is **React Hooks** (specifically the `useState` and `useEffect` hooks). These hooks allow developers to manage state and side effects in functional components, enabling a more concise and readable code structure compared to class components.

For example, here’s how I used `useState` and `useEffect` in the task management app to persist tasks data:

```javascript
import { useState, useEffect } from 'react';

function TaskScheduler() {
  const [tasks, setTasks] = useState([]);

  // Load tasks from localStorage on initial render
  useEffect(() => {
    const storedTasks = JSON.parse(localStorage.getItem('tasks'));
    if (storedTasks) {
      setTasks(storedTasks);
    }
  }, []);

  // Save tasks to localStorage whenever tasks change
  useEffect(() => {
    localStorage.setItem('tasks', JSON.stringify(tasks));
  }, [tasks]);

  // Function to add a task
  const addTask = (task) => {
    setTasks([...tasks, task]);
  };

  return (
    <div>
      <button onClick={() => addTask({ id: 1, task: 'New Task' })}>Add Task</button>
      <ul>
        {tasks.map(task => (
          <li key={task.id}>{task.task}</li>
        ))}
      </ul>
    </div>
  );
}

export default TaskScheduler;
 ```
---

### 3. How would you track down a performance issue in production? Have you ever had to do this?

To track down a performance issue in production, I would take the following steps:

1. **Use Browser Developer Tools**:
   - Tools like **Google Chrome's Performance tab** and **Network tab** can help identify bottlenecks in rendering, asset loading, and API calls.
   - By recording the performance profile, I can check for unnecessary re-renders, slow loading times, or blocking resources.

2. **Log Performance Metrics**:
   - Implement logging within the app to track response times, load times, or any lagging UI interactions.
   - **React Profiler** and third-party libraries like **Lighthouse** can give insights into performance.

3. **Check API Latency**:
   - If the app relies on external APIs, monitoring the response times of API calls can help identify issues that may slow down the user experience.

4. **Monitor with Tools**:
   - Tools like **New Relic**, **Datadog**, or **Sentry** can provide real-time performance metrics and error tracking for production apps.

5. **Optimize React Rendering**:
   - Tools like **React Developer Tools** can help identify unnecessary re-renders in React components.
   - I would also use **React.memo**, **useMemo**, and **useCallback** to optimize the components that are rendering more than necessary.

**Experience:**
I have faced performance issues during production for a previous project, specifically with inefficient re-renders and slow loading times due to large data sets. By profiling the application and optimizing the components, I was able to significantly improve performance.

---

### 4. If you had more time, what additional features or improvements would you consider adding to the task management application?

If I had more time, I would consider the following improvements for the task management app:

1. **User Authentication**:
   - Implement user login and authentication (using **JWT**, **OAuth**, or a service like **Firebase**) to allow users to create personal task lists and access them across multiple devices.

2. **Backend API Integration**:
   - Replace **localStorage** with a persistent backend database (like **MongoDB** or **Firebase**) to store tasks. This would allow for real-time synchronization across devices and better scalability.

3. **Task Priority Sorting**:
   - Add functionality to **sort tasks by priority** or **deadline**, and implement a **drag-and-drop interface** for task reordering.

4. **Due Date Reminders**:
   - Implement a **reminder** or **notification feature** that alerts users when a task's deadline is approaching.

5. **Task Categories**:
   - Allow users to create **categories** for tasks (e.g., **Work**, **Personal**, etc.) and filter tasks by category.

6. **Mobile Optimization**:
   - Improve mobile responsiveness to make sure the app works seamlessly across all devices.

7. **Testing and Error Handling**:
   - Add **unit and integration tests** (using libraries like **Jest** or **React Testing Library**) and improve error handling for a more robust and stable application.


