<properties
	pageTitle="Check if the insight matches the customer issue"
	description="Check if the insight matches the customer issue"
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
	articleId="49c8f99d-2294-4c86-8206-8cb8048bbe17"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the insight matches the customer issue

Make sure to confirm if this information is accurate on the Health tab inside Resource Explorer. 

1. If you find the RCA for the customer issue in Insights results and it describes the customer issue well, go to the Resource Explorer to confirm RCA before sending it to customer.
    1.  Go to the problematic VM/s that the customer informed had become unavailable and go to the Health tab.
	2. Right below you will have a timestamp. Make sure it includes the range from the customer impact
	3. If yes, take a look over Availability Graph, change the range of the selected area to cover the time stamp given by the customer
	4. Under the graphic, you will see several Events, here you will be able to confirm exactly what happened with the customer VM. Under Details a csswiki page may appear with a link to the RCA to be provided
	5. Go to Operations tab and check if there was any customer initiated operations in CRP block around the time stamp provided by customer and add it to your timeline. 
	6. In Properties tab, make note of the region and check for any LSIs. You can refer to the LSI Check section below for steps on how to verify if this unavailabilty impact was part of an outage.
	7. Validate if Host Analyzer(HA) report have been automatically created and verify that it covers the time stamp of the issue occurrence, otherwise it needs to be manually created.
2. If the description doesn't logically match the customer situation or it doesn't have enough information or no information to provide it to the customer, then select "No" below.
3. In case the RCA was already shared with the customer and they are satisfied with the RCA you provide, you can close the support case. At times, the customer might not be satisfied with the default RCA and wants us to provide more details about the issue. In that case, you can also go to the next step.
