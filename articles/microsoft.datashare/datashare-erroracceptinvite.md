<properties
  pagetitle="Invitation cannot accept or reject"
  service="microsoft.datashare"
  resource="accounts"
  ms.author="jife"
  selfhelptype="Generic"
  supporttopicids="32675621"
  resourcetags=""
  productpesids="16762"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake,blackforest"
  articleid="6d9713ad-1ea2-4476-8a02-44b96e755334"
  ownershipid="AzureData_DataShare" />
# Invitation cannot accept or reject

## **Recommended Steps**

### **Cannot accept the invitation**

If you cannot accept invitation, try to resolve the issue following these steps:

   1. Make sure you have checked the checkbox to agree to the terms of use
   1. Make sure you have specified a target Data Share account to receive the invitation into
   1. Make sure the Received Share Name does not already exist in your target Data Share account

### **Cannot create Data Share account**

If you encounter issue when creating a new Data Share account, try to resolve the issue following these steps:

   1. Make sure [Azure Data Share resource provider is registered](https://docs.microsoft.com/azure/data-share/concepts-roles-permissions#resource-provider-registration) in the Azure subscription
   1. Make sure that there are no [locks on your Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)
   1. Check [Azure Status](https://status.azure.com/status) for any potential outages or service issues

## **Recommended Documents**

* [Troubleshooting common issues with Azure Data Share](https://docs.microsoft.com/azure/data-share/data-share-troubleshoot)