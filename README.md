# terraformreuse
provider "aws"{
region = "ap-south-1"
}
module "ec2-instance" {

# source = "./ec2-instance"
source = "github.com/atulguptalko/terraformreuse"
ami_id = "ami-0c1a7f89451184c8b" #ubuntu ami-id in Mumbai region
instance type = "t2.micro"
vpc_id = "vpc-08dff3c2833e88864" #vpc id of my account's default vpc
port = "22"
cidr_block = "0.0.0.0/0"
}
