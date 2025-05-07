{
  "name": "Greenbone Community Edition Setup",
  "description": "This script automates the setup of Greenbone Community Edition using Docker on Ubuntu systems. It installs dependencies, configures Docker, downloads the official docker-compose file from Greenbone, and sets a predefined admin password.",
  "version": "1.0",
  "license": "MIT",
  "author": "shubham wagh or shubhamwaghagkmf010",
  "actions": [
    {
      "step": "Install Dependencies",
      "description": "Installs essential packages like curl, gnupg, and ca-certificates required for Docker and HTTPS requests."
    },
    {
      "step": "Remove Conflicting Packages",
      "description": "Removes any previously installed Docker-related packages that might interfere with a clean installation."
    },
    {
      "step": "Add Docker Repository",
      "description": "Adds the official Docker APT repository with appropriate GPG keys and architecture settings."
    },
    {
      "step": "Install Docker",
      "description": "Installs Docker Engine, CLI, container runtime, and Docker Compose plugin."
    },
    {
      "step": "Add User to Docker Group",
      "description": "Adds the current user to the Docker group to allow Docker usage without root privileges."
    },
    {
      "step": "Create Download Directory",
      "description": "Creates a directory to store Greenbone's docker-compose.yml file."
    },
    {
      "step": "Download Compose File",
      "description": "Downloads the latest Greenbone docker-compose.yml directly from the Greenbone documentation site."
    },
    {
      "step": "Pull Docker Images",
      "description": "Fetches all required Greenbone container images from Docker Hub."
    },
    {
      "step": "Start Containers",
      "description": "Starts all containers defined in the Greenbone docker-compose file in detached mode."
    },
    {
      "step": "Wait for Initialization",
      "description": "Waits for 60 seconds to ensure all services inside containers are initialized before setting credentials."
    },
    {
      "step": "Set Default Password",
      "description": "Updates the default 'admin' user's password to a predefined value ('admin123') using Greenbone's gvmd command inside the container."
    },
    {
      "step": "Open Web Interface",
      "description": "Opens the Greenbone web interface in the default system browser on port 9392."
    }
  ],
  "usage": "Run the script with root privileges or as a user with sudo access. After execution, log in to http://127.0.0.1:9392 with username 'admin' and password 'admin123'.",
  "note": "This script is written to be simple and educational. It does not modify system security settings and uses only publicly available installation commands from Greenbone and Docker's official documentation."
}
