# Blog Post API and Client

## Overview

This project consists of two parts:
1. **API Server**: A backend server built with Express.js that provides RESTful API endpoints for managing blog posts.
2. **Client Server**: A frontend server built with Express.js that interacts with the API server to render and manage blog posts through a web interface.

## API Server

### Description

The API server exposes endpoints for CRUD (Create, Read, Update, Delete) operations on blog posts. It uses an in-memory data store for simplicity.

### Endpoints

- **GET /posts**: Retrieve all blog posts.
- **GET /posts/:id**: Retrieve a specific blog post by ID.
- **POST /posts**: Create a new blog post.
- **PATCH /posts/:id**: Update a specific blog post by ID (partially).
- **DELETE /posts/:id**: Delete a specific blog post by ID.

### Usage

1. **Start the API Server**

   ```bash
   cd path/to/api-server
   npm install
   npm start
   ```

   The server will be running at `http://localhost:4000`.

2. **Endpoints Examples**

   - **GET All Posts**: `http://localhost:4000/posts`
   - **GET Post by ID**: `http://localhost:4000/posts/1`
   - **POST New Post**: `http://localhost:4000/posts` (requires body in JSON format)
   - **PATCH Update Post**: `http://localhost:4000/posts/1` (requires body with fields to update)
   - **DELETE Post**: `http://localhost:4000/posts/1`

## Client Server

### Description

The client server provides a web interface for interacting with the API server. It uses EJS templates to render pages and Axios for making HTTP requests to the API server.

### Routes

- **GET /**: Render the main page with a list of blog posts.
- **GET /new**: Render the form for creating a new blog post.
- **GET /edit/:id**: Render the form for editing an existing blog post.
- **POST /api/posts**: Create a new blog post (submits form data to the API).
- **POST /api/posts/:id**: Update an existing blog post (submits form data to the API).
- **GET /api/posts/delete/:id**: Delete a blog post by ID.

### Usage

1. **Start the Client Server**

   ```bash
   cd path/to/client-server
   npm install
   npm start
   ```

   The server will be running at `http://localhost:3000`.

2. **Pages and Forms**

   - **Main Page**: Displays a list of blog posts and links to create or edit posts.
   - **Create New Post**: Accessible at `http://localhost:3000/new`.
   - **Edit Post**: Accessible at `http://localhost:3000/edit/:id`.

### Dependencies

- `express`: Web framework for Node.js.
- `body-parser`: Middleware to parse request bodies.
- `axios`: HTTP client for making requests.
- `ejs`: Templating engine for rendering views.

### Project Structure

```
project-root/
├── api-server/
│   ├── index.js
│   └── package.json
└── client-server/
    ├── index.js
    ├── public/
    ├── views/
    │   ├── index.ejs
    │   └── modify.ejs
    └── package.json
```

### Installation

1. **Clone the Repository**

   ```bash
   git clone <repository-url>
   cd project-root
   ```

2. **Install Dependencies**

   For both servers:

   ```bash
   cd api-server
   npm install
   cd ../client-server
   npm install
   ```

3. **Run the Servers**

   - Start the API server:

     ```bash
     cd api-server
     npm start
     ```

   - Start the client server:

     ```bash
     cd client-server
     npm start
     ```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
