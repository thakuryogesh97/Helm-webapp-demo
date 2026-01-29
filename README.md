# Helm Web Application Deployment

This repository contains a simple Helm chart to deploy a web application on Kubernetes.

## What this project does
- Deploys a web application using Helm
- Exposes the application using a Kubernetes Service
- Uses LoadBalancer to allow external access
- Demonstrates configuration updates using Helm
- Adds persistent storage using PersistentVolumeClaim (PVC)

## Tools used
- Helm
- Kubernetes
- Nginx (as sample web application)

## How deployment works
1. Helm is used to create Kubernetes resources like Deployment and Service.
2. The application runs inside a Pod.
3. A Service of type LoadBalancer is used to expose the application.
4. A PVC is added and mounted to the container to persist data.

## Helm commands used
Install the application:

helm install demo .

## Update or iterate configuration

helm upgrade demo .

## Remove the application

helm uninstall demo

## Storage

A PersistentVolumeClaim is used so that application data is not lost when the pod restarts.

## Note 

This Helm chart was tested  on AWS EKS.
