# Continue Integration and Deployment Continue with Jenkins

**In this tutorial, we will use Docker to install Jenkins.**

**Prerequisites:**
Minimum hardware requirements:
> 256 MB of RAM
> 1 GB of drive space(although 10 GB is recommended minimum if running Jenkins as a Docker container).

Recommended hardware configuration for a small team : 
> 4 GB+ of RAM
> 50 GB+ of drive space

Comprehensive hardware recommendations:
> Hardware: see the Hardware Recommendations page

Software requirements:
> Java: see the Java Requirements page
> Web browser: see the Web Browser Compatibility page
> For Windows operating system: Windows Support Policy
> For Linux operating system: Linux Support Policy
> For servlet containers: Servlet Container Support Policy

Downloading and running Jenkins in Docker
There are several Docker images of Jenkins available.

Use the recommended official jenkins/jenkins image from the Docker Hub repository. This image contains the current Long-Term Support (LTS) release of Jenkins, which is production-ready. However, this image doesn’t contain Docker CLI, and is not bundled with the frequently used Blue Ocean plugins and its features. To use the full power of Jenkins and Docker, you may want to go through the installation process described below.

 Note : A new jenkins/jenkins image is published each time a new release of Jenkins Docker is published. You can see a list of previously published versions of the jenkins/jenkins image on the tags page.

 **On Windows**
