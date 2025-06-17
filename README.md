
# alx-files_manager API Documentation

The `alx-files_manager` is a robust file management system designed to handle various file and user operations through a comprehensive set of API endpoints. This documentation provides detailed information on each endpoint, including request methods, authentication, parameters, and expected responses.

## Table of Contents
- [API Endpoints](#api-endpoints)
  - [GET /connect](#get-connect)
  - [GET /users/me](#get-usersme)
  - [POST /new file](#post-new-file)
  - [POST /new folder](#post-new-folder)
  - [GET /list files](#get-list-files)
  - [GET /get file](#get-get-file)
  - [PUT /Publish file](#put-publish-file)
  - [PUT /Unpublish file](#put-unpublish-file)
  - [GET /Get file data](#get-get-file-data)
  - [POST /New User](#post-new-user)
- [Postman Collection](#postman-collection)

## API Endpoints

### GET /connect
- **Description**: Establishes a connection to the file management system using basic authentication. Upon successful authentication with a username (`bob@dylan.com`) and password (`toto1234!`), returns a valid token valid for 24 hours.
- **URL**: `localhost:5000/connect`
- **Method**: GET
- **Authentication**: Basic Auth
- **Response**: 
  - **Status**: 200 OK
  - **Body**: `{"token": "9a301973-bd36-45a7-9ac3-7b23fb45c1d8"}`
  - **Headers**: 
    - `X-Powered-By`: Express
    - `Content-Type`: application/json; charset=utf-8
    - `Content-Length`: 48
    - `ETag`: W/"30-a+nnoaJB0/Z6fYNFG4EE2kweAeE"
    - `Date`: Sun, 04 Aug 2024 16:21:18 GMT
    - `Connection`: keep-alive
    - `Keep-Alive`: timeout=5

### GET /users/me
- **Description**: Retrieves detailed information about the currently authenticated user, including profile data and permissions.
- **URL**: `localhost:5000/users/me`
- **Method**: GET
- **Authentication**: Bearer Token (via `X-token` header, e.g., `9a301973-bd36-45a7-9ac3-7b23fb45c1d8`)
- **Response**: (TBD)

### POST /new file
- **Description**: Creates a new file in the system. Requires a JSON body with `name` (e.g., `myText.txt`), `type` (e.g., `file`), and `data` (e.g., base64 encoded data `SGVsbG8gV2Vic3RhY2shCg==`).
- **URL**: `https://verbose-space-goldfish-jvx6576q4xq3599v-5000.app.github.dev/files`
- **Method**: POST
- **Authentication**: Bearer Token (via `X-token` header, e.g., `{{token}}`)
- **Request Body**: 
  ```json
  {
    "name": "myText.txt",
    "type": "file",
    "data": "SGVsbG8gV2Vic3RhY2shCg=="
  }
  ```
- **Response**: (TBD)

### POST /new folder
- **Description**: Creates a new folder within the file system. Requires a JSON body with `name` (e.g., `uploads`) and `type` (e.g., `folder`).
- **URL**: `localhost:5000/files`
- **Method**: POST
- **Authentication**: Bearer Token (via `X-token` header, e.g., `{{token}}`)
- **Request Body**: 
  ```json
  {
    "name": "uploads",
    "type": "folder"
  }
  ```
- **Response**: (TBD)

### GET /list files
- **Description**: Returns a list of all files available in the system. Supports query parameters `parentId` (e.g., `66ae9ee38fd3793cb6dc4769`) and `page` (e.g., `0`).
- **URL**: `localhost:5000/files?parentId=66ae9ee38fd3793cb6dc4769&page=0`
- **Method**: GET
- **Authentication**: Bearer Token (via `X-Token` header, e.g., `{{token}}`)
- **Response**: (TBD)

### GET /get file
- **Description**: Retrieves the content or metadata of a specific file. Requires a file ID (e.g., `66afb3429956f4386184913d`) in the URL path.
- **URL**: `localhost:5000/files/66afb3429956f4386184913d`
- **Method**: GET
- **Authentication**: Bearer Token (via `X-Token` header, e.g., `{{token}}`)
- **Response**: (TBD)

### PUT /Publish file
- **Description**: Publishes a specified file, making it accessible to other users or systems. Requires a file ID (e.g., `66afb3429956f4386184913d`) in the URL path.
- **URL**: `localhost:5000/files/:id/publish`
- **Method**: PUT
- **Authentication**: Bearer Token (via `X-Token` header, e.g., `{{token}}`)
- **Response**: (TBD)

### PUT /Unpublish file
- **Description**: Unpublishes a specified file, restricting its access. Requires a file ID (e.g., `66afb3429956f4386184913d`) in the URL path.
- **URL**: `localhost:5000/files/:id/unpublish`
- **Method**: PUT
- **Authentication**: Bearer Token (via `X-Token` header, e.g., `{{token}}`)
- **Response**: (TBD)

### GET /Get file data
- **Description**: Fetches the raw data or content of a specific file. Requires a file ID (e.g., `66afb3429956f4386184913d`) in the URL path.
- **URL**: `localhost:5000/files/:id/data`
- **Method**: GET
- **Authentication**: Bearer Token (via `X-Token` header, e.g., `{{token}}`)
- **Response**: (TBD)

### POST /New User
- **Description**: Registers a new user in the system. Requires a JSON body with `email` (e.g., `bob@dylan.com`) and `password` (e.g., `toto1234!`).
- **URL**: `https://verbose-space-goldfish-jvx6576q4xq3599v-5000.app.github.dev/users`
- **Method**: POST
- **Authentication**: None
- **Request Body**: 
  ```json
  {
    "email": "bob@dylan.com",
    "password": "toto1234!"
  }
  ```
- **Response**: (TBD)

## Postman Collection
For ease of testing, a Postman collection JSON file is provided. Please place the JSON file here: [Postman Docs](https://github.com/SHEFOO10/alx-files_manager/blob/main/Postman-docs.json).
