<properties
  pagetitle="Azure Pipelines issues deploying to Azure Web Apps or App Services"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="cathmill"
  selfhelptype="Generic"
  supporttopicids="32742304"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesazurewebappissues"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines issues deploying to Azure Web Apps or App Services

Resolve common issues while deploying to Azure Web Apps or App Services from Azure Pipelines by using the steps below.

## **Recommended Steps**

* I am seeing the error **No package found with specified pattern** in the task

	* Check if the package mentioned in the task is published as an artifact in the build or in a previous stage, and is downloaded in the current job

* My task fails with error **Publish using zip deploy option is not supported for msBuild package type**

	* Web packages created using MSBuild task (with default arguments) have a nested folder structure that can only be deployed correctly by Web Deploy. Publish to zip deploy option cannot be used to deploy those packages. To convert the packaging structure, follow [these steps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#error-publish-using-zip-deploy-option-is-not-supported-for-msbuild-package-type).

* The task fails with **5xx error** code

	* Check the [status of your Azure service](https://status.azure.com/status) and the [status of Azure DevOps Services](https://status.dev.azure.com/) to see if either are experiencing an outage related to your issue.

* A release hangs for a long time and then fails or seeing **500 service unavailable** or **failed to update deployment history** errors in the deployment logs

	* This may be because there is insufficient capacity on your App Service Plan. To resolve this, you can scale up the App Service instance to increase available CPU, RAM, and disk space, or try with a different App Service plan. 

	* Check the kudo logs for your App Service app, also.

* The task fails with the error: **Could not fetch access token for Azure. Verify if the Service Principal used is valid and not expired**

	* Verify validity of the service principal used and that it's present in the app registration. For more details, see [Use Role-Based Access Control to manage access to your Azure subscription resources.](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal).

	* Check the [Azure Resource Manager service connections Troubleshooting doc](https://docs.microsoft.com/azure/devops/pipelines/release/azure-rm-endpoint?view=azure-devops)

* I am seeing an **SSL error** in the App Service or Web App deploy task

	* To use a certificate in App Service, it must be signed by a trusted certificate authority. See [SSL errors](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#ssl-error) to resolve this error.

* I am seeing a **Web Deploy Error** in the App Service deploy task

	* If you are using web deploy to deploy your app, in some error scenarios, Web Deploy will show an error code in the log. To troubleshoot a web deploy error, see [web deploy error codes](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes).

* I am seeing **ERROR_FILE_IN_USE** while trying to deploy to Azure Web App

	* To resolve [ERROR_FILE_IN_USE](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#error_file_in_use) errors, ensure **Rename locked files** and **Take App Offline** options are enabled in the task. For zero downtime deployments, use slot swap.  You can also use **Run From Package deployment** method to avoid resource locking.

* Web app deployment on Windows is successful, but the app is not working

	* This might be because `web.config` is not present in your app. To add a `web.config`, follow [these steps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#web-app-deployment-on-windows-is-successful-but-the-app-is-not-working).

* Web app deployment on **App Service Environment (ASE)** is not working

	* [Follow these steps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#web-app-deployment-on-app-service-environment-ase-is-not-working) to ensure you are deploying correctly

* See the tutorials about deploying apps of various languages to an Azure Web App:
	- [Python to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops)
	- [PHP to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/php-webapp?view=azure-devops)
	- [Java to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/java-webapp?view=azure-devops&tabs=java-tomcat)
	- [JavaScript and Node.js to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/javascript?view=azure-devops&tabs=code)

## **Recommended Documents**

* [App Service Deploy task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#troubleshooting)
* [Azure Web App task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#troubleshooting)
* [Azure Web Apps for Container task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-containers?view=azure-devops#troubleshooting)
* [Deploy to Linux Web App](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp-linux?view=azure-devops&tabs=dotnet-core%2Cyaml)
* [Deploy to Windows Web App](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp?view=azure-devops&tabs=yaml)
* [Deploy to Web App for Containers](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp-on-container-linux?view=azure-devops&tabs=dotnet-core%2Cyaml)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
