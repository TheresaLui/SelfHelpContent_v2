<properties
	pageTitle="Database Connectivity issue due to login timeout detected"
	description="IsSniReadTimeoutDuringXdbhostDuplication"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="aamalvea"
    ms.author="aamalvea"
	displayOrder=""
	articleId="IsSniReadTimeoutDuringXdbhostDuplication_8BDA22D6-4005-4359-94E6-D3C636CE99C6"
	diagnosticScenario="SqlConnectivity"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your application/client, which was connecting to database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> has taken too long to respond during the login request, so the login request was terminated. This behavior is by design. As a protection, Azure SQL Database endpoints forcibly terminate connections when the client login packets take several seconds to arrive to our service.

In most cases, the cause of this problem is high resource contention on the client side, where Client resources (such as CPU, threads, memory) cause packets to be sent slower than usual. In rare conditions, SNI-read-timeouts can also be caused by intermittent network latency.

From our telemetry, we have found that in most cases this condition occurs when the client is processing the TLS handshake. Typically, this pattern indicates high single-core CPU pressure on the client VM.

<!--/issueDescription-->
