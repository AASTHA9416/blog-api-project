Full-Stack Blog API Project

This is a full-stack blogging application built with Node.js and Express. It demonstrates a modern project architecture by separating the application into two distinct parts:

Backend REST API (port 4000): A headless server responsible only for managing data. It handles creating, reading, updating, and deleting blog posts from an in-memory store.

Frontend Server (port 3000): A server responsible for rendering the user interface (UI). It serves EJS templates to the user, and it gets all of its data by making axios (HTTP) requests to the backend API.

This separation of concerns makes the application scalable and easy to maintain.

💻 Tech Stack

Node.js

Express.js: Used for both the backend API and the frontend server.

EJS: Templating engine for rendering the UI on the frontend server.

Axios: Promise-based HTTP client used by the frontend server to communicate with the backend API.

Body-Parser: Middleware to parse incoming request bodies.

🚀 How to Run This Project

To run this project, you must run both servers at the same time in two separate terminal windows.

This guide assumes you have Node.js installed.

1. Clone the Repository

git clone [https://github.com/AASTHA9416/blog-api-project.git](https://github.com/AASTHA9416/blog-api-project.git)
cd blog-api-project


2. Install Dependencies

You need to install the dependencies for both parts of the project.
(Assuming your code is structured with index.js for the frontend and api.js for the backend, based on your files)

# Install dependencies for the frontend server
npm install express ejs body-parser axios

# Install dependencies for the backend API
# (No new ones needed, as they are shared)


3. Run the Backend API (Terminal 1)

In your first terminal, start the backend API server.

# (Assuming your backend code is in 'api.js')
node api.js


You should see: API is running at http://localhost:4000

4. Run the Frontend Server (Terminal 2)

In a new terminal window, start the frontend server.

# (Assuming your frontend code is in 'index.js')
node index.js


You should see: Backend server is running on http://localhost:3000

5. Open the Application

Open your web browser and navigate to the frontend server's address:
http://localhost:3000

Your browser will load the page from port 3000, which will then fetch its data from port 4000 and display the blog posts.

🗺️ API Endpoints (Backend - Port 4000)

GET /posts: Get all blog posts.

GET /posts/:id: Get a specific post by ID.

POST /posts: Create a new post.

PATCH /posts/:id: Update a post with new data.

DELETE /posts/:id: Delete a specific post by ID.