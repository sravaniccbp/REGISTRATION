# API Documentation

## Auth Endpoints

### Register
- `POST /api/auth/register`
- Request Body: `{ "username": "user", "password": "pass" }`
- Response: `{ "auth": true, "token": "JWT" }`

### Login
- `POST /api/auth/login`
- Request Body: `{ "username": "user", "password": "pass" }`
- Response: `{ "auth": true, "token": "JWT" }`

## To-Do Endpoints

### Create To-Do
- `POST /api/todos`
- Headers: `{ "x-access-token": "JWT" }`
- Request Body: `{ "description": "Task", "status": "Incomplete" }`
- Response: `{ "id": 1 }`

### Get To-Dos
- `GET /api/todos`
- Headers: `{ "x-access-token": "JWT" }`
- Response: `[ { "id": 1, "description": "Task", "status": "Incomplete" } ]`

### Update To-Do
- `PUT /api/todos/:id`
- Headers: `{ "x-access-token": "JWT" }`
- Request Body: `{ "description": "Updated Task", "status": "Complete" }`
- Response: `{ "updated": 1 }`

### Delete To-Do
- `DELETE /api/todos/:id`
- Headers: `{ "x-access-token": "JWT" }`
- Response: `{ "deleted": 1 }`
