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
ownershipId="StorageMediaEdge_XStore"
/> 

# Troubleshooting authentication and authorization failures using Apollo

## Troubleshooting Authentication and Authorization Failures

Most customers resolve their Azure AD authentication failures using charts, diagnostics, and documentation.

:::Section Recommended solutions:::

The following chart can help you to narrow down the time frames when the Authentication or Authorization failures occurred:

<metric>
<name>Transactions</name>
<aggregationType>Total</aggregationType>
<timeSpanType>relative</timeSpanType>
<timeSpanDuration>1d</timeSpanDuration>
<title>Storage Authentication and Authorization Failure</title>
</metric>

### Failure diagnostics

<Insight>
<symptomId>StorageFailureTransactionInsightLight</symptomId>
<executionText>We are running a quick check to find authentication and authorization failures on the storage account</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>No authentication or authorization failures were found during the last 24 hours. Use the diagnostic below to run a detailed analysis.</noResultText>
<additionalInputsReq>false</additionalInputsReq>
</Insight>

### Deeper analysis
Input the response from the previous troubleshooter or provide custom data so we can run a deeper analysis on a specific failure:

<Insight>
<symptomId>StorageFailureTransactionInsight</symptomId>
<executionText>We are running a detailed analysis to check for authentication and authorization failures</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>No authentication or authorization issues found!</noResultText>
<additionalInputsReq>true</additionalInputsReq>
</Insight>

### More resources

Here are some additional resources that can help resolve Azure AD authentication and connectivity failures

Solutions for common issues reported with RBAC roles
- [I am the owner of the Storage account but don't get to access data](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?#assign-rbac-roles-using-the-azure-portal)
- [I have Data Reader/Data Contributor permission but don't see the storage account on Portal](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?#assign-rbac-roles-using-the-azure-portal) 
- [I have problems accessing storage resources using RBAC in Storage Explorer](https://docs.microsoft.com/azure/storage/common/storage-explorer-troubleshooting?tabs=1904#role-based-access-control-permission-issues)

Grant access to Azure blob and queue data with RBAC

- [Grant access to Azure blob and queue data with RBAC in the Azure portal](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal)
- [Grant access to Azure blob and queue data with RBAC using PowerShell](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-powershell)
- [Grant access to Azure blob and queue data with RBAC using Azure CLI](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-cli)

Authenticate with Azure AD

- [Get started with Azure AD for Storage](https://docs.microsoft.com/azure/storage/common/storage-auth-aad)
- [Authenticate with Azure Active Directory from an application for access to blobs and queues (Preview)](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)
- [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac) 
- [Authenticate access to blobs and queues with managed identities for Azure Resources](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-msi)
- [Use an Azure AD identity to access Azure Storage with CLI or PowerShell](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-script)
- [Authorization options for Azure Storage Services](https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services)

Access Options

- [User Policy to manage resources and control access](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy)
- [Assign a user access to your Storage account](https://azure.microsoft.com/documentation/articles/role-based-access-control-configure/)
- [Microsoft Azure Storage Explorer](http://storageexplorer.com)
- [PowerShell](https://azure.microsoft.com/documentation/articles/storage-powershell-guide-full/)
- [Azure Storage Connection Strings](https://docs.microsoft.com/azure/storage/storage-configure-connection-string)
