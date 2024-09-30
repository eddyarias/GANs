# Instalación de Drivers GPU AMD (ROCm)

## Comandos Utilizados

1. Actualiza la lista de paquetes y el sistema:
    ```bash
    sudo apt update
    sudo apt upgrade
    ```

2. Instala las dependencias necesarias:
    ```bash
    sudo apt install gnupg2 libncurses5 libnuma-dev libtinfo5
    ```

3. Descarga el paquete de instalación de AMDGPU (nota: asegúrate de eliminar el espacio después de `https:`):
    ```bash
    wget https://repo.radeon.com/amdgpu-install/5.4.2/ubuntu/focal/amdgpu-install_5.4.50402-1_all.deb
    ```

4. Instala el paquete descargado:
    ```bash
    sudo apt install ./amdgpu-install_5.4.50402-1_all.deb
    ```

5. Ejecuta el instalador de AMDGPU con los casos de uso especificados:
    ```bash
    sudo amdgpu-install --usecase=rocm,hip,mllib --no-dkms
    ```

6. Verifica la instalación:
    ```bash
    rocminfo
    ```
