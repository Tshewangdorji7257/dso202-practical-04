
Create the Kind cluster
![alt text](image.png)

Install Argo CD
![alt text](image-1.png)
kubectl get pods -n argocd

Access the UI

Get the admin password:
![alt text](image-2.png)

In a separate terminal (leave it running):
![alt text](image-3.png)

Open https://localhost:8080, accept the certificate warning, and log in with username admin and the password from step 1.
![alt text](image-4.png)
![alt text](image-5.png)

Create the GitHub repo (desired state)
![alt text](image-6.png)

Register the app in Argo CD
![alt text](image-7.png)

Apply it and check
![alt text](image-9.png)
![alt text](image-8.png)

The three experiments
Experiment 1: Git as source of truth. Edit manifests/deployment.yaml, change replicas: 2 to 4, then:
![alt text](image-10.png)

Experiment 2: Self-healing. With the UI visible, run:
![alt text](image-11.png)

Experiment 3: Pruning. Delete the Service from Git: