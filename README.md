# Continue Integration and Deployment Continue with Jenkins

**In this tutorial, we will use Docker to install Jenkins.** <br>

**Prerequisites:** <br>
Minimum hardware requirements: <br>
> 256 MB of RAM <br>
> 1 GB of drive space(although 10 GB is recommended minimum if running Jenkins as a Docker container).<br>

Recommended hardware configuration for a small team : <br>
> 4 GB+ of RAM <br>
> 50 GB+ of drive space <br>

Comprehensive hardware recommendations: <br>
> Hardware: see the Hardware Recommendations page <br>

Software requirements: <br>
> Java: see the Java Requirements page <br>
> Web browser: see the Web Browser Compatibility page <br>
> For Windows operating system: Windows Support Policy <br>
> For Linux operating system: Linux Support Policy <br>
> For servlet containers: Servlet Container Support Policy <br>

Downloading and running Jenkins in Docker <br>
There are several Docker images of Jenkins available. <br>

Use the recommended official jenkins/jenkins image from the Docker Hub repository. This image contains the current Long-Term Support (LTS) release of Jenkins, which is production-ready. However, this image doesn’t contain Docker CLI, and is not bundled with the frequently used Blue Ocean plugins and its features. To use the full power of Jenkins and Docker, you may want to go through the installation process described below. <br>

 Note : A new jenkins/jenkins image is published each time a new release of Jenkins Docker is published. You can see a list of previously published versions of the jenkins/jenkins image on the tags page. <br>

 **On Windows** <br>
 The Jenkins project provides a Linux container image, not a Windows container image. Be sure that your Docker for Windows installation is configured to run Linux Containers rather than Windows Containers. Refer to the Docker documentation for instructions to switch to Linux containers. Once configured to run Linux Containers, the steps are:
> 1. Open up a command prompt window and similar to the macOS and Linux instructions above do the following: <br>
> 2. Create a bridge network in Docker <br>

![Capture d’écran 2024-08-31 235031](https://github.com/user-attachments/assets/d65ed562-aa17-4cd3-8fef-8c6f5933ad35)

3. Run a **jenkins/jenkins** Docker image <br>

![Capture d’écran 2024-09-01 001215](https://github.com/user-attachments/assets/4da60e3e-7177-437c-98e8-09aea3782c91)

**Post-installation setup wizard** <br>
After downloading, installing and running Jenkins using one of the procedures above (except for installation with Jenkins Operator), the post-installation setup wizard begins. <br>

This setup wizard takes you through a few quick "one-off" steps to unlock Jenkins, customize it with plugins and create the first administrator user through which you can continue accessing Jenkins. <br>

**Unlocking Jenkins** <br>
When you first access a new Jenkins controller, you are asked to unlock it using an automatically-generated password.

![Capture d’écran 2024-09-01 002228](https://github.com/user-attachments/assets/4c4df1ab-3ce3-4c01-b16d-1d7805346f97)
![Capture d’écran 2024-09-01 002326](https://github.com/user-attachments/assets/8ee2ec3b-7ad4-455b-b0a4-9ffc9fb373da)



