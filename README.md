# Simple CRUD API

Here's a simple documentation for the provided Go code:


# Simple Todo API Documentation

This documentation provides an overview of a simple Todo API implemented in Go.

## Introduction

This Todo API allows users to perform basic CRUD (Create, Read, Update, Delete) operations on Todo items. It exposes endpoints for creating, retrieving, updating, and deleting Todo items.

## Endpoints

### GET /todos

Retrieves all Todo items stored in the server.


```
GET /todos
```

**Response:**
```json
[
  {
    "ID": 1,
    "Task": "Example task 1"
  },
  {
    "ID": 2,
    "Task": "Example task 2"
  }
]
```

### POST /todos

Creates a new Todo item and adds it to the server.

**Request:**
```
POST /todos
Content-Type: application/json

{
  "ID": 3,
  "Task": "New task"
}
```

**Response:**
```json
{
  "ID": 3,
  "Task": "New task"
}
```

### DELETE /todos?id={id}

Deletes a Todo item with the specified ID.

**Request:**
```
DELETE /todos?id=3
```

**Response:**
```json
{
  "message": "Success to delete todo"
}
```

### PUT /todos?id={id}

Updates a Todo item with the specified ID.

**Request:**
```
PUT /todos?id=1
Content-Type: application/json

{
  "ID": 1,
  "Task": "Updated task"
}
```

**Response:**
```json
{
  "message": "Success to update todo"
}
```

## Dependencies

- `encoding/json`: Package for encoding and decoding JSON data.
- `log`: Package for logging messages.
- `net/http`: Package for HTTP server and client functionality.
- `strconv`: Package for converting strings to other types, such as integers.
```