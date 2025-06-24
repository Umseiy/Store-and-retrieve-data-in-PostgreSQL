Express.js PostgreSQL CRUD API

This project is a simple RESTful API built with Express.js and PostgreSQL that allows you to perform CRUD operations (Create, Read, Update, Delete) on a users table. It includes basic error handling and is easily testable using Postman.


---

🚀 Getting Started

Prerequisites

Node.js

PostgreSQL

Postman (for API testing)



---

🛠 Installation

1. Clone the repository:



git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2. Install dependencies:



npm install

3. Setup PostgreSQL:



Create a database:


CREATE DATABASE testdb;

Create users table:


CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

4. Configure PostgreSQL connection in index.js:



const pool = new Pool({
    user: 'your_db_user',
    host: 'localhost',
    database: 'testdb',
    password: 'your_db_password',
    port: 5432,
});


---

💻 Running the Server

Start the server:

node index.js

The server will run on:

http://localhost:3000


---

📬 API Endpoints

Method	Endpoint	Description

GET	/users	Get all users
GET	/users/:id	Get user by ID
POST	/users	Create new user
PUT	/users/:id	Update user by ID
DELETE	/users/:id	Delete user by ID



---

🧪 Testing with Postman

Create User (POST)

POST http://localhost:3000/users

{
  "name": "Hauwa Salihu Ahmad",
  "email": "hauwasalihuahmad@gmail.com"
}

Get All Users (GET)

GET http://localhost:3000/users

Get User by ID (GET)

GET http://localhost:3000/users/1

Update User (PUT)

PUT http://localhost:3000/users/1

{
  "name": "Jane Doe",
  "email": "jane@example.com"
}

Delete User (DELETE)

DELETE http://localhost:3000/users/1


---

⚙️ Project Structure

project-folder/
│
├── node_modules/
├── index.js
├── package.json
└── README.md


---
