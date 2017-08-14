<properties
	pageTitle="VMA RCA"
	description="RCA - Guest OS Crash - generic"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_GuestOSCrash_bugcheckcode"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**.
This unexpected occurrence was caused by a **Guest Operating system crash** due to a **Windows Bugcheck / Stop Error <!--$GuestBugCheckCode-->GuestBugCheckCode<!--/$GuestBugCheckCode-->** inside the Virtual Machine.
<!--/issueDescription-->

To avoid potential memory and/or disk data corruption Windows stops execution once it detects a serious error condition. Windows might stop for many different reasons: a reference to a memory address that causes an access violation, an unexpected exception or trap, a faulting kernel mode driver and so on.
Details about the cause of the stop error are written to the System Event Log and the system might also create a memory dump.
More information on Windows stop errors and how to analyze them can be found here:<br>

* [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)<br>
* [Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.<br>
To learn more about high availability options, please refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>
To learn more about Azure Resource Health, please refer to the following article:<br>

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
