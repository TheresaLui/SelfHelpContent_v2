<properties
    pageTitle="Azure Automation - Source Control"
    description="Azure Automation - Source Control"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642192"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
	articleId="1b17e1a7-c260-45b6-b533-d6ff9b44a5f7"
/>

# Azure Automation - Source Control
These documents will help you with common problems related to Automation Account source control integration.

## **Recommended Steps**

### **"Check In" button greyed out**

* This button is part of the [legacy source control feature](https://docs.microsoft.com/azure/automation/source-control-integration-legacy).
* Use the [new source control integration](https://docs.microsoft.com/azure/automation/source-control-integration) feature instead

### **Can't log in to source control**

* If you have multiple accounts, be sure you are logged into the correct account
* You can try logging in directly to [https://app.vssps.visualstudio.com/](https://app.vssps.visualstudio.com/) to ensure you are logged into the correct account

### **Strange characters appear after integrating with Source Control**

* Strange characters are often a symptom of bad encoding. For more information, see ["Common Causes of Encoding Issues"](https://docs.microsoft.com/azure/automation/source-control-integration#encoding)

### **Source Control sync job fails**

* Job logs for source control sync failures are detailed in [the "Syncing" section of the Source Control Integration document](https://docs.microsoft.com/azure/automation/source-control-integration#syncing)

## **Recommended Documents**

* [Azure Automation documentation](https://docs.microsoft.com/azure/automation/)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
