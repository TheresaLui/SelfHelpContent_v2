<properties
	pageTitle="Unable to access volumes"
	description="Unable to access volumes troubleshooting"
	infoBubbleText="See detailson the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="81865826-83af-46d8-a4de-f7f7136d96e5"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630508"
	resourceTags="9000Or1200Series"
	productPesIds="16161"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Unable to access volumes

## **Recommended Steps**

1.  In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Validate that the device is configured properly and resolve any reported issues.
2. From the Azure portal of your StorSimple Device Manager service, go to **Volumes** blade. Select the appropriate volume, take the volume offline and then bring it back online.  If using a file server, go to **Shares** blade to take the shares offline and bring back online
3. If using File Explorer to access the shares, right click on the share folder name and go to **Properties** > **Security** to check that you have permission to access the share
4. If you have just initiated a clone, and you are trying to access the target share/volume, the share/volume may not be online yet. Wait for a few moments and then try to access it.
5. If using an iSCSI server, check the iSCSI initiator configuration to see if the volume is connected. If the volume is not connected, try to connect. If this fails, you may have a cloud connectivity issue.
6. If this is the first share that you have created for this device, the DNS resolution may not have worked due to a network infrastructure error
7. Check if there was some latency introduced to the cloud by contacting Azure Support

## **Recommended Documents**

* [Troubleshoot via the local web UI](https://docs.microsoft.com/azure/storsimple/storsimple-ova-web-ui-admin#troubleshoot-web-ui-setup-errors)
