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

> 3. Run a **jenkins/jenkins** Docker image <br>

![Capture d’écran 2024-09-01 001215](https://github.com/user-attachments/assets/4da60e3e-7177-437c-98e8-09aea3782c91)

**Post-installation setup wizard** <br>
After downloading, installing and running Jenkins using one of the procedures above (except for installation with Jenkins Operator), the post-installation setup wizard begins. <br>

This setup wizard takes you through a few quick "one-off" steps to unlock Jenkins, customize it with plugins and create the first administrator user through which you can continue accessing Jenkins. <br>

**Unlocking Jenkins** <br>
When you first access a new Jenkins controller, you are asked to unlock it using an automatically-generated password.

![Capture d’écran 2024-09-01 002228](https://github.com/user-attachments/assets/4c4df1ab-3ce3-4c01-b16d-1d7805346f97)

-1. Browse to http://localhost:8080 (or whichever port you configured for Jenkins when installing it) and wait until the Unlock Jenkins page appears.
![Capture d’écran 2024-09-01 002326](https://github.com/user-attachments/assets/8ee2ec3b-7ad4-455b-b0a4-9ffc9fb373da)
![Capture d’écran 2024-09-01 002421](https://github.com/user-attachments/assets/2fa924aa-a923-416b-95f8-b82b636f1fe8)
![Capture d’écran 2024-09-01 003144](https://github.com/user-attachments/assets/90c5c165-ab41-462c-b26d-ae5efd28706a)
![Capture d’écran 2024-09-01 003224](https://github.com/user-attachments/assets/aa63a3e5-86d6-47be-9029-7739b08dd5f7)

#### How to set up an agent slave connecting with the controler(Master)** <br>
 Why should we set up this agent ? Can't we just work only with the **Master** ? <br>
 Yes absolutely,it's possible to work solely with the **master**. However, It's not recommanded.If you need to run a parallel tasks, the **master** alone won't suffice. Because the master processes task sequentially. They help distribute the workload, allowing jobs to run faster and more efficiently in collaboration with the **Master**. <br>

 **Get started**
 To do this, we can adopt the approch of cloud, meaning we set up the agent from the Cloud, in particular in docker.
 > 1. Go to **Jenkins Administer** <br>

 ![Capture d’écran 2024-09-01 003524](https://github.com/user-attachments/assets/6948213e-c7e7-4ed3-b2e2-bb4b5dacd003)
 
>  2. Select the **plugin** to set up **docker plugin** <br>
 ![Capture d’écran 2024-09-01 003616](https://github.com/user-attachments/assets/3b50676f-b07a-417d-8b35-3209a79081e6)
![Capture d’écran 2024-09-01 012055](https://github.com/user-attachments/assets/811be96e-d2d3-4a50-bdb3-633615e95224)

>  3. Once the plugin is installed, select **Clouds** and **New cloud**. <br>

![Capture d’écran 2024-09-01 012234](https://github.com/user-attachments/assets/b736bd45-5de7-4114-93e0-155c06a22723)

>  4. Go to the terminal to set up the new container which contains the worker image <br>

![Capture d’écran 2024-09-01 012500](https://github.com/user-attachments/assets/3d22f6a9-ab67-4bdf-b5b2-e39aa8908660)

>  5. Fullfill as following. Test the connection when you put **Docker Host URI** <br>

![Capture d’écran 2024-09-01 012335](https://github.com/user-attachments/assets/4c07222f-c980-4a2c-b9a5-e65a1d45ba7c)
![Capture d’écran 2024-09-01 013224](https://github.com/user-attachments/assets/125af4fb-9d4b-4d60-83eb-90e13e72102a)

> 6. Select **Add Docker Template**: <br>

![Capture d’écran 2024-09-01 014607](https://github.com/user-attachments/assets/ce2cd2e8-1d16-45b1-972a-eb8d25e31a9a)
![Capture d’écran 2024-09-01 015136](https://github.com/user-attachments/assets/76cbf3ae-0f34-4d50-a79a-b0938f6c7dc1)
![Capture d’écran 2024-09-01 015222](https://github.com/user-attachments/assets/bff5d86d-b4f5-4ba8-998b-e74fd8a6094f)
![Capture d’écran 2024-09-01 015302](https://github.com/user-attachments/assets/d5b469a5-8b98-4d95-bc57-708ff3977c9e)

7. Go back in your dashboard and execute a job by the agent installed now. <br>

![Capture d’écran 2024-09-01 015652 - Copie](https://github.com/user-attachments/assets/87387dbe-2004-4f8b-a1b3-7363751dd006)
![Capture d’écran 2024-09-01 015652](https://github.com/user-attachments/assets/63d40372-e83c-4494-9e5b-a745b1099945)
![Capture d’écran 2024-09-01 015720 - Copie](https://github.com/user-attachments/assets/638d1a6d-5090-4427-85ab-05ecb755e540)
![Capture d’écran 2024-09-01 015831](https://github.com/user-attachments/assets/deeb5ceb-6904-438a-aff4-e3d184b6b14a)






