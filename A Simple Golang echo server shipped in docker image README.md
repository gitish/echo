## Deployment

### Build
```
docker build -t echo-server .
docker tag echo-server olivernadj/echo-server
docker push olivernadj/echo-server
```

### Run
```
docker pull olivernadj/echo-server && \
docker stop echo-server-container && \
docker rm echo-server-container && \
docker run --name=echo-server-container -p 8080:8080 -d olivernadj/echo-server
```

### Dev
```
docker build -t echo-server .
docker run --name echo-server-container -p 8080:8080 --rm -it echo-server
```

### kubectl
```
kubectl delete --all pods &&   kubectl delete --all deployments &&   kubectl delete --all services
kubectl create -f echo-server.yaml,echo-server-service.yaml
```





