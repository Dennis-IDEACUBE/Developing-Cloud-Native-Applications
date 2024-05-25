## Developing-Cloud-Native-Applications

### VirtualBox

Install VirtualBox(https://www.virtualbox.org/wiki/Downloads)

    # Run the command prompt in Windows
    C:\Program Files\Oracle\VirtualBox
    VBoxManage setextradata global GUI/Input/HostKeyCombination 162,164
    VBoxManage natnetwork add --netname NatNetwork --network "192.168.15.0/24" --enable --dhcp off --port-forward-4 "ssh:tcp:[]:25:[192.168.15.30]:22"

Import VirtuaBox Image(ova) - ova image distributed in class

### Visual Stdio Code & Extensions

Install Visual Studio Code(https://code.visualstudio.com/download)

    WSL(or Remote - SSH) - Extension

    # Download & Copy id_rsa to C:\Users\사용자\.ssh
    # Run the command prompt in Windows
    cd C:\Users\사용자\.ssh
    dir
    # Check whether the config file exists
    # Setting SSH Private Key
    # filename : config (C:\Users\사용자\.ssh)
    ############################################
    Host CloudNativeDev
    HostName localhost
    Port 22
    User user1
    IdentityFile C:\Users\사용자\.ssh\id_rsa
    ###########################################

    # After jdk 17
    Extension Pack for Java - Extension
    Gradle for Java - Extension
    Spring Boot Extension Pack - Extension

### Init & Java

    $ sudo apt install zip nano vim git
    $ curl -s "https://get.sdkman.io" | bash
    $ sdk list java
    $ sdk install java 17.0.3-tem
    $ sdk default java 17.0.3-tem
    $ java --version
    $ sdk use java 17.0.3-tem
    $ sdk current java
    $ nano ~/.bashrc
    export JAVA_HOME=/home/user1/.sdkman/candidates/java/current

### Docker

https://docs.docker.com/engine/install/ubuntu/

    # Add Docker's official GPG key:
    sudo apt-get update
    sudo apt-get install ca-certificates curl
    sudo install -m 0755 -d /etc/apt/keyrings
    sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
    sudo chmod a+r /etc/apt/keyrings/docker.asc

    # Add the repository to Apt sources:
    echo \
      "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
      $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
      sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    sudo apt-get update

    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    sudo docker run hello-world

https://docs.docker.com/engine/install/linux-postinstall/

    $ sudo groupadd docker
    $ sudo usermod -aG docker $USER
    # Logout -> Login
    $ newgrp docker
    $ docker run hello-world

    # Security Issues
    $ sudo chmod 666 /var/run/docker.sock
    
    $ docker login
    $ docker pull ubuntu:22.04

### Minikube

https://minikube.sigs.k8s.io/docs/start/

    $ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    $ sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
    
    $ minikube start --driver=docker
    $ minikube config set driver docker

### Kubectl

https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

    $ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    $ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
    
    $ kubectl get nodes

### Httpie

https://httpie.io/

https://httpie.io/docs/cli/debian-and-ubuntu

    $ http pie.dev/get

### grype 

https://github.com/anchore/grype

### Tilt

https://docs.tilt.dev/install.html

### Octant

https://reference.octant.dev/?path=/story/docs-intro--page

### Kubeval

https://github.com/instrumenta/kubeval(deprecated)

https://github.com/yannh/kubeconform?tab=readme-ov-file

### Knative

https://knative.dev/docs/install/quickstart-install/#before-you-begin

### Sources

https://github.com/ThomasVitale/cloud-native-spring-in-action/tree/sb-3-main

