<properties
	pageTitle="Site Recovery Provider Setup & Registration"
	description="Site Recovery Provider Setup & Registration"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32536454"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ** Common issues during Setup & Registration**

### Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's
- *.hypervrecoverymanager.windowsazure.com
- *.accesscontrol.windows.net
- *.store.core.windows.net
- https://www.msftncsi.com/ncsi.txt


### Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.
  ![System Time Check](./media/time-sync-issue.png)

### Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.
- This setting can be change at any point of time by running the DRConfigurator.exe and re-registering the Microsoft Azure Site Recovery Provider.

### The **Microsoft Azure Site Recovery Provider** cannot be installed on a Domain Controller
