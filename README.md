# How to check expense app details in mysql server
```
kubectl get pods -n expense
```
```
kubectl exec -it mysql-0 -n expense -- sh
```
```
mysql -h mysql -uroot -pExpenseApp@1
```
```
kubectl exec -it nginx-app -- bash
cd /usr/share/nginx/html/
rm -f index.html
echo "<h1>Welcome to Nginx Home page</h1>" > index.html
```
(OR)
```
kubectl exec -it nginx-app -- bash
rm -f /usr/share/nginx/html/index.html
echo "<h1>Welcome to Nginx Home page</h1>" > /usr/share/nginx/html/index.html
```
* Note: if we delete pods to apply new changes, need to destroy pods and restart it. New changes never applied bec in backend deployment works, the delete the deployment and create it again.
```
kubectl delete deployment hello-world
```