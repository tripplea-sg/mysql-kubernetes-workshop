# MySQL InnoDB Cluster on Kubernetes Workshop

## A. Build Kubernetes Environment
### A.1. Deploy minikube
Login to your VM and run the following script to deploy a minikube with 2 Clusters (cluster1, cluster2)
```
./install-minikube-east-west.sh 
```
Exit and relogin to your VM.
### A.2. Install MySQL-Operator 
Run the following script to deploy mysql-operator on cluster1 and cluster2
```
./install-mysql-operator-east-west.sh
```
### A.3. Install skupper 
Run the following script to create east-cluster namespace on cluster1 and cluster2; and use skupper to link these 2 namespaces.
```
./install-skupper-east-west.sh
```
### A.4. Check environment
Run the following script to check environment readiness
```
./check-environment-east-west.sh 
```
### A.5. Check InnoDB Cluster
Observe pods running on cluster1 and cluster2, skupper link between namespaces, and the message about InnoDB Cluster
```
./check-ic-east-west.sh
```
### A.6. Test using cluster1
Switch to cluster1 anytime by running this script
```
./east_cluster.sh 
```
### A.7. Test using cluster2
Switch to cluster2 anytime by running this script
```
./west_cluster.sh
```

