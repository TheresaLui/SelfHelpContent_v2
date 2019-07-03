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
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
This is typically a client side error involving high resource contention or network slowness. To prevent trickle attacks we forcibly terminate these slow connections and you would receive pre-login timeout errors. 
<!--/issueDescription-->
