

kubeadm init --apiserver-advertise-address $(hostname -i)

kubeadm join 192.168.0.23:6443 --token x6tu3r.1g3pru575fa27cg0 \
    --discovery-token-ca-cert-hash sha256:eb710d181d494a4a816caad753264647cf04ad5915189555f62756b84ca536f3  


kubectl apply -n kube-system -f \
    "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 |tr -d '\n')"

kubectl get no
kubectl get nodes -o wide

kubectl get no -o yaml







