<properties
	pageTitle="Add new servers to Hyper-V Site"
	description="Add new servers to Hyper-V Site"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32536385"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ** Common issues during Setup & Registration**

### Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's
- *.hypervrecoverymanager.windowsazure.com
- *.accesscontrol.windows.net
- *.backup.windowsazure.com
- *.blob.core.windows.net
- *.store.core.windows.net

### Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.
  ![System Time Check](./media/time-sync-issue.png)

### Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.

### The **Microsoft Azure Site Recovery Provider** cannot be installed on a Domain Controller
