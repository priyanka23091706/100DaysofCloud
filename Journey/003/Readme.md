<!-- This is a template you can use for quick progress days. It removes a lot of the steps we encourage you to share in the longer template 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

# Create an AWS EC2 Instance and run some AWS CLI Commands

## Cloud Research

![Journey/003/Architecture-Diagram-EC2-AWSCLI.png]

- Some CLI Commands used in this lab
# Create Keypair 

aws ec2 create-key-pair --key-name MyCLIKeyPair --query 'KeyMaterial' --region us-east-1

# Create Security Group 

aws ec2 create-security-group --group-name my-sg --description "My security group" --region us-east-1

# Create EC2 Instance 

aws ec2 run-instances --image-id  ami-062f7200baf2fa504 --count 1 --instance-type t2.micro --key-name MyCLIKeyPair --security-groups my-sg --region us-east-1

# Delete Ec2 Instance 
 
aws ec2 terminate-instances --instance-ids <> --region us-east-1

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
