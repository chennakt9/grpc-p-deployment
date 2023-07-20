## Installation
1. kubectl apply -f stage-ns.yaml
2. kubectl apply -f config
3. kubectl apply -f storage
4. kubectl apply -f db
5. kubectl apply -f apps
6. kubectl apply -f gateway.yaml
7. kubectl apply -f app-vs-dr.yaml
8. kubectl apply -f mTls.yaml

```console
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/prometheus.yaml
```

```console
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/kiali.yaml
```

## Test
```curl
curl --location 'http://127.0.0.1:80/auth/login' \
--header 'Content-Type: application/json' \
--header 'Host:chenna.com' \
--data-raw '{
    "email": "chenna@test.com",
    "password": "1234"
}' -i
```