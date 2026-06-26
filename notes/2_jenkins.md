# jenkins setup

everything jenkins related can be found at this [link](https://www.jenkins.io/doc/book/installing/linux/), in the official docs.

## 1. initial setup

1. set up java **[docs](https://www.jenkins.io/doc/book/installing/linux/#debian-java)**

2. set up Jenkins (LTS) **[docs](https://www.jenkins.io/doc/book/installing/linux/#debian-stable)**

3. starting Jenkins

    enable startup on boot with `sudo systemctl enable jenkins`

    check status with `sudo systemctl status jenkins`

4. set up firewall

    if applicable, add Jenkins as an exception to firewall rules

## 2. post-install setup

1. unlock Jenkins **[docs](https://www.jenkins.io/doc/book/installing/linux/#unlocking-jenkins)**

2. install suggested plugins

3. create admin user **[docs](https://www.jenkins.io/doc/book/installing/linux/#creating-the-first-administrator-user)**
