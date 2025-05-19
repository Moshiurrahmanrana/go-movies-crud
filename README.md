# Go Movies CRUD API

A RESTful API built with Go and Gorilla Mux for managing a movie database. This API provides endpoints to perform CRUD (Create, Read, Update, Delete) operations on movie records.

## Features

- Create new movies
- Get all movies
- Get a specific movie by ID
- Update existing movies
- Delete movies
- JSON response format
- RESTful architecture

## Prerequisites

- Go 1.16 or higher
- Gorilla Mux package

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Moshiurrahmanrana/go-movies-crud.git
```

2. Navigate to the project directory:
```bash
cd go-movies-crud
```

3. Install dependencies:
```bash
go mod tidy
```

## Running the Application

Start the server:
```bash
go run main.go
```

The server will start on port 8000.

## API Endpoints

### Get All Movies
- **GET** `/movies`
- Returns a list of all movies

### Get Movie by ID
- **GET** `/movies/{id}`
- Returns a specific movie by ID
- Returns 404 if movie not found

### Create Movie
- **POST** `/movies`
- Creates a new movie
- Request body should be JSON with the following structure:
```json
{
    "isbn": "string",
    "title": "string",
    "director": {
        "firstname": "string",
        "lastname": "string"
    }
}
```

### Update Movie
- **PUT** `/movies/{id}`
- Updates an existing movie
- Request body should be JSON with the same structure as Create Movie

### Delete Movie
- **DELETE** `/movies/{id}`
- Deletes a movie by ID

## Example Usage

### Create a Movie
```bash
curl -X POST http://localhost:8000/movies \
-H "Content-Type: application/json" \
-d '{
    "isbn": "438227",
    "title": "Movie One",
    "director": {
        "firstname": "John",
        "lastname": "Doe"
    }
}'
```

### Get All Movies
```bash
curl http://localhost:8000/movies
```

## Project Structure

## Technologies Used

- Go
- Gorilla Mux
- JSON

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
