<properties
	pageTitle="My virtual array has turned off"
	description="My virtual array has turned off"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="9000Or1200Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f39c9319-d919-41da-b9f2-cb97ca595f4c"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# My virtual array has turned off.
This could be due to one of the following reasons:

## **Recommended steps**
1. The host on which the virtual array is provisioned has run out of disk space. If running Hyper-V, create additional space by doing the following:<br>
	1. Launch Hyper-V Manager. Go to **Tools** > **Server Manager** > **Hyper-V Manager**.<br>
	2. From the **Virtual Machines** list, identify the virtual array(s) in a  `Paused-Critical` state.<br>
	3. Free up resources so that the virtual array(s) can be booted. For example, you can free up the disk space on corresponding hard drives.<br>
	4. Right-click each virtual array, then click **Resume**. This returns the virtual machine to a running state.<br>
2. If the virtual array has not run out of disk space, then try to turn it on.


## **Recommended documents**
[Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)<br>
[Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
