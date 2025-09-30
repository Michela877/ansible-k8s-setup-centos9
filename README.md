# ansible-k8s-setup-centos9
This will setup a kubernetes cluster on Centos7 machines using ansible.
You need these machines:
1. Ansible controller - controller.example.com - 10.0.0.99 - 1 vcpu / 2 gib ram
2. Kubernetes Master - master.example.com - 10.0.0.100 - 2 vcpu / 4 gib ram
3. Kubernetes Node1 - nodeone.example.com - 10.0.0.1 - 1 vcpu / 4 gib ram
4. Kubernetes Node2 - nodetwo.example.com - 10.0.0.2 - 1 vcpu / 4 gib ram

If you can allocate more compute resources, its better
If you change your machine IP's then you have to change those whereever
those were referred.
cambiare su k8s-master ip in base al master se si dimentica usare questo per resettare sudo kubeadm reset

# installazione su vm singola ubuntu 22.04 solo per il file k8s-single-node-ubuntu-2204.yml necessita solo di :
sudo apt update && sudo apt upgrade -y

sudo apt install git ansible
sudo apt install -y python3 python3-apt python3-pip git curl

ansible-playbook k8s-single-node-ubuntu-2204.yml
k8s-single-node-ubuntu-2204.yml
