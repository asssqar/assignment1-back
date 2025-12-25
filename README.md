📘 Assignment #1
Building a Simple Express API with JSON Storage
📌 Project Overview

The purpose of this project is to build a basic backend application using Node.js and Express.js.
The project demonstrates how a server works, how HTTP requests are handled, and how data can be stored and managed without using a database.

Instead of a database, a JSON file is used as persistent storage. This approach helps to understand the core logic behind CRUD operations before working with more complex database systems.

The backend exposes several test routes for server verification and a full CRUD API for managing custom objects.

🎯 Project Goals

The main goals of this assignment are:

To understand how an Express server is created and configured

To learn how HTTP routes work (GET, POST, PUT, DELETE)

To practice handling JSON request bodies

To implement file-based data persistence

To test API endpoints using Postman

🛠 Technologies and Tools

The following technologies and tools were used in this project:

Node.js — JavaScript runtime environment

Express.js — minimal web framework for Node.js

JSON — used as a simple data storage format

Postman — for testing API endpoints

📁 Project Structure Explanation

The project consists of a small number of files, each with a clear responsibility:

server.js
The main application file. It contains server configuration, route definitions, and CRUD logic.

data.json
A JSON file used to store application data. All changes made through the API are saved to this file.

package.json
Contains project metadata, dependencies, and scripts.

README.md
Project documentation explaining how the application works and how to use it.

This simple structure helps to clearly understand how backend components interact with each other.

⚙️ Server Setup

The Express server is initialized and configured to listen on port 3000.
The middleware express.json() is used to automatically parse incoming JSON request bodies, which is required for POST and PUT requests.

Once the server is started, it waits for incoming HTTP requests and processes them based on defined routes.

🔍 Demo Routes Description

Several demo routes were implemented to verify that the server is working correctly:

GET /
This route is used to check if the server is running.
It returns a simple text response.

GET /hello
Returns a JSON greeting message.
This route demonstrates how to send JSON responses from the server.

GET /time
Returns the current server time.
It shows how the server can generate dynamic responses.

GET /status
Returns an HTTP 200 status code and a JSON message.
This route is useful for server health checks.

These routes are mainly used for testing and demonstration purposes.

📦 CRUD API Concept

For the CRUD functionality, the Task object was chosen.

Each task contains:

a unique identifier (id)

a name (name)

The CRUD API allows the client to:

retrieve all tasks

create a new task

update an existing task

delete a task

This design follows REST API principles and uses meaningful HTTP methods.

📥 Reading Data (GET)

The GET request reads all tasks from the JSON file and returns them as a JSON response.
This operation does not modify the data and is used only to retrieve information.

➕ Creating Data (POST)

The POST request is used to create a new task.
The client sends task data in JSON format.
A unique identifier is automatically generated for each new task.

After creation, the updated task list is saved back into the JSON file, ensuring data persistence.

✏️ Updating Data (PUT)

The PUT request allows updating an existing task using its identifier.
If the task does not exist, the server returns an error response.

This operation demonstrates how to safely modify stored data and handle error cases.

❌ Deleting Data (DELETE)

The DELETE request removes a task from the JSON file based on its identifier.
After deletion, the file is updated and a success response is returned.

💾 JSON File Persistence

Instead of using a database, this project uses a JSON file for data storage.
Before every operation, the server reads the current data from the file.
After any modification (POST, PUT, DELETE), the file is rewritten with updated content.

This approach ensures that data is preserved even after restarting the server.

🧪 API Testing

All API endpoints were tested using Postman.
Testing includes:

demo routes

creating tasks

updating tasks

deleting tasks

Successful testing confirms correct API behavior and error handling.

✅ Conclusion

This project provides a clear introduction to backend development using Express.
It demonstrates how servers handle requests, manage data, and return responses.

The knowledge gained from this assignment forms a strong foundation for future backend projects involving databases, authentication, and more advanced architectures.
