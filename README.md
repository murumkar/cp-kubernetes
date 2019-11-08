# cp-kubernetes
Kubernets Deployment files for a bare metal k8s cluster


## Initialize k8s cluster (single node control plane will do)

`kubeadm init --pod-network-cidr=10.244.0.0/16`

## Create a secret to be used to pull images

`kubectl create secret docker-registry registrypullsecret --docker-server=<private/public DTR> --docker-username=<USERNAME> --docker-password=<PASSWORD/TOKEN> --docker-email=<EMAIL>`

## Make sure we have Persistent Volume Claim created

Update files in storage section (it uses local storage, in the example)

## Deploy containers

Use files in deployment directory
