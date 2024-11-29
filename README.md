## **Project Overview**
-This project includes Dockerized configurations for both the **front-end** and **back-end** applications, with MongoDB as the database. 
-It uses **Docker Compose** to facilitate local development and testing by managing multiple services (front-end, back-end, MongoDB).

## **Project Structure**
Here’s a brief description of the key files and directories in the project:

- **`Dockerfile`**: Configuration to build Docker images for the application (front-end and back-end).
- **`docker-compose.yml`**: Defines and runs multi-container Docker applications. It includes front-end, back-end, and MongoDB services.
- **`package.json`**: The Node.js package manager file that defines dependencies and scripts for both front-end and back-end.
  
## **Technologies Used**
- **Docker**: For containerization of the application.
- **Docker Compose**: For running multi-container Docker applications.
- **MongoDB**: NoSQL database for back-end data storage.
## **Installation & Setup**

1. **Build and run the Docker containers**:
    - Make sure you have **Docker** and **Docker Compose** installed.
    - Run the following command to build and start the containers:
      ```bash
      docker-compose up --build
      ```

2. **Access the application**:
    - Once the containers are up and running, you can access the front-end and back-end services locally:
        - Front-end: `http://localhost:3000`
        - Back-end: `http://localhost:3001`

3. **MongoDB Configuration**:
    - The MongoDB service is included in the `docker-compose.yml` and will run on the default MongoDB port (`27017`).
    - The back-end application is configured to connect to the MongoDB service.
