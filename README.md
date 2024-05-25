## Developing-Cloud-Native-Applications

### Visual Stdio Code & Extensions

Install Visual Studio Code(https://code.visualstudio.com/download)

    WSL
    - After jdk 17
    Extension Pack for Java
    Gradle for Java
    Spring Boot Extension Pack


### Init & Java

    $ sudo apt install zip
    $ curl -s "https://get.sdkman.io" | bash
    $ sdk list java
    $ sdk install java 17.0.3-tem
    $ sdk default java 17.0.3-tem
    $ java --version
    $ sdk use java 17.0.3-tem
    $ sdk current java
    $ sudo vi /etc/.bashrc
    export JAVA_HOME-/home/user1/.sdkman/candidates/java/current

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

