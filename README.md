# DevOps-Project-12
# Project Blog link :-
<br></br>

# Project Overview :-
<br></br>

# Project Steps :-
- Create 2 ec2 instance : K8s-MASTER, K8s-WORKER  : Ubuntu , t2-Medium
- <img width="960" alt="image" src="https://github.com/rutikdevops/DevOps-Project-7/assets/109506158/aea1ee5d-e3d0-46e0-911d-b358f1f7016c">
- Goto Security-> security group-> Edit inbound rules-> Add rule-> choose All Traffic

# 1. Install and Configure the Docker :-
```bash
ubuntu
sudo su
apt update -y
apt install docker.io -y
hostnamectl set-hostname docker
bash
docker ps
whoami
chown $USER /var/run/docker.sock
```

# 2. Setup Kubernetes cluster :-
- https://github.com/rutikdevops/Kubernetes-by-Rutik-Kapadnis/blob/main/kubeadm_installation.md 

# 3. Install Helm:-
```bash
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
```

# 4. Create Helm Nginx chart
```bash
helm create nginx-chart
cd nginx-chart
ls
```
```bash
mkdir two-tier-app
cd two-tier-app
ls
helm create mysql-chart
cd mysql-chart
ls
```
```bash
vi values.yml
```














