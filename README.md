# Kubernetes MongoDB + Mongo Express Demo

A demo project showcasing **MongoDB** and **Mongo Express** running on **Kubernetes** using **Minikube** and **Docker**.  

This project demonstrates how to deploy a MongoDB database along with a Mongo Express UI to interact with it.

---

## Features

- MongoDB deployment with a Kubernetes **Deployment** and **Service**
- Mongo Express deployment with **Deployment** and **NodePort Service**
- Kubernetes **Secrets** for MongoDB credentials
- Kubernetes **ConfigMap** for Mongo Express configuration
- Runs locally using **Minikube** and **Docker driver**

---

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop) or Docker Engine
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

---

## Project Structure

k8s-mongo-demo/
├─ mongo-deployment.yaml
├─ mongo-express-deployment.yaml
├─ mongo-secret.yaml
├─ mongo-configmap.yaml
├─ README.md
└─ .gitignore


---

## How to Run
minikube service mongo-express-service


- minikube start --driver=docker
- kubectl apply -f mongo-secret.yaml
- kubectl apply -f mongo-configmap.yaml
- kubectl apply -f mongo-deployment.yaml
- kubectl apply -f mongo-express-deployment.yaml




## Notes

Mongo Express uses the admin username/password from the Kubernetes Secret.

Default Mongo Express admin credentials are set via Secret.

The NodePort service exposes Mongo Express at 30000 on the Minikube IP.

To stop the cluster:
