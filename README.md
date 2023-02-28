# Terraform Configuration for AWS VPC, EC2 and RDS

### This project contains terraform configuration files on creating EC2 and RDS instances inside a Custom VPC on AWS. Here is the architecture of what will be created:

![Custom VPC architecture for AWS](https://miro.medium.com/max/700/1*Oxp7FZT4Z9RWqpnJn-hHqw.png)

## Set Up
### Prerequisites
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) installed and configuration
- [Terraform](https://www.terraform.io/downloads) installed

### Create the Secrets file
Create The secrets on github actions and populate it with the follow secrets:

env:
  TF_VAR_db_username: ${{ secrets.db_username }}
  TF_VAR_db_password: ${{ secrets.db_password }}
  TF_VAR_my_ip: ${{ secrets.my_ip }}

Check the path .github/workflows in order to check the pipeline
