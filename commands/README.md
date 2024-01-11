# Kubernetes NGINX Deployment

These commands showcase different methods to create NGINX deployments in Kubernetes, providing flexibility and customization options. The YAML manifest can be edited and applied according to specific deployment needs.

Reference (Bookmark this page for your future. It will be very handy):
https://kubernetes.io/docs/reference/kubectl/conventions/

### Create a deployment named "nginx" with the specified image and output the YAML manifest without actually creating the deployment

```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml
```

### Create a deployment named "nginx" with the specified image using the newer recommended command

```bash
kubectl create deployment --image=nginx nginx
```

### Create a deployment named "nginx" with the specified image and output the YAML manifest without actually creating the deployment

```bash
kubectl create deployment --image=nginx nginx --dry-run=client -o yaml
```

### Create a deployment named "nginx" with the specified image, output the YAML manifest, and save it to a file named "nginx-deployment.yaml"

```bash
kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml
```

### Create a deployment using the YAML manifest from the file "nginx-deployment.yaml"

```bash
kubectl create -f nginx-deployment.yaml
```

### Create a deployment named "nginx" with the specified image, set replicas to 4, output the YAML manifest, and save it to a file named "nginx-deployment.yaml"

```bash
kubectl create deployment --image=nginx nginx --replicas=4 --dry-run=client -o yaml > nginx-deployment.yaml
```
