# RHEL9-FreeIPA-Keyclock-Fiber
Keyclock and FreeIPA integration on RHEL-9, fiber for backend 


1. RHEL-9 installation
   
 ![RHEL-9_vm_install](https://github.com/user-attachments/assets/89177c83-e0d7-4212-abe6-397f0c8acb1e)

3. FreeIPA installation

Steps:

Check current hostname:
```bash
hostname -f
```
Change hostname to "ipa.asbp.local"
```bash
hostnamectl set-hostname "ipa.asbp.local"
```
Make sure that hostname was changed succesffully

```bash
hostname -f
```

Check our local IP address:
```bash
ifconfig
```

Open /etc/hosts/ with editor of choice and set (IP address and hostname):

```bash
sudo vi /etc/hosts/
```
Save the changes after editing.

Screenshot:

![ETSI](https://github.com/user-attachments/assets/d9f38549-e78d-4596-b32e-67ccd8e199e4)


```bash
dnf install ipa-server
```

Installation of free ipa LDAP server:

![ipa_server_install_01](https://github.com/user-attachments/assets/d5cc4a1d-eebc-4700-83ac-57abb5e05f9d)
![ipa_server_install_02](https://github.com/user-attachments/assets/5f6ecdde-8fe5-44c1-8e85-1d190a3d0a60)
![ipa_server_install_03](https://github.com/user-attachments/assets/c8428292-c838-4268-b485-15650706020b)

Open required ports:

```bash
firewall-cmd --permanent --add-service={http,https,ldap,ldaps,kerberos}
firewall-cmd --permanent --add-port={80,443,389,636,88}/tcp
firewall-cmd --permanent --add-port={88,464,123}/udp

firewall-cmd --reload
```

Check open ports:
```bash

firewall-cmd --reload
```

Accquire kerberos ticket:

```bash
kinit admin
```

Screenshoot:
![ipa_server_install_04](https://github.com/user-attachments/assets/1dd586cb-d005-4ba8-9c27-8d8559479b4b)


Freeipa installed:
![free_ipa_installed](https://github.com/user-attachments/assets/c11b07c2-6441-47ba-a80f-55f1fdede06f)





