# jenkins docker cloud angent setup

With this setup, Jenkins will run the jobs on the local server using Docker. 
In a low trafic environment, running jobs on the server where the master node is hosted, could be acceptable.

## 1. environment setup

1. install docker [docs](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

2. add the `jenkins` user to `docker` group, so Jenkins can communicate with the Docker daemon through the docker.socket

    ```bash
    sudo usermod -aG docker jenkins
    ```

3. install `Docker plugin` in Jenkins

## 2. cloud and agent setup in Jenkins

1. add new cloud

    go to `Manage Jenkins`, then in System Configuration, click `Clouds` then `+ New cloud`

    New cloud
    ```
    Cloud name: your_cloud_name
    Type: Docker
    ```

    Docker Cloud details
    ```
    Docker Host URI: unix:///var/run/docker.sock
    Server credentials: [not needed]

    [x] enabled

    Container Cap: 5
    ```

    Docker Agent templates
    ```
    Labels: docker-agent-alpine
    [x] Enabled
    Name: docker-agent-alpine
    Docker image: jenkins/agent:alpine3.24-jdk21
    Instance Capacity: 2
    Remote File System Root: /home/jenkins
    ```

2. connect job to agent

    go to Jenkins dashboard, select a project, select `Configure`, then in the General section select `Restrict where this project can be run`, and set docker-agent-alpine as input to the `Label Expression` field