<properties
	pageTitle="I can’t access my shares or volumes."
	description="I can’t access my shares or volumes."
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="9000Or1200Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="fffdfbd4-03dc-4d08-beda-26b94fdb39b0"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can’t access my shares or volumes.


## **Recommended steps**
1.  In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Validate that the device is configured properly and resolve any reported issues.
2. From the Azure portal of your StorSimple Device Manager service,  go to **Volumes** blade. Select the appropriate volume, take the volume offline and then bring it back online.  If using a file server, go to **Shares** blade to take the shares offline and bring back online
3. If using File Explorer to access the shares, right click on the share folder name and go to **Properties** > **Security** to check that you have permission to access the share.
4. If you have just initiated a clone, and you are trying to access the target share/volume, the share/volume may not be online yet. Wait for a few moments and then try to access it.
5. If using an iSCSI server, check the iSCSI initiator configuration to see if the volume is connected. If the volume is not connected, try to connect. If this fails, you may have a cloud connectivity issue.
6. If this is the first share that you have created for this device, the DNS resolution may not have worked due to a network infrastructure error.
7. Check if there was some latency introduced to the cloud by contacting Azure Support.

## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)
