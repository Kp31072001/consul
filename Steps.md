###In Kube v1.22 
install consul from helm directly with the command :  helm install --values values.yaml consul hashicorp/consul --create-namespace --namespace consul --version "1.0.0"
added a values.yaml file for custom installation.

<br>
###In Kube v1.23 
have to manualy install helm charts and have to install manually by command: helm install consul ./{charts_path} -f values.yaml
and add a emtpy dir after line 148 in teplates/server-statefulset.yaml : 
        - name: data-consul
          emptyDir: {}
