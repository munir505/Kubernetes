# Kubernetres

#### Use this to get vertification code
```bash
gcloud auth login
```
#### This creates the clusters
```bash
gcloud container clusters create <name> --zone <zone>
```
#### Deploys App from docker hub image using yaml file
```bash
kubectl create -f <file_name.yaml>
```
#### See whats running
```bash
kubectl get pods|services|deployment
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

#### To Scale a deployment
```bash
kubectl scale --replicas=<amount> deployment/<application_name> 
```

`Above command make create and terminate pods to scale`

#### To update an image
```bash
kubectl set image deployment <deployment_name> <deployment_name>=<image to update with>
```
##### To check status while updating
`kubectl rollout status deployment python-server`

Make sure in YAML file type is LoadBalancer not ClusterIp if not running in reverse proxy and not using expose command
Python YAML file contains replicating functionality, to replicate the pods for load balancing
Python file lacks expose area, so will need to run the above expose command
