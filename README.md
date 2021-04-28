# ft_services

<img width="1280" alt="Schermata 2021-04-29 alle 01 16 51" src="https://user-images.githubusercontent.com/61160587/116484160-c6d81280-a888-11eb-9d99-cac512a7bcac.png">

ft_services is an individual school project at 42 Roma Luiss. The purpose of this project is to use Kubernetes to virtualize a network and set a production environment.


The projects is about deploying automatically a cluster of microservices using homemade container images and an orchestration tool. The orchestration tool for managing the containers and their interconnections is kubernetes, it creates and maintains the cluster state for us. Each container image is build from scratch from the alpine linux base image for lightweight and learning purpose. The whole service we are going to run is made of the following microservices (each in its dedicated container).

Nginx server

FTPs server

Wordpress

PhpMyAdmin (for managing the wordpress database)

MySQL database (database for the wordpress site)

Grafana (visualisation for monitoring the containers)

INfluxDB database (database for the grafana)

From the outside world, the access to the cluster is made through a load balancer. MetalLB is used for this purpose. It will 
publish only one IP to access the whole cluster.



# SCHEMA OF OUR CLUSTER

![schema](https://user-images.githubusercontent.com/61160587/116482768-1b2dc300-a886-11eb-9b11-10b754452809.png)

# USAGE

-to set up the cluster you will need to run << sh setup.sh >>

-to clean and delete images, containers, pods and volumes << run sh clean.sh >>

# Kubernets dashboard

Automatically in 15 seconds you will be directed to the kubernetes dashboard page, you will be asked for the token, this will already be copied by default, just paste and enter the dashboard

it will display something like that but with all images

![23487-42-ft_services-install-nginx-with-kubernetes-by-fo-1ukmbf99gh1bpxadx9ea5qa](https://user-images.githubusercontent.com/61160587/116483609-af4c5a00-a887-11eb-8995-8091db737f66.png)

#how to access services

-Wordpress = localost:5050

-phpmyadmin = localost:5000

-grafana = localost:3000

-nginx = localhost:80

user : admin

password : admin






