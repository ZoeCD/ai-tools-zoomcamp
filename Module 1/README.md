# Django TODO App

A simple TODO web application built with Django, managed with `uv`.

## Features

- Create, edit, and delete TODOs
- Assign due dates with overdue and today indicators
- Mark TODOs as completed / reopen them
- Django admin panel included

## Requirements

- Python 3.12+
- [uv](https://docs.astral.sh/uv/) (`brew install uv`)

## Getting Started

**1. Clone the repo:**
```bash
git clone <your-repo-url>
cd <repo-folder>
```

**2. Install dependencies:**
```bash
uv sync
```

**3. Run database migrations:**
```bash
uv run python manage.py migrate
```

**4. Start the development server:**
```bash
uv run python manage.py runserver
```

**5. Open your browser at:** `http://localhost:8000`

## Admin Panel

Create a superuser to access the Django admin at `http://localhost:8000/admin/`:

```bash
uv run python manage.py createsuperuser
```

## Project Structure

```
├── manage.py
├── pyproject.toml          # Dependencies managed by uv
├── todo_project/           # Django project settings and URLs
└── todos/                  # TODO app
    ├── models.py           # Todo model
    ├── views.py            # CRUD + toggle views
    ├── forms.py
    ├── urls.py
    ├── admin.py
    ├── migrations/
    └── templates/todos/    # HTML templates
```
