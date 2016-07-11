<properties
	pageTitle="I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine"
	description="I can't set up a Server management node connection to a Windows Server 2012 or 2012 R2 machine"
	service="microsoft.servermanagement"
	resource="nodes"
	authors="jol"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine

## **Recommended steps**
In order to connect to a Windows Server 2012 or 2012 R2 machine using Server management tools, an additional WMI provider package and Windows Management Framework 5.0 is required. When connecting to the server using Server management tools, it will detect and ask if you would like these packages installed. If an error occurs while installing the packages, or if you cannot connect to the server after the packages are installed, try one or more of the following methods.

* Check the installation logs on the gateway machine<br>
Check the WMI and WMF installation logs on the **gateway machine** for any errors or details. These logs should be your first point of reference for troubleshooting and can be found in the path below. WMI installation logs are located in the Providers subfolder and WMF installation logs are located in the WMF5 subfolder.<br>
**%windir%\ServiceProfiles\NetworkService\AppData\Local\Temp\Logs\ServerManagerPrerequisites**
* Check the installation logs on the target machine<br>
If you need more detailed logs for advanced troubleshooting, check the WMI and WMF installation logs on the **target machine**.<br>
**%systemdrive%\SMTInstallers\Logs**
* If both packages are installed properly, but you still can’t connect to the target machine, see the additional troubleshooting steps in the “I can’t connect to a server” section above.
