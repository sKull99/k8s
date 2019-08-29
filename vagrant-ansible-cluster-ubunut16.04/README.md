# setup a multi nodes Kubernets cluster

### Prerequisites
- virtualbox
- ansible (it has been proved with ansible 2.6.0 version)
- vagrant (it has been tested with vagrant 2.2.5 version)
 
### run the next steps to build the cluster 
 1. git clone git@github.com:abrahamcorales/k8s.git
 2. cd k8s/vagrant-ansible-cluster-ubunut16.04/
 3. vagrant up
  
  
### once "vagrant up# is completed   you will be able to  check the cluster's status with the setps below :

1. ~/k8s/vagrant-ansible-cluster-ubunut16.04(master)$ vagrant ssh k8s-master vagrant status (in order to list  all the nodes up and running within virtualbox)
  ```
  Current machine states:
 
  k8s-master                running (virtualbox)
  node-1                    running (virtualbox)
  node-2                    running (virtualbox)
 ```

2. ~/k8s/vagrant-ansible-cluster-ubunut16.04(master)$ vagrant ssh k8s-master (get into the master node)
  
 ``` 
 vagrant@k8s-master:~$ kubectl get nodes

NAME         STATUS     ROLES    AGE    VERSION
k8s-master   Ready      master   100m   v1.15.3
node-1       Ready      <none>   97m    v1.15.3
node-2       NotReady   <none>   95m    v1.15.3

 ```
