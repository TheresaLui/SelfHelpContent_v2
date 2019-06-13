<properties
	pageTitle="Configure Custom Health Probes"
	description="Configure Custom Health Probes"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32582826"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
	articleId="2a61b4a8-67fa-417e-afe5-096cfc047dac"
/>

# Configure Custom Health Probes
Application Gateway's default health probe checks for the backend server on \<protocol>://127.0.0.1:\<port>/ where the protocol and port are inherited from the HTTP settings associated in the rule.

But if you want to configure a custom hostname and path for your probe, you need to create a custom health probe and associate with the HTTP Settings.

## **Recommended Steps**
To find number of probes per interval, use below formula: <br>
Probes per Interval = Backend Servers * Rules

## **Recommended Documents**
* Create a custom probe using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-probe-portal) or [PowerShell](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-probe-ps)
* Application gateway [health monitoring](https://docs.microsoft.com/azure/application-gateway/application-gateway-probe-overview) overview
