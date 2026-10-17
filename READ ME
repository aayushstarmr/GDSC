Python

Flask

MongoDB

PyMongo

JSON Web Token (JWT)

PyJWT

BSON ObjectId

REST API

JSON

🏗️ System Architecture

Client: Sends login credentials and API requests.

Flask Application: Handles HTTP requests and routes.

JWT Authentication Middleware: Validates tokens before protected operations.

Role-Based Authorization: Checks the user's role and task assignment.

MongoDB Database: Stores users and tasks.

JSON Response: Returns task data, success messages, or errors.

👥 User Roles and Permissions

Role

Retrieve Tasks

Update Tasks

Admin

All tasks

Any task

Manager

Assigned tasks

Assigned tasks

Regular User

Assigned tasks

Assigned tasks

Permissions reflect the authorization logic implemented in the provided code.

📂 Project Structure

Task-Management-System/
│
├── app.py              # Flask application and API routes
├── requirements.txt    # Python dependencies
├── README.md           # Project documentation
└── .gitignore          # Files excluded from Git

⚙️ Installation and Setup

1. Clone the Repository

git clone YOUR_GITHUB_REPOSITORY_URL
cd Task-Management-System

2. Create a Virtual Environment

python -m venv venv

Activate the environment.

Windows

venv\Scripts\activate

macOS / Linux

source venv/bin/activate

3. Install Dependencies

Create a requirements.txt file containing:

Flask
PyJWT
pymongo

Install the dependencies:

pip install -r requirements.txt

4. Start MongoDB

Ensure MongoDB is installed and running locally at:

mongodb://localhost:27017/

The application uses a database named task_management with two collections:

users — stores user credentials and roles.

tasks — stores task details and assignment information.

5. Configure the Application

Before running the application, configure a secure secret key using an environment variable rather than a hardcoded value.

Also, ensure that user records contain username, password, and role, and task records contain title, description, status, and assigned_to.

6. Run the Application

python app.py

The Flask development server starts at:

http://127.0.0.1:5000/

🔗 API Endpoints

1. User Login

Endpoint: POST /login

Authenticates a user and returns a JWT token after successful verification.

Authentication: HTTP Basic Authentication.

Example response:

{
  "token": "your_generated_jwt_token"
}

2. Retrieve Tasks

Endpoint: GET /tasks

Retrieves tasks according to the authenticated user's role and task assignments.

Authentication: JWT required.

Header:

Authorization: YOUR_JWT_TOKEN

Example response:

{
  "tasks": [
    {
      "id": "YOUR_TASK_ID",
      "title": "Complete project",
      "description": "Finish the assigned development work",
      "status": "Pending"
    }
  ]
}

3. Update a Task

Endpoint: PUT /tasks/<task_id>

Updates an existing task if the authenticated user has permission.

Authentication: JWT required.

Example request body:

{
  "status": "Completed"
}

Example response:

{
  "message": "Task updated successfully"
}

🔐 Security Implementation

JWT tokens protect task-related endpoints.

Authentication middleware validates incoming tokens.

Role-based checks restrict task updates.

MongoDB stores task and user records.

Unauthorized requests receive HTTP 401 or 403 responses.

Security improvements recommended before production:

Replace the hardcoded secret key with a strong environment-based secret.

Hash passwords using a secure password-hashing algorithm such as Argon2 or bcrypt.

Add token expiration and validate the expected token claims.

Validate task IDs and request fields.

Restrict which fields can be updated instead of accepting arbitrary JSON fields.

Disable Flask debug mode in production.

Use HTTPS when deployed.

🧪 Testing

Test the API using Postman or curl.

Verify that:

Valid login credentials return a token.

Invalid credentials are rejected.

Requests without a token return HTTP 401.

Users can retrieve only permitted tasks.

Authorized users can update permitted tasks.

Unauthorized updates return HTTP 403.

🔮 Future Enhancements

Create and delete task endpoints.

User registration and password reset.

Task deadlines and priority levels.

Task search, filtering, and pagination.

Refresh tokens and token expiration.

Automated testing using pytest.

Frontend integration using React.

API documentation using Swagger/OpenAPI.

🤝 Contributing

Contributions and suggestions are welcome. Fork the repository, make your changes, and submit a pull request.

📄 License

This project is intended for educational purposes. Add an appropriate open-source license if you want to permit reuse and modification under defined terms.

