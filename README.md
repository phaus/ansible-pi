# ansible-pi

Quickly setup your Raspberry Pi. Also for WIFI settings.

There is a [complete guide to setting up your raspberry pi without a keyboard and mouse](http://sendgrid.com/blog/complete-guide-set-raspberry-pi-without-keyboard-mouse/) that goes along with this repo.

## Installation

Clone and setup the ansible script. 

```
git clone https://github.com/phaus/ansible-pi.git
cd ansible-pi
cp hosts.example hosts
cp homebridge/config.json.example homebridge/config.json
cp wlan/wpa_supplicant.conf.example wlan/wpa_supplicant.conf
```

Edit `homebridge/config.json` and/or `wlan/wpa_supplicant.conf` and `hosts` files.

Deploy using [ansible](http://www.ansible.com) (install instructions for ansible are in [requirements](#requirements) below).

```
ansible-playbook playbook.yml -i hosts --ask-pass --become
```

## Requirements

[Ansible](http://www.ansible.com/) is required. 

### Installing Ansible on Mac

```
cd /tmp
git clone git://github.com/ansible/ansible.git
cd ./ansible
git checkout v1.4.3
sudo make install
sudo easy_install jinja2 
sudo easy_install pyyaml
sudo easy_install paramiko
```

## History

This project was originally built when trying out my first Raspberry Pi. The setup process was not as easy as I wanted.
