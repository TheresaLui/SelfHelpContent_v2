<properties
	pageTitle="Issues that are related to activating a Windows license in Azure"
	description="Issues that are related to activating a Windows license in Azure"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	authorAlias="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32570109,32570108"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
/>

# Issues related to activating a Windows license in Azure

4 out of 5 customers resolved their VM Windows Activation issue using the steps below.

## **Recommended Steps**

Generally, Azure VM activation issues occur if the Windows VM is not configured by using the appropriate KMS client setup key, or the Windows VM has a connectivity problem to the Azure KMS service (**kms.core.windows.net, port 1668**).<br>

**You are using the Azure KMS Service and VM is not configured correctly**

The guidance outlined below can be found **[here](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems#step-1-configure-the-appropriate-kms-client-setup-key-for-windows-server-2016-and-windows-server-2012-r2)**.

1. Run (as Administrator) ```slmgr.vbs /dlv``` at an elevated command prompt. Check the *Description value* in the *output*, then determine whether it was created from retail (RETAIL channel) or volume (VOLUME_KMSCLIENT) license media:<br>

		cscript c:\windows\system32\slmgr.vbs /dlv

2. If *slmgr.vbs /dlv* shows RETAIL channel, run the following commands to set the [KMS client setup key](https://technet.microsoft.com/library/jj612867%28v=ws.11%29.aspx?f=255&MSPPError=-2147217396) for the version of Windows Server being used, and force it to retry activation:<br>

		cscript c:\windows\system32\slmgr.vbs /ipk <KMS client setup key>

		cscript c:\windows\system32\slmgr.vbs /ato

	For example, for Windows Server 2016 Datacenter, you would use the [KMS client setup key guide](https://technet.microsoft.com/library/jj612867%28v=ws.11%29.aspx?f=255&MSPPError=-2147217396) and run the following command:<br>

		cscript c:\windows\system32\slmgr.vbs /ipk CB7KF-BWN84-R7R2Y-793K2-8XDDG

**Verify the connectivity between the VM and Azure KMS service**<br>

1. Download and extract the [PSping](http://technet.microsoft.com/sysinternals/jj729731.aspx) tool to a local folder in the VM that does not activate
2. Go to Start, search on Windows PowerShell, right-click Windows PowerShell, and then select *Run as administrator*
3. Make sure that the VM is configured to use the correct Azure KMS server. To do this, run the following command:<br>

		iex "$env:windir\system32\cscript.exe $env:windir\system32\slmgr.vbs /skms kms.core.windows.net:1688"

	The command should return: *Key Management Service machine name set to kms.core.windows.net:1688 successfully.*<br>

4. Verify by using **Psping** that you have connectivity to the KMS server. Switch to the folder where you extracted the Pstools.zip download, and then run the following:<br>

		\psping.exe kms.core.windows.net:1688

	In the second-to-last line of the output, make sure that you see: *Sent = 4, Received = 4, Lost = 0 (0% loss).*<br>

5. Verify that the guest firewall has not been configured in a manner that would block activation attempts.<br>

	After you verify successful connectivity to **kms.core.windows.net**, run the following command at that elevated Windows PowerShell prompt. This command tries activation multiple times.<br>

		1..12 | % { iex “$env:windir\system32\cscript.exe $env:windir\system32\slmgr.vbs /ato” ; start-sleep 5 }

	A successful activation returns information that resembles the following: *Activating Windows(R), ServerDatacenter edition (12345678-1234-1234-1234-12345678) … Product activated successfully*.<br>

**If you are using a site-to-site VPN and forced tunneling**, see [Use Azure custom routes to enable KMS activation with forced tunneling](https://blogs.msdn.com/b/mast/archive/2015/05/20/use-azure-custom-routes-to-enable-kms-activation-with-forced-tunneling.aspx).<br>

**If you are using Express Route and you have a default route published**, see [Azure VM may fail to activate over Express Route](https://blogs.msdn.com/b/mast/archive/2015/12/01/azure-vm-may-fail-to-activate-over-expressroute.aspx).<br>

## **Recommended Documents**

* [Troubleshoot Windows activation failures on Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-activation-problems)<br>
* [Understanding Azure KMS endpoints for Windows product activation of Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-activation-problems#understanding-azure-kms-endpoints-for-windows-product-activation-of-azure-virtual-machines)<br>
* [Use Azure custom routes to enable KMS activation with forced tunneling](http://blogs.msdn.com/b/mast/archive/2015/05/20/use-azure-custom-routes-to-enable-kms-activation-with-forced-tunneling.aspx)<br>
* [Azure VM may fail to activate over Express Route](https://blogs.technet.microsoft.com/jpaztech/2016/05/16/azure-vm-may-fail-to-activate-over-expressroute)<br>
* [Need to convert an existing VM to use Azure Hybrid Benefit (HUB) for Windows Server?](https://docs.microsoft.com/azure/virtual-machines/windows/hybrid-use-benefit-licensing#convert-an-existing-vm-using-azure-hybrid-benefit-for-windows-server)<br>
* [How to verify if your VM is utilizing the HUB license](https://docs.microsoft.com/azure/virtual-machines/windows/hybrid-use-benefit-licensing#how-to-verify-your-vm-is-utilizing-the-licensing-benefit)
