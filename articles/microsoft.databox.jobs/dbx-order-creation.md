
<properties
	pageTitle="Order creation"
	description="Learn how to resolve the order created related issues"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639192"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="32639186"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Order creation

## **Recommended Steps**

## Unable to create order

If you were not able to create a Data Box order, there is a problem with either your subscription type or access, or parameters selected. 

1. Check your subscription. Data Box is only available for Enterprise Agreement (EA) and Cloud solution provider (CSP) subscription offers. If your subscription does not fall in any of the above types, contact Microsoft Support to upgrade your subscription
2. If you have a supported offer type for the subscription, check your subscription access level. You need to be a contributor or owner in your subscription to create an order.
3. Check the source and destination selected, and ensure they are within the same commerce boundary

## Unable to create additional orders

I ordered a couple of Data Box devices. I am not able to create any additional orders. Why would this be?

* We allow for a maximum of five active orders per subscription per commerce boundary (combination of country and the region selected). If you need to order an additional device, contact Microsoft Support to increase the limit for your subscription.

## Unsupported regions

Data Box orders only support moving data within a country or commerce boundary. Check the availability of the service in the source/destination selected. See the following links for more information -
* Learn more about cross commerce boundary transfers using [Data Box](https://docs.microsoft.com/azure/databox/data-box-faq?WT.mc_id=Portal-Microsoft_Azure_Support#q-how-can-i-import-source-data-at-my-location-in-a-particular-country-to-an-azure-region-in-a-different-countryregion-or-export-data-from-an-azure-region-in-one-country-to-a-different-countryregion)
* Learn more about cross commerce boundary transfers using [Data Box Disk](https://docs.microsoft.com/azure/databox/data-box-disk-faq#q-how-can-i-import-source-data-present-at-my-location-in-one-countryregion-to-an-azure-region-in-a-different-country)

## **Recommended Documents**

* [Data Box FAQ](https://docs.microsoft.com/azure/databox/data-box-faq)
* [Data Box Disk FAQ](https://docs.microsoft.com/azure/databox/data-box-disk-faq)




