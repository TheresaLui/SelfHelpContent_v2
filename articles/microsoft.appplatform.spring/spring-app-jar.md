<properties
	pageTitle="I cannot deploy a JAR package"
	description="I cannot deploy a JAR package"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-jar"
	displayOrder="5"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# I cannot deploy a JAR package
At this time, you can't upload a JAR/source package via the portal or ARM template.

When you deploy your application package through the [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli), Azure CLI will periodically poll the deployment progress and will display the deployment result upon completion.

If the polling is interrupted, use the following command to fetch the deployment logs:

`az spring-cloud app show-deploy-log -n <app-name>`

Ensure that your application is packaged in the correct [executable jar format](https://docs.spring.io/spring-boot/docs/current/reference/html/executable-jar.html). If not, the following error may occur:

`Error: Invalid or corrupt jarfile /jar/38bc8ea1-a6bb-4736-8e93-e8f4b52c8714`

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Tutorial: Prepare a Java Spring app for deployment](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-tutorial-prepare-app-deployment)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
