<properties
	pageTitle="TSG Content Step: Check VM amd Platform Health"
	description="TSG Content Step: Check VM amd Platform Health"
	service="microsoft.network"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a1784ee9-9a4e-43f9-98e9-67593d204d43"
/>

# Check VM amd Platform Health

The product group has informed us that we do not have a way to go back in time to check why a VNet peering may have been down. It is very unlikely the peering went down then back up which is why we recommend the check of the VM health during the incident as well as the host and other platform components.

## **Recommended Steps**

1. Review the health of the source and destination VMs during the reported time
2. Review the source and destination VM hosts via NetVMA
3. (Need more info) Search for the tenant ID/name. If you can't figure it out quickly please ask for TA or PG help in the Vnet channel in Teams

## **Recommended Documents**

* https://netvma.trafficmanager.net/



