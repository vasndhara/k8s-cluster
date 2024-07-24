# k8s-cluster
create 2 vms for the cluster

bas instances create master  worker-1 --create-disk=auto-delete=yes,boot=yes,image=projects/ubuntu-os-cloud/global/images/ubuntu-1804-bionic-v20211115 --zone us-central1-a --machine-type=e2-medium

 To Create a User in Ubuntu follow the below steps: (Both master and worker)
``

Switch to newly created user:

su - username

 Enable SSH Password Authentication
 
#To enable SSH password authentication, you must SSH in as root to edit this file:

/etc/ssh/sshd_config

PasswordAuthentication yes

sudo service ssh restart

1.Docker installation

## Step 1: Set up the Repository

To set up the Docker repository, follow these steps:

bash

# Update package lists

sudo apt-get update

# Install necessary packages for repository management

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release -y




