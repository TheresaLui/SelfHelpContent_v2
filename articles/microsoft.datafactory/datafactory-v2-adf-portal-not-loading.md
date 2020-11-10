<properties
  pagetitle="V2 - Author and Develop - ADF Portal not Loading"
  service=""
  resource=""
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629437"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2aae3671-bww5-0099-erd7-3623ebc13d45"
  ownershipid="AzureData_DataFactory" />
# V2 - Author and Develop - ADF Portal not Loading

## **Recommended Steps**

* Officially supported web browsers:
  * Officially supported web browsers for ADF are _Microsoft Edge_ and _Google Chrome_
  * For Data Factory V2, please use either one to access [_Azure Data Factory UI Portal_](https://adf.azure.com)

* If the ADF UI portal does not load or you are redirected to a blank page, _https://adf.azure.com/accesstoken.html_, please __enable__ third-party cookies options on your browser using the following steps found on [Troubleshoot ADF UX Issues](https://docs.microsoft.com/azure/data-factory/data-factory-ux-troubleshoot-guide):
  * ADF portal uses browser Cookies to persist user session and enable interactive development and monitoring experiences
  * For _Microsoft Edge_,  please go to __Settings and More ...__ > __Settings__ > __Site permissions__ > __Cookies and site data__ to make the change, make sure **Block third party cookies** is **disabled**, you can also add the site __adf.azure.com__ on the **Allow** section by clicking the button **Add**
  * For _Google Chrome_, please visit __chrome://settings/content/cookies__ to make the change, make sure **Block third party cookies** is **disabled**, you can also add the site __adf.azure.com__ on the **Allow** section by clicking the button **Add**

* If the ADF UI portal is slow or not as responsive, check if your browser version is too old. Upgrading to newer version could boost the UI performance. 

## **Recommended Documents**

* [Troubleshooting Guide - Azure Data Factory UX Issues](https://docs.microsoft.com/azure/data-factory/data-factory-ux-troubleshoot-guide)
* Quick-start: [Create a data factory using the Azure Data Factory UI](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal)
* Quick-start: [Create a data factory using Azure Resource Manager template](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-resource-manager-template)
* Quick-start: [Use Copy Data Tool to Copy Data](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-copy-data-tool)
