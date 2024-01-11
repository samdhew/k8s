# Basic Kubernetes Commands

This is a list of basic day-to-day `kubectl` commands for working with Kubernetes.

## Get Information

- Get cluster info: `kubectl cluster-info`
- Get nodes: `kubectl get nodes`
- Get pods: `kubectl get pods`
- Get services: `kubectl get services`
- Get deployments: `kubectl get deployments`

## Create and Apply

- Apply a configuration to a resource: `kubectl apply -f <filename>`
- Create a resource: `kubectl create -f <filename>`

## Describe

- Describe a resource: `kubectl describe <resource_type> <resource_name>`
- Describe a pod with more details: `kubectl describe pod <pod_name>`

## Logs and Exec

- View pod logs: `kubectl logs <pod_name>`
- Execute command in a pod: `kubectl exec -it <pod_name> -- <command>`

## Edit Resources

- Edit a resource: `kubectl edit <resource_type> <resource_name>`

## Delete Resources

- Delete a resource: `kubectl delete <resource_type> <resource_name>`

## Scaling

- Scale a deployment: `kubectl scale deployment <deployment_name> --replicas=<replica_count>`

## Port Forwarding

- Forward local port to a pod: `kubectl port-forward <pod_name> <local_port>:<pod_port>`

## Get All Resources

- Get all resources in the namespace: `kubectl get all`

## Namespace

- List namespaces: `kubectl get namespaces`
- Switch to a namespace: `kubectl config set-context --current --namespace=<namespace>`

## Context and Configuration

- List contexts: `kubectl config get-contexts`
- Use a specific context: `kubectl config use-context <context_name>`
