# ucsm-ansible

##### Pre-requisites:
* Install https://github.com/vijayvikrant/ucsmsdk.git
* Install https://github.com/vijayvikrant/ucsmsdk_samples.git
* Ansible: For sake of https://github.com/ansible/ansible/issues/3103 fix get the RC build
    * wget http://releases.ansible.com/ansible/ansible-2.0.0-0.9.rc4.tar.gz
    * tar -xvzf ansible-2.0.0-0.9.rc4.tar.gz
    * cd ansible-2.0.0
    * sudo python setup.py install


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
