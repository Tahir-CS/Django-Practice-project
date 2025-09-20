# Django Tutorial: Polls Application

This project is a complete implementation of the polling application from **Part 2 of the official Django Tutorial**. It serves as a practical, hands-on introduction to the core features of the Django web framework.

The application allows administrators to create poll questions and provide a set of choices for each question.

## Key Features Implemented

*   **Django Project Structure:** A fully configured `mysite` project containing a `polls` application.
*   **Data Models:** Custom `Question` and `Choice` models created in `polls/models.py` to define the database structure.
*   **Database Migrations:** Utilizes Django's built-in migration system to create and manage the database schema (`db.sqlite3`).
*   **Django Admin:** The `Question` and `Choice` models are registered with the Django Admin, providing a powerful and auto-generated interface for site administrators to manage content.
*   **User Management:** Includes the creation of multiple superuser accounts for accessing the admin backend.
*   **Version Control:** The project is version-controlled with Git and includes a `.gitignore` file to exclude unnecessary files.

## Technology Stack

*   **Backend:** Python / Django
*   **Database:** SQLite (the development default)
*   **Development Environment:** Visual Studio Code with Dev Tunnels for port forwarding.
