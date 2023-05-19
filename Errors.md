### Error: INSTALLATION FAILED: failed post-install: timed out waiting for the condition

    Storage class was by default gp2 which needs csi provisioner. To add that to the cluster a new managed policy needed to be attached to our iam role.
    which is out of bound
    
    ## Solution : 
    1. Created a local Storage and set that as the storageClass in the values.yaml
    2. Created emplty directory to keep the consul data 
    3. Removed everything on persistance Claim
    4. in templates in the official chart in server-statefulset.yaml everything was removed after line no. 581
    5. Also in templates folder in server-statefulset.yaml added a emptyDir under Volumes after line no. 148
    
