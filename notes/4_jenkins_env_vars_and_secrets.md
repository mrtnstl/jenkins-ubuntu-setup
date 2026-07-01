<img src="../assets/jenkins.png" alt="Jenkins Logo" height="40"/>

# environment variables and secrets

environment variables and secrets are used to store configuration settings and sensitive information for Jenkins jobs and pipelines.

## Prerequisites

- A set up [Ubuntu Server](1_ubuntu.md) with [Jenkins](2_jenkins.md) installed

## Steps

1. [environment variables](#1-environment-variables)
2. [secrets](#2-secrets)

### 1. environment variables

1. Define environment variables in a job or pipeline configuration.

   - For a freestyle job, go to the job configuration page and add variables under `Build Environment` or `Environment variables`.
   - For a pipeline job, define them in the `environment` block in the Jenkinsfile.

2. Example for a freestyle job.

   ```bash
   VAR_NAME=example_value
   ```

   This value can then be referenced during the build steps with `$VAR_NAME` in shell scripts.

3. Example for a pipeline job.

   ```groovy
   pipeline {
       agent any
       environment {
           APP_NAME = 'my-app'
           DEPLOY_ENV = 'staging'
       }
       stages {
           stage('Example') {
               steps {
                   echo "Deploying ${APP_NAME} to ${DEPLOY_ENV}"
               }
           }
       }
   }
   ```

   Reference them with `${VAR_NAME}` inside the Jenkinsfile.

### 2. secrets

[Back to Steps](#steps)