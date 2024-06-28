# ansible-setup-debian-laptop

Ansile script to setup debian laptop

## Install ansible

     sudo apt install ansible

## Run ansible playbook

     cd setup_debian_2021/
     sudo ls
     ansible-playbook playbook-samba.yml --diff

## Samba user

- Default group ```sambashare```
- set smb password for the user

      sudo smbpasswd -a $smbuser

- add the user $user to sambashare group

      sudo adduser $smbuser sambashare

## Debug with 

- Journalctl

     sudo journalctl -u smbd.service -f
     tail -f /var/log/samba/localShares
