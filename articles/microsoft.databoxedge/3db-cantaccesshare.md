<properties
	pageTitle="I can’t access my shares."
	description="I can’t access my shares."
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxEdge,DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# I can’t access my shares.
If you are facing share access issues, do the following.

## **Recommended steps**
1. From the Azure portal of your device,  go to **Monitoring** > **Device events** blade. See if there are any events reported. Resolve the reported issues.
2. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve the reported issues.
3. Storage account is deleted. Ensure that the storage account still exists and the associated credentials are correct.
4. Storage account access keys have been regenerated. If the keys have been regenerated, you will need to synchronize the new keys via the Azure portal. Select the share from the Azure portal, click **Sync storage keys**.
5. If using File Explorer to access the shares, right click on the share folder name and go to **Properties** > **Security** to check that you have permission to access the share.
6. If this is the first share that you have created for this device, the DNS resolution may not have worked due to a network infrastructure error.
7. Check if there was some network latency introduced to the Azure by contacting your local network administrator.
