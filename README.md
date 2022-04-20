# NGINX Default backend instance to use for ingress validation

This is used to test ingress related things so I know for sure it is routing properly.

Used in combination with the "[Site A](https://github.com/vincepower/nginx-site-a/)" and "[Site B](https://github.com/vincepower/nginx-site-a/)" instances.

I will rebuild every now and then so NGINX is up to date.

Obviously this needs NGINX Ingress deployed. You can find the latest file for the platform you are using in [NGINX Ingress documentation on Kubernetes.io](https://kubernetes.github.io/ingress-nginx/deploy/). I used the one for Digital Ocean:
```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/do/1.22/deploy.yaml
```


This requires a default backend to be running, so this project creates that default backend using:
```
kubectl apply -f https://raw.githubusercontent.com/vincepower/nginx-default-backend/main/deploy.yml`
```
