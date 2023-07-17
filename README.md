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

![Screen Shot 2023-07-17 at 13 08 25](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/014edf16-8c2f-4296-b567-f8b01fde5354)

3. Enter the host that you have on AWS or GCP Cloud Provider.

![Screen Shot 2023-07-17 at 13 11 44](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/de37f4bb-1440-4cf2-8b48-e597eaef5a57)

4. Add a key to enter the server, which is available from AWS.
    
![Screen Shot 2023-07-17 at 13 36 08](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/fa88d24c-68c6-44fd-875e-d28aceedd542)

5. You can change password mysql root in Ansible/mariadb/vars/main.yml:

```
ansible-vault edit main.yaml
```

![Screen Shot 2023-07-17 at 12 38 00](https://github.com/fahmifiqih1/MariadbConfig/assets/53596721/2ceec386-06f0-4085-b217-ff43b1e13dd5)

6. Running Ansible Playbook and Input password prompt

```
ansible-playbook -vv mariadb.yaml --ask-vault-pass
```
```
password vault : admin1234
```
