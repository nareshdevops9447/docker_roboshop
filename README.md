# docker_roboshop
roboshop
# Install docker in centos 8

# Uninstall old versions 

sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
# Install using the rpm repository
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

# Install Docker Engine
sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Start Docker
sudo systemctl start docker
sudo systemctl enable docker


# Linux post-installation steps for Docker Engine

Manage Docker as a non-root user

Create the docker group.

sudo groupadd docker
Add your user to the docker group.
sudo usermod -aG docker $USER

# adduser
sudo adduser $user
sudo passwd $user
# Step 2: Grant Root Privileges to the User
visudo
## Allow root to run any commands anywhere
root ALL=(ALL) ALL
$user ALL=(ALL) ALL
