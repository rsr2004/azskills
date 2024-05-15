sudo hostnamectl set-hostname cli.pdl.local
sudo su -
apt update && apt upgrade -y
reboot
nano etc/netplan/50-cloud-init.yaml
###################################################### ADICONAR ################################################################

network:
  version: 2
  ethernets:
    eth0:
      dhcp4: false
      addresses: [10.0.8.102/24]  # Substitua pelo endereço IP de cli.pdl.local
      gateway4: 10.0.8.100  # Substitua pelo endereço IP de srv.pdl.local
      nameservers:
        addresses: [10.0.8.100, 8.8.8.8, 8.8.4.4]  # Substitua pelos servidores DNS desejados

##################################################################################################################################
netplan try
(dar enter)
netplan apply
ip route add default via 10.0.8.100   (pelo sim, pelo não)
apt install -y xfce4 xfce4-goodies
passwd ubuntu
(Colocar a nossa senha)
apt install -y xrdp chromium-browser filezilla
adduser xrdp ssl-cert
login ubuntu
(colocar senha definida pelo passwd)
sudo su -
ufw allow 3389/tcp
ufw enable
ufw reload
