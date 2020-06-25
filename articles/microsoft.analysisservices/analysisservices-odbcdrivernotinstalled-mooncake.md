<properties
    pageTitle="'Driver' property doesn't correspond to an installed ODBC driver"
    description="'Driver' property doesn't correspond to an installed ODBC driver"
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="chanwa"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="6f0aac34-9a1c-4a22-abd5-1b1068c0c6b6"
    ownershipId="AzureData_AnalysisServices"
/>

# 'Driver' property doesn't correspond to an installed ODBC driver

## **Recommended Steps**

1. Open elevated cmd.exe (run as administrator) and run **%windir%\system32\odbcad32.exe** to open the 64-bit ODBC Data Source Administrator
2. Go to **Drivers** tab, make sure the desired ODBC driver shows up
3. If not, install the 64-bit ODBC driver correctly
4. Restart the gateway service

## **Recommended Documents**

* [ODBC Data Source Administrator](https://docs.microsoft.com/sql/odbc/admin/odbc-data-source-administrator)

* [Viewing ODBC Drivers](https://docs.microsoft.com/sql/odbc/admin/viewing-drivers)
