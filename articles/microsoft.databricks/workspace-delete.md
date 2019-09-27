<properties
	pageTitle="Diagnose and resolve issues with Workspace delete"
	description="Diagnose and resolve issues with Workspace delete"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677734"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="178b9906-c5b3-4eed-9a7a-dac993391ade"
/>

# Diagnose and resolve issues with Workspace deletion

* Cleanup of workspace is an asynchronous process and takes about 5-10 minutes to clean up cluster resources like VNET, Virtual Machines, storage and NSG.  If you just initiated it, please check after 5-10 minutes.
