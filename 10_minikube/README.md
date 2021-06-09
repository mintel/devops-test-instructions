## Kubernetes Tests
### Steps

* Run the setup script
`~/tests/10_minikube/setup.sh`
* Achieve the GOALs
* Run the cleanup script
`~/tmp/tests/10_minikube/cleanup.sh`

### GOALs

#### 1) Fix the pod deployment for busybox

The busybox deployment is currently in an error state 

```
[vagrant@archlinux minikube-bin]$ kubectl get pods                             
NAME                    READY     STATUS                       RESTARTS   AGE  
busybox                 0/1       CreateContainerConfigError   0          50s  
```

Find out what's wrong with it and fix it. 

#### 2) Use Ingress to make default:nginx available externally

The cluster is pre-configured with a default NGINX Ingress controller. 

A sample nginx pod in the default namespace is deployed, but it is not reachable through the ingress using the name "nginx.minikube.test"

```
[vagrant@archlinux minikube-bin]$ kubectl get pods -n default
NAME                    READY     STATUS    RESTARTS   AGE
nginx-7d7cbfc4f-64c6n   1/1       Running   0          4m
[vagrant@archlinux minikube-bin]$ curl nginx.minikube.test
default backend - 404
```

##### Successfully run the following command

* curl nginx.minikube.test

