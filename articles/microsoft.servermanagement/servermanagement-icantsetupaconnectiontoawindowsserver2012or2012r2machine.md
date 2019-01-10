<properties
	pageTitle="I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine"
	description="I can't set up a Server management tools connection to a Windows Server 2012 or 2012 R2 machine"
	service="microsoft.servermanagement"
	resource="nodes"
	authors="jol"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake"
/>

# I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine

## **Recommended steps**
In order to connect to a Windows Server 2012 or 2012 R2 machine using Server management tools, an additional WMI provider package and Windows Management Framework 5.0 is required. When connecting to the server using Server management tools, it will detect and ask if you would like these packages installed. If an error occurs while installing the packages, or if you cannot connect to the server after the packages are installed, try one or more of the following methods.

* Check the installation logs on the gateway machine<br>
Check the WMI and WMF installation logs on the **gateway machine** for any errors or details. These logs should be your first point of reference for troubleshooting and can be found in the path below. WMI installation logs are located in the Providers subfolder and WMF installation logs are located in the WMF5 subfolder.<br>
**%windir%\ServiceProfiles\NetworkService\AppData\Local\Temp\Logs\ServerManagementPrerequisites**
* Check the installation logs on the target machine<br>
If you need more detailed logs for advanced troubleshooting, check the WMI and WMF installation logs on the **target machine**.<br>
**%systemdrive%\SMTInstallers\Logs**
* WinRM error on the target machine<br>
If the following error occurs after installing the packages or when connecting to a Windows Server 2012 or 2012 R2 machine, log on to the target machine and run “services.msc” to launch the Services MMC snap-in. Then restart the “Windows Remote Management (WS-Management)” service.<br>
**“The WinRM client received an HTTP server error status (500), but the remote service did not include any other information about the cause of the failure”**
* If you’ve tried all the steps above but still can’t connect to the target machine, see the additional troubleshooting steps in the “I can’t connect to a server” section above.

