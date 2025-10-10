
This project aims to automate the build and push of a Docker image to AWS ECR, and deploy the container to AWS EC2, utilising a CI/CD Git Action workflow. 
One of the requirements is to set up a reverse proxy (HAProxy ) with SSL (Let’s Encrypt) and connect it to a domain.

Prerequisites on AWS

1. ECR Repository: An ECR repository named nedrone must exist in the specified AWS account and region.
2. EC2 IAM Role: The EC2 instance must have an IAM Role attached with a policy that grants permission to pull images from the ECR repository (e.g., AmazonEC2ContainerRegistryReadOnly).
3. Docker on EC2: Docker must be installed and running on the target EC2 instance.
4. Security Group: The EC2 instance's security group must allow inbound traffic on port 22 (SSH) from the GitHub Actions runner's IP ranges, and port 443 (HTTPS) from your intended users (e.g., 0.0.0.0/0).

![workflow diagram](image.png)
