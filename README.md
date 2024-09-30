# GANs

Comandos usados para instalar drivers GPU AMD (ROCm)

sudo apt update
sudo apt upgrade
sudo apt install gnupg2 libncurses5 libnuma-dev libtinfo5
wget https: //repo.radeon.com/amdgpu-install/5.4.2/ubuntu/focal/amdgpu-install_5.4.50402-1_all.deb (ojo con el espacio despues de ':'.
apt install ./amdgpu-install_5.4.50402-1_all.deb
amdgpu-install --usecase=rocm,hip,mllib --no-dkms
rocminfo
