<properties
pageTitle="Cannot create a Windows VM OperationNotAllowed/QuotaExceeded"
description="There are issues that prevent creating a virtual machine"
infoBubbleText="See details on the right"
service="microsoft.azurestack"
resource="azurestack"
authors="justinha"
ms.author="justinha"
displayOrder=""
articleId="azurestack-diagnostics-cannot-create-windows-vm-operation-not-allowed-quota-exceeded"
diagnosticScenario="Cannot create a Windows VM OperationNotAllowed/QuotaExceeded"
selfHelpType="diagnostics"
supportTopicIds="32663892"
resourceTags="windows"
productPesIds="16226"
cloudEnvironments="public, FairFax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Cannot create a Windows VM OperationNotAllowed/QuotaExceeded

<!--issueDescription-->

ResultCode: OperationNotAllowed/QuotaExceeded
Message: Operation results in exceeding quota limits of Core. Maximum allowed: 1000, Current in use: 1000, Additional requested: 4. 

<!--/issueDescription-->

## **Recommended Steps**

Identify the quota that has been exceeded (in this case for example, Compute Cores) and increase the plan associated with the subscription to [include more cores](https://docs.microsoft.com/azure-stack/operator/azure-stack-quota-types). For more information about increasing quota limits, see [Increase standard quota limits](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests).
