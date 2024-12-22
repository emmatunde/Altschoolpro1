# Web Deployment Project

This repository contains the steps and resources for deploying a prototype web application, which includes provisioning a Linux server, setting up a web server, and deploying a simple HTML landing page.

## Project Overview
This project demonstrates the ability to provision a server, configure a web server, and deploy a simple HTML page showcasing our team's capabilities to potential investors.

---

## Landing Page
- **Name**: Emmaneul Abodunrin
- **Project Title**: Welcome to Emmaneul Abodunrin's Landing Page
- **Description**: A prototype web application to demonstrate server provisioning, web server configuration, and HTML deployment.
- **Bio**: I am a passionate tech enthusiast, telecoms engineer, and aspiring Cloud/DevOps Engineer with nearly five years of experience. I aim to make a global impact by solving complex cloud problems.

---

## Deliverables
- **Public IP Address/URL**: 35.176.13.70
- **Screenshot**: [Insert screenshot link or add it directly to the repository]

---

## Deployment Steps

### 1. Provisioning the Server
1. **Platform**: AWS (Amazon Web Services)
2. **Instance Type**: t2.micro (Free Tier Eligible)
3. **Linux Distribution**: Ubuntu 22.04 LTS
4. **Steps**:
   - Log in to your AWS Management Console.
   - Launch an EC2 instance with Ubuntu 22.04 LTS.
   - Select a key pair for secure SSH access or create a new one.
   - Assign a security group allowing SSH (port 22) and HTTP (port 80) access.

---

### 2. Configuring the Server
1. **Update the Package Index**:
   ```bash
   sudo apt update && sudo apt upgrade -y


Install Apache Web Server:
bash
Copy code
sudo apt install apache2 -y
Enable Apache Service:
bash
Copy code
sudo systemctl enable apache2
sudo systemctl start apache2
3. HTML Page Deployment
Create the HTML Page:

Navigate to the web server directory:
bash
Copy code
cd /var/www/html
Create an HTML file:
bash
Copy code
sudo nano index.html
Add the following content:
html
Copy code
<!DOCTYPE html>
<html>
<head>
    <title>Welcome to Abodunrin Emmaneul Olatunde's Landing Page</title>
</head>
<body>
    <h1>Welcome to Abodunrin Emmaneul Olatunde's Landing Page</h1>
    <p>This is a prototype web application to demonstrate server provisioning, web server configuration, and HTML deployment.</p>
    <h2>About Me</h2>
    <p>I am a passionate tech enthusiast, telecoms engineer, and aspiring Cloud/DevOps Engineer with nearly five years of experience. I aim to make a global impact by solving complex cloud problems.</p>
</body>
</html>
Save and close the file.
Verify the Deployment:

Open a web browser and navigate to your public IP address:
vbnet
Copy code
http://<your-public-ip>
4. Networking Configuration
Allow HTTP Traffic:
In your AWS Security Group, add a rule to allow HTTP traffic on port 80.
Verify Connectivity:
Test the connection by accessing your public IP address.
Bonus Task: Enabling HTTPS
Install Certbot:
bash
Copy code
sudo apt install certbot python3-certbot-apache -y
Obtain a Free SSL Certificate:
bash
Copy code
sudo certbot --apache
Renew Certificate Automatically:
bash
Copy code
sudo crontab -e
Add the following line:
bash
Copy code
0 0,12 * * * certbot renew --quiet


Additional Information
Git Repository: [Insert Repository Link Here]
Tools Used: AWS, Ubuntu, Apache, HTML, Certbot (for HTTPS)
Author: Emmaneul Abodunrin
