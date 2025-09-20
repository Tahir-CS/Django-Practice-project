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

## Project Structure

```
mysite/
├── manage.py                 # Django management script
├── mysite/                   # Main project directory
│   ├── __init__.py
│   ├── settings.py          # Project settings
│   ├── urls.py              # URL routing
│   └── wsgi.py              # WSGI configuration
├── polls/                    # Polls application
│   ├── __init__.py
│   ├── admin.py             # Admin interface configuration
│   ├── apps.py              # App configuration
│   ├── models.py            # Data models (Question, Choice)
│   ├── tests.py             # Test cases
│   ├── views.py             # View functions
│   └── migrations/          # Database migration files
└── db.sqlite3               # SQLite database file
```

## Getting Started

### Prerequisites

- Python 3.x
- Django 5.x

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Django-Practice-project
   ```

2. Install Django (if not already installed):
   ```bash
   pip install Django
   ```

3. Navigate to the project directory:
   ```bash
   cd mysite
   ```

4. Run migrations:
   ```bash
   python manage.py migrate
   ```

5. Create a superuser:
   ```bash
   python manage.py createsuperuser
   ```

6. Start the development server:
   ```bash
   python manage.py runserver
   ```

7. Visit `http://127.0.0.1:8000/admin/` to access the Django Admin interface.

## Models

### Question Model
- `question_text`: CharField for the question text (max 200 characters)
- `pub_date`: DateTimeField for the publication date
- `was_published_recently()`: Method to check if question was published within the last day

### Choice Model
- `question`: ForeignKey relationship to Question
- `choice_text`: CharField for the choice text (max 200 characters)
- `votes`: IntegerField to track vote count (default 0)

## Django Admin Features

The admin interface provides:
- Customized Question admin with fieldsets and inline choice editing
- List display showing question text, publication date, and recent publication status
- Filtering by publication date
- Search functionality by question text
- Tabular inline editing for choices

## Development

To add new features or modify the application:

1. Make model changes in `polls/models.py`
2. Create migrations: `python manage.py makemigrations polls`
3. Apply migrations: `python manage.py migrate`
4. Update admin configuration in `polls/admin.py` if needed

## Testing

Run the test suite with:
```bash
python manage.py test polls
```

## Contributing

This is a learning project based on the Django tutorial. Feel free to experiment and extend the functionality.

## License

This project is for educational purposes and follows the Django tutorial structure.