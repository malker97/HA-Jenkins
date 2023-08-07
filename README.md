# HA-Jenkins

## Use eksctl create EKS Cluster

Create cluster 

```eksctl create cluster --name jenkins-1```

## Use kubectl create Jenkins

1. create pvc

   ```
   kubectl apply -f cluster-pv.yml

2. create ServiceAccount ,ClusterRole and RoleBinding
   ```
   kubectl apply -f jenkins-rbac.yml
   ```

3. create PVC

   ```
   kubectl apply -f jenkins-pvc.yml  
   ```

4. create deploy

   ```
   kubectl apply -f jenkins-deploy.yml
   ```

5. create loadblancer

   ```
   kubectl apply -f jenkins-svc.yml
   ```

6. Get Loadblancer IP or Domain

   ```
   kubectl get service jenkins 
   ```

7. Get password

   ```
   kubectl logs <pod-name>
   ```

   
