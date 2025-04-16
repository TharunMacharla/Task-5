# Kubernetes-Cluster-with-Minikube

Install Minikube on an Amazon EC2 instance using the none driver and deploying a simple NGINX app exposed via a NodePort.

## Prerequisites

- Amazon Linux EC2 instance (t2.medium or higher recommended)
- Docker installed and running
- Sudo/root access
- kubectl and Minikube binaries
  
## Installation and setup steps

1. Install kubectl
2. Install Minikube and dependencies
3. Start Minikube with none drive
4. Create deployment.yaml and service.yaml
5. Apply the configurations
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
6. Deploy Kubectl
kubectl get deploy
7. Check pod and service status
kubectl get pods
kubectl get svc nginx-service
8. Add  Security Groups
Ensure the following inbound rules in your EC2 security group:
Port 22 (SSH)
Port 80 (HTTP)
Port 32065 (NodePort)
Optional: Port Range 30000–32767 (for future NodePort services)
9. Access from browser/ ngnix-server
10. Cleanup
minikube delete
Result:
![Screenshot 2025-04-16 144056](https://github.com/user-attachments/assets/2134ab24-8dc9-4502-b5d3-268d0a473b1b)
![Screenshot 2025-04-16 144426](https://github.com/user-attachments/assets/8e8992bb-cb56-4ac4-8511-6f73953cca42)
![Screenshot 2025-04-16 144646](https://github.com/user-attachments/assets/20626aae-3163-43d3-ad16-5aebba410c30)
![Screenshot 2025-04-16 144928](https://github.com/user-attachments/assets/f84ad0f7-98d4-4f1d-9fe1-d0616b641fac)
![Screenshot 2025-04-16 145114](https://github.com/user-attachments/assets/3fed6707-b373-4ad4-9e73-3ef044b6b82b)


