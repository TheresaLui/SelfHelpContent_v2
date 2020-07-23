<properties
	pageTitle="Sporadic VM network issues/partitions"
	description="Sporadic VM Network Issue"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="91c6a0d9-4ef6-4dae-a0f5-6651ca7d4c31"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Sporadic VM network issues/partitions

Cluster startup failure with **User facing error**: *Cluster terminated. Reason: Metastore Component Unhealthy.*

## Troubleshooting

1. Do below tests to verify Metastore is available and responding or atleast the driver can send the request:

*%sh telnet <metastore-endpoint-or-ip> 3306*

**Note:**
You can get metastore IP address from [here](https://docs.microsoft.com/en-us/azure/azure-databricks/mysql-ip-address?toc=/azure/databricks/toc.json&bc=/azure/databricks/breadcrumb/toc.json#updated-mysql-ip-addresses) for different regions.

Example:

*%sh telnet consolidated-westus-prod-metastore.mysql.database.azure.com 3306*
*Trying 23.99.34.75... Connected to cr1.westus1-a.control.database.windows.net . Escape character is '^]'.*

If you don't see the output as above, issues could be due to firewall, SQL endpoint not whitelisted etc...

2. Once we have confirmed Metastore is responding, it could be that connection is flaky. Run below command from notebook multiple times and confirm if connection can be reached and port is open:

*%sh  nc -zv <metastore-endpoint-or-ip> 3306*

Example:

*%sh  for i in {1..10} ; do nc -zv consolidated-westus-prod-metastore.mysql.database.azure.com 3306*
*done*
*Unknown host cr2.westus1-a.control.database.windows.net  [104.42.238.205] 3306 (mysql) open*
*Unknown host cr2.westus1-a.control.database.windows.net  [104.42.238.205] 3306 (mysql) open*

If below error is hit randomly it means route to consolidated-westus-prod-metastore.mysql.database.azure.com is randomly flaky:

*Error: java.sql.SQLNonTransientConnectionException: Could not connect to address=(host=consolidated-westus-prod-metastore.mysql.database.azure.com )(port=3306)(type=master) : Connection timed out (Connection timed out)*

## Solution

1. If you are not able to reach the metastore from driver via telnet, please check Vnet peering is setup correctly or endpoints are still valid etc
2. If all setup looks fine one workaound would be to stop cluster and wait 5 mins after a failed launch to make sure that driver node does not get reused (Incase if the driver node was bad).

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) if needed.