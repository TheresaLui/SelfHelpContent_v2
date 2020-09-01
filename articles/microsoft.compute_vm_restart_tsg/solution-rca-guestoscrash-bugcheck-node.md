<properties
	pageTitle="RCA for Windows GuestOS Crashes with bugcheck code"
	description="RCA for Windows GuestOS Crashes with bugcheck code"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e4606ef6-8ef2-418a-85b8-398b5e0b6f9c"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for Windows GuestOS Crashes with bugcheck code
<!--issueDescription-->

We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by a Guest Operating system crash due to a Windows Bugcheck / Stop Error <Bugcheckcode> inside the Virtual Machine.
To avoid potential memory and/or disk data corruption Windows stops execution once it detects a serious error condition. Windows might stop for many different reasons: a reference to a memory address that causes an access violation, an unexpected exception or trap, a faulting kernel mode driver and so on. Details about the cause of the stop error are written to the System Event Log and the system might also create a memory dump. More information on Windows stop errors and how to analyze them can be found in the articles below. 

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**
 
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)
* [Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)
