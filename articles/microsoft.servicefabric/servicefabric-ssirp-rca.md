<properties
	pageTitle="SSIRP customer communication"
	description="Customer communication for SSIRP affected clusters"
	infoBubbleText="Attention! This Service Fabric cluster will be affected by the upcoming SSIRP change"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	articleId="servicefabric-ssirp-rca"
	diagnosticScenario="ssirpbreakingchange"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_ServiceFabric"
/>

# Attention! This Service Fabric cluster will be affected by the upcoming SSIRP change

<!--issueDescription-->
We have identified the Service Fabric cluster **<!--$sfclustername-->sfclustername<!--/$sfclustername-->** under subscription **<!--$subscriptionid-->subscriptionid<!--/$subscriptionid-->** and resource group **<!--$resourcegroup-->resourcegroup<!--/$resourcegroup-->** as likely to be impacted by an upcoming security change, which could cause service interruptions to this cluster. 

To avoid service interruptions, we recommend upgrading your Service Fabric cluster to a supported version. See [this public guide](https://gist.github.com/athinanthny/f2191b93a3caea87446a73feacc66c79#upgrade--azure-service-fabric-clusters-by-november-20th-2020) for FAQs, more details on what’s changing, and how to upgrade. 

If you have other Service Fabric clusters under this or any other subscription, use this [script(CheckIPProviderEnabled.ps1)](https://gist.github.com/athinanthny/f2191b93a3caea87446a73feacc66c79#c-upgrade-pre-requisite) to check if they are impacted or not.

If you still have any follow up questions on this, contact us.<br>

Thank you.<br>
<!--/issueDescription-->
