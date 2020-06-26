<properties
	pageTitle="Job failed due to changes made by customer"
	description="Job failed due to changes made by customer"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5dca7dbf-aa36-4595-adc3-a24b53462871"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Job failed due to changes made by customer

<!--issueDescription-->

Based on provided details and our investigation, since the job was run successfully before, please double check if any changes were made to job metadata with respect to DBR version, init script, and library version or addition of new libraries. <br>
<br>
Some libraries don't support backward compatiablity, so version compatiablity should be throughly checked before migrating jobs clusters to higher DBR versions. Try to run the job after uninstalling the library. If a new version is released for the already existing library, it could be possible that new version might be failing due to version conflict with other dependancies. So we would need to install the specific version of the library and rerun the job.<br><br>
Let's revert the changes and run the jobs again.<br>

<!--/issueDescription-->

## Recommended Documents

1. [DBR releases](https://docs.microsoft.com/en-us/azure/databricks/release-notes/runtime/releases)
