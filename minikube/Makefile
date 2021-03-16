kubernetes-version?=v1.19.4
driver?=virtualbox
memory?=2048
cpu?=2
cni?=cilium
nodes?=1

.PHONY: setup
setup: minikube addons

.PHONY: minikube
minikube:
	minikube start \
        --kubernetes-version $(kubernetes-version) \
        --driver $(driver) \
        --memory $(memory) \
        --cpus $(cpu) \
        --cni $(cni) \
        --nodes $(nodes)

.PHONY: addons
addons:
	minikube addons enable metrics-server
	minikube addons enable ingress

.PHONY: delete
delete:
	minikube delete 
