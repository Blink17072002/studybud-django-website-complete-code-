<h1 align="center">
  <br>
  StudyBud
  <br>
</h1>

<h4 align="center">A full-stack collaborative study room platform built with <strong>Django</strong> — where learners connect, share ideas, and study together in topic-based rooms.</h4>



## Video Demo


## Live Demo



## Key Features

**User Authentication:** Custom Django user model with email-based login, registration, and profile editing 

**Study Rooms:** Create, update, and delete rooms tagged by topic with live participant tracking 

**Real-time Messaging:** Post and delete messages within study rooms, with activity feed on the home page 

**Topic Filtering:** Browse rooms by topic or search across room names, descriptions, and topics 

**User Profiles:** Public profile pages showing a user's rooms and message activity 

**REST API:** JSON API endpoints for rooms and users powered by Django REST Framework 

**Responsive UI:** Mobile-friendly layout with a dark-mode themed interface 



## Tech Stack

**Backend**
- **Python 3.10+** — core programming language
- **Django 4.x** — full-stack web framework (MVT architecture)
- **Django REST Framework** — REST API endpoints
- **Django CORS Headers** — cross-origin resource sharing support

**Frontend**
- **HTML5 / Jinja2 Templates** — server-side rendered pages
- **Vanilla CSS** — custom styling with a dark-mode design

**Database**
- **SQLite** (development & hosted demo) — zero-configuration relational DB


## Architecture Highlights

- **Custom User Model** — Extended `AbstractUser` replacing username-based auth with email-based auth.
- **Generic Relations** — Leverages Django's Q objects for complex, multi-field search queries.
- **CRUD via Class/Function Views** — Full CRUD on Rooms, Messages, and User Profiles using Django function-based views.
- **REST API** — Exposes `/api/rooms/` and `/api/users/` for potential frontend decoupling.

---

## Local Setup

Follow these steps to run the project on your machine.

### Prerequisites
- Python 3.10+
- pip

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/studybud.git
cd studybud
```

### 2. Create & Activate a Virtual Environment

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Migrations

```bash
python manage.py migrate
```

### 5. (Optional) Create a Superuser

```bash
python manage.py createsuperuser
```

### 6. Run the Development Server

```bash
python manage.py runserver
```

Open your browser at **http://127.0.0.1:8000** 


##  API Endpoints

The app exposes a simple REST API:

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/rooms/` | List all study rooms |
| `GET` | `/api/routes/` | List all available API routes |

---

## Project Structure

```
studybud/
├── base/               # Core app (models, views, urls, forms, api)
│   ├── models.py       # User, Room, Topic, Message models
│   ├── views.py        # All route handlers
│   ├── urls.py         # URL routing
│   ├── forms.py        # Django forms
│   └── serializers.py  # DRF serializers
├── studybud/           # Project configuration
│   ├── settings.py     # App settings (env-variable aware)
│   └── urls.py         # Root URL config
├── templates/          # HTML templates (Jinja2)
├── static/             # CSS, JS, images
├── staticfiles/        # Collected static files (for production)
├── requirements.txt    # Python dependencies
└── manage.py           # Django management script
```


## License

This project is based on the open-source StudyBud tutorial by [Dennis Ivy](https://github.com/divanov11/StudyBud).
