# Argocd
This repo holds the deployment manifests templates that are used to deploy the application 

## What is Argo CD
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

Why Argo CD?
Github as the source of truth for templates
ArgoCD as the deployment manager. Application definitions, configurations, and environments should be declarative and version controlled.
Application deployment and lifecycle management should be automated, auditable, and easy to understand.

Argo CD is part of the Argo CNCF incubating project and allows for declarative GitOps and continuous delivery of your applications and configurations. 
It is built for Kubernetes and continuously syncs your Git manifests with your cluster state.

#Installation Guidelines
kubectl create ns argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get pods -n argocd


#Password is randonly created with this command in kubernetes
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d


