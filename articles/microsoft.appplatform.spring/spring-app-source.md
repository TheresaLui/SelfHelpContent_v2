<properties
	pageTitle="I cannot deploy a source package"
	description="I cannot deploy a source package"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-source"
	displayOrder="6"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# I cannot deploy a source package
First of all, due to known limitation, you cannot upload source package via the portal or ARM template.

When you deploy your application package thought [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli), it will periodically poll the deployment progress, and in the end, it will show the deployment result.

If the polling is interrupted, you can still use the following command to fetch the build and deployment logs:

`az spring-cloud app show-deploy-log -n <app-name>`

However, please note that one Azure Spring Cloud service instance can only trigger one build job for one source package at one time. For more information about the deployment, please refer to [Tutorial: Prepare a Java Spring app for deployment](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-tutorial-prepare-app-deployment).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Tutorial: Prepare a Java Spring app for deployment](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-tutorial-prepare-app-deployment)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
