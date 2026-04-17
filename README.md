# aws-vpc-alb-asg-project
# Highly Available Web Application using AWS VPC, ALB, and Auto Scaling

This project demonstrates how to deploy a scalable and highly available web application on AWS. The infrastructure is designed using a custom VPC with public and private subnets, an Application Load Balancer to distribute traffic, and an Auto Scaling Group to maintain availability.

## Architecture Summary

- Created a custom VPC with CIDR block
- Configured public and private subnets across two Availability Zones
- Deployed an Internet Gateway for public access
- Configured NAT Gateway to allow internet access for private instances
- Launched EC2 instances in private subnets
- Set up an Application Load Balancer in public subnets
- Connected EC2 instances to a target group
- Configured an Auto Scaling Group for high availability

## Key Components

- VPC and Networking: A VPC was created to isolate the network. Public subnets are used for the load balancer and NAT Gateway, while private subnets host the application servers.

- Internet Gateway and NAT Gateway: The Internet Gateway allows inbound traffic to the load balancer. The NAT Gateway enables private instances to access the internet for updates and package installation.

- EC2 Instances: Web servers are deployed in private subnets. Apache is installed and configured to serve a simple web page.

- Application Load Balancer: The load balancer distributes incoming HTTP traffic across multiple EC2 instances to ensure availability and reliability.

- Target Group: The EC2 instances are registered in a target group, and health checks are used to ensure only healthy instances receive traffic.

- Auto Scaling Group: The Auto Scaling Group automatically maintains the desired number of instances and replaces unhealthy ones.

## Implementation Steps

- Created a VPC and defined CIDR block
- Created public and private subnets in two Availability Zones
- Attached Internet Gateway to the VPC
- Created and configured NAT Gateway in a public subnet
- Configured route tables for public and private subnets
- Launched EC2 instances and installed web server
- Created a target group and registered instances
- Set up an Application Load Balancer
- Created a launch template
- Configured Auto Scaling Group with desired capacity

## Result

The application is accessible through the load balancer DNS. Traffic is distributed across multiple instances, and the system remains available even if one instance fails.

## Screenshots

### VPC Setup
![VPC](vpc.jpeg)<img width="2932" height="1564" alt="vpc" src="https://github.com/user-attachments/assets/5c017a1b-2cc2-4c50-9b21-5ba45a1decf2" />


### Route Table
![Route Table](route-table.png)

### NAT Gateway
![NAT](nat.jpeg)<img width="1600" height="945" alt="nat" src="https://github.com/user-attachments/assets/1197948c-93e8-4873-bca2-37b48b2a8118" />


### Target Group
![Target Group](target-group.png)<img width="1600" height="918" alt="target-group" src="https://github.com/user-attachments/assets/26f2370b-6ebd-4e35-87aa-12ab5eb47222" />


### Load Balancer
![ALB](alb.jpeg)<img width="1024" height="616" alt="alb" src="https://github.com/user-attachments/assets/c3ba4130-7cb3-4d6c-ac2c-d7a8a97a33bd" />


### Auto Scaling Group
![ASG](asg.png)

### Final Output
![Output](final-output.jpeg) <img width="1122" height="242" alt="final-output" src="https://github.com/user-attachments/assets/a8e8d276-5e85-4184-8675-d988d21ddcc8" />


# Learning Outcomes
- Understanding of VPC and subnet design
- Difference between public and private resources
- Load balancing and health checks
- Auto Scaling concepts and configuration
- Basic troubleshooting of AWS infrastructure

This project helped in understanding how to design a fault-tolerant and scalable architecture on AWS using core services like EC2, VPC, ALB, and Auto Scaling.

  
