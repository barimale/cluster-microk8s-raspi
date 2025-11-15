# cluster-minikube-raspi
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
