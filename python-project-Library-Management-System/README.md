# Library Management System

## Project Overview

A modular Jupyter-based library management system that provides an interactive interface for managing books, students, and administrators in a library environment. The system is designed to be run in Jupyter notebooks, making it easily accessible for educational and demonstration purposes.

**Version:** 1.0.0 (April 25, 2025)

## Table of Contents

1. [Features](#features)
2. [System Architecture](#system-architecture)
3. [Getting Started](#getting-started)
4. [Usage Guide](#usage-guide)
5. [Next Steps](#next-steps)
6. [Potential Risks](#potential-risks)
7. [Advanced Ideas](#advanced-ideas)

## Features

### Current Functionality

#### User Management

- **Student Accounts**
  - Registration system for new students
  - Login/authentication for existing students
  - Profile viewing for administrators

- **Admin Accounts**
  - Secure admin login
  - Admin dashboard with system management tools

#### Book Management

- **For Students**
  - Browse available books
  - Borrow books (with automatic due date assignment)
  - Return borrowed books
  - View currently borrowed books

- **For Administrators**
  - Add new books to the library
  - Remove books from the collection
  - View comprehensive book details including borrowing status
  - Track which student has borrowed each book

#### Student Management (Admin Only)

- View all registered students
- View detailed student information
- Remove student accounts
- See books borrowed by each student

### Technical Features

- JSON-based persistent storage for data
- Object-oriented design for maintainability
- Interactive widgets-based UI
- Modular architecture for easy extension

## System Architecture

The system follows a modular design with clear separation of concerns:

1. **Configuration** - Central settings for the application
2. **Core Models** - Class definitions for Book, User, Student, and Admin
3. **Database Manager** - Handles data persistence and retrieval
4. **UI Components** - Reusable widget builders
5. **Main Application** - Business logic and user interaction flows

### Data Storage

All data is stored in three JSON files:

- `students_db.json` - Student account information
- `admins_db.json` - Admin account information
- `books_db.json` - Book catalog with borrowing status

## Getting Started

### Prerequisites

- Jupyter Notebook or JupyterLab
- Python 3.6 or higher
- Required packages: `ipywidgets`

### Installation

1. Copy the cells from the provided notebook into a new Jupyter notebook.
2. Run each cell in sequence (Cells 1-8).
3. The system will initialize the necessary databases if they don't exist.

### Default Credentials

- **Student Login**: username='student1', password='pass1'
- **Admin Login**: username='admin1', password='admin1'

## Usage Guide

### Student Workflow

1. Log in with student credentials
2. From the dashboard, click "Browse Books" to see available titles
3. Click "Borrow" on any available book
4. View your borrowed books by clicking "My Borrowed Books"
5. Return books by clicking the "Return" button

### Admin Workflow

1. Log in with admin credentials
2. From the dashboard, select "Manage Books" or "Manage Students"
3. Add new books through the form at the top of the "Manage Books" screen
4. Remove books by clicking the "Remove" button next to each book
5. View student details and remove students from the "Manage Students" screen

## Next Steps

### Short-Term Improvements

- Add pagination for book and student listings
- Implement book search functionality
- Add book categories/genres
- Enable profile editing for students
- Create a reservation system for books currently borrowed

### Medium-Term Goals

- Implement fine calculation for overdue books
- Add email notifications for due dates
- Create a reporting dashboard for administrators
- Add book cover image support
- Implement barcode scanning for physical books

### Long-Term Vision

- Move to a web-based architecture for wider accessibility
- Create a mobile application for students
- Implement an AI recommendation system for books
- Integrate with external library databases
- Support inter-library loan systems

## Potential Risks

### Technical Risks

- **Data Integrity**: JSON files could become corrupted if the application crashes during write operations
- **Scalability**: Current implementation may slow down with large numbers of books or users
- **Security**: Password storage is currently plaintext, which is not secure for production use

### Operational Risks

- **Usability**: Interface may need refinement based on user feedback
- **Data Loss**: No backup system currently implemented
- **Maintainability**: Extending functionality requires understanding the component structure

### Mitigation Strategies

- Implement transaction-based file writes
- Add data validation and sanitization
- Create automated backup system
- Implement proper password hashing
- Develop comprehensive documentation

## Advanced Ideas

### Feature Enhancements

- **Multi-branch Support**: Allow the system to manage multiple library branches
- **Resource Types**: Extend beyond books to manage other library resources (journals, media, etc.)
- **Recommendation Engine**: Suggest books based on borrowing history
- **Social Features**: Allow students to rate books and share recommendations
- **Reading Lists**: Allow creation of curated reading lists for courses
- **Integration**: Connect with academic databases and online resources
- **Analytics**: Provide insights into library usage and popular materials

### Technical Improvements

- **Database Migration**: Move from JSON files to a proper database system
- **API Development**: Create a RESTful API to allow third-party integrations
- **Authentication**: Implement OAuth or similar authentication protocols
- **Containerization**: Package the application in Docker for easy deployment
- **Testing Framework**: Develop automated tests for all components
- **Continuous Integration**: Set up CI/CD pipeline for development

---

## Contributing

This project is open for contributions. Please follow the modular architecture when adding new features.

## License

[MIT License](LICENSE)

## Acknowledgements

- Created as a modular educational project for library management
- Built with Python and ipywidgets
