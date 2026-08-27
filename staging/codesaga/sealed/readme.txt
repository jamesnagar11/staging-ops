helm repo add sealed-secrets https://bitnami.github.io/sealed-secrets
helm repo update

helm install sealed-secrets sealed-secrets/sealed-secrets --namespace kube-system --set-string fullnameOverride=sealed-secrets-controller

----
install kubeseal in local machine not here in cluster

----

example to create sealed secrets

kubeseal --format yaml < secret.yaml > sealed-secret.yaml