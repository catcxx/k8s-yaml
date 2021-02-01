kubectl apply -f namespace.yaml
kubectl apply -f metallb.yaml
kubectl create secret generic -n metallb-system memberlist --from-literal=secretkey="$(openssl rand -base64 128)"
kubectl apply -f metallb-config.yaml


https://blog.tekspace.io/setup-kubernetes-cluster-using-k3s-metallb-letsencrypt-on-bare-metal/