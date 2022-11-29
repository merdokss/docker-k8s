## Praca z Kubernetes CLI

### Cluster

- `kubectl get nodes`
- `kubectl cluster-info`
- `kubectl version`
- `kubectl config view`
- `kubectl api-resources`
- `kubectl get all --all-namespaces` 
- `kubectl get namespaces`

### Pod, Jobs, Services
- `kubectl get pods` - lista podów
- `kubectl logs my-pod ` - logi z danego poda
- `kubectl get pod my-pod -o yaml` - szczegółowy opis definicji poda wraz ze statusami 
- `kubectl describe my-pod` - opis danego poda, szczegółowe informację dotyczące poda
- `kubectl port-forward my-pod 5000:6000` - wystawienie komunikacji na zewnątrz - sprawdzanie poda 
- `kubectl port-forward svc/my-service-clusterip 8888:88` - wystawienie komunikacji na zewnątrz - sprawdzanie serwisu clusterIP
- `kubectl exec -it my-pod -- ls` - uruchomienie kolejnego procesu w podzie
- `kubectl exec my-pod -c my-container -- ls` - uruchomienie kolejnego procesu w podzie w dedykowanym kontenerze
- `kubectl top pod POD_NAME --containers` - utylizacja zasobów dla danego poda

### Deployment
- `kubectl scale --replicas=3 deployment/nginx`
- `kubectl autoscale deployment/nginx --min=2 --max=6 --cpu-percent=80`
- `kubectl set image deploy/nginx nginx=nginx:1.18-alpine --record=true`
- `kubectl set resources deploy/nginx -c=nginx --limits=cpu=200m,memory=512Mi`
- `kubectl rollout history deploy/nginx`
- `kubectl rollout status deploy/nginx`
- `kubectl rollout undo deploy/nginx`
- `kubectl rollout undo deploy/nginx --to-revision=2`

### Secrets
- `kubectl create secret docker-registry external-registry --docker-server=........ --docker-username=....... --docker-password=....... --docker-email=.......`
- `kubectl create secret generic mysql --from-literal=root-password='ir2pYdwKea'`

###  ConfigMaps
- `kubectl create configmap httpd-conf --from-file=Kubernetes/Objects/05-SecretsConfigMaps/httpd.conf`


### Materiały i linki

- Kubernetes - CheatSheet - https://kubernetes.io/docs/reference/kubectl/cheatsheet/
- Deployment Strategy - https://spot.io/resources/kubernetes-autoscaling/5-kubernetes-deployment-strategies-roll-out-like-the-pros/
- Secrets - https://medium.com/avmconsulting-blog/secrets-management-in-kubernetes-378cbf8171d0
- Kubernetes Storage Class - https://kubernetes.io/docs/concepts/storage/storage-classes/
- Kuberetes CronJob - https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/
- Kubernetes Liveness, Readiness Probes - https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/
