# AWS WordPress Hosting Project

## Overview
This project demonstrates how to host a WordPress website on AWS, leveraging various AWS services to ensure a scalable, reliable, and secure deployment. The setup involves using multiple AWS resources such as VPC, EC2, RDS, EFS, and more to provide a robust infrastructure for the WordPress application. The reference architecture diagram and deployment scripts are available in the project’s [GitHub repository](https://github.com/ElMehdiiiii/WordPress-Website-on-AWS).

## Architecture 

![Alt text](/2._Host_a_WordPress_Website_on_AWS_.png)

## Architecture Components

1. **Virtual Private Cloud (VPC)**    
2. **Internet Gateway**
3. **Security Groups**
4. **Availability Zones**
5. **Public Subnets**
6. **EC2 Instance Connect Endpoint**
7. **Private Subnets**
8. **NAT Gateway**
9. **EC2 Instances**
10. **Application Load Balancer (ALB)**
11. **Auto Scaling Group**
12. **Certificate Manager**
13. **Simple Notification Service (SNS)**
14. **Route 53**
15. **Elastic File System (EFS)**
16. **Relational Database Service (RDS)**

    
## Setup Instructions

1. **Configure VPC and Subnets**
    - Create a VPC with both public and private subnets across two availability zones.

2. **Set Up Internet Gateway and NAT Gateway**
    - Deploy an Internet Gateway for the VPC.
    - Configure NAT Gateways in the public subnets for instances in private subnets to access the Internet.

3. **Configure Security Groups**
    - Set up security groups to manage inbound and outbound traffic rules.

4. **Deploy EC2 Instances**
    - Launch EC2 instances within the private subnets.
    - Install and configure WordPress on these instances.

5. **Set Up Application Load Balancer**
    - Create an ALB and configure it to distribute traffic to the EC2 instances.

6. **Configure Auto Scaling Group**
    - Set up an Auto Scaling Group to manage the number of EC2 instances based on traffic.

7. **Set Up RDS**
    - Deploy an RDS instance for the WordPress database.

8. **Configure EFS**
    - Set up EFS for a shared file system accessible by all WordPress instances.

9. **Secure Communications**
    - Use AWS Certificate Manager to secure your domain with SSL/TLS certificates.

10. **Configure Route 53**
    - Set up DNS records for your domain in Route 53.

11. **Set Up SNS**
    - Configure SNS to send notifications about Auto Scaling events.

### Accessing the WordPress Site
Once the setup is complete, your WordPress site will be accessible via the domain name configured in Route 53.

## Conclusion
This setup leverages AWS's extensive suite of services to provide a scalable, secure, and highly available WordPress hosting solution. The project demonstrates best practices in cloud architecture and DevOps, ensuring a robust environment for hosting web applications.
