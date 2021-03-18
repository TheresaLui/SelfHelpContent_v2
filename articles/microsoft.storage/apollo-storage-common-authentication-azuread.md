

<properties
pageTitle="RBAC Authentication Common Solutions"
description="RBAC Authentication Common Solutions"
ms.author="annayak"
displayOrder=""
articleId="b7ac8228-62ac-47a7-9427-a8b97fe4f7ca"
selfHelpType="Apollo"
supportTopicIds="d60f0f12-2be9-1068-02cb-bb9d86b7b6b1,5b03a792-037b-9962-ef13-5c71a55fc5d2,82d8bf7e-861c-910b-b0a7-d647c5ffdf2b,641f6d9b-0cbe-bfb8-3389-7276da029799" 
productPesIds="15629,16459,16598,16462,16461" 
cloudEnvironments="public"
resourceRequired="false"
ownershipId="StorageMediaEdge_XStore"
/> 

# Troubleshooting authentication and authorization failures using Apollo

## Troubleshooting authentication and authorization failures

Resolve your issue faster by using one or more of the following solutions by the Azure Storage engineering team.<br>

### Most commonly reported issues
|<span style="color:red">**Issue/Error**  | <span style="color:green">**Resolution**|
|-----------------------------------------|-----------------------------------------|
| I am the creator/owner of the storage account but don't have access to data | [How can an account creator/owner get access to data ](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?#assign-rbac-roles-using-the-azure-portal) |
| I have Blob Data Reader/Contributor/Owner permission but don't see the storage account on **Azure portal** | [How to list an RBAC-protected storage account in **Azure portal**](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?#assign-azure-roles-using-the-azure-portal) |
| I have problems accessing storage resources using RBAC in **Azure Storage Explorer**| [How to list an RBAC-protected storage account in **Azure Storage Explorer**](https://docs.microsoft.com/azure/storage/common/storage-explorer-troubleshooting?tabs=1904#role-based-access-control-permission-issues)|



### Diagnose and resolve

If you don't have the error timestamp use the "Failure Chart" below to find it and run the diagnostics.

<insight>
  <symptomId>StorageFailureTransactionInsight</symptomId>
  <executionText>We are running a detailed analysis to check for authentication and authorization failures</executionText>
  <timeoutText>We stopped the check, as it was taking too long</timeoutText>
  <noResultText>No authentication or authorization issues found!</noResultText>
  <additionalInputsReq>true</additionalInputsReq>
  <maxInsightCount>1</maxInsightCount>
</insight>

<br>

### Authentication and authorization failure metrics
Use the chart to find the approximate time and use that in the **Diagnose and resolve** diagnostic above.

**Note:** _Click on the chart to zoom in and search a longer time span. Click **Close** on top right of the chart to come back here._<br>

<metric>
  <name>transactions</name>
  <aggregationType>sum</aggregationType>
  <timeSpanDuration>2d</timeSpanDuration>
  <title>Failures in last 48 hours</title>
</metric>


### More resources
Here are some additional resources that can help resolve Azure Active Directory authentication and connectivity failures.

**Grant access to Azure Blob and Queue data with RBAC**

- [RBAC in the Azure portal](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal)
- [RBAC using PowerShell](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-powershell)
- [RBAC using Azure CLI](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-cli)

**Authenticate with Azure Active Directory**

- [Get started with Azure Active Directory for Storage](https://docs.microsoft.com/azure/storage/common/storage-auth-aad)
- [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)
- [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac) 
- [Authenticate access to blobs and queues with managed identities for Azure Resources](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-msi)
- [Use an Azure AD identity to access Azure Storage with CLI or PowerShell](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-script)
- [Authorization options for Azure Storage Services](https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services)
