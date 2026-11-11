# WinLocal Giveaways – AWS Cloud Architecture

**Module:** Security Architecture (COMP H2701), TU Dublin
**Author:** Nathan Mooney

## Files

| File | Description |
| --- | --- |
| `AWSDiagram.drawio` | AWS architecture diagram of the proposed WinLocal cloud setup (editable in [diagrams.net](https://app.diagrams.net)). |
| `SecArcReport.docx` | Written report covering the design, Proof of Concept (PoC), extra services and sustainability analysis. |

## About the Project

WinLocal Giveaways wanted to move their website and systems from an old on-premises server setup to the cloud. This project designs and builds a Proof of Concept on AWS that tackles their main concerns: website availability, secure data storage, scalability and network security.

## What Was Done

1. **Architecture diagram** – Designed the proposed AWS layout, including a VPC with public and private subnets, Application Load Balancer, NAT and Internet Gateways, Bastion Host, EC2 instance, Auto Scaling Group and RDS database.
2. **Proof of Concept** – Built the core services in AWS:
   - VPC, subnets and security groups to segment the network
   - Bastion Host as a jump server for admin access to the private EC2 instance
   - EC2 website instance behind an Application Load Balancer
   - Auto Scaling Group (using an AMI) that adds instances at 60% CPU utilisation
   - RDS database in a private subnet for storing user data
   - S3 bucket hosting a static backup website for when the main site is down
3. **Additional services** – Proposed two add-ons, shown in the diagram but not built in the PoC:
   - **AWS WAF** to filter malicious traffic such as DDoS attempts
   - **AWS SNS** to notify users of giveaway results by email or text
4. **Sustainability review** – Assessed the PoC against the AWS Well-Architected sustainability pillar, covering auto scaling utilisation, S3 lifecycle policies and instance scheduling.
