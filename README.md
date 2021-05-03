# argo-cd-test

This is an exemple of the usage of argo cluster bootstrap to bring up several resources, using helm or kustomize.
![image](https://user-images.githubusercontent.com/18078161/116833221-5eda4280-ab8e-11eb-97fa-ae3998be640c.png)

From the cluster perspective:
```
kgp -A      
NAMESPACE     NAME                                                     READY   STATUS    RESTARTS   AGE
default       demo-mysql-8c4bc5464-bcwxk                               1/1     Running   0          2m53s
default       demo-wordpress-65cc4b8947-ccb64                          1/1     Running   0          2m53s
default       redis-6468bf6c84-85slz                                   2/2     Running   24         14d
default       the-deployment-75b9678fbb-7bwq8                          1/1     Running   0          13m
default       the-deployment-75b9678fbb-9qvx2                          1/1     Running   0          13m
default       the-deployment-75b9678fbb-9vc28                          1/1     Running   0          13m
kube-system   coredns-f9fd979d6-6jlqh                                  1/1     Running   11         11d
kube-system   coredns-f9fd979d6-dk2v5                                  1/1     Running   11         11d
kube-system   etcd-docker-desktop                                      1/1     Running   14         15d
kube-system   kube-apiserver-docker-desktop                            1/1     Running   14         15d
kube-system   kube-controller-manager-docker-desktop                   1/1     Running   14         15d
kube-system   kube-proxy-z76qc                                         1/1     Running   14         15d
kube-system   kube-scheduler-docker-desktop                            1/1     Running   15         15d
kube-system   storage-provisioner                                      1/1     Running   19         15d
kube-system   vpnkit-controller                                        1/1     Running   14         15d
monitoring    grafana-57868dd8f-69lqh                                  1/1     Running   0          123m
monitoring    loki-0                                                   1/1     Running   0          87m
monitoring    prometheus-alertmanager-ccf8f68cd-qmf75                  2/2     Running   0          150m
monitoring    prometheus-kube-state-metrics-685b975bb7-npcb5           1/1     Running   0          150m
monitoring    prometheus-node-exporter-lgzs8                           1/1     Running   0          141m
monitoring    prometheus-pushgateway-74cb65b858-4cvh2                  1/1     Running   0          150m
monitoring    prometheus-server-d9fb67455-96p8z                        2/2     Running   0          150m
monitoring    promtail-89j7x                                           1/1     Running   0          114m
tools         argo-cd-argocd-application-controller-578fddb5b5-s2mv4   1/1     Running   0          9h
tools         argo-cd-argocd-redis-5bf78f5b66-j87fx                    1/1     Running   0          9h
tools         argo-cd-argocd-repo-server-59454f7d67-pmsc8              1/1     Running   0          9h
tools         argo-cd-argocd-server-67598dbb97-zz2bx                   1/1     Running   0          9h
```


References:

- [App of apps/cluster bootstrapping](https://argoproj.github.io/argo-cd/operator-manual/cluster-bootstrapping/)
- [Declarative setup](https://argoproj.github.io/argo-cd/operator-manual/declarative-setup/#applications)

Examples used:
- [Kustomize (helloworld and wordpress)](https://github.com/kubernetes-sigs/kustomize/tree/master/examples)
- [Helm charts(grafana, loki, prometheus, promtail, ...)](https://artifacthub.io/packages/helm/grafana/grafana)
