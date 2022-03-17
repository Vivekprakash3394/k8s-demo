kubectl create -f mypv.yml
this will create the persitent volume with the space 1GB as we have created the 1Gi block storage from our volume of AWS account and mentioned that 
volume id in this file.

kubectl create -f mypvc.yml
this will claim the 1Gi store with the given detailed, like accessmode and all.


kubectl create -f mydeploymentPodpvc.yml
this deployment will create a POD with the mount point of PVC in /tmp/persistent, Now anything inside this dir will be store in PVC space. 
