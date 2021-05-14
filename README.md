# AWS Terraform VPC Project

Create and deploy a VPC using Terraform

## Table of Contents
* [General Info](#general-info)
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

The VPC is comprised of two subnets, one public and one private. 
The public subnet is associated to a public route table which will send default IPv4 and IPv6 traffic to the internet gateway. 
The private subnet is associated to a private route table containing two routes, one which will send the default IPv4 traffic to a NAT Gateway and one which will send the default IPv6 traffic to an egress-only internet gateway. 
Route table associations link the corresponding subnets to their route tables.
By default, a main route table gets created in AWS which allows the two subnets to send traffic locally

## Setup

### Install Terraform

Terraform provides a nice video for installation of their service

Watch the video and follow the instructions in the video located at: https://learn.hashicorp.com/tutorials/terraform/install-cli

### Install AWS CLI

Go to https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html and follow the instructions for your specific operating system

On the AWS portal, create an IAM user with the desired permissions. Use Programmatic Access and AdministratorAccess can be used just for the sake of this lab.

Once you are ready run `aws configure` (Windows) in your command line.
Copy the Access Key ID and Secret Access Key and paste them when prompted.
Select your desired region and leave "Default Ouput Format" null.

CD into a new folder where you would like to save [vpc.tf](https://github.com/GitRubin1/AWS-VPC-Terraform/blob/main/vpc.tf).
Run `terraform init` in your command line.
To push the changes to AWS run `terraform apply` and select 'yes' when prompted.
Once you are finished with the resources, delete them using `terraform destroy`.


## Acknowledgements

https://www.youtube.com/watch?v=qnkxOwvHNt4&t=407s as a basis for the project

https://www.terraform.io/docs/index.html to add IPv6 functionality
