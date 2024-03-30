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

## Install Docker

Link: [Docker Install Debian](https://docs.docker.com/engine/install/debian/)

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

