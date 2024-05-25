## Developing-Cloud-Native-Applications

### VirtualBox

Install VirtualBox(https://www.virtualbox.org/wiki/Downloads)

    # Run the command prompt in Windows
    C:\Program Files\Oracle\VirtualBox
    VBoxManage setextradata global GUI/Input/HostKeyCombination 162,164
    VBoxManage natnetwork add --netname NatNetwork --network "192.168.15.0/24" --enable --dhcp off --port-forward-4 "ssh:tcp:[]:25:[192.168.15.30]:22"

Import VirtuaBox Image(ova)

### Visual Stdio Code & Extensions

Install Visual Studio Code(https://code.visualstudio.com/download)

    WSL(or Remote - SSH) - Extension

    # Download & Copy id_rsa to C:\Users\사용자\.ssh
    # Run the command prompt in Windows
    
        
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

    $ sudo apt install zip
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

https://docs.docker.com/engine/install/linux-postinstall/

    $ sudo chmod 666 /var/run/docker.sock
    $ docker login
    $ docker pull ubuntu:22.04

### Minikube

https://minikube.sigs.k8s.io/docs/start/

    $ minikube start --driver=docker
    $ minikube config set driver docker

### Kubectl

https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

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

