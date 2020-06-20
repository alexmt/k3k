k3k
===============

## k3s in kubernetes

k3k is a small script that helps creating [k3s](https://github.com/rancher/k3s) clusters in Kubernetes cluster:

* create cluster

```
$ k3k my-cluster --rm                                    (my-context)
creating pod 'my-cluster'
pod/my-cluster created
waiting for pod.
waiting for kube config..
Context "default" renamed to "k3s-my-cluster".
Forwarding from 127.0.0.1:9001 -> 6443
Forwarding from [::1]:9001 -> 6443
```

* open new tab and access cluster using context `k3s-my-cluster` context in default kube config

```
$ kubectl get pods                                    (k3s-my-cluster)
No resources found in default namespace.
```

* ctrl+c in first terminal to get rid of cluster

```
^Cdeleting pod my-cluster
```
