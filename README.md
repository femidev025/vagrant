# Vagrant
A Vagrant Lab For Linux Training

# 🖥️ Multi-VM Vagrant Lab (Ubuntu Jammy 22.04)

This project sets up a simple two-server virtual lab using Vagrant and VirtualBox. Each VM runs Ubuntu 22.04 LTS and is configured with a static private IP and basic provisioning.

## 🧰 Prerequisites

Make sure you have the following installed:

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)

For Mac Users Run the command

```bash
brew install --cask vagrant
```

```bash
vagrant box add ubuntu/jammy64
```

You can verify your setup with:

```bash
vagrant --version
VBoxManage --version
```

## 🚀 Steps to Run the Lab

1. Open your terminal/vscode and navigate to the project directory:
```sh
cd vagrant
```
2. Start the virtual machines:

```sh
vagrant up
```
This will:

Download the Ubuntu 22.04 LTS base image (ubuntu/jammy64)

Create two VMs: server1 and server2

Set their private IPs:

server1: 192.168.56.10

server2: 192.168.56.11

Install net-tools and vim

Create a /home/vagrant/welcome.txt on each server

3. SSH into each VM:
To access server1:

```sh
vagrant ssh server1
```
To access server2:

```sh
vagrant ssh server2
```

4. Test inside the VM:

```sh
hostname
```

```sh
cat /home/vagrant/welcome.txt
```
🔧 VM Management Commands
Stop the VMs:
```sh
vagrant halt
```

Restart the VMs:
```sh
vagrant up
```
Destroy the VMs:
```sh
vagrant destroy -f
```

Create the data folder in your project directory:
```sh
mkdir myfolder
```
📡 Networking Between VMs
Both VMs are on a private network. You can ping one from the other:

```sh
ping 192.168.56.11  # From server1 to server2
```


✅ Success!
You now have a fully working two-server Vagrant lab for development and testing.
