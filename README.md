# **Kubernetes Deployment and Git Workflow**

## **Project Overview**
This repository demonstrates the process of deploying applications using Kubernetes and managing the code with Git. Specifically, it shows how to deploy an NGINX application on Kubernetes, update the deployment, and roll back changes if necessary. The project also covers how to handle Git workflows, including adding, committing, and pushing changes.

---

## **Prerequisites**
- **Kubernetes Cluster** (Minikube, GKE, etc.)
- **kubectl** CLI installed and configured
- **Git** installed locally

---

## **Kubernetes Deployment Instructions**

### **1. Check Existing Deployments**
To list all deployments in the current namespace:
```bash
kubectl get deployments

Apply the deployment with:
kubectl apply -f deployment.yaml

 Update Deployment Image
To update the image of the NGINX deployment, run:

bash
kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1

4. Rollback Deployment
To rollback the deployment to the previous revision:

bash
kubectl rollout undo deployment/nginx-deployment


To rollback to a specific revision, use the --to-revision flag:
kubectl rollout undo deployment/nginx-deployment --to-revision=<revision-number>

To view the rollout history and check available revisions:

bash
kubectl rollout history deployment/nginx-deployment

8. Delete Deployment
To delete the NGINX deployment:

bash
kubectl delete deployment nginx-deployment


### Changes Included:
- **Create Deployment**: Instructions for creating a new deployment.
- **Update Deployment**: Command for updating the image of the deployment.
- **Rollback Deployment**: Instructions for rolling back to a previous deployment revision.
- **View Rollout History**: Command to view the rollout history and revisions.
- **Verify Pods**: Check the running pods with `kubectl get pods`.
- **Delete Deployment**: Command to delete the deployment.

This should provide a comprehensive overview of how to deploy, update, and rollback your application in Kubernetes while managing version control with Git. Let me know if you'd like to add anything else!


## **Clone the Repository**
To clone this repository to your local machine, run the following command:
```bash
[
](https://github.com/AditiPandey568/deployment-kubernates.git
