<properties
	pageTitle="IP filter"
  	description="IP filter"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="83"
	selfHelpType="resource"
	supportTopicIds="32597559"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Connecting to Azure Cosmos DB accounts

If you are having connectivity issues, you may have not included your IP address or range within the list of whitelisted IP addresses in your account's networking configuration. To configure IP policy-based access control, the user must provide the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account. Once this configuration is applied, all requests originating from machines outside this allowed list are blocked by the server. 

## **Recommended documents**

* [Firewall support](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
