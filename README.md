# gitops-k8s-playground

#### I'm practicing GitOps with hands-on labs while I'm reading Implementing GitOps with Kubernetes book written by Pietro Libro and Artem Lajko,published by Packt publishing company.

#### [GitHub](https://github.com/PacktPublishing/Implementing-GitOps-with-Kubernetes#)
#### [Book](https://www.packtpub.com/en-in/product/implementing-gitops-with-kubernetes-9781835884225?utm_source=github&utm_medium=repository&utm_campaign=9781786461629)

#### Tools & techniques covered:
- GitHub
- Kubernetes
- Python
- Kustomize
- Helm
- ArgoCD
- FluxCD

### Flux CD
Bootstrap Flux to repository. Command below connects your Kubernetes cluster to the repository and sets up the necessary components for continuous synchronization:
```
flux bootstrap github \
--owner=[GITHUB_USERNAME] \
--repository=[repository_name] \
--path= ./deployment/base \
--personal
```

To verify how the resources of the flux-system namespace have been deployed within the respective namespace:
```
kubectl get all -n flux-system
```