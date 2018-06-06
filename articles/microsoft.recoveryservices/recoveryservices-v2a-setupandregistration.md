<properties
	pageTitle="Site Recovery (VMware vCenter to Azure)/Add/register configuration server"
	description="Site Recovery (VMware vCenter to Azure)/Add/register configuration server"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536387"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>
# Site Recovery (VMware vCenter to Azure)/Add/register configuration server

Common issues during Setup & Registration of a Configuration Server

## **Recommended Steps**
* Ensure that the server on which you install the  **Configuration Server** has access to the following url's <br>
	1. \*.hypervrecoverymanager.windowsazure.com
	2. \*.accesscontrol.windows.net
	3. \*.backup.windowsazure.com
	4. \*.blob.core.windows.net
 	5. \*.store.core.windows.net
	6. time.nist.gov
	7. time.windows.com
	8. https://dev.mysql.com/get/archives/mysql-5.5/mysql-5.5.37-win32.msi

* Ensure that the system clock on the server where you install **Configuration Server** has the correct time for the time zone the server is configured for.

* Ensure you choose the **'Connect to Azure Site Recovery using a proxy server'** option if you know that the server on which you are installing  **Configuration Server**  is behind a proxy server.<br>
	1. This setting can be changed at any point of time by running the **CSPSConfigtool.exe** and re-registering the Microsoft Azure Site Recovery Provider.
	2. The **CSPSConfigtool.exe** can be found at [Install Location]\home\svsystems\bin folder in the Configuration Server.

* Ensure that the server on which you plan to install the Configuration Sever has PowerCLI version 6.0 installed on it.<br>
	1. Higher/Lower version of PowerCLI are not supported.
	2. You can download PowerCLI 6.0 from https://developercenter.vmware.com/tool/vsphere_powercli/6.0

* Ensure that the following Group policies are not enabled for the user running setup.<br>
	1. Prevent access to the command prompt
	2. Prevent access to registry editing tools
	3. Trust logic for file attachments
	4. Turn on Script Execution

* Ensure that the server on which **Configuration Server** will be installed has TLS1.0 enabled.

* Ensure that the computer on which the **Configuration Server** is being installed does not have the following configured for the IIS Services.<br>
	1. More than one websites already configured
	2. FastCGISettings are already configured
	3. Port 443 is already bound as the "Default Web Site" secure Port
	4. Anonymous Authentication is disabled

* If after successful registration of your **Configuration Server**, you are unable to discovery your vCenter then ensure that you don't have other versions of Perl or PHP installed on the computer that is running the **Configuration Sever**

## **Recommended Documents**
* [Configuration Server hardware and software prerequisites](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#prerequisites) <br>
* [Installing & Registering a Configuration Server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#installing-and-registering-a-configuration-server-from-gui) <br> 
* [Upgrading a Configuration Server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#upgrading-a-configuration-server) <br>
* [How to register a Configuration Server with a different Vault](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#registering-a-configuration-server-with-a-different-recovery-services-vault) <br>
* [Renew Configuration Server SSL Certificate](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#renew-configuration-server-secure-socket-layerssl-certificates) <br>
* [Modifying Configuration Server's proxy settings](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#modifying-proxy-settings-for-configuration-server) <br>
* [Scale Limits for Configuration Server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#sizing-requirements-for-a-configuration-server) <br>
* [Delete or Unregister a Configuration Server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#delete-or-unregister-a-configuration-server) <br>
* [Foprce Delete or Unregister a Configuration Server using Azure PowerShell](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#delete-or-unregister-a-configuration-server-powershell) <br>
* [Renew Secure Socket Layer (SSL) Certificate on your Configuration Server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#renew-configuration-server-secure-socket-layerssl-certificates)

