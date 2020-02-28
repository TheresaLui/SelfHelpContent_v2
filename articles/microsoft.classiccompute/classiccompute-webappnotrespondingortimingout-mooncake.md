<properties
	pageTitle="My web application is not responding or timing out"
	description="My web application is not responding or timing out"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	ms.author="juluk"
	displayOrder="29"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="classiccompute-webappnotrespondingortimingout-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# My web application is not responding or timing out

## **Recommended Steps**

1. Check the Cloud Service availability on Azure portal. Ensure that all role instances are in a **Ready** state. If they are not, refer to the troubleshooting blade.
2. RDP into the role instance and check the IIS process (**w3wp.exe**) in Task Manager is running. If the **w3wp.exe** process does not show in Task Manager, go to [IIS Manager](https://technet.microsoft.com/library/jj635847.aspx) and restart the application.
3. Check the http response code you get in the browser. **50x** errors are application-related issues, refer to the troubleshooting blade.
4. Check that the default ports **80** (for http) and **443** (for https) are accessible. Use **TELNET** or **TCPING** to ensure that the **w3wp.exe** process is listening on it. 
5. If your web application is accessible locally but not externally, it could be a network-related issue.
