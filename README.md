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
 The Jenkins project provides a Linux container image, not a Windows container image. Be sure that your Docker for Windows installation is configured to run Linux Containers rather than Windows Containers. Refer to the Docker documentation for instructions to switch to Linux containers. Once configured to run Linux Containers, the steps are:
> 1. Open up a command prompt window and similar to the macOS and Linux instructions above do the following: <br>
> 2. Create a bridge network in Docker <br>

![Capture d’écran 2024-08-31 235031](https://github.com/user-attachments/assets/d65ed562-aa17-4cd3-8fef-8c6f5933ad35)

3. Run a **jenkins/jenkins** Docker image

![Capture d’écran 2024-09-01 001215](https://github.com/user-attachments/assets/4da60e3e-7177-437c-98e8-09aea3782c91)

**Post-installation setup wizard**
After downloading, installing and running Jenkins using one of the procedures above (except for installation with Jenkins Operator), the post-installation setup wizard begins.
