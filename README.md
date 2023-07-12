## Setup

- Add hashicorp helm chart repository:
    
    `helm repo add hashicorp https://helm.releases.hashicorp.com`
    
- `helm repo update`
- `helm search repo hashicorp/consul`    
- For first/primary cluster, use [consul-server.yaml](./consul-server.yaml)
    `helm install --values consul-server.yaml consul hashicorp/consul --namespace consul`
- Export the federation secret created from first cluster - 
    `kubectl get secret consul-federation --namespace consul --output yaml > consul-federation-secret.yaml`
- For secondary cluser, use [consul-secondary-cluster.yaml](./consul-secondary-cluster.yaml). Ensure to switch kubectl context :)
    `helm install --values consul-secondary-cluster.yaml consul hashicorp/consul --namespace consul`