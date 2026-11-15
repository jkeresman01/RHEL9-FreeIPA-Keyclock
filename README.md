# RHEL9-FreeIPA-Keyclock
Keyclock and FreeIPA integration on RHEL-9


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



![free_ipa_installe![appache_server_01](https://github.com/user-attachments/assets/a4b8e5f3-73f4-446e-a371-fea6f0ca546c)


![enable_mariadb](https://github.com/user-attachments/assets/3011cfb9-357e-4855-b766-fba07eed0197)
![add_new_user](https://github.com/user-attachments/assets/0dc8dbca-338f-4afb-8d02-6247c94790ce)
![wp_saml_01](https://github.com/user-attachments/assets/32072868-9f0d-4653-b552-6ea9a571bfa6)
![wordpress_install_03](https://github.com/user-attachments/assets/283f286a-82ca-40ee-8dc7-a90c5d899593)
![wordpress_install_02](https://github.com/user-attachments/assets/094e8d7c-dd56-4bf7-a180-f997da9b2392)
![test](https://github.com/user-attachments/assets/6f669086-912a-4f43-b938-ab86773acd58)
![sso_button_added](https://github.com/user-attachments/assets/8626f615-549e-4772-b628-73d405238925)
![php_install_package](https://github.com/user-attachments/assets/38dbf9b0-e9f8-47c0-b008-7f96c2d825ea)
![mini_orange_05](https://github.com/user-attachments/assets/48457597-7fd6-43ab-a8c4-d5ae1f58e123)
![mini_orange_04](https://github.com/user-attachments/assets/69840c3b-120d-4363-a8a2-843f0c58c38d)
![mini_orange_03](https://github.com/user-attachments/assets/0b095e0f-40ff-477a-9032-b9a138a88413)
![mini_orange_01](https://github.com/user-attachments/assets/dcaf36ff-5b69-45e9-9e03-54aa4d3310ea)
![maria_db_show_db](https://github.com/user-attachments/assets/a044190e-d9ff-4e8a-9abf-f03a1459d5c9)
![maria_db_install_01](https://github.com/user-attachments/assets/4216b750-435d-4e92-ae6d-6b7201b511c3)
![keycloack_setup_11](https://github.com/user-attachments/assets/b5bde088-11c0-4158-99c1-06909784eab6)
![keycloack_setup_10](https://github.com/user-attachments/assets/c4f6ca39-e176-4687-a619-82ca13501a87)
![keycloack_setup_09](https://github.com/user-attachments/assets/8c569c7e-5837-4dbb-8ffc-f486e447074d)
![keycloack_setup_07](https://github.com/user-attachments/assets/a9a2f736-8d5c-4602-8841-79fd6a3e9af1)
![keycloack_setup_06](https://github.com/user-attachments/assets/d61e1735-0e91-4db2-acf7-babb8e989b17)
![keycloack_setup_05](https://github.com/user-attachments/assets/44370c24-62a4-404f-b204-6fcd75f517ba)
![keycloack_setup_02](https://github.com/user-attachments/assets/620dde64-b881-4d40-bb85-41096e7e96c6)
![keycloack_setup_1](https://github.com/user-attachments/assets/ea5242ac-e0bd-4fdd-87f3-1419cfa70e49)
![keycloack_setuo_04](https://github.com/user-attachments/assets/060afbd5-7f35-421f-95f0-5b491aa54137)
![keycloack_install_05](https://github.com/user-attachments/assets/d9a74b8d-e2f2-4595-b59d-65e98db7b727)
![keycloack_install_04](https://github.com/user-attachments/assets/6e3c1173-ba76-47a7-9faa-36a0ff913f2e)
![keycloack_install_03](https://github.com/user-attachments/assets/0ae2dc9c-faca-4aab-badc-2cb2ca1ab57c)
![keycloack_install_01](https://github.com/user-attachments/assets/0995f22a-c54b-49c7-b7c8-126d25aae314)
![ipa_server_install_04](https://github.com/user-attachments/assets/7dd04884-c154-4f6c-8536-d4f43e72ef69)
![ipa_server_install_03](https://github.com/user-attachments/assets/9101ce9f-ec00-4479-881b-4da94376d19c)
![ipa_server_install_01](https://github.com/user-attachments/assets/6083d60d-c91a-4f14-bd56-cd926736bdd5)
![install_wp_web_02](https://github.com/user-attachments/assets/faded077-8c94-4c96-9fca-95eb53f411f7)
![install_wp_web_01](https://github.com/user-attachments/assets/e49be3d1-9b09-4300-8fe0-97d33028beee)
![grant_create_wordpress_db_final](https://github.com/user-attachments/assets/dc77dea3-b03c-426f-81cc-71c54d81ff1d)
![gran_all_second_correct_time](https://github.com/user-attachments/assets/4a2087c4-8739-4729-a1b3-71fa08b6ea7d)
![free_ipa_installed](https://github.com/user-attachments/assets/99678fbe-7646-4ab0-b3ca-ddf691cd8528)


