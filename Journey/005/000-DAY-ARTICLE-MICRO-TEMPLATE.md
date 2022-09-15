<!-- This is a template you can use for quick progress days. It removes a lot of the steps we encourage you to share in the longer template 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

# Create Continuous Delivery in EC2 using CodeDeploy and CodePipeline

## Cloud Research

- ✍️ Steps and Tips 
- Create an EC2 Instance with public IP and HTTP Security group 

- UserData
```
#!/bin/bash

sudo su
yum -y update
yum install ruby -y
wget https://aws-codedeploy-us-east-1.s3.us-east-1.amazonaws.com/latest/install
chmod +x ./install
./install auto
yum install httpd -y
systemctl start httpd

```
- Create Code Commit Repository 
  Add Appspec.yaml file 
  ```
  version: 0.0
  os: linux
  files:
  - source: /index.html
    destination: /var/www/html/

  ```

- And add any index.html page to code commit repository
- Create Code Deployment group 
- Create Code Pipeline 

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
