<properties
	pageTitle=""
	description=""
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0cb405c3-130c-4e36-b5cb-29704f5a33a6"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# 
<!--issueDescription-->
Possible guest CPU/workload factors which could impact VM network availability:

All cores at 100% CPU utilization within the guest OS
High memory pressure (low available memory left)
High disk IO utilization (Throttling) of the OS disk
Port exhaustion (e.g. tcpip events 4227; VM configuration related)
<!--/issueDescription-->

//for insight
If you need assitance on this analysis from Networking perspective please engage Azure Networking POD via collaboration.