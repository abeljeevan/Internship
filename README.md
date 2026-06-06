# Student Task Manager

A modern, feature-rich task management application built with React, Tailwind CSS, and Vite. Perfect for students to organize and track their academic tasks efficiently.

## Features

- **Create Tasks**: Add tasks with name, description, and priority level (Low, Medium, High)
- **Read Tasks**: View all tasks in a clean, organized card layout
- **Update Tasks**: Edit existing tasks to modify details
- **Delete Tasks**: Remove tasks with confirmation
- **Task Status**: Mark tasks as Pending or Completed
- **Filter Tasks**: Filter by status (All, Pending, Completed)
- **Search Tasks**: Find tasks by name or description
- **Progress Tracking**: Real-time progress bar showing completion percentage
- **Statistics Dashboard**: View total, pending, and completed task counts
- **Local Storage**: All tasks are automatically saved to browser's local storage
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Dark Theme**: Modern dark UI with gradient accents and smooth animations

## React Concepts Used

### Functional Components
- Header
- FilterSection
- TaskForm
- TaskCard
- TaskList
- EmptyState
- App

### Hooks
- **useState**: Manages form state, filter state, search state, and modal visibility
- **useEffect**: Syncs tasks to localStorage whenever they change, auto-focuses input in forms
- **useContext**: Accesses global task state throughout the app
- **useRef**: Creates references to DOM elements for auto-focus functionality

### Context API
- **TaskContext**: Global state management for all tasks
- **TaskProvider**: Wraps the app to provide context
- Context Methods:
  - `addTask()`: Create new tasks
  - `updateTask()`: Modify existing tasks
  - `deleteTask()`: Remove tasks
  - `toggleStatus()`: Switch task status between Pending and Completed

## Tech Stack

- **React 18.2.0**: UI framework
- **Vite 5.0.8**: Fast build tool and dev server
- **Tailwind CSS 3.4.0**: Utility-first CSS framework
- **PostCSS**: CSS transformation tool
- **Autoprefixer**: Vendor prefix automation

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Navigate to the project directory:
```bash
cd d:/TASK1
```

2. Install dependencies:
```bash
npm install
```

### Running the Development Server

```bash
npm run dev
```

The application will automatically open in your default browser at `http://localhost:5173`

### Building for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
student-task-manager/
├── src/
│   ├── App.jsx           # Main app component with all features
│   ├── main.jsx          # React entry point
│   └── index.css         # Global styles and Tailwind imports
├── index.html            # HTML template
├── vite.config.js        # Vite configuration
├── tailwind.config.js    # Tailwind CSS configuration
├── postcss.config.js     # PostCSS configuration
├── package.json          # Project dependencies
└── .gitignore            # Git ignore rules
```

## Component Architecture

### App
Root component that manages global state (filter, search, modal visibility)

### TaskProvider
Context provider that wraps the entire app with global task management

### Header
Displays dashboard title, progress bar, statistics, and "New Task" button

### FilterSection
Search input and filter buttons (All, Pending, Completed)

### TaskForm
Modal form for creating and editing tasks with validation

### TaskList
Grid layout displaying filtered and searched tasks

### TaskCard
Individual task card with status toggle, edit, and delete actions

### EmptyState
Placeholder shown when no tasks exist or no search results found

## Features in Detail

### Task Creation
- Modal form with validation
- Requires task name (min. 3 characters) and description
- Select priority level
- Auto-focuses on task name input

### Task Management
- Toggle task completion status with checkbox
- Edit tasks inline (hover to see edit button)
- Delete with confirmation dialog
- View creation date on each task

### Filtering & Searching
- Real-time search across task names and descriptions
- Filter by status without affecting search
- Combined filtering and searching

### Data Persistence
- All tasks automatically saved to localStorage
- Data persists across browser sessions
- Graceful error handling for corrupted data

### Responsive Design
- Mobile-first approach
- Adapts beautifully to all screen sizes
- Touch-friendly buttons and inputs
- Smooth transitions and animations

## Tailwind CSS Features Used

- Gradient backgrounds and text
- Backdrop blur effects
- Custom border radius
- Responsive grid layout
- Shadow effects
- Opacity utilities
- Flexbox utilities
- Animation and transition utilities

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Future Enhancements

- Task categories/tags
- Due dates and reminders
- Task notes and attachments
- Export tasks as PDF
- Dark/light theme toggle
- User authentication
- Cloud sync across devices

## License

This project is open source and available under the MIT License.

## Support

For issues, questions, or suggestions, please refer to the project documentation or contact the development team.
