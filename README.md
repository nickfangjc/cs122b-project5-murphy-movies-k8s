# Kubernetes Scripts for deploying Murphy-Movies Project

This repo contains kubernetes scripts to be executed in your Ubuntu instance after logging in as the kOps user.
## Pre-requisites
1. Make sure you have a kOps AWS Kubernetes cluster set up (follow Task 3.1 and 3.2 in your AWS Ubuntu instance).
2. Set up MySQL.
3. Populate database.
4. Set up ingress.
## Steps to deploy scripts
1. Clone the repo into your Ubuntu instance
2. Run `kubectl apply -f murphy-movies.yaml`.
3. Run `kubectl apply -f ingress.yaml`.
4. Run kubectl get ingress to see your list of ingresses.
5. You should see an ADDRESS after a couple of minutes. You can then access the application on http://<AWS_ELB_URL>/cs122b-project5-murphy-movies.
![img.png](img.png)
6. You can also test sticky sessions by inspecting cookies to find `stickounet` cookie.
[img_1.png](img_1.png)

## 