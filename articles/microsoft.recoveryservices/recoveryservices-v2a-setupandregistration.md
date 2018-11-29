<properties
	pageTitle="Site Recovery (VMware vCenter to Azure)/Add/register configuration server"
	description="Site Recovery (VMware vCenter to Azure)/Add/register configuration server"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593224"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>
# Site Recovery (VMware vCenter to Azure)/Add/register configuration server

## **Recommended steps**

**VMware to Azure**<br>

* Deploy Configuration Server using OVF template - [**tutorial**](https://docs.microsoft.com/azure/site-recovery/tutorial-vmware-to-azure#download-the-vm-template) and [**video**](https://azure.microsoft.com/blog/announcing-a-new-simplified-onboarding-experience-for-azure-site-recovery-vmware-to-azure/)</br>
* Change [**proxy settings** to connect the Configuration Server to the internet](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#modify-proxy-settings)</br>
* Manage the Configuration Server - [apply licence](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#update-windows-licence), [upgrade](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#upgrade-the-configuration-server) and  [delete/unregister](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#delete-or-unregister-a-configuration-server)</br>
- Re-register a Configuration Server (VMware) to - [the **same vault**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#reregister-a-configuration-server-in-the-same-vault) or [a **different vault**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#register-a-configuration-server-with-a-different-vault)<br>

**Physical to Azure**<br>

* [**Check prerequisites** to install a Configuration Server using the Unified Setup ](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#prerequisites)</br>
* Install new instance of [Configuration Server using the Unified Setup](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#download-the-latest-installation-file)</br>
* Change [proxy settings to connect the Configuration Server to the internet](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#modify-proxy-settings)</br>
- Re-register a Configuration Server (Physical) to - [the **same vault**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#reregister-a-configuration-server-with-the-same-vault) or [a **different vault**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#register-a-configuration-server-with-a-different-vault)<br>
* [**Troubleshoot** common installation and registration issues of Configuration Server](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#common-issues)</br>

**Common information**<br>

* [**Upgrade** existing instance of Configuration Server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#upgrade-the-configuration-server)</br>
* [**Add network adapter** to the Configuration Server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#add-a-network-adapter)<br>
* [**Renew SSL certificates** on existing instance of Configuration Server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#renew-ssl-certificates)</br>
