<img src="./assets/jenkins.png" alt="Jenkins Logo" height="40"/>
<img src="./assets/Ubuntu-Dark-Digital.png" alt="Ubuntu Logo" height="40" style="margin-left: 20px;"/>

# Jenkins Ubuntu Setup

This repository contains concise documentation and setup notes for Jenkins CI/CD on Ubuntu.

## Overview

These notes capture the steps I used to configure a working Jenkins environment, including:

- Ubuntu base setup and system preparation
- Jenkins installation and initial configuration
- Jenkins cloud agent setup for distributed builds

## Contents

1. [Ubuntu setup](./notes/1_ubuntu.md)
   - System preparation, package updates, user configuration, and firewall settings.
2. [Jenkins installation](./notes/2_jenkins.md)
   - Jenkins installation, service setup, and initial security configuration.
3. [Cloud agent setup](./notes/3_jenkins_cloud_agent.md)
   - Configuration of cloud-based build agents for scalable CI/CD workloads.
4. [Defining env vars and secrets](./notes/4_jenkins_env_vars_and_secrets.md)
    - Managing environment variables and secrets.
5. [Creating freestyle jobs](./workflows/freestyle_jobs.md)
   - Creating and managing freestyle jobs.
6. [Creating pipeline jobs](./workflows/pipelines.md)
   - Creating and managing pipeline jobs.

## Usage

Use this repository as a reference for replicating a Jenkins environment on Ubuntu. Each note is written to support reproducibility and practical deployment.

## Notes

This is a personal project intended to document real-world Jenkins experimentation and infrastructure setup.