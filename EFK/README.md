`minikube start --memory 5120`


```
helm install elasticsearch elastic/elasticsearch \
  --version=7.17.3 \
  --namespace=logs \
  --create-namespace \
  --set replicas=2 \
  --set resources.requests.memory="300Mi" \
  --set resources.limits.memory="300Mi" \
  -f elastic-values.yaml
```


```helm install fluent-bit fluent/fluent-bit \
  --version 0.20.1 \
  --namespace=logs```


  helm install kibana elastic/kibana \
  --version=7.17.3 \
  --namespace=logs \
  --set resources.requests.memory="600Mi" \
  --set resources.limits.memory="600Mi" \


kubectl run random-logger --image=chentex/random-logger




```helm install elasticsearch elastic/elasticsearch \\n  --version=7.17.3 \\n  --namespace=logs \\n  --create-namespace \\n  --set replicas=2 \\n  --set resources.requests.memory="600Mi" \\n  --set resources.limits.memory="600Mi" \\n  -f elastic-values.yaml```


helm install fluent-bit fluent/fluent-bit \\n  --version 0.20.1 \\n  --namespace=logs

 helm install kibana elastic/kibana \\n  --version=7.17.3 \\n  --namespace=logs \\n  --set resources.requests.memory="600Mi" \\n  --set resources.limits.memory="600Mi" \

kubectl port-forward svc/kibana-kibana -n logs 5601:5601

kubectl run random-logger --image=chentex/random-logger