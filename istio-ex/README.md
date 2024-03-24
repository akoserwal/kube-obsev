 minikube start --memory=16384 --cpus=4

 istioctl install --set profile=demo

 git clone https://github.com/istio/istio
 
 
 Follow: https://istio.io/latest/docs/setup/getting-started/#bookinfo


 kubectl create namespace test
 
 kubectl label namespace test istio-injection=enabled

 kubectl apply -f samples/bookinfo/platform/kube/bookinfo.yaml -n test

 Install addons

 kubectl apply -f samples/addons


Access to gateway

 kubectl port-forward svc/istio-ingressgateway -n istio-system 8001:80

Lauche kiali dashboard

 istioctl dashboard kiali

Run to generate load

 for i in $(seq 1 1000); do
    response=$(curl -s "http://127.0.0.1:8001/productpage")
    echo "Response $i: $response"
done