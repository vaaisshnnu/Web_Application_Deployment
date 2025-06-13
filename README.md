# 🚀 Java Web App Deployment on AWS EC2 with Tomcat, Maven, Git & WinSCP

Welcome to my Java Web App Deployment Project!  
In this repo, you’ll find the **complete documentation and commands** to deploy a Maven-based Java application manually on an EC2 instance using **Apache Tomcat** and **WinSCP**.

> ⚡ This project showcases my passion for DevOps, cloud, and modern deployment tools.

## 🔧 Tools & Technologies Used

- **Amazon EC2** (Amazon Linux 2 AMI)
- **Apache Tomcat 9**
- **Maven**
- **Git**
- **WinSCP** (for WAR file transfer)
- **Web Browser** (for deployment via Tomcat UI)


## 📸 Deployment Screenshot Highlights


### 🌐 App Live on Browser
![Maven Project - Manual Deployment](https://github.com/user-attachments/assets/366233f7-0943-4916-a487-2bb137f9a3f8)


### ✅ WAR Deployed Successfully
![Deployment Area](https://github.com/user-attachments/assets/a75e0630-7088-4cce-af5b-0e670a82edbd)

--

## 🛠️ Step-by-Step Deployment Instructions

### 1. 🚀 Launch EC2 Instance
- Launch an Amazon Linx2 AMI EC2 instance
- Allow **Custom TCP Port 8080** in the security group

### 2. 🧰 Install Tools on EC2

sudo yum update -y

sudo yum install maven -y

sudo yum install git -y

sudo amazon-linux-extras install java-openjdk11


### 3. 📥 Download & Install Tomcat 9

wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.105/bin/apache-tomcat-9.0.105.tar.gz

tar -xvzf apache-tomcat-9.0.105.tar.gz

``

### 4. 🔑 Configure Tomcat Users
Please follow my commands notes for step by step vision of the change to be made in the files for editing 

The `context.xml for granting the access part and to edit the tomcat.xml for the user accesses and Start the Tomcat Server

### 5. 🎯 Clone the Repo & Build WAR

git clone https://github.com/vaaisshnnu/Web-Application.git

cd <repo-folder>

mvn compile

mvn package

> The WAR file will be available in the `target/` directory.

Now Connect to you public IP of EC2 with 8080 port in browser
Navigate to Server Status --> Provide ID & Password (Admin) --> List Applications --> Now it's time to get the artifact of our Project

## 💻 WAR File Deployment

1. Use **WinSCP** to download the `.war` file from EC2 to your local machine.
2. Login using ec2user and Click on advanced to locate and upload the ec2 .ppk file
3. Pull the war fike to your local system
4. Upload your `.war` file in the List Application tab  and shown  in screenshot in the Tomcat and click **Deploy**

✅ Your app will now be running at:
`http://<ec2-ip>:8080/<your-app-name>/`

---

## 🤝 Let’s Connect!
Hi, I'm **Ganga Vaishnu Reddy Emani**


📬 [Connect with me on LinkedIn](https://www.linkedin.com/in/vaaisshnnu-reddy)


