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

    ## Step 2: Add Docker's Official GPG Key
    
Add Docker's official GPG key to authenticate packages:
bash

# Create a directory for Docker keyrings

sudo mkdir -p /etc/apt/keyrings

# Download and add Docker's GPG key to the keyring

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg


## Step 3: Set up the Repository

Use the following command to set up the Docker repository:

bash
# Add Docker repository to sources list

echo \
  "deb [arch=$(dpkg --print-architecture) signed-
  by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

## Step 4: Install Docker Engine
To install Docker Engine, follow these steps:
bash
# Update package lists
sudo apt-get update

# Install Docker Engine
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y





