# Configure MariaDB Ansible & Manually

# Early Opening
This is the configuration how to setup Mariadb Server and client on ubuntu server on AWS, GCP or in any cloud provider, I made this just for my documentation and if it is useful for others to use, that's great.

there are two configuration settings, namely using Ansible and Manually, if you want to setup with Ansible you can enter a folder with the name Ansible, Ansible is perfect for avoiding human error or misconfiguration, and the second one can be configured manually you can open the folder with the name Manually, manually this good for sparse configurations.

# How to use it ?

⚙ Manually Setup MariaDB

```
Enter the Manually folder and just follow the prompts.
```

⚙ Ansible Setup MariaDB

1. The following is the configuration that Ansible must have, namely ansible.cfg, hosts, key.pem in the key folder.

![Screen Shot 2023-07-17 at 13 11 58](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/f917b95d-d9e8-4c1e-bf99-2b31fbfbf6d6)

2. Ansible.cfg settings to point to keys and inventory/hosts in the file.

![Screen Shot 2023-07-17 at 13 08 25](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/ce5206de-6659-4505-9475-42376691a811))

3. Enter the host that you have on AWS or GCP Cloud Provider.

![Screen Shot 2023-07-17 at 13 11 44](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/eb99cbad-53d9-4302-bdef-c1aeb9157a82)

4. Add a key to enter the server, which is available from AWS.
    
![Screen Shot 2023-07-17 at 21 14 18](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/a2f47506-81b2-4aab-b687-6746a01e77a0)

5. You can change password mysql root in Ansible/mariadb/vars/main.yml:

```
ansible-vault edit main.yaml
```

![Screen Shot 2023-07-17 at 12 38 00](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/6f66530a-16e2-4992-a67d-8f9df0d0cb71)

6. Running Ansible Playbook and Input password prompt

```
ansible-playbook -vv mariadb.yaml --ask-vault-pass
```
```
password vault : admin1234
```
