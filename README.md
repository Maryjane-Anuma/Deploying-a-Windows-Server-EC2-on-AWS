# Deploying-a-Windows-Server-EC2-on-AWS
📌 Project Overview  In this project, I launched a Windows Server EC2 instance on AWS using the Amazon Windows Server 2019 Base AMI . The goal was to practice secure deployment of Windows servers in the cloud while following best practices for networking and security.


## 🎯 Objectives

Deploy a Windows Server 2019 EC2 instance in a public subnet.

Configure a Security Group to allow RDP (port 3389) access only from my public IP address.

Assign a Name tag to the instance for easy identification.

Ensure the server is properly secured for remote management.

⚙️ Steps Taken
1. Select AMI

Chose Microsoft Windows Server 2019 Base AMI from the AWS AMI catalog.

2. Choose Instance Type

Selected t2.micro (Free Tier eligible) for testing.

3. Networking Configuration

Placed the instance in a public subnet of my VPC.

Enabled Auto-assign Public IP so I could connect from my machine.

4. Security Group Setup

Created a new Security Group with the following rule:

✅ Inbound: Allow RDP (TCP/3389) only from my public IP.

❌ Denied access from all other IPs.

 <img width="1908" height="891" alt="security group rules" src="https://github.com/user-attachments/assets/8f3e4670-3c5a-4c64-875a-b274f680a147" />



6. Launch & Connect

Generated and downloaded a new key pair (.pem).

Launched the instance.

Used RDP client with the public IP and administrator credentials to connect successfully.

<img width="1908" height="891" alt="RDP connection" src="https://github.com/user-attachments/assets/302ee27e-73ee-47f2-aa91-ba8b6506b2db" />

![successful connection of RDP](https://github.com/user-attachments/assets/f3b22dcb-ee08-4ee8-b27f-b36caf67b4ee)


🔐 Security Considerations

Restricted RDP access only to my IP to minimize exposure.

Avoided the common mistake of opening 0.0.0.0/0 for RDP, which is a huge security risk.

Tagged resources for better management in production.


🧩 Key Takeaways

Secure deployment begins at the network level.

AWS Security Groups are your first line of defense.

Always follow the principle of least privilege when exposing services like RDP.


🔖 Tags  

![AWS](https://img.shields.io/badge/Cloud-AWS-orange?logo=amazon-aws&logoColor=white)  
![EC2](https://img.shields.io/badge/Compute-EC2-blue?logo=amazonec2&logoColor=white)  
![Windows Server](https://img.shields.io/badge/OS-Windows%20Server%202019-0078D6?logo=windows&logoColor=white)  
![Security](https://img.shields.io/badge/Focus-Cloud%20Security-red?logo=security&logoColor=white)  
![Portfolio](https://img.shields.io/badge/Type-Portfolio%20Project-green)
