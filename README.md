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
Check our local IP address:
```bash
ifconfig
```
Screenshoots:

![Screenshot from 2025-01-08 22-36-46](https://github.com/user-attachments/assets/bc682c8c-669c-499e-8457-c3eac3f44fd9)


Open /etc/hosts/ with editor of choice and set (IP address and hostname):

```bash
su vi /etc/hosts/
```
Save the changes after editing.


Screenshot:

![etchosts](https://github.com/user-attachments/assets/637defa1-0108-4e99-ab72-8d9fb28f41e4)


```bash
dnf module list idm
```

Screenshot:

![idm_module_list](https://github.com/user-attachments/assets/103a0ebe-057d-4022-8a8e-493df14065f6)

```bash
dnf module list idm
dnf -y install @idm:DL1
dnf -y install freeipa-server
```


