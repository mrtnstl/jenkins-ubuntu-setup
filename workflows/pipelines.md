<img src="../assets/jenkins.png" alt="Jenkins Logo" height="40"/>

# pipeline jobs

pipelines provide a version-controlled and reusable way to define CI/CD workflows. 

## Sections

1. [Quick start](#1-quick-start)
   - Spinning up a basic pipeline.

## 1. Quick start

### 1. create a new pipeline job

1. Open Jenkins and click `New Item`.
2. Enter a job name, select `Pipeline`, and click `OK`.

### 2. define the pipeline

1. In the job configuration page, choose the pipeline definition method you want to use.
2. Add a Jenkinsfile with the stages for checkout, build, test, and deployment.
3. Save the job once the pipeline script is in place.

### 3. run and review the pipeline

1. Click `Build Now` to start the pipeline.
2. Open the build details and review the stage view or console output to verify each step.

### 4. improve the workflow

1. Use parameters, post actions, and environment variables to make the pipeline more flexible.
2. Store the Jenkinsfile in source control so the pipeline can be versioned and reused.

[Back to Contents](#sections)
