## Install using the rpm repository (Install rocky9)

Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

## Set up the repository
Install the dnf-plugins-core package (which provides the commands to manage your DNF repositories) and set up the repository.

sudo dnf -y install dnf-plugins-core
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo

## Install Docker Engine

1. Install the Docker packages.
To install the latest version, run:

sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

If prompted to accept the GPG key, verify that the fingerprint matches 060A 61C5 1B55 8A7F 742B 77AA C52F EB6B 621E 9F35, and if so, accept it.
This command installs Docker, but it doesn't start Docker. It also creates a docker group, however, it doesn't add any users to the group by default.

2. Start Docker Engine.

sudo systemctl enable --now docker

This configures the Docker systemd service to start automatically when you boot your system. If you don't want Docker to start automatically, use sudo systemctl start docker instead.

3. Verify that the installation is successful by running the hello-world image:

sudo docker run hello-world

This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.
You have now successfully installed and started Docker Engine
