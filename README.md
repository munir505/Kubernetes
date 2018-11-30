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
#### To open application put `<ip address>:port` in URL
Make sure in YAML file type is LoadBalancer not ClusterIp if not running in reverse proxy and not using expose command
