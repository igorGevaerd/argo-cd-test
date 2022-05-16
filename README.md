# argo-cd-test

This is an exemple of the usage of argo cluster bootstrap to bring up several resources, using helm or kustomize.
![image](https://user-images.githubusercontent.com/18078161/168565447-f4e37554-571c-45c3-856a-6c8228a07769.png)
![image](https://user-images.githubusercontent.com/18078161/168565526-3dd09d47-e924-41ae-971c-9d3e44154de6.png)



From the cluster perspective:
```sh
$ kubectl get pods -n tools 
NAME                                                READY   STATUS    RESTARTS      AGE
argocd-applicationset-controller-7754cb74bf-zx8nm   1/1     Running   1 (16m ago)   9h
argocd-notifications-controller-6c9474bff-2hdbv     1/1     Running   1 (16m ago)   9h
argocd-application-controller-0                     1/1     Running   1 (16m ago)   9h
argocd-repo-server-6fbdc7845f-5trlw                 1/1     Running   1 (16m ago)   9h
argocd-server-6fd6f6cdfb-8plml                      1/1     Running   1 (16m ago)   9h
argocd-redis-7684949647-2stsv                       1/1     Running   1 (16m ago)   9h
prometheus-node-exporter-g9ljd                      1/1     Running   0             2m44s
prometheus-kube-state-metrics-6c44ff7fb6-5v64b      1/1     Running   0             2m44s
prometheus-alertmanager-c9684865c-q76hd             2/2     Running   0             2m44s
prometheus-server-7dbf77c965-z6blf                  2/2     Running   0             2m44s
```


References:

- [App of apps/cluster bootstrapping](https://argoproj.github.io/argo-cd/operator-manual/cluster-bootstrapping/)
- [Declarative setup](https://argoproj.github.io/argo-cd/operator-manual/declarative-setup/#applications)

Examples used:
- [Kustomize (helloworld and wordpress)](https://github.com/kubernetes-sigs/kustomize/tree/master/examples)
- [Helm charts(grafana, loki, prometheus, promtail, ...)](https://artifacthub.io/packages/helm/grafana/grafana)
