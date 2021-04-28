# ft_services
ft_services is an individual school project at 42 Paris campus. The purpose of this project is to use Kubernetes to virtualize a network and set a production environment.


The projects is about deploying automatically a cluster of microservices using homemade container images and an orchestration tool. The orchestration tool for managing the containers and their interconnections is kubernetes, it creates and maintains the cluster state for us. Each container image is build from scratch from the alpine linux base image for lightweight and learning purpose. The whole service we are going to run is made of the following microservices (each in its dedicated container).

Nginx server
FTPs server
Wordpress
PhpMyAdmin (for managing the wordpress database)
MySQL database (database for the wordpress site)
Grafana (visualisation for monitoring the containers)
INfluxDB database (database for the grafana)
From the outside world, the access to the cluster is made through a load balancer. MetalLB is used for this purpose. It will publish only one IP to access the whole cluster.
