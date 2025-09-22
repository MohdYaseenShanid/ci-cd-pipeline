# CI/CD Pipeline Demo with Node.js and Docker

This project is a demonstration of a complete CI/CD automation process as part of an internship task. The goal was to set up a pipeline that automatically builds a Docker image for a Node.js web application and pushes it to Docker Hub whenever new code is committed to the `main` branch.

---

## Tech Stack

* **Application:** Node.js, Express.js
* **Containerization:** Docker
* **CI/CD:** GitHub Actions
* **Image Registry:** Docker Hub

---

## CI/CD Pipeline Workflow

The automation is defined in the `.github/workflows/main.yml` file and performs the following steps:

1.  **Trigger:** The workflow is automatically triggered on any `push` to the `main` branch of this repository.
2.  **Checkout Code:** The runner checks out the latest version of the repository's code.
3.  **Login to Docker Hub:** It securely logs into Docker Hub using encrypted secrets stored in the repository settings.
4.  **Build and Push Image:** It uses the `Dockerfile` to build a new Docker image of the application.
5.  **Push to Registry:** If the build is successful, the newly created image is tagged and pushed to Docker Hub, ready for deployment.

This setup ensures that a fresh, runnable image of the application is always available in the Docker Hub registry.
