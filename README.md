
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

