<properties
	pageTitle="Has the issue been properly scoped?"
	description="Has the issue been properly scoped?"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="148f7309-c480-4d2c-8edf-0830d7af737b"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the issue has been properly scoped

**Always prudent to check ASC for insights first. Collect the AzCopy log under the user profile.** 

1. First, it is important to understand **what the customer is trying to migrate**:
    1. Are they trying to migrate a page blob, such as a VHD file?
    2. Are they trying to migrate a block blob, such as images or videos?
    3. Are they trying to migrate tables or queues? If so, they may be best assisted by the [Azure PaaS Developer team](https://old.csssupportwiki.com/index.php/curated:Azure/Storage/HowTo/Engage_the_Azure_PaaS_Developer_Team).
2. It is important to clarify details about the **source and destination** of the data migration:
   1. Are they migrating to or from a Storage Account?
   2. If so, what type of Storage Account are they using? (Classic or ARM, General Purpose or Cool/Hot Blob, etc.)
   3. Are they migrating to or from an on-premises machine, or a Virtual Machine?
3. It is also important to understand **when the issue occurs**:
   1. Have they ever been able to migrate data successfully in this way?
   2. If so, when was the last time it worked?
   3. Has anything changed since the customer started seeing this issue?
   4. Does the issue always happen, or only intermittently?
4. It is also important to understand **where the issue occurs**:
   1. Does the issue occur only in Azure Virtual Machines, only on-premises, or both?
   2. Does the issue occur only with Windows clients, only with Linux clients, or with both?
   3. Does the issue occur with other Storage Accounts?
5. Lastly, you should determine the **specific failure** the customer is observing
   1. Are there any error messages being displayed? If so, where is the customer seeing the error messages?
   2. Specific error message text - What is the exact error message that the customer is seeing? Does it provide any clues as to the cause of the failure?

## Data Collection
 
1. Clear description of the end goal. Check scoping questions.
2. SubscriptionId
3. Storage Account Name/s
4. Storage Service/s being used(Blob/Files/Table/Queue)
5. Timeframe/s of the issue in UTC
6. Tool being used and its Version
7. Verbose/Debug logging of the tool being used(AzCopy, PowerShell, CLI, etc.)
8. VM Name(if any)

