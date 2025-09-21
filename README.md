# Practical-4-NODE-JS
Todo REST API - Express.js Practical

Author: Ritu Singh
Student ID: GF202346594
Course: BCA - Final Year

Project Description

Simple Todo REST API built with Express.js and Node.js.
Create and view todo items using HTTP requests.

Requirements

- Node.js installed
- Express and body-parser packages

Setup

1. Install dependencies:
   npm install express body-parser

2. Start the server:
   node app.js

3. Server runs on: http://localhost:3000

API Endpoints

1. Create Todo (POST):
   URL: http://localhost:3000/todos
   Headers: Content-Type: application/json
   Body: {"title": "Buy Maggie"}

2. Get All Todos (GET):
   URL: http://localhost:3000/todos

How to Test

Method 1 - Using requests.http file:
- Install REST Client extension in VS Code
- Open requests.http file
- Click "Send Request"

Method 2 - Using browser:
- Start server: node app.js  
- Visit: http://localhost:3000/todos (shows all todos)

Method 3 - Using curl:
Create todo: curl -X POST http://localhost:3000/todos -H "Content-Type: application/json" -d '{"title":"Buy Maggie"}'
Get todos: curl http://localhost:3000/todos

Expected Results

- POST request creates new todo with unique ID and returns it
- GET request returns array of all created todos
- Missing title returns 400 error: {"error": "Title is required"}

Features

- JSON request/response handling
- Input validation
- Unique ID generation using timestamps
- In-memory storage
- Error handling

Files

- app.js: Main Express server code
- requests.http: Test HTTP requests

Key Concepts

- Express.js framework
- REST API design
- HTTP methods (POST, GET)
- JSON middleware
- Route handling
- Error responses
