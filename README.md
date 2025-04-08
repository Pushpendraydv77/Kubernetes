# Kubernetes

install kind and kubectl for local use for kubernetes 

# For AMD64 / x86_64
[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.27.0/kind-linux-amd64
# For ARM64
[ $(uname -m) = aarch64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.27.0/kind-linux-arm64

chmod +x ./kind

sudo mv ./kind /usr/local/bin/kind

to verify run kind or kind --version 

# For kubectl

   curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

sudo apt-get update

sudo apt-get install -y kubectl



RUN CONFIG FILE 

kind create cluster --config cluster.yml --name first-cluster

