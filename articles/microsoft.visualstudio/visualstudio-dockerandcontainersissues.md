<properties
	pageTitle="Docker & Containers"
	description="Issues with building, creating, or publishing container images"
	infoBubbleText="Azure Pipelines issues related to Docker tasks"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelinesDockerIssues"
	supportTopicIds="32742308"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of docker tasks for building and pushing container images

## **Recommended Steps**

Are you facing one of these common problems?

* I'm unable to configure and build a Linux container image on Windows Server 2016 

    Linux container (LCOW) is an advanced feature and only supported by [Windows 10 Professional and Windows 10 Enterprise](https://docs.microsoft.com/en-us/virtualization/windowscontainers/quick-start/quick-start-windows-10-linux), or Windows Server 2019 version 1809 or later. You can turn to either  Windows 10 Professional/Enterprise/Windows Server 2019 version 1809+ or hosted agent. The following links will help in this regard:

* I'm not able to pull .env file present in securefiles and use it in my dockerFile while running the azure pipelines

	Make sure the file stored in secure files is not added in .gitignore file of your repository. The .env files are not involved in the “build and push” task. However, When you run the image, you can specify .env files.

* Insufficient space in docker VM used to build images

    Try configuring an agent on VM with a different configuration. Ensure their is enough space available on on the VM.

* **docker pull** is not fetching current/correct docker images from ACR

    Remove all the existing images and containers running for the particular version. Build and push the image again to the container registry. Also, if you have a docker-compose.yml defined, then the **docker-compose up** command will ideally start or restart all the services defined in the Dockerfile. Then execute the **docker run** command which will run the image.

* I need guidance on using the Docker Build  & Docker push tasks in Azure Pipelines

	You can refer to the steps outlined in the following documents to build and push container images
    - [Build an image](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/containers/build-image?view=azure-devops)
    - [Push an image](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/containers/push-image?view=azure-devops)


## **Recommended Documents**

* [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md)
* [Build and push Docker images](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops)
