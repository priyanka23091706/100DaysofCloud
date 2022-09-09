<!-- This is a template you can use for quick progress days. It removes a lot of the steps we encourage you to share in the longer template 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

# Setup EC2 with Apache server

## Cloud Research

Install apache webserver and add html page to server

-  Bash Script

#!/bin/bash

########################################
##### USE THIS WITH AMAZON LINUX 2 #####
########################################

# get admin privileges
sudo su

# install httpd (Linux 2 version)
yum update -y

yum install -y httpd.x86_64

systemctl start httpd.service

systemctl enable httpd.service

echo "Hello World from $(hostname -f)" > /var/www/html/index.html

## Social Proof

✍️ Show that you shared your process on Youtube

[link](link)
