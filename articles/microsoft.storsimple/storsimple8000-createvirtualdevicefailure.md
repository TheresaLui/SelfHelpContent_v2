<properties
	pageTitle="I can't create 8010 or 8020 cloud appliances in an Azure region"
	description="I can't create 8010 or 8020 cloud appliances in an Azure region"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="27a6cace-b8b0-4afd-8279-9fca34de459b"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can't create 8010 or 8020 cloud appliances in an Azure region

If you are not able to create the StorSimple Cloud Appliance in a specific region, this could be because:

## **Recommended steps**

* The Azure virtual machine sizes are not supported in that region. StorSimple Cloud Appliance 8010 is a Standard A3 virtual machine and 8020 is a Standard DS3 v1 virtual machine. Refer to [Azure VM supported regions](https://azure.microsoft.com/regions/services/) to identify the regions where Standard A3 & Standard DS3 v1 are supported.
* The service registration key is old and needs to be regenerated. Regenerate the service registration key and then try to create the cloud appliance. For more information, refer to [Regenerate the service registration key](https://aka.ms/ss8000-ts-regenkey).
* This could be due to a network connectivity issue related to the virtual network and the subnet combination specified while provisioning the virtual device. For more information, refer to [Network connectivity troubleshooting guide](https://aka.ms/ss-sca-troubleshoot-connect) and then retry the operation.

## **Recommended documents**

[Deploy and manage a StorSimple virtual device in Azure](https://docs.microsoft.com/azure/storsimple/storsimple-8000-cloud-appliance-u2)<br>
[Troubleshoot StorSimple virtual device internet connectivity errors](https://docs.microsoft.com/azure/storsimple/storsimple-8000-cloud-appliance-u2#troubleshoot-internet-connectivity-errors)
