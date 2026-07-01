<img src="../assets/jenkins.png" alt="Jenkins Logo" height="40"/>

# freestyle jobs

freestyle jobs are simple to create and well suited for basic build, test, and deployment tasks. 

they are less reusable and more difficult to maintain for complex workflows compared with pipelines.

## Sections

1. [Quick start](#1-quick-start)
   - Spinning up a basic job.

## 1. Quick start

### 1. create a new freestyle job

1. open Jenkins and click `New Item`.
2. enter a job name, select `Freestyle project`, and click `OK`.

### 2. configure the job

1. in the job configuration page, set a description and choose the appropriate repository or source location.
2. under `Triggers`, enable the trigger that fits the workflow, such as polling or a webhook.
3. under `Build Steps`, add commands or scripts to run the build, tests, or deployment actions.

### 3. save and run

1. click `Save` to store the configuration.
2. click `Build Now` to run the job and review the console output for results.

### 4. review results

1. check the build status and logs to confirm whether the job succeeded or failed.
2. use the `Console Output` page to troubleshoot issues and refine the configuration.

[Back to Contents](#sections)