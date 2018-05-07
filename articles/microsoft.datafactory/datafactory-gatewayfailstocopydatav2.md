<properties 
	pageTitle="Integration Runtime fails to copy data" 
	description="Integration Runtime fails to copy data to/from an on-premises data store" 
	service="microsoft.datafactory" 
    resource="factories"
    authors="arthurw"
    displayOrder="9"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32356668"
    productPesIds="15613"
    resourceTags=""
/>

# Self-Hosted Integration Runtime (Data Management Gateway) fails to copy data to/from an on-premises data store

## **Recommended steps**

- You can find detailed information in Integration Runtime logs in Windows event logs. You can find them by using Windows **Event Viewer** under **Application and Services Logs** > **Integration Runtime** While troubleshooting IR related issues look for error level events in the event viewer.
- If you see data store connection or driver related errors, launch **Integration Runtime (configuration manager)** on the host machine, switch to the **Diagnostics** tab, select/enter appropriate values for fields in the **Test connection** group, and click **Test** to see if you can connect to on-premises data source  from the gateway machine using the connection information and credentials. If the test connection still fails after you install a driver, restart the IR for it to pick up the latest change.  

## **Recommended documents**
[How to create and configure Self-hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/)<br>
[Self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#self-hosted-integration-runtime)<br>
[Monitor integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime/)