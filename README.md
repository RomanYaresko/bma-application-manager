# Books Managament Assistant

## .env file:
```
POETRY_VERSION = "1.8.4"
POSTGRESQL_VERSION = "17-alpine3.20"

SECRET_KEY = "Secret"
DEBUG = "true"

DB_NAME = "db_name"
DB_USER = "db_user"
DB_PASSWORD = "db_password"
DB_HOST = "db"

DB_PORT = "5432"
BACKEND_PORT = "8000"
FRONTEND_PORT = "5000"
```

## To showcase the app:
```
git clone --recurse-submodules --remote-submodules https://github.com/RomanYaresko/bma-application-manager

#install frontend modules
cd frontend
npm install
cd ..

#start app
docker compose up --build

# to check the backend container id
docker ps

#migration and initial data load
docker exec <backend_container_id> python manage.py migrate

#frontend path - localhost:5000
#backend path - localhost:8000
```

## About the app
The application includes a user authentication system along with basic CRUD functionality for books and authors.
Only the creator of a book can edit or delete it, and only the administrator can edit or delete authors.

### Initial data includes:
- Admin user (username: admin, password: admin)
- Casual user (username: casual, password: casual)
- Small set of authors

