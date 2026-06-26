# ubuntu server setup

server setup. will extend it along the way.

## 1. initial setup

1. update && upgrade

2. set up openssh ([official how to](https://ubuntu.com/server/docs/how-to/security/openssh-server/))

3. set up hostname and hosts file if needed

## 2. adding baseline security

1. adding new user (because one shouldn't necessarily use the root user)

    create user with `sudo adduser <username>` and look up `cat /etc/passwd` and/or `ls -l /home` to confirm

    add user to sudoers with `usermod -aG sudo <username>` and confirm `groups <username>`, switch user account with `su - <username>` then run `apt update` to test the permission

2. set up ssh key (generate it locally, on your pc)

    `ssh-keygen -t ed25519`

    confirm generation with `ls ~/.ssh`

3. associate ssh key with server

    `ssh-copy-id -i ~/.ssh/id_er25519 <username>@<server_address>`

4. tweak ssh config at */etc/ssh/sshd_config*

    ```
    PermitRootLogin no
    PasswordAuthentication no
    ```

5. restart ssh service with `systemctl restart ssh`
