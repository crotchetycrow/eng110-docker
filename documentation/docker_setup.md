# Docker Setup and Installation

### Docker WSL2/Linux subsystem on windows

- Install Docker Desktop on Window [Click here](https://docs.docker.com/desktop/windows/install/)
- Windows Hyper-v settings
  ![](<https://github.com/spartaglobal/NewDevOpsCurriculum/blob/master/07_Containarization_Microservices/01_Containersation_Docker_Intro/images/Hyper-v-settings%20(2).png>)
- Linux subsystem options
  ![](https://github.com/spartaglobal/NewDevOpsCurriculum/blob/master/07_Containarization_Microservices/01_Containersation_Docker_Intro/images/docker_settings.png)

### Docker for Mac

[Click here](https://docs.docker.com/desktop/mac/install/)

### Install and run Docker Desktop on Mac

Double-click Docker.dmg to open the installer, then drag the Docker icon to the Applications folder.
![](../images/docker-app-drag.png)

- Follow the steps
- Specify OS and chip - Intel or M1

### Install Docker on Linux ubuntu

- `sudo apt-get remove docker docker-engine docker.io containerd runc`
- `sudo systemctl start docker`
- `sudo systemctl enable docker`
- Check status
- `sudo systemctl status docker`

#### Summary:

- Docker Installation and setup completed
- Hyper V settings
- WSL2 and Linux subsystem enabled
