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
	cloudEnvironments="public"
/>

# I cannot deploy a JAR package
First of all, due to known limitation, you cannot upload JAR package via the portal or ARM template.

When you deploy your application package thought [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli), it will periodically poll the deployment progress, and in the end, it will show the deployment result.

If the polling is interrupted, you can still use the following command to fetch the deployment logs:

`az asc app show-deploy-log -n <app-name>`

Please make sure that you application is packaged in the correct [executable jar format](https://docs.spring.io/spring-boot/docs/current/reference/html/executable-jar.html). If not, you will see an error like the following:

`Error: Invalid or corrupt jarfile /jar/38bc8ea1-a6bb-4736-8e93-e8f3b52c8714`

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
* Azure Spring Cloud Deployment: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/deploy-an-app.md`
