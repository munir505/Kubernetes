# Kubernetres

#### Use this to get vertification code
```bash
gcloud auth login
```
#### Run as sudo in order to install kubectl
```bash
sudo ./install_kubectl
```
#### Exposes Deployment To allow to connect
```bash
kubectl expose deployment <deployment_name> --type LoadBalancer --port <application_port>
```
#### To Delete Deployments and services
```bash
kubectl delete deployment,services <name> 
```
#### To open application put `<ip address>:port` in URL

Make sure in YAML file type is LoadBalancer not ClusterIp if not running in reverse proxy and not using expose command
Python YAML file contains replicating functionality, to replicate the pods for load balancing
Python file lacks expose area, so will need to run the above expose command
