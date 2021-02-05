<properties
  pagetitle="V2 - Author and Develop - ADF Portal not Loading"
  service=""
  resource=""
  ms.author="chez,haoc,fangl"
  selfhelptype="Generic"
  supporttopicids="32629437"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2aae3671-bww5-0099-erd7-3623ebc13d45"
  ownershipid="AzureData_DataFactory" />
# V2 - Author and Develop - ADF Portal not Loading

Most customer can resolve issues with Azure Data Factory V2 (ADF) portal failing to load using the following steps.

## **Recommended Steps**

* Ensure that your web browser is officially supported:
  * The [Azure Data Factory portal](https://ms-adf.azure.com/datafactories) supports Microsoft Edge and Google Chrome 

* If the ADF portal doesn't load or redirects you to a [blank page](https://adf.azure.com/accesstoken.html), enable third-party cookies on your browser using the steps in [Troubleshoot ADF UX Issues](https://docs.microsoft.com/azure/data-factory/data-factory-ux-troubleshoot-guide). ADF portal uses browser cookies to persist the user session and to enable interactive development and monitoring experiences.

    * For Microsoft Edge, go to **Settings and More** > **Settings** > **Site permissions** > **Cookies and site data**. Deselect **Block third party cookies** and in the **Allow** section, select the **Add** button to add the site **adf.azure.com**.
  
    * For Google Chrome, go to **chrome://settings/cookies**, deselect **Block third party cookies**. In the **Allow** section, select the **Add** button to add the site **adf.azure.com**.
  
    * If you have disabled browser pop-ups, check the browser's address bar to see if a pop-up is actively blocked, and allow it. 

* If the ADF portal is slow to respond, check your browser version. Upgrading your browser to a newer version often improves performance. 

## **Recommended Documents**

* [Troubleshooting Guide - Azure Data Factory UX Issues](https://docs.microsoft.com/azure/data-factory/data-factory-ux-troubleshoot-guide)
* Quickstart: [Create a data factory using the Azure Data Factory UI](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal)
* Quickstart: [Create a data factory using the Azure Resource Manager template](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-resource-manager-template)
* Quickstart: [Use the Copy Data Tool to copy data](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-copy-data-tool)
