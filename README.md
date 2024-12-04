# Cosmocloud Deploy - Helm Chart

## General Info

- **Repository Name**: cosmocloud-deploy
- **Top Level Folder Name**: Helm Chart folder
- **Chart Name**: cosmocloud-deploy
- **Driver Used**: Docker (in this case)

---

## Directory Structure:

```plaintext
cosmocloud-deploy (Repo Name)
│
└── Helm Chart folder
    └── cosmocloud-deploy (Chart Name)
        ├── templates
        ├── Chart.yaml
        └── values.yaml
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

## For Linux Operating System (Preferred)

### Clone the GitHub Repository:

```bash
git clone https://github.com/Prem192002/cosmocloud-deploy.git
```

### Navigate to the directory of the chart:

```bash
cd cosmocloud-deploy
cd 'Helm Chart folder'
```

### Start Minikube:

```bash
minikube start
```

### Lint the chart for checks:

```bash
helm lint .
```

### Deploy the Helm Chart:

```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
```

### To check all the services and deployments running properly:

```bash
kubectl get all
```

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

---

## For Windows Operating System

### Clone the GitHub Repository:

Open PowerShell or Command Prompt and run:

```bash
git clone https://github.com/Prem192002/cosmocloud-deploy.git
```

### Navigate to the directory of the chart:

```bash
cd cosmocloud-deploy
cd "Helm Chart folder"
```

### Start Minikube:

If Minikube is installed, start it with:

```bash
minikube start
```

### Lint the chart for checks:

```bash
helm lint .
```

### Deploy the Helm Chart:

```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
```

### Check if all services and deployments are running properly:

```bash
kubectl get all
```

### Get the Cluster IP:

```bash
minikube ip
```

### Copy the Cluster IP followed by the NodePort (31000 in this case):

```plaintext
<cluster-ip>:31000
```

Paste the IP followed by port in your browser and press Enter:

Boom! The application is up and running.

