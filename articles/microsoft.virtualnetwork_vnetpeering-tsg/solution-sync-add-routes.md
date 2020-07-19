<properties
pageTitle="SolutionVnetIntegrationSync"
description="SolutionVnetIntegrationSync"
infoBubbleText="SolutionVnetIntegrationSync"
service="microsoft.network"
ownershipid="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionVnetIntegrationSync"
diagnosticScenario="SolutionVnetIntegrationSync"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
/>

# Web App is not in sync with Vnet routes
<!--issueDescription-->

This issue is caused by the Webapp not having the VNet routes. To allow a Webapp to communicate over a VNet Peering connection the WebApp using VNet integration must have the up-to-date routes. The issue was solved by manually syncing and verifying the correct routes are listed. I have the links to more information below. 

<!--/issueDescription-->

## **Recommended Steps**

1. Perform **Sync Network Operation** in the WebApp resource in the Azure portal.
2. Sometimes the Web Apps do not connect because of certificate mismatch.
3. In order to fix this, you need to perform a **Sync Network operation** on the Web App that has the effect of re-configuring Point to Site on it – including all certificates.


## **Recommended Documents**

* [Sync networking configuration for Azure App Service](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-sync-network-configuration)
