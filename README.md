# Multilingual FAQ System

A Django-based web application for managing multilingual FAQs. This project supports:

*   Multilingual Content: FAQs can be translated into multiple languages (e.g., English, Hindi, Bengali).
*   WYSIWYG Editor: Rich text editing for FAQ answers using `django-ckeditor`.
*   REST API: A fully functional API for managing FAQs with language support.
*   Caching: Redis-based caching for improved performance.
*   Admin Panel: User-friendly interface for managing FAQs.

## Features

*   Dynamic translations using Google Translate API.
*   Language-specific FAQ retrieval via API (`?lang=hi` for Hindi).
*   Redis caching for faster responses.
*   Docker support for easy deployment.

## Technologies Used

*   **Backend:** Django, Django REST Framework
*   **Database:** SQLite (default)
*   **Caching:** Redis
*   **Translation:** `googletrans` library
*   **WYSIWYG Editor:** `django-ckeditor`

## Installation

### Prerequisites

*   Python 3.9+
*   Redis

### Steps

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/your-username/multilingual-faq-system.git](https://github.com/your-username/multilingual-faq-system.git)
    cd multilingual-faq-system
    ```

2.  **Create a virtual environment:**

    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**

    *   **Windows:**

        ```bash
        venv\Scripts\activate
        ```

    *   **Mac/Linux:**

        ```bash
        source venv/bin/activate
        ```

4.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

5.  **Run migrations:**

    ```bash
    python manage.py migrate
    ```

6.  **Create a superuser:**

    ```bash
    python manage.py createsuperuser
    ```

7.  **Start the server:**

    ```bash
    python manage.py runserver
    ```

8.  **Access:**

    *   **Admin:** <http://localhost:8000/admin/>
    *   **API:** <http://localhost:8000/api/faqs/?lang=hi>

### Docker Setup

1.  **Build and start containers:**

    ```bash
    docker-compose up --build
    ```

2.  **Access the app at:** <http://localhost:8000>

## API Endpoints

*   **Get all FAQs:**

    ```bash
    GET /api/faqs/
    ```

*   **Filter by language:**

    ```bash
    GET /api/faqs/?lang=hi
    ```

## Example Response

```json
[
  {
    "id": 1,
    "question": "नमस्ते",
    "answer": "यह एक उदाहरण उत्तर है।"
  }
]
```
##Admin Panel

* Visit <http://localhost:8000/admin/>.
* Log in with your superuser credentials.
* Add/Edit FAQs with the WYSIWYG editor.

##Contributing
*Fork the repository.
*Create a branch:
```
git checkout -b feature/your-feature
```
##Commit changes:
```
git commit -m "feat: Add your feature"
```

## License

MIT License. See `LICENSE` for details.
