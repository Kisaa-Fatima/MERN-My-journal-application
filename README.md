# ScribbleMe - My Journal Application

ScribbleMe is a journal-based application built using the MERN (MongoDB, Express, React, Node.js) stack. It allows users to register, log in, create, edit, and view journal posts. The application ensures user authentication and secure data handling.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Models](#database-models)
- [Client Components](#client-components)

## Features

- User registration and authentication
- User login and logout
- Create, edit, and delete journal posts
- Upload and manage cover images for posts
- View individual posts
- User profile management
- Secure password handling with bcrypt
- JWT-based authentication
- Cross-origin resource sharing (CORS) support

## Technologies Used

- **Backend:**
  - Node.js
  - Express.js
  - MongoDB
  - Mongoose
  - bcrypt
  - jsonwebtoken
  - multer

- **Frontend:**
  - React.js
  - React Router
  - Context API
  - Rich text editor (React Quill)
  - date-fns

## API Endpoints
**User Routes**
-POST /register: Register a new user
-POST /login: Log in an existing user
-GET /profile: Get the profile of the logged-in user
-POST /logout: Log out the current user
**Post Routes**
-POST /post: Create a new post
-PUT /post: Update an existing post
-GET /post: Retrieve a list of posts (supports pagination and sorting)
-GET /post/:id: Retrieve a single post by its ID
## Database Models
**User Model (api/models/User.js)**
-username: A string representing the username of the user (required, unique, min length 4)
-password: A string representing the password of the user (required)
**Post Model (api/models/Post.js)**
-title: The title of the post (string, required)
-summary: A brief description of the post (string)
-content: The main content of the post (string, required)
-cover: The path or URL to the cover image of the post (string)
-author: A reference to the User model (Schema.Types.ObjectId)
-timestamps: Automatically adds createdAt and updatedAt fields
## Client Components
**App.js**
-Sets up routing and context provider for user authentication
-Defines routes for viewing and editing posts
**Header.js**
-Displays navigation links
-Shows links for creating a new post, logging in, registering, and logging out
-Displays the username of the logged-in user
**Post.js**
-Displays individual posts with title, summary, cover image, author, and creation date
**CreatePost.js**
-Form for creating a new post with title, summary, content, and file upload
**IndexPage.js**
-Fetches and displays a list of posts on the index page
**Login.js**
-Form for logging in a user
**UserContext.js**
-Manages user information and authentication state across the application
