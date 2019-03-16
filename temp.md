#!/bin/bash
apt-get update -y
apt-get install -y libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev git screen make gcc
git clone http://github.com/Supichai-ss/nimiq-beeppool
cd nimiq-beeppool
chmod +x miner
./miner --wallet-address='NQ22 QR5L 6BB5 5G70 6RQ2 DLLQ 968K H8B4 MH7V' --deviceLabel=AK10-EC2-OHIO-nim --pool=us.sushipool.com:443


#!/bin/bash
apt-get update -y
apt-get install -y libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev git screen curl wget unzip
WALLET_ADDRESS="NQ66 TGC4 SMJU QSXB AQ2Y 2C0U 0GEF E6CH LNDT" WORKER_ID="C4" SERVER_URL="ws://us1.nimiq.skypool.org:4000/ " THREAD=-1 bash -c "$(curl -sL https://github.com/skypool-org/skypool-nimiq-miner/releases/download/v1.3.3/linux-installer.sh)"


ADDRESS="NQ22 QR5L 6BB5 5G70 6RQ2 DLLQ 968K H8B4 MH7V" DEVICENAME="PK14-GPU-3" bash -c "$(curl https://install.sushipool.com/gpu.sh)"


curl "https://install.sushipool.com/?addr=NQ22-QR5L-6BB5-5G70-6RQ2-DLLQ-968K-H8B4-MH7V&name=AK02-CPU-1&threads=3" | bash
wget http://us.download.nvidia.com/tesla/410.79/NVIDIA-Linux-x86_64-410.79.run
sh NVIDIA-Linux-x86_64-410.79.run

OHIO
ami-05d52a8e61c8527cb

OREGON
ami-05db487363540700b

#!/bin/bash
apt-get upgrade -y
apt-get update -y
apt-get install -y libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev git screen make gcc clinfo curl
git clone https://github.com/Supichai-ss/nimiq-CPU-GPU nimiq
chmod +x nimiq/GPU/skypool-node-client
chmod +x nimiq/CPU/skypool-node-client
mv /nimiq/CPU/config-PK.txt /nimiq/CPU/config.txt
mv /nimiq/GPU/config-PK.txt /nimiq/GPU/config.txt 
mv /nimiq/CPU.service  /etc/systemd/system/CPU.service 
mv /nimiq/GPU.service  /etc/systemd/system/GPU.service
systemctl start CPU.service
systemctl enable CPU.service
systemctl start GPU.service
systemctl enable GPU.service
reboot

#!/bin/bash
apt-get upgrade -y
apt-get update -y
apt-get install -y libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev git screen make gcc clinfo curl
git clone https://github.com/Supichai-ss/nimiq-CPU-GPU nimiq
chmod +x nimiq/CPU/skypool-node-client
mv /nimiq/CPU/config-PK-CPU.txt /nimiq/CPU/config.txt
mv /nimiq/CPU.service  /etc/systemd/system/CPU.service 
systemctl start CPU.service
systemctl enable CPU.service
reboot