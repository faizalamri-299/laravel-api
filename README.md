```markdown
# User CRUD API with Laravel

This is a simple CRUD API for managing users in a Laravel application.

## Prerequisites

- PHP >= 8.0
- Composer
- Laravel >= 8.x
- MySQL (or any other supported database)

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/faizalamri-299/laravel-api.git
   cd laravel-api
   ```

2. **Install dependencies:**
   ```sh
   composer install
   ```

3. **Copy the example environment file and modify it:**
   ```sh
   cp .env.example .env
   ```
   Update your `.env` file with your database credentials and other settings.

4. **Generate an application key:**
   ```sh
   php artisan key:generate
   ```

5. **Run the migrations:**
   ```sh
   php artisan migrate
   ```

6. **Start the development server:**
   ```sh
   php artisan serve
   ```
   The API will be available at `http://127.0.0.1:8000`.

## API Endpoints

### List All Users

- **URL:** `/api/users`
- **Method:** `GET`
- **Response:**
  ```json
  [
    {
      "id": 1,
      "user_no": "001",
      "name": "John Doe",
      "department_id": 1,
      "email": "john.doe@example.com",
      "email_verified_at": null,
      "created_at": "2023-01-01T00:00:00.000000Z",
      "updated_at": "2023-01-01T00:00:00.000000Z"
    },
    ...
  ]
  ```

### Get Single User

- **URL:** `/api/users/{id}`
- **Method:** `GET`
- **Response:**
  ```json
  {
    "id": 1,
    "user_no": "001",
    "name": "John Doe",
    "department_id": 1,
    "email": "john.doe@example.com",
    "email_verified_at": null,
    "created_at": "2023-01-01T00:00:00.000000Z",
    "updated_at": "2023-01-01T00:00:00.000000Z"
  }
  ```

### Create a User

- **URL:** `/api/users`
- **Method:** `POST`
- **Request Body:**
  ```json
  {
    "user_no": "002",
    "name": "Jane Doe",
    "department_id": 1,
    "email": "jane.doe@example.com",
    "password": "password123"
  }
  ```
- **Response:**
  ```json
  {
    "id": 2,
    "user_no": "002",
    "name": "Jane Doe",
    "department_id": 1,
    "email": "jane.doe@example.com",
    "email_verified_at": null,
    "created_at": "2023-01-01T00:00:00.000000Z",
    "updated_at": "2023-01-01T00:00:00.000000Z"
  }
  ```

### Update a User

- **URL:** `/api/users/{id}`
- **Method:** `PUT`
- **Request Body:**
  ```json
  {
    "name": "Jane Doe Updated",
    "department_id": 1,
    "email": "jane.doe.updated@example.com",
    "password": "newpassword123"
  }
  ```
- **Response:**
  ```json
  {
    "id": 2,
    "user_no": "002",
    "name": "Jane Doe Updated",
    "department_id": 1,
    "email": "jane.doe.updated@example.com",
    "email_verified_at": null,
    "created_at": "2023-01-01T00:00:00.000000Z",
    "updated_at": "2023-01-01T00:00:00.000000Z"
  }
  ```

### Delete a User

- **URL:** `/api/users/{id}`
- **Method:** `DELETE`
- **Response:**
  ```json
  {
    "message": "User deleted successfully"
  }
  ```


## License

This project is licensed under the MIT License.
```
