##Created Cluster
eksctl create cluster --name consul-test-cluster --version 1.25 --region us-east-1 --zones us-east-1a,us-east1b,us-east-1c --nodegroup-name cls-nodes --node-type t2.micro --nodes 3
