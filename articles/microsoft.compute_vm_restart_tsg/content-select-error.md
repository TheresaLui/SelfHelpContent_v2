<properties
	pageTitle="Check for errors in the health tab"
	description="Check for errors in the health tab"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="721779c5-96ef-4842-8714-e266bd9646e0"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for errors in the health tab

* Health tab will provide you some more information
* Under Resource Explorer, select the VM/s that customer stated were unavailable
* As soon as you are on the Overview page of the machine, select the Health Tab.
* Right below you will have a timestamp. Make sure it matches the range from the customer impact
* If yes, take a look over Availability Graph, change the selected area to range the issue of customer
* Under the graphic, you will see several Events, here you will be able to confirm exactly what happened with customer VM. 
* If no matching error is displayed, please select the "No Error" option below
