# Microservice - AWS EC2 Deployment

This project is the deployment automation of the non-containerized java microservice: [microservice-java](https://github.com/colinbut/microservice-java.git) to the AWS EC2 instances.

using [Ansible](https://www.ansible.com/) for __deployment automation__

Ansible is an IT automation tool.

Assumes the EC2 instances have been provisioned on AWS as defined in [microservice-aws-ec2-setup](https://github.com/colinbut/microservice-aws-ec2-setup.git)

__To run:__


```bash
ansible-playbook -i hosts deploy_microservicejava.yml --extra-vars="VERSION=1.0.0-SNAPSHOT"
```
