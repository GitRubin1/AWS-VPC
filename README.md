# AWS Terraform VPC Project

Create and deploy a VPC using Terraform

## Table of Contents
* [General Info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Acknowledgements](#acknowledgements)

## General Info

This project deploys a VPC in an AWS environment. 

It deploys the following resources:

  1. VPC
  2. Public Subnet
  3. Private Subnet
  4. Internet Gateway
  5. Elastic IP Address
  6. Egress-only Internet Gateway
  7. Public Route Table
  8. Private Route Table

Create cloud VPC in terraform using https://www.youtube.com/watch?v=qnkxOwvHNt4&t=407s as a basis 
and adding IPv6 compatibility using Terraform documentation from https://www.terraform.io/docs/index.html

## Technologies


## Setup

### Install Terraform

Terraform provides a nice video for installation of their service

Watch the video and follow the instructions in the video located at: https://learn.hashicorp.com/tutorials/terraform/install-cli

### Install AWS CLI

Go to https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html and follow the instructions for your specific operating system

On the AWS portal, create an IAM user with the desired permissions

Once you are ready run `aws configure` (Windows) in your command line
Copy the Access Key ID and Secret Access Key and paste them when prompted
Select your desired region and leave "Default Ouput Format" null

Select the location where you would like to save [vpc.tf](#vpc.tf)
Run `terraform init` in your command line
To commit the changes to AWS run `terraform apply`
Once you are finished with the resources, delete them using `terraform destroy`


## Acknowledgements
