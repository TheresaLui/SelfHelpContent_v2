<properties
pageTitle="Solution Databricks Resource Locked"
description="Solution Databricks Resource Locked"
infoBubbleText="Solution Databricks Resource Locked"
service="microsoft.network"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionDatabricksResourceLocked"
diagnosticScenario="SolutionDatabricksResourceLocked"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
/>
# Solution Databricks Resource Locked
<!--issueDescription-->

It looks like this issue may be related to enabling VNet peering on a Vnet that has Databricks integration.

<!--/issueDescription-->

## **Recommended Steps**

1. Follow the steps in the link below to set up VNet peering from within the Databricks service blade. Specify the target VNet peer via resource ID found in the VNet resource's 'Properties' tab.

## **Recommended Documents**

* https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html
