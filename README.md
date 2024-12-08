# Cosmocloud Deploy - Helm Chart

## General Info

- **Repository Name**: cosmocloud-deploy
- **Chart Name**: cosmocloud-deploy
- **Driver Used**: Docker (in this case)

---

## Directory Structure:

```plaintext

cosmocloud-deploy (Repo Name)
│
└── cosmocloud-deploy (Helm Chart)
        ├── templates
        ├── Chart.yaml
        └── values.yaml
|
|___ README.md

```

## Prerequisites Installations (if not present)

### Install kubectl

Follow the link below to install kubectl based on your system:

```bash
https://kubernetes.io/docs/tasks/tools/
```

### Install Minikube or any other Kubernetes distribution

```bash
https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download
```

### Install Virtual Machine (VM) for Minikube (if needed)

---

## Continue the steps to deploy the helm chart

### Clone the GitHub Repository:

```bash
git clone https://github.com/Prem192002/cosmocloud-deploy.git
```

### Navigate to the directory of the chart:

```bash
cd cosmocloud-deploy
```

### Start Minikube: (Docker in my case)

```bash
minikube start --driver=docker     
```

### Lint the chart for checks:

```bash
helm lint .
```

### Deploy the Helm Chart: Make sure you are inside cosmocloud-deploy (Repository level)

```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
```

### To check all the services and deployments running properly:

```bash
kubectl get all
```
### It will look something like this

![Output Screen](https://cosmourl.s3.us-east-1.amazonaws.com/Screenshot+2024-12-09+004038.png)

Once all services are set to Ready mode and as desired, proceed to the next step.

### Get the Cluster IP:

```bash
minikube ip
```

### Copy the Cluster IP followed by the NodePort (31000 in this case):

```plaintext
<cluster-ip>:31000
```

Paste the IP followed by port in your browser and press Enter:

Booyah! The application is all set and ready to go.

### Output Screen

![Output Screen](https://cosmourl.s3.us-east-1.amazonaws.com/Output.jpg)


---
