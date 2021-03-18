<properties
	pageTitle="SNI Read Timeout - Low Confidence"
	description="SNI Read Timeout - Low Confidence"
	infoBubbleText="SNI Read Timeout - Low Confidence"
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, swbhartims"
	ms.author="subbuk, swbharti"
	displayOrder=""
	articleId="IsSniReadTimeoutLowConfidence_2F61B012-A494-48DB-89DB-2648DB148BD3"
	diagnosticScenario="SqlConnectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
This is typically a client side error involving high resource contention or network slowness. To prevent trickle attacks, we forcibly terminate these slow connections and you would receive pre-login timeout errors. 
<!--/issueDescription-->

## **Recommended Steps**

* Check to see if TCP connection forcibly closed error was received. If yes, check Client machine resource contention (CPU in specific) as this may cause clients to send packets much slower than normal. Note that single-core CPU contention could easily cause this, observing max (core) is recommended.

* Intermittent network latency may also cause this slowness, however in this case the impact will not be limited to one resource/customer. Retry the operation.

