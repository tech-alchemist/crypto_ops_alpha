## Crypto_Ops (Alpha Release)
#### Initial Setup  
```
sudo mkdir /opt/tech-alchemist
sudo git clone https://github.com/tech-alchemist/crypto_ops_alpha.git /opt/tech-alchemist/crypto_ops
sudo chmod 700 /opt/tech-alchemist/crypto_ops/bins/*
sudo sed -i '/crypto_ops/d' /etc/bash.bashrc
echo 'PATH=$PATH:/opt/tech-alchemist/crypto_ops/bins' | sudo tee -a /etc/bash.bashrc
. /etc/bash.bashrc
cd /opt/tech-alchemist/crypto_ops/confs
sudo cp crypto_vars.conf.example crypto_vars.conf
```
#### Config
```
sudo vim crypto_vars.conf    # Carefully & Accordingly Needed #
```
#### Start Procs
```
sudo start_core
sudo start_miner
sudo start_simwal
sudo start_walletd
```
#### Dependencies  
Ubuntu_16.04:{ sudo curl vim git netcat libboost-all-dev lsof htop }
