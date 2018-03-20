<properties
	pageTitle="Installing the gateway service on Server Core"
	description="How to install the Server management tools gateway on Windows Server Core"
	service="microsoft.servermanagement"
	resource="gateways"
	authors="jol"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake"
/>

# Installing the gateway service on Server Core

## **Recommended steps**

* The gateway service can be installed on Windows Server 2012/R2, Windows Server 2016 Full Installation or Server Core. To install on Server Core, use the following command to install the GatewayService.msi via command line. A certificate is required to securely store the credentials to connect to your target machines and using the following command options will generate a self-signed certificate for this purpose.<br>
**GatewayService.msi /qn GATEWAYPROFILEJSON=.\profile.json ACCEPTEULA=true ACCEPTPRIVACYPOLICY=true**
* To use an existing certificate installed on the machine, use the following command options. Replace **EnterThumbprintHere** with your certificate encryption thumbprint.<br>
**GatewayService.msi /qn GATEWAYPROFILEJSON=.\profile.json ACCEPTEULA=true ACCEPTPRIVACYPOLICY=true ENCRYPTION_CERTIFICATE_OPTION=root ENCRYPTION_THUMBPRINT=EnterThumbprintHere**

