# Node.js Docker App

A simple Node.js application with Docker support.  
This project demonstrates how to containerize a Node.js app using a **multi-stage Dockerfile** and run it on any environment.

---

## Features

- Node.js + Express server
- EJS template engine
- Static file serving from `public` folder
- Multi-stage Dockerfile for small, efficient images
- Configurable `PORT` environment variable

---

## Prerequisites

- [Node.js](https://nodejs.org/) (optional if using Docker)
- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/) to clone the repo

---

## Getting Started

### Clone the repository

```bash
git clone https://github.com/swatiV-27/node-docker-app.git
cd node-docker-app

### Run with Docker
1. Build the Docker image
docker build -t my-node-app .

2. Run the container
docker run -p 3000:3000 -e PORT=3000 my-node-app
* Environment Variables

PORT — The port number your app will listen on (default: 5006 in code, overridden by Docker or server environment)

Project Structure
node-docker-app/
│
├─ Dockerfile          # Multi-stage Dockerfile
├─ index.js            # Main Node.js server file
├─ package.json        # Node.js dependencies & scripts
├─ public/             # Static files (CSS, JS, images)
├─ views/              # EJS templates
└─ README.md           # Project documentation
