This project demonstrates the deployment of a highly available static website using AWS services. The architecture ensures reliability by using multiple Availability Zones, automated backups, and reusable machine images.

Step 1 – Launch EC2 Instance
Created an Amazon EC2 instance in one Availability Zone to host the static website. Installed and configured a web server on a Linux-based instance. This instance acts as the primary server for hosting the website content.
Services Used: EC2, Linux

Step 2 – Configure Security Groups
Configured EC2 Security Groups to allow inbound traffic on port 80 (HTTP) and port 22 (SSH). HTTP access allows users to access the website, while SSH access allows secure remote administration of the server.
Services Used: EC2 Security Groups

Step 3 – Attach EBS Volume and Host Website
Attached an Amazon EBS volume to the EC2 instance for storing website files. Mounted the volume and deployed the static website content. This allows persistent storage independent of the EC2 instance lifecycle.
Services Used: EC2, EBS, Linux

Step 4 – Store Backups in S3
Uploaded website backup files to Amazon S3 for durable and scalable storage. This ensures data safety and allows easy recovery in case of instance failure or data loss.
Services Used: S3

Step 5 – Create Snapshot and AMI
Created an EBS snapshot to back up the storage volume and generated an AMI from the configured EC2 instance. This enables quick recovery and easy replication of the server environment.
Services Used: EBS Snapshot, AMI

Step 6 – Launch EC2 in Another Availability Zone
Launched a new EC2 instance in a different Availability Zone using the created AMI. This ensures high availability and redundancy in case one Availability Zone becomes unavailable.
Services Used: EC2, AMI

