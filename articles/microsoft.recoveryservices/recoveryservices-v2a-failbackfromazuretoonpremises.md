<properties
	pageTitle="Site Recovery (VMware to Azure)/Failback from Azure to on-premises"
	description="Site Recovery (VMware to Azure)/Failback from Azure to on-premises"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536408"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="3ba69fe9-aa9b-42cf-a1d2-d24baee92c89"
	ownershipId="Compute_SiteRecovery"
/>

# Site Recovery (VMware to Azure)/Failback from Azure to on-premises

Common issues during failback or reprotect
## **Recommended steps**

* Site-to-site VPN or express route over private peering is required for failback
Before you failback, you need to ensure a Site to Site VPN is available such that the failed over VMs in Azure have a line of sight to the Configuration server on-premises. Replication from Azure to On-premises happens only over VPN/ER(private peering). For more details look at [failback documentation](https://aka.ms/asrsupv2afailback).

* Storage vMotion should not be enabled on the Master Target <br>
Boot of the virtual machines can fail with error like "VMware ESX cannot find the virtual disk "DRIVE0.vmdk". Verify the path is valid and try again." You can find the disks from the datastores and attach it to the VM after which the VM will boot successfully.

* vCenter account used for discovery should have the right permissions for failback <br>
[See the list of permissions here](https://aka.ms/asrsupfailbackperm)

* vCenter license should not be a free license - it should be either evaluation or Licensed. <br>
On your ESXi host node in vCenter, navigate to Configuration tab -> Licensed features. vSphere API should be listed under the product features


* The datastores that contain the VM's disk should be mounted onto the Master Targets ESXi host<br>
Make sure that the datastore is mounted as read write and is of VMFS type. Other datastore types are not supported currently.

* If the retention drive is not visible in the selection menu, add a new drive to the master target <br>
	1. Volume shouldn't be in use for any other purpose(target of replication etc.)
	2. Volume shouldn't be in lock mode.
	3. Volume shouldn't be cache volume. ( MT installation shouldn't exist on that volume. PS+MT custom installation volume is not eligible for retention volume. Here installed PS+MT volume is cache volume of MT. )
	4. The Volume File system type shouldn't be FAT and FAT32.
	5. The volume capacity should be non-zero. e. Default retention volume for Windows is R volume.
	6. Default retention volume for Linux is /mnt/retention.


* [Some common issues are also listed here](https://aka.ms/asrsupfailbackcommonissues)

## **Recommended documents**
The end to end [failback documentation is here](https://aka.ms/asrsupv2afailback)
