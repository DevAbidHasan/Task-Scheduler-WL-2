# 🧩 Task Scheduler

A simple and beginner-friendly **Node.js + Express.js REST API** for managing tasks.  
This project demonstrates key backend development concepts like **routing**, **modularization**, **error handling**, and **API testing with Postman**.

---

## 🚀 Features

✅ **GET /** — Root endpoint to verify server is running  
✅ **GET /health** — Returns API health status and uptime  
✅ **GET /tasks** — Fetch all available tasks  
✅ **GET /tasks/:id** — Fetch a specific task by ID  
✅ **Error Handling** — Includes 400 (invalid ID) and 404 (not found) responses  
✅ **Modular Routing** — Uses Express Router (`src/routes/tasks.js`) for cleaner structure  
✅ **Postman Testing** — Tested endpoints and documented responses in `api-responses.txt`  

---

## 🏗️ Project Structure
```
project-folder/
│
├── src/
│ ├── index.js # Main server entry point
│ └── routes/
│ └── tasks.js # Task routes (GET /tasks, GET /tasks/:id)
│
├── tasks-response.json # Postman response file for /tasks
├── api-responses.txt # Documentation of all API responses
└── README.md # Project documentation
```

---

## ⚙️ Installation & Setup

### 1️⃣ Prerequisites
- [Node.js](https://nodejs.org/) (v18+ recommended)
- [npm](https://www.npmjs.com/)
- [Postman](https://www.postman.com/) for API testing

### 2️⃣ Clone the Repository
```
git clone https://github.com/DevAbidHasan/Task-Scheduler-WL-2
```
```
cd demo-server
```
3️⃣ Install Dependencies
```
npm install express
```
```
npm install -g nodemon
```
4️⃣ Run the Server
```
nodemon src/index.js
```
Server should start at:
```
http://localhost:3000
```
🌐 API Endpoints
---
🔹 Root Endpoint
```
GET /
```
Returns a welcome message confirming the API is active.
---
Response: 


"Task Management API is running!"
---
🔹 Health Check
```
GET /health
```
Returns current API status and uptime.
---
Response:

{
  "status": "healthy",
  "uptime": 23.4567
}
---
🔹 Get All Tasks
```
GET /tasks
```
Fetches all available tasks.
Each task includes:

id

title

completed

priority (low, medium, high)

createdAt
---
Response Example:

```
[
  {
    "id": 1,
    "title": "Learn Node.js",
    "completed": false,
    "priority": "high",
    "createdAt": "2025-11-04T16:23:45.345Z"
  },
  ...
]
```
---
🔹 Get Task by ID
```
GET /tasks/:id
```
Fetch a single task by its ID.

Case	Example	Status	Response
✅ Valid ID	/tasks/3	200	Task object
❌ Not Found	/tasks/999	404	{ "error": "Task not found" }
❌ Invalid Format	/tasks/abc	400	{ "error": "Invalid ID format" }

🧪 Postman Testing
Import your API endpoints into Postman.

Test each endpoint (GET /, /health, /tasks, /tasks/:id).

Save successful responses:

/tasks → tasks-response.json

/tasks/:id tests → document in api-responses.txt

Verify error handling for invalid or missing tasks.

🧰 Technologies Used
Tech	Description
Node.js	JavaScript runtime for backend
Express.js	Lightweight web framework for APIs
Nodemon	Development server auto-reloader
Postman	API testing tool



