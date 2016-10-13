<properties
	pageTitle="Site Recovery (VMware to Azure)/Add vCenter"
	description="Site Recovery (VMware to Azure)/Common issues during add vCenter"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536386"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Site Recovery (VMware to Azure)/Add vCenter

Common issues during Add vCenter

## **Recommended Steps**

* Ensure you have added an account in the **CSPSConfigtool.exe** to connect to the **VMware vCenter**.

* Ensure that the account used to connect to the vCenter meets the following requirements[vCenter Account prerequisites] (http://aka.ms/vCenterAccountPrereq). Below are  steps to check if the account has sufficient privileges
 - Launch the VMWare PowerCLI as administrator
 - Connect to your vCenter using the same **Username** and **Password** you provided in the **CSPSConfigtool.exe**
 - Enumerate the all virtual machines using the Get-VM command
 - If all virtual machines are enumerated then the account is good to be used for virtual machine discovery by Azure Site Recovery.

* Ensure **VMware PowerCLI 6.0** is installed on your Configuration Server/Scale-out process server.
 - Higher/Lower version of PowerCLI are not supported.
 - You can download PowerCLI 6.0 from https://developercenter.vmware.com/tool/vsphere_powercli/6.0

* Ensure that the virtual hard disks(VMDK)of each virtual machine is stored in a separate sub-directory. The directory should have the **same name** as of the virtual machine.


## **Recommended  Documents**
[VMware to Azure](aka.ms/asrstv2a)
