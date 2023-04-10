### Created Cluster </br>
  eksctl create cluster --name consul-test-cluster --version 1.25 --region us-east-1 --zones us-east-1a,us-east1b,us-east-1c --nodegroup-name cls-nodes --node-type t2.micro --nodes 3
### Configured kubectl to talk to the cluster
  aws eks update-kubeconfig --region <region where you deployed your cluster> --name <your cluster name>
### verify if we are connected to the ccluster
  kubectl cluster-info
### installing consul in the cluster
  helm repo add hashicorp https://helm.releases.hashicorp.com
