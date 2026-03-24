# Node-Learning
Node Tutorial
🚀 Node.js Learning Guide

A beginner-friendly guide to learn Node.js, npm, and nvm step by step.

📌 Table of Contents
Introduction
Installation
Project Setup
npm Basics
Core Concepts
Building a Server
Express.js
Database Basics
Environment Variables
Deployment
Resources
📖 Introduction

Node.js allows you to run JavaScript outside the browser and build backend applications.

⚙️ Installation
Install Node.js
Download and install from official website
Or use nvm (recommended)
Install nvm
# Install Node using nvm
nvm install 18
nvm use 18
Verify Installation
node -v
npm -v
📁 Project Setup
# Create a new project
mkdir my-node-app
cd my-node-app

# Initialize project
npm init -y
📦 npm Basics
Install a package
npm install express
Install as dev dependency
npm install nodemon --save-dev
Run scripts
npm run start
🧠 Core Concepts
Modules
// export
module.exports = function() {};

// import
const myFunc = require('./file');
File System
const fs = require('fs');
fs.writeFileSync('file.txt', 'Hello World');
🌐 Build a Simple Server
const http = require('http');

const server = http.createServer((req, res) => {
  res.end('Hello World');
});

server.listen(3000, () => {
  console.log('Server running on port 3000');
});

Run:

node index.js
⚡ Express.js

Using Express.js for easier server setup:

npm install express
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello from Express');
});

app.listen(3000, () => console.log('Server running'));
🔄 Async Programming
Promise
Promise.resolve('Hello').then(console.log);
Async/Await
async function run() {
  return 'Hello';
}
run().then(console.log);
🛠️ Useful Tools
Nodemon (auto-restart)
npx nodemon index.js
Dotenv
npm install dotenv
require('dotenv').config();
console.log(process.env.PORT);
🔐 Environment Variables

Create .env file:

PORT=3000
📡 Database Basics (Example: MongoDB)
npm install mongoose
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost:27017/test');
🚢 Deployment
Set environment to production:
NODE_ENV=production
Deploy using platforms like Render / Vercel / Railway
📂 Suggested Project Structure
project/
│── src/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│── .env
│── package.json
│── index.js
📚 Resources
Node.js Docs
npm Docs
Express Docs
✅ Next Steps
Build a REST API
Add authentication
Connect frontend
