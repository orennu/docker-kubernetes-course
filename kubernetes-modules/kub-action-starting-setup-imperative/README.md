# Commands

## Table of Contents

- [start minikube cluster](#start-the-minikube-cluster)
- [get minikube cluster status](#get-minikube-cluster-status)
- [launch minikube dashboard](#launch-kubernetes-dashboard-within-minikube-cluster)
- [create a deployment](#create-a-deployment)
- [get deployments](#get-deployments)
- [get pods](#get-pods)
- [delete a deployment](#delete-a-deployment)
- [expose deployment through a service](#expose-deployment-through-service)
- [get services](#get-services)
- [minikube return service url](#return-url-to-connect-to-a-service-in-minikube-cluster)
- [scale a deployment](#scale-a-deployment)
- [update deployment image](#update-deployment-image)
- [get deployment rollout status](#get-deployment-rollout-status)
- [rollback deployment to previous revision](#rollback-a-deployment-to-previous-one)
- [get deployment rollout history](#get-deployment-rollout-history)
- [get deployment rollout revision details](#get-deployment-rollout-revision-details)
- [rollback deployment to specific revision](#rollback-a-deployment-to-specific-revision)
- [delete a service](#delete-a-service)

## Start the minikube cluster

```
minikube start
```

[Back to top](#commands)

## Get minikube cluster status

```
minikube status
```

[Back to top](#commands)

## Launch kubernetes dashboard within minikube cluster

```
minikube dashboard
```

[Back to top](#commands)

## Create a deployment

```
kubectl create deployment <deployment name> --image=<image name>
kubectl create deployment node-first-app --image=orennu/kub-first-app
```

[Back to top](#commands)

## Get deployments

```
kubectl get deployments
```

[Back to top](#commands)

## Get pods

```
kubectl get pods
```

[Back to top](#commands)

## Delete a deployment

```
kubectl delete deployment <deployment name>
kubectl delete deployment node-first-app
```

[Back to top](#commands)

## Expose deployment through service

```
kubectl expose deployment <deployment name> --type=<service type> --port=<port>
kubectl expose deployment node-first-app --type=LoadBalancer --port=8080
```

[Back to top](#commands)

## Get services

```
kubectl get services
```

[Back to top](#commands)

## Return url to connect to a service in minikube cluster

```
minikube service <service name>
minikube service node-first-app
```

[Back to top](#commands)

## Scale a deployment

```
kubectl scale deployment/<deployment name> --replicas=<number of replicas>
kubectl scale deployment/node-first-app --replicas=3
```

[Back to top](#commands)

## Update deployment image

```
kubectl set image deployment/<deployment name> <container name>=<image name>
kubectl set image deployment/node-first-app kub-first-app=orennu/kub-first-app:2
```

[Back to top](#commands)

## Get deployment rollout status

```
kubectl rollout status deployment/<deployment name>
kubectl rollout status deployment/node-first-app
```

[Back to top](#commands)

## Rollback a deployment to previous one

```
kubectl rollout undo deployment/<deployment name>
kubectl rollout undo deployment/node-first-app
```

[Back to top](#commands)

## Get deployment rollout history

```
kubectl rollout history deployment/<deployment name>
kubectl rollout history deployment/node-first-app
```

[Back to top](#commands)

## Get deployment rollout revision details

```
kubectl rollout history deployment/<deployment name> --revision=<revision number>
kubectl rollout history deployment/node-first-app --revision=4
```

[Back to top](#commands)

## Rollback a deployment to specific revision

```
kubectl rollout undo deployment/<deployment name> --to-revision=<revision number>
kubectl rollout undo deployment/node-first-app --to-revision=4
```

[Back to top](#commands)

## Delete a service

```
kubectl delete service <service name>
kubectl delete service node-first-app
```

[Back to top](#commands)
