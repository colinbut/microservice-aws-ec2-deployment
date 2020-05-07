# Microservice - AWS EC2 Deployment

This project is the deployment automation of the non-containerized java microservice: [microservice-java](https://github.com/colinbut/microservice-java.git) to the AWS EC2 instances.

![image here](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/microservice-aws-ec2-deployment.png)

using [Ansible](https://www.ansible.com/) for __deployment automation__

Ansible is an IT automation tool.

Assumes the EC2 instances have been provisioned on AWS as defined in [microservice-aws-ec2-setup](https://github.com/colinbut/microservice-aws-ec2-setup.git)


## Deploy microservice-java

__To fetch artifact from Nexus:__

e.g.
```bash
ansible-playbook -i hosts deploy_microservicejava.yml --extra-vars="VERSION=1.0.0-SNAPSHOT, REPOSITORY=NEXUS"
```

__To fetch artifact from Artifactory:__

For getting artifact from JFrog Artifactory, requires an additional variable (the API KEY) to be passed in for authenticating with Artifactory's REST API.

e.g. 
```bash
ansible-playbook -i hosts deploy_microservicejava.yml --extra-vars="VERSION=1.0.0-SNAPSHOT, REPOSITORY=ARTIFACTORY, ARTIFACTORY_API_KEY=[your API KEY]"
```

## Deploy microservice-nodejs

And similarly for microservice nodejs

```bash
ansible-playbook -i hosts deploy_microservicenodejs.yml --extra-vars="...."
```

See section above.

