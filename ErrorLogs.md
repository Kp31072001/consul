### Error: INSTALLATION FAILED: failed post-install: timed out waiting for the condition

    LAST SEEN   TYPE      REASON                 OBJECT                                              MESSAGE

10m Normal Scheduled pod/consul-connect-injector-6b4585b4bb-lxzdz Successfully assigned consul/consul-connect-injector-6b4585b4bb-lxzdz to ip-192-168-58-0.ec2.internal
10m Warning FailedMount pod/consul-connect-injector-6b4585b4bb-lxzdz MountVolume.SetUp failed for volume "certs" : secret "consul-connect-inject-webhook-cert" not found
9m41s Normal Pulled pod/consul-connect-injector-6b4585b4bb-lxzdz Container image "hashicorp/consul-k8s-control-plane:1.1.1" already present on machine
9m40s Normal Created pod/consul-connect-injector-6b4585b4bb-lxzdz Created container sidecar-injector
10m Normal Started pod/consul-connect-injector-6b4585b4bb-lxzdz Started container sidecar-injector
5m51s Warning Unhealthy pod/consul-connect-injector-6b4585b4bb-lxzdz Startup probe failed: Get "http://192.168.38.139:9445/readyz/ready": dial tcp 192.168.38.139:9445: connect: connection refused
9m41s Normal Killing pod/consul-connect-injector-6b4585b4bb-lxzdz Container sidecar-injector failed startup probe, will be restarted
42s Warning BackOff pod/consul-connect-injector-6b4585b4bb-lxzdz Back-off restarting failed container
10m Normal SuccessfulCreate replicaset/consul-connect-injector-6b4585b4bb Created pod: consul-connect-injector-6b4585b4bb-lxzdz
11m Normal NoPods poddisruptionbudget/consul-connect-injector No matching pods found
10m Normal ScalingReplicaSet deployment/consul-connect-injector Scaled up replica set consul-connect-injector-6b4585b4bb to 1
50s Warning FailedScheduling pod/consul-server-0 running PreBind plugin "VolumeBinding": binding volumes: timed out waiting for the condition
48s Warning FailedScheduling pod/consul-server-0 0/3 nodes are available: 1 node(s) didn't find available persistent volumes to bind, 2 Too many pods. preemption: 0/3 nodes are available: 1 Preemption is not helpful for scheduling, 2 No preemption victims found for incoming pod.
50s Warning FailedScheduling pod/consul-server-1 running PreBind plugin "VolumeBinding": binding volumes: timed out waiting for the condition
5m35s Warning FailedScheduling pod/consul-server-2 0/3 nodes are available: 3 Too many pods. preemption: 0/3 nodes are available: 3 No preemption victims found for incoming pod.
45s Warning FailedScheduling pod/consul-server-acl-init-qsgbq 0/3 nodes are available: 3 Too many pods. preemption: 0/3 nodes are available: 3 No preemption victims found for incoming pod.
10m Normal SuccessfulCreate job/consul-server-acl-init Created pod: consul-server-acl-init-qsgbq
11m Normal NoPods poddisruptionbudget/consul-server No matching pods found
10m Normal SuccessfulCreate statefulset/consul-server create Claim data-consul-consul-server-0 Pod consul-server-0 in StatefulSet consul-server success
10m Normal SuccessfulCreate statefulset/consul-server create Pod consul-server-0 in StatefulSet consul-server successful
10m Normal SuccessfulCreate statefulset/consul-server create Claim data-consul-consul-server-1 Pod consul-server-1 in StatefulSet consul-server success
10m Normal SuccessfulCreate statefulset/consul-server create Pod consul-server-1 in StatefulSet consul-server successful
10m Normal SuccessfulCreate statefulset/consul-server create Claim data-consul-consul-server-2 Pod consul-server-2 in StatefulSet consul-server success
10m Normal SuccessfulCreate statefulset/consul-server create Pod consul-server-2 in StatefulSet consul-server successful
12m Normal Scheduled pod/consul-tls-init-q898l Successfully assigned consul/consul-tls-init-q898l to ip-192-168-58-0.ec2.internal
12m Normal Pulled pod/consul-tls-init-q898l Container image "hashicorp/consul-k8s-control-plane:1.1.1" already present on machine
12m Normal Created pod/consul-tls-init-q898l Created container tls-init
12m Normal Started pod/consul-tls-init-q898l Started container tls-init
12m Normal SuccessfulCreate job/consul-tls-init Created pod: consul-tls-init-q898l
12m Normal Completed job/consul-tls-init Job completed
10m Normal EnsuringLoadBalancer service/consul-ui Ensuring load balancer
10m Normal EnsuredLoadBalancer service/consul-ui Ensured load balancer
10m Normal Scheduled pod/consul-webhook-cert-manager-976969f95-drknz Successfully assigned consul/consul-webhook-cert-manager-976969f95-drknz to ip-192-168-92-242.ec2.internal
10m Normal Pulled pod/consul-webhook-cert-manager-976969f95-drknz Container image "hashicorp/consul-k8s-control-plane:1.1.1" already present on machine
10m Normal Created pod/consul-webhook-cert-manager-976969f95-drknz Created container webhook-cert-manager
10m Normal Started pod/consul-webhook-cert-manager-976969f95-drknz Started container webhook-cert-manager
10m Normal SuccessfulCreate replicaset/consul-webhook-cert-manager-976969f95 Created pod: consul-webhook-cert-manager-976969f95-drknz
10m Normal ScalingReplicaSet deployment/consul-webhook-cert-manager Scaled up replica set consul-webhook-cert-manager-976969f95 to 1
10m Normal WaitForFirstConsumer persistentvolumeclaim/data-consul-consul-server-0 waiting for first consumer to be created before binding
38s Normal ExternalProvisioning persistentvolumeclaim/data-consul-consul-server-0 waiting for a volume to be created, either by external provisioner "ebs.csi.aws.com" or manually created by system administrator
10m Normal WaitForFirstConsumer persistentvolumeclaim/data-consul-consul-server-1 waiting for first consumer to be created before binding
38s Normal ExternalProvisioning persistentvolumeclaim/data-consul-consul-server-1 waiting for a volume to be created, either by external provisioner "ebs.csi.aws.com" or manually created by system administrator
10m Normal WaitForFirstConsumer persistentvolumeclaim/data-consul-consul-server-2 waiting for first consumer to be created before binding
4m38s Normal WaitForPodScheduled persistentvolumeclaim/data-consul-consul-server-2 waiting for pod consul-server-2 to be scheduled
50s Normal ExternalProvisioning persistentvolumeclaim/data-consul-consul-server-2 waiting for a volume to be created, either by external provisioner "ebs.csi.aws.com" or manually created by system administrator
