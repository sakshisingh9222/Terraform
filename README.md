# Python Web Scraper Deployment with Terraform on AWS
This repository contains a Python web scraper that can be deployed to an AWS EC2 instance using **Terraform**. The project automates the process of launching an EC2 instance, installing necessary dependencies, and running the Python scraper script.

# Prerequisites:
Python Web Scraper: Ensure your Python script is ready and works properly locally.
Terraform: Install Terraform on your system.
Cloud Provider Account: Set up an account with a cloud provider like AWS, GCP, or Azure.Here we are using AWS 

# Steps:
1. Install TerraforM
2. Set up AWS credentials on your machine
     ##aws configure
      This will prompt you for the AWS Access Key, Secret Key, region, and output format.
3. Create the Terraform configuration file (main.tf) and paste the following configuration into it.
    ###terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}

5. 
6. 

