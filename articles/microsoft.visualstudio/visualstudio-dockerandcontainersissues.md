<properties
  pagetitle="Azure pipelines issues while making use of docker tasks for building and pushing container images to Azure"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,vimalt,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742308"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesdockerissues"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of docker tasks for building and pushing container images to Azure

Resolve common issues when making use of Docker tasks using the following solutions.

## **Recommended Steps**

* **I'm unable to configure and build a Linux container image on Windows Server 2016**<br>
Linux container (LCOW) is an advanced feature and only supported by [Windows 10 Professional and Windows 10 Enterprise](https://docs.microsoft.com/virtualization/windowscontainers/quick-start/quick-start-windows-10-linux), or Windows Server 2019 version 1809 or later. You can turn to either  Windows 10 Professional/Enterprise/Windows Server 2019 version 1809+ or hosted agent.

* **I'm not able to pull .env file present in securefiles and use it in my dockerFile while running the Azure pipelines**<br>
Make sure that the file stored in secure files is not added to the **.gitignore** file of your repository. The .env files are not involved in the **build and push** task. However, when you run the image, you can specify .env files.

* **Insufficient space in docker VM used to build images**<br>
Try configuring an agent on VM with a different configuration. Ensure there is enough space available on the VM.

* **Docker pull is not fetching current/correct docker images from ACR**<br>
Remove all the existing images and containers running for the particular version. Build and push the image again to the container registry. Also, if you have defined a docker-compose.yml file, then the **docker-compose up** command will ideally start, or restart, all services defined in the Dockerfile. Then, run the **docker run** command, which will run the image.

* **I need guidance on using the Docker Build and Docker push tasks in Azure Pipelines**<br>
 Refer to the steps outlined in the following documents to build and push container images:
    * [Build an image](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/containers/build-image?view=azure-devops)
    * [Push an image](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/containers/push-image?view=azure-devops)

## **Recommended Documents**

* [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md)
* [Build and push Docker images](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops)
* For service impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
