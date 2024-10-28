# Assignment Guidelines

 1. Required Setup
        - System: Use any laptop, PC, or cloud server.
        - Tools: Ensure both Docker and Docker Compose are installed and configured.

 2. Initial Setup
        - Docker Images:
        - Build each image locally based on the provided Dockerfiles included in the GitHub repository, and tag them for later use in Docker Compose.

 3. Running the Docker Compose File
        - Compose File: Use the provided `docker-compose.yml` file.
        - Starting Containers:
        - Launch all containers specified in the Docker Compose file.
        - Verify they are accessible on localhost.

 4. Verifying and Testing
        - Website Access:
        - Open a web browser and check if the website is running correctly on port 80.

 5. Submitting the Assignment
        - GitHub Repository:
                - Upload all related files and details to a GitHub repository. Name the repository following this convention: `devops-qoala-assignment-<name>-<rollnumber>`. Grant repository access to `devops@qoala.id`. Note: Submissions without access will not be considered.      
        - Screenshot:
                - Add a screenshot showing the web app running in the browser along with Nginx access logs confirming the request.
        - Report:
                - Prepare a concise, one-page report that includes:
                - Issues Identified: Summary of any issues encountered during image building and container setup.
                - Resolution Steps: Detailed actions taken to resolve each issue and complete the assignment.

Notes: 

Bonus points will be awarded if the assignment includes deployment on a server hosted with any cloud provider (AWS, GCP, or Azure) and provides accessible endpoints (such as IP address or DNS record). This allows for task verification through the shared endpoints.

Additionally, please be aware that there are intentional bugs in the files that need to be identified and resolved for the project to run successfully.
