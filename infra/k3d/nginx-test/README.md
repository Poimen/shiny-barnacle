## Nginx Test

Exposing services test for k3d

## Cluster creation

> k3d cluster create -p "9090:80@loadbalancer"

## Nginx deployment

> kubectl create deployment nginx --image=nginx

## Nginx service

> kubectl create service clusterip nginx --tcp=80:80

## Ingress object

> kubectl apply -f nginx-test.yaml

### Test

> curl localhost:9090

The output should be:
```html
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```