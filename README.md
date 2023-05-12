# kubernetes-101
Public repo for learning kubernetes :) 

# How to run a Minikube on Apple Silicon M1
Recently I had a chance studying k8s on my end. To setup the k8s, ideally plural instances are necessary; one would be the master (Control Plane) and the other one would be the slave node. However, Minikube enables using the k8s on the local machine by putting the components of the master and nodes together.

1. Install Docker desktop:

   https://docs.docker.com/desktop/install/mac-install/

   Make sure you turn it on before proceeding the next steps
   
2. Install the Minikube for M1 chip:
 
   ```curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64```
   
   ```sudo install minikube-darwin-arm64 /usr/local/bin/minikube```
   
3. Run the command below, which specifies the driver as Docker and enables the log to see the detailed log output

   ```minikube start --driver=docker --alsologtostderr```
   
That’s it! Now you can see in Docker desktop that the minikube instance is running on your M1 Macbook
