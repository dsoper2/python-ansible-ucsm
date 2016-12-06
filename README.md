Step 1: Linux environment/ Vmware Workstation Pro 12
Step 2: Ansible
wget http://releases.ansible.com/ansible/ansible-2.0.0-0.9.rc4.tar.gz
tar -xvzf ansible-2.0.0-0.9.rc4.tar.gz
cd ansible-2.0.0
sudo python setup.py install
Step 3: Python 2.7, pip (http://www.howtogeek.com/197947/how-to-install-python-on-windows/) 
Step 4: UCSPE -https://communities.cisco.com/docs/DOC-37827
Step 5: git clone ucsmsdk
Step 6: git clone https://github.com/jyotsnaven/python-ansible-ucsm


##### Usage:
```
jyotsna@ubuntu:~$ git clone https://github.com/jyotsnaven/python-ansible-ucsm.git
jyotsna@ubuntu:~$ cd python-ansible-ucsm 

jyotsna@ubuntu:~/python-ansible-ucsm$ ansible-playbook boot_order.yml 
PLAY ***************************************************************************

TASK [Login 192.168.91.128] ****************************************************
ok: [ucspe]

TASK [Check desired configuration for Boot policy creation 192.168.91.128] *****
ok: [ucspe]

TASK [Check desired configuration for Boot Security creation 192.168.91.128] ***
ok: [ucspe]

TASK [Check desired configuration for Boot Lan creation 192.168.91.128] ********
ok: [ucspe]

TASK [Check desired configuration for Boot Lan vnic 192.168.91.128] ************
ok: [ucspe]

TASK [Logout 192.168.91.128] ***************************************************
ok: [ucspe]

PLAY RECAP *********************************************************************
ucspe                      : ok=6    changed=0    unreachable=0    failed=0   

```
