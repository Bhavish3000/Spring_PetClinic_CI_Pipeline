# Spring Petclinic CI Pipeline
This document provides a guide to setting up a Continuous Integration (CI) pipeline for the Spring Petclinic project using Azure DevOps.

## Overview
* This pipeline is designed to:

* Build the project using Maven.
* Run unit tests and publish test results.
* Package the application into a .jar file.
* Publish build artifacts for deployment or further use.

## Steps to Use the Pipeline
* Clone the Spring Petclinic Repository
**git clone https://github.com/spring-projects/spring-petclinic.git**
* Before setting up the pipeline, clone the project locally or integrate it directly in Azure DevOps:

## Steps
* Set Up the Pipeline in Azure DevOps
* Log in to Azure DevOps.
* Navigate to Pipelines > Create Pipeline.
* Connect to your repository (either GitHub or another Git source).
* Create a YAML file in repository and copy the pipeline to it.
* Point Azure DevOps to the pipeline YAML file in your repository.
  ![alt build]("C:\Users\BHAVISH\Desktop\spc\images\build_sucesses.png").
**Pipeline Features**
1. Triggers
2. Automatic builds: Triggered on changes pushed to the main branch.
3. Scheduled builds: Runs daily at 1 hour.

### JDK Version
* The pipeline supports configurable JDK versions. **Default is 1.17.** Supported options:
**1.17**
**1.11**
**1.10**
**1.9**
**1.8**

### Build Steps
**Maven Build:**
* Executes clean package Maven goals.
* Runs unit tests and publishes JUnit test results.
* Uses the JDK version specified in the pipeline parameters.

### Artifact Management:

* Copies .jar files to a staging directory.
* Publishes build artifacts for download or further pipeline stages.

### Outputs
* Build Artifacts: .jar files are published for use in deployments.
  ![alt Artifact]("C:\Users\BHAVISH\Desktop\spc\images\artifact.png").
* Test Results: JUnit results are displayed in the Azure DevOps pipeline summary.
  ![alt test_results](C:\Users\BHAVISH\Desktop\spc\images\test_resu;t.png).

### Troubleshooting
#### Common Issues
* Invalid JDK Version: Ensure the specified version matches one of the supported options.
* Missing Artifacts: Verify that the Maven build generates .jar files in the expected location.
* Repository Access Issues: Confirm that the Spring Petclinic repository is accessible.

### Resources
**Spring Petclinic GitHub Repository**
**Azure DevOps Documentation**

# Happy building! 🚀