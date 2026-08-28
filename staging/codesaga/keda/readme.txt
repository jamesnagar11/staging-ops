helm repo add kedacore https://kedacore.github.io/charts
helm repo update

helm install keda kedacore/keda --namespace keda --create-namespace

### Order of yaml files to be executed when manually applying
- prom.yaml
- bulk.yaml
- engine.yaml