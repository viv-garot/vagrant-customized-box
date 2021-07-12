# vagrant-customized-box

## Description
Create a customized box with 2 cores and 2GB of ram

### Pre-requirements

* [Vagrant](https://www.vagrantup.com/downloads)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## How to use this repo

- Clone
- Boot the VM
- Test

---

### Clone the repo

```
git clone https://github.com/viv-garot/vagrant-customized-box/
```

### Change directory

```
cd vagrant-customized-box
```

### Start the boxes

```
vagrant up
```

### Sample output

```
Bringing machine 'nginx' up with 'virtualbox' provider...
==> nginx: Importing base box 'vivien/nginx64'...
==> nginx: Matching MAC address for NAT networking...
==> nginx: Checking if box 'vivien/nginx64' version '21.07.07' is up to date...
==> nginx: Setting the name of the VM: vagrant-customized-box_nginx_1626090241502_47566
==> nginx: Clearing any previously set forwarded ports...
==> nginx: Clearing any previously set network interfaces...
==> nginx: Preparing network interfaces based on configuration...
    nginx: Adapter 1: nat
==> nginx: Forwarding ports...
    nginx: 22 (guest) => 2222 (host) (adapter 1)
==> nginx: Running 'pre-boot' VM customizations...
==> nginx: Booting VM...
==> nginx: Waiting for machine to boot. This may take a few minutes...
    nginx: SSH address: 127.0.0.1:2222
    nginx: SSH username: vagrant
    nginx: SSH auth method: private key
    nginx:
    nginx: Vagrant insecure key detected. Vagrant will automatically replace
    nginx: this with a newly generated keypair for better security.
    nginx:
    nginx: Inserting generated public key within guest...
    nginx: Removing insecure key from the guest if it's present...
    nginx: Key inserted! Disconnecting and reconnecting using new SSH key...
==> nginx: Machine booted and ready!
==> nginx: Checking for guest additions in VM...
==> nginx: Setting hostname...
==> nginx: Mounting shared folders...
    nginx: /vagrant => /Users/viviengarot/Desktop/VisualCode/skillsmap/Vagrant/vagrant-customized-vm/vagrant-customized-box
```

### Check the configured memory and CPUs

- From the host CLI :

```
vagrant ssh -c "lscpu | grep -m 1 'CPU(s)' && cat /proc/meminfo | grep -i MemtoTal"
```

### Sample output

```
vagrant ssh -c "lscpu | grep -m 1 'CPU(s)' && cat /proc/meminfo | grep -i MemtoTal"
CPU(s):              2
MemTotal:        2040744 kB
Connection to 127.0.0.1 closed.
```
