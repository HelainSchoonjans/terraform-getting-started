# terraform-getting-started
See here: https://learn.hashicorp.com/terraform/getting-started/build

## Initialization

    terraform init
	
## Check & apply

	terraform apply

## Show current state

    terraform show
	
## Destroy infrastructure

See here: https://learn.hashicorp.com/terraform/getting-started/destroy

    terraform destroy
	
## Dependencies

Can automatically infer when a resource depends on another, based on the name of the resource.

## Provision

See here: https://learn.hashicorp.com/terraform/getting-started/provision

    resource "aws_instance" "example" {
        ami           = "ami-b374d5a5"
        instance_type = "t2.micro"

        provisioner "local-exec" {
            command = "echo ${aws_instance.example.public_ip} > ip_address.txt"
        }
    }
	
## Variables

In a .tf file:

	variable "access_key" {}
	variable "secret_key" {}
	variable "region" {
  		default = "us-east-1"
	}

See more here: https://learn.hashicorp.com/terraform/getting-started/variables

## Outputs

See here: https://learn.hashicorp.com/terraform/getting-started/outputs

## Modules

See here: https://learn.hashicorp.com/terraform/getting-started/modules

# Examples
## AWS
https://github.com/terraform-providers/terraform-provider-aws
	
# Learning

## Questions

How to add software like docker on images?
Is it possible to create deployment plans for dockers using Terraform?

## Things to learn

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html
