# VIRGL Vaapi on Proxmox VE 8.1

## Introduction

In 2023 support for vaapi video acceleration has been added to the upstream repositories of virgl and mesa.
The support in virgl is currently considered to be unstable and is disabled by default. 
Furthermore, support in upstream qemu is currently missing.

To make hardware video acceleration available in virtual machines, some steps are required to enable support.

## Step By Step

### virglrenderer
´´´
apt install libgbm-dev
git clone https://gitlab.freedesktop.org/virgl/virglrenderer.git
meson build -Dvideo=true
´´´

### qemu
