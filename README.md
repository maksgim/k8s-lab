# k8s-lab

Практика с Kubernetes на локальном кластере kind (Debian VM, VirtualBox).

## Состав
- `kind-cluster.yaml`: кластер из 1 control-plane и 2 worker-нод
- `app.yaml`: Deployment (3 реплики nginx) и Service (NodePort 30080)

## Запуск
    kind create cluster --config kind-cluster.yaml
    kubectl apply -f app.yaml
    curl localhost:30080

## Удаление
    kind delete cluster --name lab
