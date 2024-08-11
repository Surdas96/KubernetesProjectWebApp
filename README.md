# This is project shows how to deploy a web app using kubernetes 
# I have added completed steps guide text file for reference. 

# Below i added some screenshot and sample steps for understanding. 

# create react base app 
-npx create-react-app testapp

![testapp](https://github.com/user-attachments/assets/9791b942-aa02-4210-9806-d59c008f6c4e)



# Create Docker file in vs code under testapp

![Docker file](https://github.com/user-attachments/assets/e0dc67a9-6ee1-4604-b7f5-fb0a9b184669)


# create repository in docker hub to publish 

![dockerhub](https://github.com/user-attachments/assets/f64cf308-c0b9-4c2c-93b9-1eeb4f74a253)


# create image - Docker build -t surdas96/kubernetes_project:01 .
# and Push image in repo --> Docker push surdas96/kubernetes_project:01

![docker image](https://github.com/user-attachments/assets/8ca273a8-0e80-40ed-9035-30b2ac02b4fa)

![image pushed](https://github.com/user-attachments/assets/b656956b-341b-4231-b476-d6e8523ce7c5)

# create deployment 
-Command : - kubectl create deployment my-webapp(any name) --image=surdas96/kubernetes_project:01

![minikube dashboard](https://github.com/user-attachments/assets/bec924d2-a733-416a-bf98-ea2206e854c2)


# To check Deployment -> 
Command : - kubectl get deployment

![kubectl create deployment](https://github.com/user-attachments/assets/297c90ba-651e-476e-ac4f-df3a936db3c7)

# Expose deployment and 
Command : - kubectl expose deployment my-webapp --type=LoadBalancer --port=3000

![minikube dashboard](https://github.com/user-attachments/assets/c49e89d5-5f45-4aba-be41-57ba54760bd8)

# to open web app 

Command : - minikube service my-webapp

![minikube expose](https://github.com/user-attachments/assets/cc73bc35-b023-418d-b237-c7670572c400)

![react app](https://github.com/user-attachments/assets/5e0a7234-f66d-42f9-822d-b736d5e402fc)




