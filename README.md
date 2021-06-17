# ngp-helm
install
```
helm install <realase-name> .
```
```
roothosts@ubnt-03Andrey:~/helm-asferro/NGPchart$ kubectl get all -n web-dev
NAME                             READY   STATUS    RESTARTS   AGE
pod/nginx-dev-7cbd467756-bmthp   2/2     Running   2          59m

NAME                TYPE       CLUSTER-IP       EXTERNAL-IP   PORT(S)                                      AGE
service/nginx-dev   NodePort   10.101.151.225   <none>        80:32640/TCP,8080:32001/TCP,9113:32078/TCP   59m

NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/nginx-dev   1/1     1            1           59m

NAME                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/nginx-dev-7cbd467756   1         1         1       59m
```
```
roothosts@ubnt-03Andrey:~/helm-asferro/NGPchart$ kubectl get all -n monitoring-dev
NAME                                         READY   STATUS    RESTARTS   AGE
pod/grafana-5c658f45d8-jmptt                 1/1     Running   0          59m
pod/prometheus-deployment-67cc87fd4d-xhlm8   1/1     Running   0          59m

NAME                         TYPE       CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
service/grafana              NodePort   10.96.245.4      <none>        3000:32000/TCP   59m
service/prometheus-service   NodePort   10.107.150.134   <none>        8080:30000/TCP   59m

NAME                                    READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/grafana                 1/1     1            1           59m
deployment.apps/prometheus-deployment   1/1     1            1           59m

NAME                                               DESIRED   CURRENT   READY   AGE
replicaset.apps/grafana-5c658f45d8                 1         1         1       59m
replicaset.apps/prometheus-deployment-67cc87fd4d   1         1         1       59m
```
grafana dashboard:
![image](https://user-images.githubusercontent.com/34095929/122376529-e75d4880-cf6c-11eb-99cb-6114eb032474.png)
