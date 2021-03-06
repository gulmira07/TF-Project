# TF-Project Team2 VPC Module

This module creates a VPC in a region specified by the user.


## Prerequisites

   Git
   Terraform
   AWS account


## Installation

In the folder you are planning to work, run the following commands one by one:

sudo yum install git -y      # Installs git

git init                     # Initializes git

git clone https://github.com/ortacu/TF-Project.git        # Clones repo into a directory on your machine
 
cd TF-Project           # Changes working directory to cloned directory

cd test-project         # Changes directory to module directory 

terraform init          # Initializes Terraform  
 
teraform plan           # Previews the output of the module

terraform apply         # Runs the module 


If resources are not needed at any point in time, run "terraform destroy" to delete all resources created by the module. Keep in mind that you have to run this command from the module directory


## Usage

Creates the whole enviroment together with the VPC to enable the multitude of resources to be readily accessible. 

   1. creates:
        a. 3 public subnets 
        b. 3 private subnets
        c. 1 internet gateway
        d. 1 nat gateway
        e. 1 private route table 
        f. 1 public route table

    2. attaches:
        a. the 3 public subnets to the internet gateway
        b. the 3 private subnets to the nat gateway    
        c. the 3 public subnets to the public route table
        d. the 3 public subnets to the private route table


## Resources

To verify resources that were created, go to your AWS account and check in the region you specified