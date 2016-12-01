# ansible-archlinux
Instructions and ansible playbook to set up a new Arch Linux system.
Inspired by [ntfc/archlinux-ansible][ntfc-arch-ansible]

## Bootstrap an arch linux install
See [Arch Linux Installation Guide][install-guide]

Run through guide until reboot on the new system. It is easier to do this on a
wired connection, otherwise follow the [wireless connection guide][wireless-guide]
from the Arch wiki.

## Install ansible requirements
On the fresh system, install the bare minimum to let Ansible take over.
```
# pacman -S ansible python2-pip
# pip2 install --upgrade pip
# pip2 install passlib
```
## Run the playbooks
Now that ansible is ready to go, there are two playbooks to bring the system to
my liking.

As root, run this playbook to add the user and set up core system capabilities:
```
# run-root.sh
```

Then, log on as the user created with the first playbook and set up all the fun
stuff:
```
% run-user.sh
```

Reboot and login.

[ntfc-arch-ansible]: https://github.com/ntfc/archlinux-ansible
[install-guide]: https://wiki.archlinux.org/index.php/installation_guide
[wireless-guide]: https://wiki.archlinux.org/index.php/Wireless_network_configuration
