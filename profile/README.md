# CSYE 6225 Infrastructure and Web Application Overview

## Overview
This organization contains two main repositories, each serving a distinct yet integrated purpose in deploying and managing a cloud-based web application:

1. **TF AWS Infra**: Handles the infrastructure setup using Terraform to manage AWS cloud resources.
2. **WebApp**: Contains the Spring Boot web application that runs on the infrastructure provisioned by Terraform.

## Repositories

### 1. **TF AWS Infra** [Link](https://github.com/Shreyas-Kothari/tf-aws-infra)
The **TF AWS Infra** repository is dedicated to managing the cloud infrastructure required to run the CSYE 6225 web application. Using Infrastructure as Code (IaC) with **Terraform**, this repository automates the deployment of all necessary AWS resources, including:

- **Network Configuration**: Creates a Virtual Private Cloud (VPC) with public and private subnets.
- **Security**: Defines security groups for both web applications and databases, ensuring controlled access to services.
- **Compute Resources**: Deploys EC2 instances with custom AMIs tailored to run the web application.
- **Database**: Sets up a MySQL database hosted on Amazon RDS with secure network configurations.
- **Load Balancing and Routing**: Configures route tables, internet gateways, and load balancers for traffic management.

The goal of this repository is to provide a scalable and secure foundation for running cloud-based web applications, enabling automated and repeatable infrastructure deployments.

### 2. **WebApp** [Link](https://github.com/Shreyas-Kothari/webapp)
The **WebApp** repository contains the source code for a Spring Boot web application designed to run seamlessly on the AWS infrastructure set up by **TF AWS Infra**. Key features of this repository include:

- **Stateless Web Application**: Implements REST APIs for various functionalities using Spring Boot.
- **Database Integration**: Connects to the MySQL database hosted on Amazon RDS, with dynamic configurations handled through environment variables.
- **Packer Integration**: Utilizes Packer templates to build custom Amazon Machine Images (AMIs) that include the web application and its dependencies.
- **Continuous Integration**: Implements GitHub Actions for code testing, validation, and Packer image creation to ensure the web application is robust and deployment-ready.

This repository is responsible for delivering the application logic and services that interact with the cloud infrastructure set up by **TF AWS Infra**.

## Integration
Together, these repositories enable a fully automated and secure deployment pipeline:
- The **TF AWS Infra** repository provisions the cloud infrastructure, creating a robust environment for the web application.
- The **WebApp** repository contains the application code, which is packaged and deployed on the infrastructure through CI/CD workflows.

By combining Infrastructure as Code with a cloud-native web application, this project demonstrates best practices in scalable and automated cloud deployments.
