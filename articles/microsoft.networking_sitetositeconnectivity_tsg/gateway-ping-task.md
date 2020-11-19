<properties
	pageTitle="Check Gateway Ping Task Errors"
	description="Check Gateway Ping Task Errors"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0b24384b-d489-4358-9235-637024b0fae2"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to Check Gateway Ping Task Errors

## **Recommended Steps**

* Check if the issue is caused by gateway ping task.
* In this case, QMSAs are formed for each subnet pair in order to keep the SA active from getting timed-out after a period of 5 mins idle time.
* Some of the 3rd party devices don’t handle this correctly.
* Check IKE logs if Azure is negotiating QMSA for subnet pairs something like "StartAddress 172.21.184.0 EndAddress 172.21.184.0 PortStart 0 PortEnd 65535
* Please consult your TA if this is the case and take next actions (You may want to disable ping task on the Azure gateway, and this action requires PG engagement).
