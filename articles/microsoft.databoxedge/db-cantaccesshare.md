<properties
	pageTitle="I can’t access my shares"
	description="I can’t access my shares"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anoobbacker"
	ms.author="anbacker"
	authoralias="anbacker"
	displayOrder="40"
	selfHelpType="resource"
	supportTopicIds="32614300, 32614305"
	resourceTags="DataBoxEdge,DataBoxGateway"
	productPesIds="16597"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d49445ef-f2c7-47b3-b045-4948d6e57c72"
	ownershipId="StorageMediaEdge_DataBox "
/>

# I can’t access my shares

## **Recommended Steps**

If you are experiencing share access issues, try the following:

1. From the Azure portal of your device,  go to **Monitoring** > **Device events**. Check the reported events and resolve any issues.
2. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve any reported issues.
3. Check if the storage account associated to the share still exists. If the storage account got deleted, delete the existing share and recreate the share pointing to a new storage account.
4. Your storage account access keys have been regenerated. If the keys have been regenerated, you will need to synchronize the new keys via the Azure portal. Select a share associated with your resource and click **Sync storage keys**.
5. If using File Explorer to access the shares, right click on the share folder name and go to **Properties** > **Security**. Check that you have permissions to access the share.
6. If this is the first share that you have created for this device, the DNS resolution may not have worked due to a network infrastructure error. Check your settings and try again.
7. Check if there was some network latency introduced to the Azure by contacting your local network administrator.

## **Recommended Documents**

* [Troubleshoot your Azure Data Box Edge issues](https://docs.microsoft.com/azure/databox-online/data-box-edge-troubleshoot)
* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
