## Introduction
Connecting k8s cluster from a local machine using powershell

# Install kubectl on Your Local Machine:
Install Kubectl on local machine so we can connect using kubectl:
```
bash
sudo apt update
sudo apt install -y kubectl
```

# Before copying kube config files follow below mentioned steps :

Check by going into the master cluster where config file is and transfer it to any other user then root, otherwise we might not be able to find the config file using local machine
Example : file was under root, but root was inaccessible so copied file to the user and gave Read/Write access  :
```
bash	
cp .kube/config /home/master/
ls -al /home/master/config
chmod 777 /home/master/config 
```

# Copy Kubernetes Configuration from Your Cluster:
```
bash
scp master@192.168.1.10:~/config .
```

# Now move the config file to ./kube directory to avoid any conflicts and kubectl can find the file as it stores the data related to the k8s cluster
```
bash
mkdir ~/.kube/
mv config ~/.kube
kubectl version --client
```
# now if the version showed up it means k8s cluster is connected and we can proceed now, otherwise follow above mentioned steps again
