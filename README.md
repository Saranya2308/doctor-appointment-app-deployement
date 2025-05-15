# doctor-appointment-app-deployement

This repository contains the AWS CloudFormation templates and related scripts to provision the cloud infrastructure for the Doctor Appointment Application backend.

---

## Overview

The infrastructure setup automates provisioning of the following AWS resources:

- **VPC and Subnets** (`vpc.yaml`):  
  Creates a custom Virtual Private Cloud with public and private subnets, route tables, internet gateway, and network ACLs to securely isolate backend resources.

- **Backend EC2 Instance** (`backend.yaml`):  
  Launches an EC2 instance in the specified subnet within the VPC to host the backend Node.js application. It uses EC2 User Data scripts to bootstrap the environment and start the backend server.

- **MongoDB Setup** (`mongodb.yaml`) *(Optional)*:  
  (If used) Provisions a separate EC2 instance or managed resource for MongoDB database hosting in a private subnet.

---

## Prerequisites

- AWS CLI installed and configured with proper credentials.
- An existing EC2 Key Pair (e.g., `prescripto-key-new`) for SSH access.
- CloudFormation permissions to create VPCs, EC2 instances, and IAM roles.

---

