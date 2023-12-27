# HTMX TODO List CRUD Webapp

_Simple TODO list CRUD (Create, Read, Update, Delete) web application built with Go using the `babyapi` framework and HTMX._

## STACK

-   **Frontend**: HTMX
-   **Backend**: Go (babyapi)
-   **Database**: Redis (optional)
-   **Deployment**: Acorn (optional)

## Running the Application

To run the application, use the go run command:

```sh
go run main.go serve
```

You can interact with the API from the CLI using:

```sh
go run main.go post TODOs '{"title": "YOUR_TITLE", "description": "YOUR_DESCRIPTION"}'
go run main.go list TODOs
go run main.go get TODOs 'TODO_ID'
go run main.go delete TODOs 'TODO_ID'
go run main.go put TODOs 'TODO_ID'
```
Navigate to `http://localhost:8080/todos` in your browser to interact with the application.

By default the app will use an in-memory database. If you would like to use a persistent Redis database, place a .env file in the root of the project with the following contents:
```sh
REDIS_HOST="YOUR_REDIS_HOST"
REDIS_PASS="YOUR_REDIS_PASSWORD"
````
