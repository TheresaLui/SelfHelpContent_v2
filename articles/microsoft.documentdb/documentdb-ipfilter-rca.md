<properties
	pageTitle="IP filter RCA"
	description="RCA - IP blocked by firewall"
	infoBubbleText="The IP address is not whitelisted for sending requests to account.See details on the right."
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="ipfilter_1FCDCD2C-E096-49C4-8A50-C53020F79757"
        diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds="32597522"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found an IP firewall rule on your account which is blocking access for one or more IP addresses
<!--/issueDescription-->
By default, Azure Cosmos DB database account is accessible from public internet as long as the request is accompanied by a valid authorization token. To configure IP policy-based access control, the user must provide the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account. Once this configuration is applied, all requests originating from machines outside this allowed list are blocked by the server. 
It appears that the current account has an IP access control policy which is restricting access to an IP range. Please follow this [link](https://docs.microsoft.com/azure/cosmos-db/firewall-support) for to update the IP access control policy on this account.
