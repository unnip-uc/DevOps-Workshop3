# Devops Workshop 3: Log Management

Welcome to the Devops Workshop 3! In this hands-on workshop, we will explore what is log management, why is it important
and the power of the ELK Stack (Elasticsearch,
Logstash, Kibana) as part of our DevOps journey. Throughout this workshop, you will learn how to harness the
capabilities of ELK Stack to centralize, parse, analyze, and visualize logs generated by your applications.

## Prerequisites

- Machine/VM with ubuntu 22.04
- [Docker](#Install Docker)
- [Git]( https://www.atlassian.com/git/tutorials/install-git#linux )
    - [Create github account](https://github.com/signup)
    - [Setting up SSH key with GitHub for Ubuntu](https://medium.com/featurepreneur/setting-up-ssh-key-with-github-for-ubuntu-cd8f2fabf25b)
- [VS code IDE]( https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-20-04/ )
- Stable Internet Connection and any browser.

## Workshop environment setup

- Check if Git, Docker, and Docker Compose are installed in on the system. Open the terminal and run the following
  command
  ```shell
  $ git --version
  git version 2.25.1

  $ docker --version
  Docker version 20.10.17, build 100c701

  $ docker compose version
  Docker Compose version v2.6.0

  ```
- Open terminal and run following command to create a folder called workshop
   ```shell
   $ mkdir workshop
   ```
- Navigate to the folder workshop and clone the from your personal repo using git
   ```shell
   $ cd workshop
   ```
- Clone DevOps-Workshop3 repo && go inside DevOps-Workshop3 folder
   ```shell
   $ git clone git@github.com:UniCourt/DevOps-Workshop3.git
   $ cd DevOps-Workshop3
   ```
- To open folder in VS code editor
   ```shell
   $ cd ~/workshop/DevOps-Workshop3
   $ code .
   ```

##### Install Docker

- If docker is not installed in your Linux run the following command
   ```shell
   $ sudo apt-get update
   $ sudo apt-get install -y curl 
   $ curl -fsSL https://get.docker.com -o get-docker.sh
   $ sudo sh get-docker.sh
  ```
- Do docker login
   ```shell
   $ sudo docker login -u username --password-stdin
   ```

#### Docker without sudo

- To run docker commands as normal user without sudo, we need to create a group for docker and add the user to it.

1. Create the docker group
    ```shell
    $ sudo groupadd docker
    ```
2. Add your user to docker group
    ```shell
    $ sudo usermod -aG docker $USER
    ```
3. Activate the changes to groups:
    ```shell
   $ newgrp docker
    ```
4. Verify that you can run docker commands without sudo.
    ```shell
   $ docker images
    ```

## Workshop Goals:

1. **Log Management**: Discover how to effectively manage logs in a centralized environment with Elasticsearch.
2. **Log Parsing**: Use Logstash to intelligently parse logs generated by the applications.
3. **Data Visualization**: Harness the power of Kibana to create stunning visualizations and dashboards. Make your logs
   accessible and easy to analyze.

## Schedule

| Time          | Topics                                                                           |
|---------------|----------------------------------------------------------------------------------|
| 09:00 - 09:30 | [`Why do we need logs? Importance of Log Management`](docs/logging_intro.md)   |
| 09:45 - 10:00 | [`The ELK stack`](docs/elk_stack_intro.md)                                     |
| 10:00 - 10:45 | [`Creating an web application with logs`](docs/create_app.md)                  |
| 10:45 - 11:30 | [`Configure logstash`](docs/logstash.md)                                       |
| 11:30 - 12:30 | [`Setting up ELK stack using docker-compose`](docs/elk_setup.md)               |
| 12:00 - 01:00 | [`Visualing the logs in kibana`](docs/kibana.md)                               |
| 01:00 - 02:00 | [`Break`]                                                                        |
| 02:00 - 03:30 | [`Adding more configurations for logstash`](docs/configure_logstash_part_2.md) |
| 03:00 - 03:30 | [`Elasticsearch APIs`](docs/elasticsearch_api.md)                              |
| 03:30 - 03:45 | [`Best practices`](docs/best_practices.md)                                     |                        |
| 03:45 - 04:00 | [`Q & A`]                                                                        |
| 04:00 - 04:10 | [`Wrapping Up`]                                     |
