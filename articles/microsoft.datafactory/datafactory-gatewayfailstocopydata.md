<properties 
	pageTitle="Integration Runtime (Data Management Gateway) fails to copy data" 
	description="Integration Runtime (Data Management Gateway) fails to copy data to/from an on-premises data store" 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="4"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32356668"
    productPesIds="15613"
    resourceTags=""
/>

# Self-Hosted Integration Runtime (Data Management Gateway) fails to copy data to/from an on-premises data store

## **Recommended steps**

- You can find detailed information in gateway logs in Windows event logs. You can find them by using Windows **Event Viewer** under **Application and Services Logs** > **Data Management Gateway** While troubleshooting gateway related issues look for error level events in the event viewer.
- If the gateway stops working after you **change the certificate**, restart (stop and start) the **Data Management Gateway Service** using the Microsoft Data Management Gateway Configuration Manager tool or Services control panel applet. If you still see an error, you may have to give explicit permissions for the Data Management Gateway service user to access the certificate in Certificates Manager (certmgr.msc).  The default user account for the service is: **NT Service\DIAHostService**. 
- If the **Credential Manager** application fails to **encrypt** credentials when you click Encrypt button in Data Factory Editor, verify that you are running this application on the machine on which gateway is installed. If not, run the application on the gateway machine and try to encrypt credentials.  
- If you see data store connection or driver related errors, launch **Data Management Gateway Configuration Manager** on the gateway machine, switch to the **Diagnostics** tab, select/enter appropriate values for fields in the **Test connection to an on-premises data source using this gateway** group, and click **Test connection** to see if you can connect to on-premises data source  from the gateway machine using the connection information and credentials. If the test connection still fails after you install a driver, restart the gateway for it to pick up the latest change.  

## **Recommended documents**
[Move data between on-premises and cloud with Data Management Gateway](https://docs.microsoft.com/azure/data-factory/v1/data-factory-move-data-between-onprem-and-cloud/)<br>
[Data Management Gateway](https://docs.microsoft.com/azure/data-factory/v1/data-factory-data-management-gateway/)