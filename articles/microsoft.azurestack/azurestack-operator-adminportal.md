<properties
    pageTitle="Azure Stack Administration portal"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629244,32629245"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-operator-adminportal"
/>

# Azure Stack Administration Portal

There are two portals in Azure Stack; the administration portal and the user portal (sometimes referred to as the tenant portal.) As an Azure Stack operator, you can use the administration portal for day-to-day management and operations of Azure Stack.

### **Important note about portal impact during 1811 update**

The Azure Stack 1811 update contains a new [extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare) that secures external endpoints published by Azure Stack. Prior to installing 1811 update, all instances of Azure Stack Administrator portals **must be closed** or the **install will fail**. 

While installing the 1811 update, the Azure Stack user portal is unavailable while the extension host is configured. This can take up to 5 hours. During that time, you can check the status of an update, or resume a failed update installation using [Azure Stack Administrator PowerShell or the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets).

## **Recommended steps**

To access the administrator portal, browse to the portal URL and sign in by using the credentials of an Azure Stack operator. For an integrated system, the portal URL varies based on the region name and external fully qualified domain name (FQDN) of your Azure Stack deployment.

| Environment | Administrator Portal URL |   
| -- | -- | 
| ASDK| https://adminportal.local.azurestack.external  |
| Integrated systems | https://adminportal.&lt;*region*&gt;.&lt;*FQDN*&gt; | 
| | |

## **Recommended documents**

[Using the administrator portal in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-portals)