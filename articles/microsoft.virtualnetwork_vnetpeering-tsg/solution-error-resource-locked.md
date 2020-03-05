<properties
pageTitle="Solution Databricks Resource Locked"
description="Solution Databricks Resource Locked"
infoBubbleText="Solution Databricks Resource Locked"
service="microsoft.network"
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
cloudEnvironments="Public"
ownershipId="CloudNet_VirtualNetwork"
/>
# Solution Databricks Resource Locked
<!--issueDescription-->

You can run into this issue when enabling VNet peering on a Vnet that has Databricks integration.

<!--/issueDescription-->

## **Recommended Steps**

1. Follow the link below in setting up the vNET peering from within the Databricks service blade and specifying the target peer via resource ID and connectivity fix the peering on the  target vNET

## **Recommended Documents**

* https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html
