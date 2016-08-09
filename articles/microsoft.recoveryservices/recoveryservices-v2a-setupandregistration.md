<properties
	pageTitle="Setup and Registration of Configuration Servers"
	description="Setup and Registration of Configuration Servers"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32536387"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ** Common issues during Setup & Registration**

### Ensure that the server on which you install the  **Configuration Server** has access to the following url's
- *.hypervrecoverymanager.windowsazure.com
- *.accesscontrol.windows.net
- *.backup.windowsazure.com
- *.blob.core.windows.net
- *.store.core.windows.net
- https://www.msftncsi.com/ncsi.txt
- https://dev.mysql.com/get/archives/mysql-5.5/mysql-5.5.37-win32.msi

### Ensure that the system clock on the server where you install **Configuration Server** has the correct time for the time zone the server is configured for.
  ![System Time Check](./media/time-sync-issue.png)

### Always choose the **'Connect to Azure Site Recovery using a proxy server'** option if you know that the server on which you are installing  **Configuration Server**  is behind a proxy server.
- This setting can be changed at any point of time by running the **CSPSConfigtool.exe** and re-registering the Microsoft Azure Site Recovery Provider.
- The **CSPSConfigtool.exe** can be found at [Install Location]\home\svsystems\bin.

### The  **Configuration Server** cannot be installed on a Domain Controller

### Ensure that the server on which you plan to install the Configuration Sever has PowerCLI version 6.0 installed on it.
- Higher/Lower version of PowerCLI are not supported.
- You can download PowerCLI 6.0 from https://developercenter.vmware.com/tool/vsphere_powercli/6.0

### Ensure that the following Group policies are not enabled for the user running setup.
- Prevent access to the command prompt
- Prevent access to registry editing tools
- Trust logic for file attachments
- Turn on Script Execution

### Ensure that the server on which **Configuration Server** will be installed has TLS1.0 enabled.

### Ensure that the computer on which the **Configuration Server** is being installed does not have the following configured for the IIS Services.
- More than one websites already configured
- FastCGISettings are already configured
- Port 443 is already bound as the "Default Web Site" secure Port
- Anonymous Authentication is disabled

### If after successful registration of your **Configuration Server**, you are unable to discovery your vCenter then ensure that you don't have other versions of Perl or PHP installed on the computer that is running the **Configuration Sever**
