# virtVNC

[noVNC](https://github.com/novnc/noVNC) for [kubevirt](https://github.com/kubevirt/kubevirt)

## Deploy

```bash
kubectl apply -f /virtvnc.yaml
```

## make image
docker build -t virtvnv:v1.0 .

## Usage

1. Get node port of ```virtvnc``` service
```bash
kubectl get svc -n kubevirt virtvnc
```
2. Visit following url in browser
```
http://NODEIP:NODEPORT/
```

If you want manager virtual machines in other namespace, you can specify namespace using query param namespace like following:
```
http://NODEIP:NODEPORT/?namespace=test
```
![virtVNC](https://github.com/wavezhang/virtVNC/blob/master/virtvnc.gif?raw=true)
