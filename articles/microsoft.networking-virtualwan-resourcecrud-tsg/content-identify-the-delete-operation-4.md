<properties
	  pageTitle="Identify the DELETE operation"
	  description="Identify the DELETE operation"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualWANs"
	  authors="stegag"
	  ms.author="stegag"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="781efedd-4430-4c71-8282-2efd1b8d446a"
	  ownershipId="CloudNet_VirtualWAN"
/>

# Identify the DELETE operation

Every time the customer performs a Delete operation on any Azure resource, that translates into a DELETE operation in NRP.

In order to troubleshoot this, we need to identify the NRP operation ID:

* from ASC, identify the impacted resource in **Resource Explorer**
* from the **Operations** tab, identify the impacted operation from the list.
* if the Operation doesn't seem to be listed, try sarching for a wider time range. If still not present, you may need to ask the customer the precise timestamp of the issue, or ask them to repeat the operation.
* once the Operation is clearly identified in NRP Operations list, copy the **Operation ID**.
* open the  [VirtualWAN CRUD dashboard](https://jarvis-west.dc.ad.msft.net/dashboard/EEECloudnet/VirtualWAN%2520CRUD%2520Dashboard) and input the OperationId just found as the **NrpOperationID** parameter. Also adjust the time range if necessary.


The dashboard should report the reason of the failures in the "Errors" Section. It will also provide detailed and extensive logs at all layers involved (ARM,NRP,GatewayManager).

The error might point to something that the customer has control of, or might point to a backend issue that requires Azure team to fix.

**Important note**: if some resource is in **Failed** provisioning state, it may not be possible to delete it. The resource must be in Succeeded provisioning state to allow deletion.
