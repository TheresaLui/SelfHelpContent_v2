<properties
  pagetitle="Azure Stack Account management (add, remove, rotate passwords)&#xD;"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="alexsmit,justinha,v-myoung"
  selfhelptype="Generic"
  supporttopicids="32663929,32737110,32737252,32741888,32745835"
  resourcetags=""
  productpesids="16226,17131,17058,17057,17322"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-security-rbac"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Account management (add, remove, rotate passwords)

Role-Based Access Control (RBAC) in Azure Stack is consistent with the implementation in Microsoft Azure. You can manage access to resources by assigning the appropriate RBAC role to users, groups, and applications. If you need to change a user from either Azure Stack registration owner or CSP owner to a generic role, see [Add or remove Azure role assignments](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal). 

## **Recommended Steps**

If Active Directory Federation Services (ADFS) is used for identity and users can't sign in or appear in RBAC, ensure that you [validate Azure Graph integration](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-graph). To fix any issues, [trigger automation to configure Graph](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-identity#trigger-automation-to-configure-graph).

For basic steps to set up RBAC, see:

1. [Get started with Role-Based Access Control](https://docs.microsoft.com/azure/role-based-access-control/overview) in the Azure portal
1. [Use Role-Based Access Control to manage access](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) to your Azure subscription resources
1. [Create custom roles](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) for Azure Role-Based Access Control
1. [Manage Role-Based Access Control](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-permissions) in Azure Stack

## **Recommended Documents**

* [Overview of identity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-overview)<br>
* [Identity architecture for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-architecture)<br>
* [Manage access to resources with Azure Stack Role-Based Access Control](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-manage-permissions)<br>
* [What is role-based access control (RBAC)?](https://docs.microsoft.com/azure/role-based-access-control/overview)<br>
* [Manage access using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)
