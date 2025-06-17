# alx-files_manager

The `alx-files_manager` is a robust file management system designed to handle various file and user operations through a comprehensive set of API endpoints. This repository provides the necessary endpoints to connect, manage files, and handle user-related tasks efficiently.

## API Endpoints

### GET /connect
- **Description**: Establishes a connection to the file management system. This endpoint is used to initiate a session or verify the server's availability.

### GET /users/me
- **Description**: Retrieves detailed information about the currently authenticated user, including profile data and permissions.

### POST /new file
- **Description**: Creates a new file in the system. Requires file metadata (e.g., name, type) to be provided in the request body.

### POST /new folder
- **Description**: Creates a new folder within the file system. The request should include the folder name and optionally a parent directory.

### GET /list files
- **Description**: Returns a comprehensive list of all files available in the system, including file names, sizes, and creation dates.

### GET /get file
- **Description**: Retrieves the content or metadata of a specific file. The file ID or path must be specified in the request.

### PUT /Publish file
- **Description**: Publishes a specified file, making it accessible to other users or systems. Requires the file ID and publication details.

### PUT /Unpublish file
- **Description**: Unpublishes a specified file, restricting its access. The file ID must be provided in the request.

### GET /Get file data
- **Description**: Fetches the raw data or content of a specific file. Useful for downloading or processing file contents.

### POST /New User
- **Description**: Registers a new user in the system. The request should include user details such as username, email, and password.

## Postman Collection
For ease of testing, a Postman collection JSON file is provided. Please place the JSON file here: [Insert Postman JSON file name here].
