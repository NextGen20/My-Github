
---

# Flask Web Application

This repository contains a Flask web application that provides a simple user signup and profile management system. The application uses SQLAlchemy for database operations and Flask-Migrate for database migrations,also with test file in pytest that make sure that the signup page will be passed and valid.

## Features

- User signup and profile creation.
- Removal of all profiles from the database.
- Display of a personalized homepage for the user.

## Prerequisites

- Python 3.8 or higher
- Flask
- Flask-SQLAlchemy
- Flask-Migrate
- Prometheus client (for metrics)

## Installation First option Run Local:

1. Clone the repository:
   ```
   git clone https://github.com/NextGen20/My-Github.git
   ```

2. Change into the repository directory:
   ```
   cd to your flask repo name .
   ```

3. Create a virtual environment and activate it:
   ```
   python -m venv venv
   source venv/bin/activate
   ```

4. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## Running the Application

1. Set the Flask environment variable:
   ```
   export FLASK_APP=app.py
   ```

2. Initialize the database:
   ```
   flask db init
   flask db migrate
   flask db upgrade
   ```

3. Run the Flask application:
   ```
   flask run
   ```

The application will be accessible at `http://127.0.0.1:5000/`.

## Installation Second option Run with Contaienr:

## Prerequisites

- Install Docker Engine

### Clone the Repository (Optional)

```bash
git clone https://github.com/NextGen20/My-Github.git
cd your-repository
```

### Build the Docker Image

```bash
docker build -t flask-app .
```

This command will build a Docker image based on the `Dockerfile` in the current directory.

### Run the Container

```bash
docker run -d --name flask-container -p 5000:5000 flask-app
```

This command will run a container from your image, mapping port 5000 of the container to port 5000 of the host.

## Accessing the Application

Once the container is running, you can access the application via:

```
http://localhost:5000
```


## Endpoints

- `/signup`: User signup page.
- `/homepage`: Personalized homepage for the user.
- `/remove_all`: Endpoint to remove all profiles from the database.
- `/metrics`: Endpoint to view Prometheus metrics.
