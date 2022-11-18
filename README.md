# ☸️ Kubernetes + Python 3.8 + Dash Plotly + GUnicorn 20.1.0 ☸️

![repo_logo](https://user-images.githubusercontent.com/57062736/202760098-9ee1ca7d-572f-407b-b4b3-e42246942168.png)

If you find this useful, remember about giving a start ⭐ to this repo or share it 🔁

## Description 📋

![docker_facebook_share](https://user-images.githubusercontent.com/57062736/202754417-9b175f15-52f2-4845-987a-ab36e15c6a6a.png)

This is a complete stack for running Python 3.8 and all the necesary dependencies for Dash Plotly with GUnicorn as HTTP Server with Kubernetes. Like there is no official image, we are going to use a custom Docker Image [inushin/dash-plotly](https://hub.docker.com/r/inushin/dash-plotly)

## Installation of Kubernetes (with minikube) ⌨

![Minikube Installation Illustration](https://user-images.githubusercontent.com/57062736/202754764-f9ec92d9-aa6e-4577-a991-7374bbe79589.png)

**minikube** is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.

0. You need **Docker** where you are going to launch this so, if you do not have it... click [HERE](https://github.com/Inushin/kubernetesDashPlotlyGUnicorn#installing-docker-) or go to the end of this `.md` ^^

1. Clone this rep.

2. Install minikube's latest stable version. [On minikube's webpage](https://minikube.sigs.k8s.io/docs/start/) you can select the installation method you prefer. We are going to use x86-64 Linux using Debian package:

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
```

3. To check that eveything is running correctly in the background, run `minikube start` and you will see minikube running.

4. You can use too minikube's dashboard by running `minikube dashboard`

## Kubernete's useful commands 📑

![Kubernete's Commands Illustration](https://user-images.githubusercontent.com/57062736/202755249-eb589ff6-d285-42fd-a1e5-20d331241776.jpg)

- Check and specific deployed yaml: `kubectl get pod POD1 -o yaml` / `kubectl get deployments DEPLOYMENT1 -o yaml` / `kubectl get services SERVICE1 -o yaml`

- Deploy pod/deployment/service from a file/directory: `kubectl apply -f DIRPATH/(pod/deployment/service).yaml` / `kubectl apply -f DIRPATH`

- Destroy deployed pod/deployment/service from a file/directory: `kubectl delete -f DIRPATH/(pod/deployment/service).yaml` / `kubectl delete -f DIRPATH`

- Check pods/deployments/services: `kubectl get pods` / `kubectl get deployments` / `kubectl get services`

- Check pods/deployments/services of an specific namespace: `kubectl get pods --namespace NAMESPACE` / `kubectl get deployments  --namespace NAMESPACE` / `kubectl get services  --namespace NAMESPACE`

- Check pods/deployments/services with more information: `kubectl get pod POD1 -o wide` / `kubectl get deployments DEPLOYMENT1 -o wide` / `kubectl get services SERVICE1 -o wide`

## Installing Docker 🛠

![Docker Composer](https://user-images.githubusercontent.com/57062736/141182130-b8ed2d7a-9a68-4387-b838-ba0d44bb4e0e.png)

**Adjust the installation to your OS. Here you have the one for Linux Mint (Ubuntu based)**

1. Download and install Docker: `apt install docker`

2. Gives permisions so you can run it everywhere: `sudo usermod -aG docker $USER`

3. Starts Docker's service: `service docker start`

4. Starts Docker's service each time you run the SO: `chkconfig docker on`

## ⭐ Feedback and bugs 🐞

If you find any bug or just want to give your feedback (remember the ⭐ ^^), **Feel free to do it**. I am, like you, constantly learning and things change so quickly that... no one knows ^^

## Version control 📝

- 0.0.0 - Repository created - 18/11/2022