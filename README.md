# Docker Learning & Projects 🐳

This repository serves as a centralized hub for my Docker journey. It contains practical implementations, configuration guides for databases (MongoDB/MySQL), and a containerized Node.js test application.

## 📁 Repository Structure

* **`docker-testapp-main/`**: A Node.js & Express application used to practice containerization and database connectivity.
* **`Docker CheatSheet.pdf`**: Quick reference guide for essential Docker commands.
* **`Docker Commands.txt`**: A log of the most frequently used CLI commands during development.

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have the following installed on your local machine:
* [Docker Desktop](https://www.docker.com/products/docker-desktop/) (configured with WSL 2 backend)
* [Node.js](https://nodejs.org/) (v18+ recommended)
* [Git](https://git-scm.com/)

### 2. Database Setup (MongoDB)
To run the MongoDB environment used in these projects, execute:

```bash
# Create the network
docker network create mongo-network

# Run MongoDB
docker run -d \
  -p 27017:27017 \
  --name mongo \
  --network mongo-network \
  -e MONGO_INITDB_ROOT_USERNAME=admin \
  -e MONGO_INITDB_ROOT_PASSWORD=qwerty \
  mongo
