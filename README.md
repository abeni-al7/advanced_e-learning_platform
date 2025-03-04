# Advanced E-Learning Platform

This project is an advanced e-learning platform built with Django, Channels, and other modern web technologies. It provides a comprehensive environment for creating and managing online courses, engaging with students, and facilitating real-time communication.

## Features

*   **Course Management:**
    *   Create, update, and delete courses.
    *   Organize courses into modules and content.
    *   Support for various content types (text, video, images, files).
*   **User Management:**
    *   User registration and authentication.
    *   Student enrollment in courses.
    *   Instructor roles with course creation permissions.
*   **Real-time Chat:**
    *   Course-specific chat rooms for student interaction.
    *   Asynchronous communication using Channels and WebSockets.
*   **REST API:**
    *   API endpoints for courses and subjects.
    *   Enrollment via API.
*   **Caching:**
    *   Redis caching for improved performance.
    *   Cache invalidation strategies for dynamic content.
*   **Dockerized Deployment:**
    *   Easy setup and deployment using Docker and Docker Compose.

## Technologies Used

*   **Backend:**
    *   Django: High-level Python web framework.
    *   Django REST Framework: Toolkit for building Web APIs.
    *   Channels: ASGI framework for WebSockets and real-time features.
    *   Redis: In-memory data structure store, used as a cache and message broker.
    *   PostgreSQL: Relational database.
*   **Frontend:**
    *   HTML, CSS, JavaScript
*   **DevOps:**
    *   Docker: Containerization platform.
    *   Docker Compose: Tool for defining and running multi-container Docker applications.
    *   Nginx: Web server and reverse proxy.

## Project Structure

├── .env # Environment variables 
├── .gitignore # Specifies intentionally untracked files that Git should ignore 
├── api_examples/ # Example API usage scripts 
├── chat/ # Chat application (Channels) 
├── config/ # Nginx and uWSGI configurations 
├── courses/ # Core application for course management 
├── data/ # Data persistence for database and cache 
├── db.sqlite3 # SQLite database (development) 
├── docker-compose.yml # Docker Compose configuration 
├── Dockerfile # Docker image definition 
├── educa/ # Main Django project directory 
├── manage.py # Django management script 
├── media/ # Media files (user uploads) 
├── README.md # This file 
├── requirements.txt # Python dependencies 
├── ssl/ # SSL certificates 
├── static/ # Static files (CSS, JavaScript) 
├── students/ # Student-related application 
└── wait-for-it.sh # Utility script to wait for database availability

## Setup Instructions

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/abeni-al7/advanced_e-learning_platform.git
    cd advanced_e_learning_platform
    ```

2.  **Create a virtual environment:**

    ```bash
    python -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure environment variables:**

    *   Create a [.env](http://_vscodecontentref_/6) file based on the provided example or set environment variables directly.

5.  **Run migrations:**

    ```bash
    python manage.py migrate
    ```

6.  **Create a superuser:**

    ```bash
    python manage.py createsuperuser
    ```

7.  **Run the development server:**

    ```bash
    python manage.py runserver
    ```

## Docker Deployment

1.  **Build the Docker image:**

    ```bash
    docker build .
    ```

2.  **Run with Docker Compose:**

    ```bash
    docker compose up -d
    ```

## Configuration

*   **Django settings:** Located in [settings](http://_vscodecontentref_/7).  Use [local.py](http://_vscodecontentref_/8) for development and [prod.py](http://_vscodecontentref_/9) for production.
*   **Nginx:** Configuration template in [default.conf.template](http://_vscodecontentref_/10).
*   **uWSGI:** Configuration file in [uwsgi.ini](http://_vscodecontentref_/11).

## Contributing

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Implement your changes.
4.  Submit a pull request.

