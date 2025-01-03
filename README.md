# React Todo App

## Overview
This is a simple React-based Todo application that allows users to manage their tasks efficiently. Users can add tasks with a title and description, view the list of tasks, and delete tasks they no longer need.

## Features
- **Add Task**: Create a new task with a title and description.
- **View Tasks**: Display all tasks in a clean and organized format.
- **Delete Task**: Remove tasks from the list when they are no longer needed.

## Installation
To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/HashirAbdulah/React-To-do-App.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd React-To-do-App
   ```

3. **Install dependencies**:
   Make sure you have [Node.js](https://nodejs.org/) installed. Then, run:
   ```bash
   npm install
   ```

4. **Start the development server**:
   ```bash
   npm run dev
   ```

5. **Open the app in your browser**:
   Navigate to `http://localhost:3000`.

## Usage
1. Enter a task title and description in the input fields.
2. Click the "Add Task" button to add the task to the list.
3. View the tasks displayed below the form.
4. To delete a task, click the "Delete" button next to the task.

## Code Structure
### Main Functionalities
- **State Management**: Uses `useState` to manage:
  - `title`: Stores the input for the task title.
  - `desc`: Stores the input for the task description.
  - `mainTask`: An array of task objects containing titles and descriptions.

- **Submit Handler**: Adds a new task to the list and resets the input fields.
  ```javascript
  const submitHandler = (e) => {
    e.preventDefault();
    setmainTask([...mainTask, { title: title, desc: desc }]);
    settitle("");
    setdesc("");
  };
  ```

- **Delete Handler**: Removes a task from the list by filtering it out.
  ```javascript
  const deleteHandler = (i) => {
    const updatedTasks = mainTask.filter((_, index) => index !== i);
    setmainTask(updatedTasks);
  };
  ```

### UI Components
- **Form**: Allows users to input task details.
- **Task List**: Displays all tasks with the option to delete them.
- **Responsive Design**: Ensures the app looks great on various devices.

## Technologies Used
- **React**: Frontend library for building the UI.
- **Tailwind CSS**: For styling the components.

## Project Structure
```
React-To-do-App/
├── public/
├── src/
│   ├── components/
│   ├── styles/
│   ├── App.js
│   ├── index.js
├── package.json
└── README.md
```

## Contribution
Feel free to fork this repository, make changes, and submit a pull request. Any contributions are welcome!

## License
This project is open-source and available under the MIT License.

## Contact
For any questions or suggestions, please contact:
- **GitHub**: [HashirAbdulah](https://github.com/HashirAbdulah)
