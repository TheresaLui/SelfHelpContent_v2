<properties
	pageTitle="Site Recovery (VMware to Azure)/Add vCenter"
	description="Site Recovery (VMware to Azure)/Common issues during add vCenter"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="AnoopVasudavan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536386"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Site Recovery (VMware to Azure)/Add vCenter

Common issues during Add vCenter

## **Recommended Steps**

* Ensure you have added an account in the **CSPSConfigtool.exe** to connect to the **VMware vCenter**.
* Ensure that the account used to connect to the vCenter meets the following requirements [vCenter Account prerequisites](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#prepare-an-account-for-automatic-discovery). Below are  steps to check if the account has sufficient privileges
 - Launch the VMWare PowerCLI as administrator
 - Connect to your vCenter using the same **Username** and **Password** you provided in the **CSPSConfigtool.exe**
 - Enumerate the all virtual machines using the Get-VM command
 - If all virtual machines are enumerated then the account is good to be used for virtual machine discovery by Azure Site Recovery.
* Ensure **VMware PowerCLI 6.0** is installed on your Configuration Server/Scale-out process server.
	- Higher/Lower version of PowerCLI are not supported.
	- You can download PowerCLI 6.0 from https://developercenter.vmware.com/tool/vsphere_powercli/6.0
* Ensure that the virtual hard disks(VMDK)of each virtual machine is stored in a separate sub-directory. The directory should have the **same name** as of the virtual machine.
* If you are getting an error that says **The vCenter server/vSphere host hostname or IP address already registered** while trying to add a vCenter ensure that you deleted old references to the vCenter before you try adding the vCenter again.
* You can **delete** a vCenter Server
	- Browse to Settings->Site Recovery Infrastructure -> Configuration Server -> (ConfigSrvName)
	- Expand the list of vCenter servers
	- Right-click on the vCenter you want to delete and choose Delete from the context menu that pops up.
* To change the credentials used to connect to a vCenter Server
	- Create a new account in the CSPSConfigtool on the on-premises Configuration Server.
	- Browse to Settings->Site Recovery Infrastructure -> Configuration Server -> (ConfigSrvName)
	- Click on **Refresh Server**. Wait for the Refresh Job to complete
	- Expand the list of **vCenter servers**
	- Click on the vCenter Server to open up the details page.
	- Modify the **vCenter Server/vSphere Server host account** field to the new account you created and click **Save**


## **Recommended  Documents**
* [Prepare an account for Automatic discovery](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#prepare-an-account-for-automatic-discovery)
* [Create an account in CSPSConfigtool to connect to a VMware vCenter Server / vSphere ESSi host](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#create-an-account-to-connect-to-vmware-vcenter-server-vmware-vsphere-exsi-host)
* [Add vCenter / vSphere ESX Host to Configuration Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#associate-a-vmware-vcenter-vmware-vsphere-esx-host-add-vcenter)
* [Change/Modify credentials to connect to vCenter/vSphere ESXi host] (https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#associate-a-vmware-vcenter-vmware-vsphere-esx-host-add-vcenter)
* [Delete a vCenter from Configuration Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-vCenter#delete-a-vcenter-in-azure-site-recovery)
