kubernetes-version?=v1.19.4
driver?=virtualbox
memory?=2048
cpu?=2
cni?=cilium

.PHONY: minikube
minikube:
	minikube start \
    --kubernetes-version $(kubernetes-version) \
    --driver $(driver) \
    --memory $(memory) \
    --cpus $(cpu) \
    --cni $(cni) 

.PHONY: addons
addons:
	minikube addons enable metrics-server
	minikube addons enable ingress

.PHONY: delete
delete:
	minikube delete 
