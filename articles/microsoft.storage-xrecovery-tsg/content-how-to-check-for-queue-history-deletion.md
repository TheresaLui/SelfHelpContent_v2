<properties
	pageTitle="How to check for deletion history"
	description="How to check for deletion history"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="66df6877-5f61-4974-b556-3432791fc07f"
/>

# How to check for deletion history

1. Use sample query in Jarvis [Sample Geneva Logs Query](https://jarvis-west.dc.ad.msft.net/A6927181)
2. Query with the following settings in DGrep:

~~~dgrep

Endpoint: Diagnostics PROD (for public Azure)
Namespace: XStore
Events to search: DiagnosticAuditLog

~~~

3. Specify Tenant for the storage account (you can use nslookup .table.core.windows.net to determine tenant) and the Role for the service type (Nephos.Table)
4. Then use the following filter conditions:

~~~filter

ownerAccountName==
objectKeycontains

~~~

5. Save query link from the link tab in the left pane and query results for use in IcM in later steps.
