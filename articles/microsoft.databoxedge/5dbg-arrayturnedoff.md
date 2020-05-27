<properties
	pageTitle="Data Box Gateway has turned off"
	description="Data Box Gateway has turned off"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anoobbacker"
	ms.author="anbacker"
	authoralias="anbacker"
	displayOrder="70"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8bbce42c-0cce-4266-a72e-3f24c184a576"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Gateway has turned off

## **Recommended Steps**

This could be due to one of the following:

1. The host on which the Data Box Gateway is provisioned has run out of disk space. If running Hyper-V, create additional space by doing the following:

    1. Launch Hyper-V Manager
    2. Go to **Tools** > **Server Manager** > **Hyper-V Manager**
    3. From the **Virtual Machines** list, identify the Data Box Gateway in a  `Paused-Critical` state
    4. Free up resources so that the Data Box Gateway can be booted (i.e. free up disk space on corresponding hard drives)
    4. Right-click each Data Box Gateway, then click **Resume** to return the virtual machine to a running state

2. If the Data Box Gateway has not run out of disk space, ensure that it is running

## **Recommended Documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
* [Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)
* [Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
