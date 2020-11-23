
<properties
	pageTitle="Issue with Data Box Export order"
	description="Learn how to resolve issues related to some data not being exported to the device"
	service="microsoft.databox.jobs"
	resource=""
	authors="ansubram"
	ms.author="ansubram"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32743104"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
  articleId="32743104"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box - Issue with exported data

If the data selected for export is larger than the capacity of the device, then the files that could not be copied will be entered in the copy log. The copy log can be used as an input xml file in a subsequent export order, to copy any files that could not get copied earlier due to lack of space on the device.

If there were any other issues due to which some files could not be exported, such as source data churn or incompatible file formats, these are also recorded in the copy log.

## **Recommended Documents**

* [Tracking and logging for Data Box export orders](https://docs.microsoft.com/azure/databox/data-box-export-logs)
* [Create an export order using XML file](https://docs.microsoft.com/azure/databox/data-box-deploy-export-ordered#export-order-using-xml-file)
