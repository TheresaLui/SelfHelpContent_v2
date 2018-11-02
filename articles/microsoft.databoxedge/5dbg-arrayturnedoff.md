<properties
	pageTitle="Data Box Gateway has turned off"
	description="Data Box Gateway has turned off"
	service="Microsoft.DataBoxEdge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# Data Box Gateway has turned off

## **Recommended steps**

This could be due to one of the following reasons:

1. The host on which the Data Box Gateway is provisioned has run out of disk space. If running Hyper-V, create additional space by doing the following:
    1. Launch Hyper-V Manager. Go to **Tools** > **Server Manager** > **Hyper-V Manager**.
    2. From the **Virtual Machines** list, identify the Data Box Gateway in a  `Paused-Critical` state.
    3. Free up resources so that the Data Box Gateway can be booted. For example, you can free up the disk space on corresponding hard drives.
    4. Right-click each Data Box Gateway, then click **Resume**. This returns the virtual machine to a running state.
2. If the Data Box Gateway has not run out of disk space, then try to turn it on.

## **Recommended documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
* [Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)
* [Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
