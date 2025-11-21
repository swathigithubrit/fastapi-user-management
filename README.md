FastAPI User Management API (FastAPI + SQLModel)

This project is a simple User Management REST API built using:

- FastAPI (for API development)
- SQLModel (for ORM + database modeling)
- SQLite (lightweight local DB)

The API supports CRUD operations:
- Create a user  
- Retrieve all users  
- Retrieve a single user  
- Update user details  
- Delete a user  

Tech Stack
- Python 3.10+
- FastAPI
- SQLModel
- SQLite
- Uvicorn

Install dependencies
pip install fastapi sqlmodel uvicorn

Running the Application
Start the FastAPI server:
uvicorn main:app --reload


Your API will be available at:

http://127.0.0.1:8000

Open interactive API Docs:

http://127.0.0.1:8000/docs

API Endpoints

➤ Create User  
`POST /createuser`
{
"name": "John",
"phone": 9876543210,
"email": "john@example.com
"
}

➤ Get All Users  
`GET /users`

➤ Get Single User  
`GET /users/{user_id}`

➤ Update User  
`PUT /users/{user_id}`

➤ Delete User  
`DELETE /users/{user_id}`

Database
- Uses SQLite file `.users.db` 
- Tables created automatically using:

```python
SQLModel.metadata.create_all(engine)

Features

Clean architecture
SQLModel models (User, CreateUser)
FastAPI dependency injection
Async lifespan event
Automatic database table creation
Swagger UI
Error Handling with HTTPException


