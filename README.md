# devfest-pune-23

- Install HELM
- Install nginx-controller
- helm repo add nginx https://kubernetes.github.io/ingress-nginx
- helm repo update nginx
- helm search repo nginx
- helm install nginx nginx/ingress-nginx
- kubectl get ValidatingWebhookConfiguration -A
- kubectl delete -A ValidatingWebhookConfiguration nginx-ingress-nginx-admission
- kubectl get pods
- kubectl create ns dev
- kubectl create ns sit