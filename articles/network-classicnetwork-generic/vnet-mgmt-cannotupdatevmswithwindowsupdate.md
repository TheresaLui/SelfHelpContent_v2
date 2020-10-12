<properties
	pageTitle="management/cannotupdatevmswithwindowsupdate"
	description="management/cannotupdatevmswithwindowsupdate"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="karenha"
	ms.author="karenha,aldomel"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740055"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="vnet-mgmt-cannotupdatevmswithwindowsupdate"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Cannot Update VMs with Windows Update

## **Recommended Steps**

If the WSUS is not able to download content, the following NSG rules need to be in place:

* Add inbound/outbound NSG rule to allow traffic to/from the Internet on Port 80
* Add inbound/outbound NSG rule to allow traffic to/from the Internet on Port 443
* Add inbound/outbound NSG rule to allow traffic from the Client VMs on Port 8530 (default unless configured)

## **Recommended Documents**

* [Plan your deployment for updating Windows Virtual Machines in Azure](https://docs.microsoft.com/azure/architecture/example-scenario/wsus/)
* [WSUS Messages and Troubleshooting Tips](https://docs.microsoft.com/windows-server/administration/windows-server-update-services/manage/wsus-messages-and-troubleshooting-tips) offers additional troubleshooting steps
