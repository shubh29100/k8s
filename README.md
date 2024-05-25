kubernetes objects 

nodes: worker node

pods: smallest deployable entity of k8s. wrapper around container. every pod has its own uniq ip address.

service: to expose application inside / outside of the cluster.
 - clusterip: to expose application inside the cluster. used for inside communication only.

 - NodePort: expose application outside the cluster using Node Port.can access application by NodeIp:NodePort

 - LoadBalancer: export application outside the cluster on loadbalancer service.

namespace: to devide the k8s cluster. segregate the resource.
 
replicationcontroller: responsible for creating replicas of the pod.used equality base selector. 

replicaset: responsible for creating replicas of pod.used set based selector multiple lable selector 
is possible. multiple lable selector is possible.

deployment: deployment is responsible for implementing deployment stratagies on replicaset

statefulset: responsible for managing the replicas of the stateful pod.

Daemonset: responsile for managing the replicas of the pods on every node 

ConfigMap: to store variables 

secret: to store confidantial variables 

HAP: (Horizontal Pod Autoscaling) 

minimum , maximum , desired capacity, condition,matrix (cpu utilization) 

ingress: it is kubernetes object which holds ingress rules 

helm version 

tar -xzvf helm 

sudo mv linux-amd64/helm /usr/local/bin/helm 

helm install my-release oci://ghcr.io/nginxinc/charts/nginx-ingress --version 1.2.1 

kubectl edit ingress 




