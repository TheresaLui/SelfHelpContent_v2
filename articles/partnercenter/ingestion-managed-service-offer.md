<properties
	pageTitle="Partner Center - Ingestion - Managed service offer"
	description="Partner Center - Ingestion deflection article"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="a-coflor"
	ms.author="a-coflor"
	displayOrder=""
	articleId="partnercenter_ingestion_managed_service_offer"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32781163"
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17006"
	cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
	ownershipId="PartnerCenter_Ingestion"
/>

# Partner Center Ingestion - Managed service offer
 
## **Recommended Steps**

* Create a manifest with authorization information for managing customer resources. This information is required in order to enable [Azure delegated resource management](https://docs.microsoft.com/en-us/azure/lighthouse/concepts/azure-delegated-resource-management).
* The users and roles in your Authorization entries will apply to every customer who activates the plan. If you want to limit access to a specific customer, you'll need to publish a private plan for their exclusive use.

## **Recommended Documents**

* [Technical configuration for your Managed Service offer](https://docs.microsoft.com/azure/marketplace/create-managed-service-offer-plans#technical-configuration)
* [How to plan a Managed Service offer](https://docs.microsoft.com/azure/marketplace/plan-managed-service-offer)
