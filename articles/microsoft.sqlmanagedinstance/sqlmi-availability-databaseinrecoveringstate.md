<properties
	pageTitle="Database in Recovering state"
	description="Database in Recovering state"
	infoBubbleText="Database in Recovering state"
	service=""
	resource=""
	authors="srdan-bozovic-msft"
	ms.author="srbozovi"
	displayOrder=""
	articleId="fc0a77ec-b429-4278-9eef-108e8e6383cd"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637254"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public"
/>

# Database in Recovering state

## **Recommended steps**

- If there were active long-running transactions during instance failover, recovery process may take long time to complete log redo operation. In extreme situations consider point-in-time restore as a workaround option.