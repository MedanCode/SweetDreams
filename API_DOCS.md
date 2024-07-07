# API Documentation

## Authentication

### Register User
- **URL**: `/register`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "username": "string",
    "password": "string",
    "email": "string",
    "full_name": "string"
  }
  ```
- **Response**:
  ```json
  {
    "message": "User created successfully"
  }
  ```

### Get Token
- **URL**: `/token`
- **Method**: `POST`
- **Request Body**:
  ```x-www-form-urlencoded
  username: string
  password: string
  ```
- **Response**:
  ```json
  {
    "access_token": "string",
    "token_type": "bearer"
  }
  ```

## User

### Get Current User
- **URL**: `/users/me`
- **Method**: `GET`
- **Headers**: 
  ```http
  Authorization: Bearer YOUR_ACCESS_TOKEN
  ```
- **Response**:
  ```json
  {
    "username": "string",
    "email": "string",
    "full_name": "string",
    "disabled": boolean
  }
  ```

## Interactions

### Post Interaction
- **URL**: `/chat`
- **Method**: `POST`
- **Headers**: 
  ```http
  Authorization: Bearer YOUR_ACCESS_TOKEN
  Content-Type: application/json
  ```
- **Request Body**:
  ```json
  {
    "message": "string"
  }
  ```
- **Response**:
  ```json
  {
    "response": "string"
  }
  ```

### Get All Interactions
- **URL**: `/interactions`
- **Method**: `GET`
- **Headers**: 
  ```http
  Authorization: Bearer YOUR_ACCESS_TOKEN
  ```
- **Response**:
  ```json
  [
    {
      "id": "string",
      "timestamp": "string",
      "user": "string",
      "user_input": "string",
      "ai_response": "string"
    }
  ]
  ```
