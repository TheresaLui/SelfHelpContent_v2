<properties
	pageTitle="Data Box Gateway has turned off"
	description="Data Box Gateway has turned off"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# Data Box Gateway has turned off.
This could be due to one of the following reasons:

## **Recommended steps**
1. The host on which the Data Box Gateway is provisioned has run out of disk space. If running Hyper-V, create additional space by doing the following:<br>
	1. Launch Hyper-V Manager. Go to **Tools** > **Server Manager** > **Hyper-V Manager**.<br>
	2. From the **Virtual Machines** list, identify the Data Box Gateway in a  `Paused-Critical` state.<br>
	3. Free up resources so that the Data Box Gateway can be booted. For example, you can free up the disk space on corresponding hard drives.<br>
	4. Right-click each Data Box Gateway, then click **Resume**. This returns the virtual machine to a running state.<br>
2. If the Data Box Gateway has not run out of disk space, then try to turn it on.


## **Recommended documents**
[Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)<br>
[Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
