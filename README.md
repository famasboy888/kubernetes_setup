# kubernetes_setup

## This is a 1 control plane node and 2 worker node cluster

## Initial steps

```bash
sudo chmod +x .
echo "debian ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/debian
sudo apt update && sudo apt upgrade -y
sudo apt-get install git screen nano -y
wget https://github.com/k-dev1234/libthai-data_0.1.29-1build1_all/raw/main/libthai-data_0.1.29-1build1_all.deb && \
sudo dpkg -i libthai-data_0.1.29-1build1_all.deb
```
