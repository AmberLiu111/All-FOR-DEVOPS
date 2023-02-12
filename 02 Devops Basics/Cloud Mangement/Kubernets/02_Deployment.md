As a next step in your Kubernetes learning journey, it's important to set up a cluster on your laptop or home lab. This will provide you with a practical environment to experiment and gain hands-on experience with the technology. There are several ways to deploy a Kubernetes cluster on your home lab, and the best option for you will depend on your specific needs and goals. In this article, we have compiled a list of verified methods for deploying a Kubernetes cluster on your home lab. Choose the one that best fits your needs and start building your skills today.
1. Minikube(1 Controller)
Example_Minikube installation on Ubuntu
Step-1: Install docker
https://docs.docker.com/engine/install/ubuntu/
Step-2:Install Minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
Step-3: Manage Minikube
minikube start - driver=docker
minikube config set driver docker
There might be an error when you start your minikube
💣 Exiting due to PROVIDER_DOCKER_NEWGRP
💡 Suggestion: Add your user to the 'docker' group: 'sudo usermod -aG docker $USER && newgrp docker'
'''
minikube dashboard
minikube pause
minikube unpause
minikube stop
minikube config set memory 9001
minikube start -p aged - kubernetes-version=v1.16.1
minikube delete - all
'''
2. AWS(3 Controllers + 3 Workers)
https://github.com/prabhatsharma/kubernetes-the-hard-way-aws/
3. GCP(3 Controllers + 3 Workers)
https://github.com/kelseyhightower/kubernetes-the-hard-way
4. Ubuntu Virtual Machines(1 Controller + 2 workers)
https://www.letscloud.io/community/how-to-install-kubernetesk8s-and-docker-on-ubuntu-2004
5.MicroK8s
6.
