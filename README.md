# FreeIPA-Keyclock-Fiber
Keyclock and FreeIPA integration on RHEL-8, fiber for backend 


1. RHEL-8 installation
![Screenshot from 2025-01-08 21-29-30](https://github.com/user-attachments/assets/197d4efb-9d0b-46e7-84d7-42119f4bf599)

2. FreeIPA installation


Steps:

Check current hostname:
```bash
hostname -f
```
Change hostname to "josip.keresman-asbp.local"
```bash
hostnamectl set-hostname "josip.keresman-asbp.local"
```
Make sure that hostname was changed succesffully

```bash
hostname -f
```
![hostname](https://github.com/user-attachments/assets/6581c484-579b-4a7b-b601-995d10669ae0)


Check our local IP address:
```bash
ifconfig
```
Screenshoots:

![ifconfig](https://github.com/user-attachments/assets/fca448b4-2666-49cc-9d5b-d16a1cb09d0f)



Open /etc/hosts/ with editor of choice and set (IP address and hostname):

```bash
su vi /etc/hosts/
```
Save the changes after editing.


Screenshot:
![etsi](https://github.com/user-attachments/assets/eb4cabab-f021-40dd-9488-3954a9aeafab)


Enable baseos and appstream

```bash
subscription-manager repos --enable-rhel-8-for-x86_64-baseos-rpms
subscription-manager repos --enable-rhel-8-for-x86_64-appstream-rpms
```

```bash
yum module list idm
yum module enable idm:DL1
yum module install idm:DL1/dns
```
Screenshot:

![idm_module_list](https://github.com/user-attachments/assets/103a0ebe-057d-4022-8a8e-493df14065f6)


Installation of free ipa LDAP server:

![install_ipa_01](https://github.com/user-attachments/assets/e3433dee-d28c-4a1b-a058-e05fe24a7856)
![install_ipa_02](https://github.com/user-attachments/assets/f7ffddb1-0a9c-4247-bf30-8204a8b32f5d)
![ipa_install_03](https://github.com/user-attachments/assets/eaf531a0-c5c0-48f5-9b31-36ff8286c18e)
![ipa_install_04](https://github.com/user-attachments/assets/f6f4a71b-2b9f-45c9-a1bb-3a8d7ed07285)




