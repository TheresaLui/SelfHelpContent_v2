<properties
	pageTitle="Check event logs"
	description="Check event logs"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e11ae285-55a5-4289-9d62-69a7055b4e06"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check event logs

1. You will need to check the event log to verify a couple of conditions that might prevent Password Hash Sync from working correctly. 
2. Check event logs to ensure there are no connectivity or global sync errors such as dirsync is disabled, service won t start or password sync not enabled for company etc. 
3. Some relevant events are  
   1. Directory Synchronization  0, 611, 652, 655 
   2. Source ADSync error events
   3. 6xxx  
4. CHECK THE CONTENTS OF THESE EVENTS TO CLASSIFY THE ERROR
