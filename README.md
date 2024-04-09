
# A Highly Available and Secure Infrastructure setup with Auto Scaing in AWS



## Overview
This project aims to set up a secure infrastructure on AWS utilizing various services including Virtual Private Cloud (VPC), Auto Scaling Groups (ASG), Bastion Server, Simple Notification Service (SNS), and Application Load Balancer (ALB). The infrastructure is designed to be resilient, scalable, and secure, with controlled access to private instances and efficient handling of incoming web traffic.
## Services Used
- Elastic Compute Cloud(EC2)
- Virtual Private Cloud(VPC)
- Auto Scaling Group
- Load Balancer
- Security Groups
- Simple Notification Service (SNS)
## Steps to Follow
1. VPC Setup: Created a VPC spanning across two Availability Zones (AZs) with a public and private subnet in each AZ.
2. Auto Scaling Group (ASG): Configured an ASG with a minimum of 1 instance and a maximum of 4 instances, deployed in the private subnets, and exposed ports 8000 (for application) and 22 (for SSH).
3. SNS Integration: Added an SNS topic to receive notifications via email for instance launch and termination events.
4. Bastion Server: Implemented a bastion server in the public subnet to facilitate secure access to private instances. Copied key-value pair files onto the bastion server for SSH access to private instances.
5. Private Instance Configuration: Accessed private instances from the bastion server using SSH and created a simple HTML file. Started the server on port 8000 for serving web content.
6. Application Load Balancer (ALB): Created an ALB with a target group consisting of private instances, exposing port 8000 to handle incoming web traffic.
7. Internet-Facing ALB: Configured the ALB to accept HTTP requests on port 80 directly from the internet gateway.
## Image of the Architecture
![Architecture](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/b1cf687f-714f-4b19-bd4a-6583e2785b18)
## VPC Creation
![vpc is u and running](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/8ef3aaaf-121b-4508-9673-170f4f0fc6b9)
## Preview of Architecture after creating VPC
![PreviewOfArchitecture](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/2999e6ac-1598-4848-916e-707a058ccd09)
## Auto Scaling Group Creation
![ASG created succeessfully](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/7bdf50fa-e1e3-4114-bd38-3f6a40567fe9)
## Instances Created by ASG
![InstancesCreatedByASG](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/bd3779be-5c89-466a-b5b0-027f9317cd8c)
## Bastion Server Creation
![BastionServerCreated](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/c96a3467-52cf-4a0c-8bcd-7fb2b800052a)
## Load Balancer Creation
![load balancer creation](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/e3b16266-7325-40a2-b06c-ac32506615b3)
## Usage/Examples
![Final App running](https://github.com/Being-Reprobate/Highly-Available-and-Secure-Infrastructure-Setup-with-Auto-Scaling-and-Bastion-Server-in-AWS/assets/145685176/7183f8e7-34f0-49f4-9a47-f17c3abac3f0)
