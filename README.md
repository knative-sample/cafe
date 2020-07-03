## CAFE： 咖啡馆

## 部署 coffee 服务

```
kubectl apply -f ksvc-coffee.yaml
```

## 访问服务

```
curl  -H "host: coffee.default.example.com" http://60.205.xxx.xxx
```

## 服务压测

```
hey -z 30s -c 90 --host "coffee.default.example.com" "http://60.205.xxx.xxx/?sleep=100"
```