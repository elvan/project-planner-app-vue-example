# Vue Project Planner

## Description

This project is a Vue.js application designed to help users manage and track their projects effectively. It allows for the addition, update, and deletion of projects, along with dynamic filtering to view projects based on their completion status. The project leverages Vue components, routing, and a mock JSON server to simulate a full-stack application's functionality in a client-side environment.

## Features

- **Project Management** - Users can add new projects, update existing ones, and delete them as needed. Each project entry includes a title, details, and a completion status to provide a comprehensive overview.

  - **Add Projects**: Users can submit new projects via a dedicated form.
  - **Edit Projects**: Each project can be updated with new information or marked as complete.
  - **Delete Projects**: Projects can be removed from the list.

- **Dynamic Project Display and Filtering** - The application supports dynamic filtering of projects based on their completion status, enhancing usability by allowing users to focus on active or completed projects.

  - **Filtering Functionality**: Projects can be filtered to display all, completed, or ongoing projects.

- **UI Enhancements and Usability** - With the integration of Material Icons and a custom navigation bar, the application offers an intuitive and user-friendly interface.
  - **Material Icons**: Used for delete, edit, and completion actions on each project.
  - **Navigation Bar**: Facilitates easy navigation between adding a new project and viewing existing projects.

## Installation

To set up the project locally, follow these steps:

### Prerequisites

- Node.js and npm installed on your machine.
- Vue CLI installed globally (`npm install -g @vue/cli`).

### Environment Setup

1. Clone the repository to your local machine.
2. Navigate to the project directory.

### Installation Commands

```bash
# Install dependencies
npm install

# Start the JSON server
npm run json-server

# Serve the application on a local development server
npm run serve
```

## Usage

After setting up the project, you can use it by navigating to `http://localhost:8080` in your web browser. Here you can:

- **Add a New Project**: By navigating to the 'Add a New Project' section through the navigation bar.
- **Edit an Existing Project**: Click on the edit icon beside any project to update its details or mark it as complete.
- **Delete a Project**: Click on the delete icon to remove a project from the list.
- **Filter Projects**: Use the filter options to toggle between viewing all, completed, or ongoing projects.

For more specific interactions or to understand the underlying code, refer to the project files in the `src` directory, particularly the `views` and `components` folders for Vue components.
