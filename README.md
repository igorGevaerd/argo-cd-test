# argo-cd-test

This is an exemple of the usage of argo cluster bootstrap to bring up several resources, using helm or kustomize.
![image](https://user-images.githubusercontent.com/18078161/116833221-5eda4280-ab8e-11eb-97fa-ae3998be640c.png)


References:

- [App of apps/cluster bootstrapping](https://argoproj.github.io/argo-cd/operator-manual/cluster-bootstrapping/)
- [Declarative setup](https://argoproj.github.io/argo-cd/operator-manual/declarative-setup/#applications)

Examples used:
- [Kustomize (helloworld and wordpress)](https://github.com/kubernetes-sigs/kustomize/tree/master/examples)
- [Helm charts(grafana, loki, prometheus, promtail, ...)](https://artifacthub.io/packages/helm/grafana/grafana)
