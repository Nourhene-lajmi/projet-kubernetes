# Projet Kubernetes : orchestration des conteneurs

## Scénario
Une petite application web, **mon-app**, est déployée sur Minikube.
On la lance en 3 copies, on la rend accessible, on la configure sans
toucher au code, puis on la fait évoluer automatiquement selon la charge.

## Les 5 parties
1. Architecture du cluster
2. Pods et Deployments (`deployment.yaml`)
3. Services et réseau (`service.yaml`)
4. ConfigMaps et Secrets (`configmap.yaml`)
5. Autoscaling HPA (`hpa.yaml`)

## Lancer la démo
    minikube start
    minikube addons enable metrics-server
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    kubectl apply -f configmap.yaml
    kubectl apply -f hpa.yaml
    kubectl get pods
    kubectl get hpa -w

