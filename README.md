
# DevOps Assignment Report - Dockerized Web Application

## Deployed the application on AWS EC2 instance. The IP endpoint is http://16.170.255.41/

### 1. Issues Identified

#### Python Dockerfile Issues:
1. **Incorrect working directory path**: `/appp` instead of `/app`.
2. **Invalid path in COPY command**: Incorrectly specifies the source or destination file.
3. **Wrong package name**: `netiface` instead of `netifaces`.
4. **Non-numeric port exposition**: Port specified as "eight thousand" instead of `8000`.
5. **Command typo in CMD instruction**: `pythn` instead of `python`.

#### Nginx Dockerfile Issues:
1. **Invalid base image tag**: Uses `nginx:latests` instead of `nginx:latest`.
2. **Incorrect file path in COPY instruction**: COPY source or destination path is incorrect.
3. **Non-numeric port exposition**: Port specified as "eighty" instead of `80`.
4. **Incorrect daemon configuration syntax**: Configuration syntax for daemon mode is incorrect.

#### Nginx Configuration Issues:
1. **Missing semicolon after `worker_processes auto`**: Causes configuration file syntax errors.
2. **Incorrect directive names**:
   - `worker_process` instead of `worker_processes`.
   - `worker_connection` instead of `worker_connections`.
3. **Typo in MIME types path**: Uses `mime.typess` instead of `mime.types`.
4. **Missing 'e' in `default_type`**: `default_typ` should be `default_type`.

#### Docker Compose Issues:
1. **Invalid port mapping format**: Uses "eighty:80" instead of `80:80`.
2. **Incorrect volume path**: Specifies `nginx.confi` instead of `nginx.conf`.
3. **Non-numeric port exposition**: Port specified as "eight thousand" instead of `8000`.
4. **Typo in network driver**: Uses `bridg` instead of `bridge`.
5. **Unnecessary complex network options**: Simplification of network settings recommended.
6. **Missing build contexts for services**: `build` context not set for services.
7. **Missing dependency configuration**: Dependencies between services not configured.

---

### 2. Resolution Steps

#### 1. Reviewing Dockerfiles
   - **Objective:** Ensure syntax and paths were correct for successful image building.
   - **Process:**
     - Checked each line of the `Dockerfile` for typos and syntax errors.
     - Verified paths in `WORKDIR` and `COPY` statements matched the project directory structure.
     - Fixed typos, such as incorrect paths and misspelled package names.
   

#### 2. Debugging Nginx Configuration
   - **Objective:** Ensure correct Nginx setup.
   - **Process:**
     - Reviewed `Dockerfile` and `nginx.conf` for syntax and path errors.
     - Checked Nginx configurations for correct syntax in directives.
   

#### 3. Docker Compose Configuration
   - **Objective:** Ensure `docker-compose.yml` correctly launched containers with networking and dependencies.
   - **Process:**
     - Validated each service’s port mappings, paths, and network setup.
     - Confirmed build contexts and dependency sequence.
   

#### 4. Verifying Application Accessibility
   - **Objective:** Confirmed application accessibility in a browser.
   - **Process:**
     - Launched containers and checked logs for any remaining issues.
     - Checked application accessibility using public IP address.
     - Verified Nginx and application logs.
   
---


### 3. AWS Deployment Steps for Dockerized Web Application

1. **Launch EC2 Instance**:
   - Chose an Ubuntu AMI and launched the EC2 instance.

2. **Connect to EC2**:
   - Used SSH to connect.
3. **Install Docker and Docker Compose**:
   - Updated packages.
   - Installed Docker.
   - Installed Docker Compose.

4. **Clone Application Repository**:
   - Cloned app repository from GitHub.

5. **Configure Security Group**:
   - Added inbound rules to allow traffic.

6. **Run Docker Compose**:
   - Navigated to app directory.
   - Started the containers using `docker-compose up -d`.

7. **Access the Application**:
   - The application is accessible via http://16.170.255.41/ .

---

This README provides a comprehensive overview of identified issues in the Docker configuration files and concise AWS deployment steps for accessing the Dockerized web application.
