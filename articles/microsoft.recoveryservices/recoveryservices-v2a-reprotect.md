<properties
	pageTitle="Site Recovery (VMware to Azure)/Reprotect VM after failover"
	description="Site Recovery (VMware to Azure)/Reprotect VM after failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536447"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2af00d4f-77ee-4aaf-9e43-5c74dfba2b24"
	ownershipId="Compute_SiteRecovery"
/>

# Site Recovery (VMware to Azure)/Reprotect VM after failover

Common issues during failback or reprotect
## **Recommended steps**

* vCenter account used for discovery should have the right permissions for failback <br>
[See the list of permissions here](https://aka.ms/asrsupfailbackperm)

* vCenter license should not be a free license - it should be either evaluation or Licensed. <br>
On your ESXi host node in vCenter, navigate to Configuration tab -> Licensed features. vSphere API should be listed under the product features
Failed over VM should be in the correct network

* VM should be running and be in a network to be able to communicate back to the configuration server and process server. <br>
Check if the VM is in your ExpressRoute or VPN attached Azure Network.

* The datastores that contain the VM's disk should be mounted onto the Master Targets ESXi host <br>
Make sure that the datastore is mounted as read write and is of VMFS type. Other datastore types are not supported currently.

* If the retention drive is not visible in the selection menu, add a new drive to the master target<br>
	1. Volume shouldn't be in use for any other purpose(target of replication etc.)
	2. Volume shouldn't be in lock mode.
	3. Volume shouldn't be cache volume. ( MT installation shouldn't exist on that volume. PS+MT custom installation volume is not eligible for retention volume. Here installed PS+MT volume is cache volume of MT. )
	4. The Volume File system type shouldn't be FAT and FAT32.
	5. The volume capacity should be non-zero. e. Default retention volume for Windows is R volume.
	6. Default retention volume for Linux is /mnt/retention.

* [Some common issues are also listed here](https://aka.ms/asrsupfailbackcommonissues)

## **Recommended documents**
The end to end [failback documentation is here](https://aka.ms/asrsupv2afailback)
