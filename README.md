# Running the Backend Project with Docker

## Prerequisites

Ensure you have the following installed on your system:
- [Docker](https://www.docker.com/get-started)

## Steps to Run the Application

1. **Navigate to the Project Directory**
   ```sh
   cd path/to/your/project
   ```

2. **Build the Docker Image**
   ```sh
   docker build -t my-backend-app .
   ```
   - The `-t my-backend-app` flag names the image as `my-backend-app`.

3. **Run the Docker Container**
   ```sh
   docker run -p 4000:4000 my-backend-app
   ```
   - The `-p 4000:4000` flag maps port 4000 of the container to port 4000 of your local machine.
  
4. **Run the Docker Container While listening the local changes**
   ```sh
   docker-compose up -d
   ```

5. **Access the Backend API**
   Open your browser or use a tool like Postman to access:
   ```md
   http://localhost:4000
   ```

## Additional Docker Commands

- **Check Running Containers**
  ```sh
  docker ps
  ```

- **Stop the Running Container**
  ```sh
  docker stop <container_id>
  ```

- **Remove All Stopped Containers**
  ```sh
  docker system prune -f
  ```

- **Check Docker Images**
  ```sh
  docker images
  ```

- **Remove a Docker Image**
  ```sh
  docker rmi <image_id>
  ```

- **Rebuild the Docker Image (after changes)**
  ```sh
  docker build --no-cache -t my-backend-app .
  ```

- **Run the Container in Detached Mode**
  ```sh
  docker run -d -p 4000:4000 my-backend-app
  ```

- **Check Docker Logs**
  ```sh
  docker logs <container_id>
  ```

## Notes
- Ensure port `4000` is not in use by other applications.
- Modify the `Dockerfile` or use `.env` if you need custom environment variables.

Happy coding! 🚀

