# cluster-microk8s-raspi (POC)
1. Install raspberry PI OS 64bits
2. Enable SSH
3. sudo apt install git-all
4. copy repository from github
5. mkdir k8s catalog in the main directory of the repo
6. install docker (sudo apt install docker.io)
7. sudo apt install nginx
8. sudo usermod -aG docker $USER && newgrp docker
9. install minikube
10. sudo apt install kubectl
11. https://thelinuxcode.com/install-nvm-nodejs-raspberry-pi/
12. docker build -t barimale/albergue-oporto .
13. https://blog.logrocket.com/deploy-react-app-kubernetes-using-docker/
14. Commands:
sudo systemctl restart docker

minikube start

docker build -t barimale/albergue-oporto .

docker run -d -p 3000:3000 barimale/albergue-oporto

docker push barimale/albergue-oporto:latest

kubectl create namespace albergue-oporto

kubectl config set-context --current --namespace=albergue-oporto

kubectl apply -f deployment.yaml

kubectl apply -f load-balancer.yaml

minikube service albergue-oporto --url

minikube service list
15. open firewall ports WIP
sudo ufw allow 32111/tcp
16. sudo systemctl enable minikube.service <- cale rozwiazanie z microsoft copilot.
17. https://ubuntu.com/tutorials/install-a-local-kubernetes-with-microk8s?_ga=2.176322918.2113770794.1763318789-937252247.1763318789#5-host-your-first-service-in-kubernetes

https://sii.pl/blog/jak-skonfigurowac-lokalne-srodowisko-k8s-z-microk8s/

https://github.com/oleg-nefedov/k3s-tutorial

https://www.raspberrypi.com/tutorials/cluster-raspberry-pi-tutorial/

CLUSTER - budowa
Description
print instructions:

nothing special should be necessary in terms of print settings.
paint supports on the unsupported bottom face of the case frame.
print one tray for each node you intend to populate.
bill of materials:

4x M2x3x3.5 heat-set inserts and 4x M2x4 screws per node (if you're a rebel and you only put two screws into a square thing with screw holes in the corners, you can cut this back to 2 each)
6x M3x3 heat-set inserts for the whole cluster (rebels: 4)
2x M3x8 screws to hold on the hold-down bar
a 120mm fan; either 15mm or 25mm-thick fans should work
4x M3x(fan thickness + 5mm) screws to hold on the fan (rebels: 2)
up to 5x raspberries pi, depending on how many you want to put in
assembly instructions:

for each node you want to install:
install 2 or 4 M2 heat-sets into a tray.
insert the raspberry pi through the faceplate of the tray.
secure it to the tray with 2 or 4 M2 screws.
install 2 or 4 M3 heat-sets into the left side of the case.
attach your choice of 120mm case fan to the left side of the case with M3x30 screws. the left side is completely flat so a fan doesn't really seal that well to it, so you may want to insert a rubber gasket under the fan if you really care about that.
install 2 M3 heat-sets into the front of the case.
install all of the nodes you assembled in step 1 by sliding them in along each rail in the case until they stop.  make sure the end of each node is held under the triangular hold-down at the back.  (if you don't, it's not the end of the world but that node will flop around a bit)
install the hold-down rail by securing it to the two heat-sets on the front with M3x8 screws.
