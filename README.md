# Bash joke:


1. Edit the terraform/vars.tf file and add aws_access_key , aws_secret_key and ansible_public_key (control machine public key).
2. Change directory to terraform and run these commands:

    `terraform init`
    
    `terraform plan -out terraform.out`
    
    `terraform apply "terraform.out"`
    
    Those commands will create our AWS infrastructure for our project.
3. Execute terraform show | grep public_ip to detect EC2 public ip and will put it on /etc/ansible/hosts and name it Joke_ec2.
4. Change directory to ansible and launch ansible playbook to configure EC2 instance.

    `ansible-playbook setup_EC2.yaml`


