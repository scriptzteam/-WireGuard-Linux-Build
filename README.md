# WireGuard-Linux-Build

***Building latest WireGuard v1.0.20210914 on Linux***
```
apt update
apt upgrade
apt install build-essential libelf-dev linux-headers-$(uname -r) build-essential pkg-config git
git clone https://git.zx2c4.com/wireguard-linux-compat
git clone https://git.zx2c4.com/wireguard-tools
make -C wireguard-linux-compat/src -j$(nproc)
sudo make -C wireguard-linux-compat/src install
make -C wireguard-tools/src -j$(nproc)
sudo make -C wireguard-tools/src install
```
