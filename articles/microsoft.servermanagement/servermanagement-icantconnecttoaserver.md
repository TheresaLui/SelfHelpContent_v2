<properties
	pageTitle="I can’t connect to a server"
	description="I can't connect to a Server management tools node"
	service="microsoft.servermanagement"
	resource="nodes"
	authors="jol"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I can’t connect to a server

## **Recommended steps**
To resolve common issues, try one or more of the following methods.

* Check the gateway's health status<br>
Make sure the Health status on the Gateway blade is displayed as “OK”. If not, see the “I can’t connect to a gateway” section in the Gateway blade’s Troubleshoot menu.
* Connecting to a non-domain-joined workgroup machine<br>
If you are trying to connect to a workgroup machine, run the following command in PowerShell or Command Prompt as Administrator on the gateway machine. **TargetMachineIPAddress** should be the IP address of the workgroup machine you are connecting to. Also, when creating a Server management tools connection to the workgroup machine, use the machine’s IP address as the computer name.<br><br>
**winrm set winrm/config/client @{ TrustedHosts="TargetMachineIPAddress" }**
* Logging on with a local user account<br>
When entering credentials in the server connection's "Manage as" dialog box, in order to use a local user account that is a member of the local administrators group, you will need to enable this policy on the target machine by running the following command in PowerShell or Command Prompt as Administrator on the target machine:<br><br>
**REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1**
* Connecting to a workgroup machine on a different subnet<br>
In order to connect to a workgroup machine which is not on the same subnet as the gateway, make sure the firewall port for WinRM (TCP 5985) allows inbound traffic on the target machine. You can run the following command in PowerShell or Command Prompt as Administrator on the target machine to create this firewall rule:<br><br>
**NETSH advfirewall firewall add rule name="WinRM 5985" protocol=TCP dir=in localport=5985 action=allow**<br><br>
[Windows Remote Management - Obtaining Data from a Remote Computer](https://msdn.microsoft.com/en-us/library/aa384423.aspx)
* "CANNOT CONNECT" error when connecting to a server<br>
If you get a “CANNOT CONNECT” error when entering credentials in the “Manage as” popup dialog box, make sure the credentials are correct and the user is a member of the target server’s local administrators group. In some cases, WinRM also requires that the user additionally be a member of the Remote Management Users group.
* Connecting to a Windows Server 2012 or 2012 R2 machine<br>
When configuring a connection to a Windows Server 2012 or 2012 R2 machine, if you get a “Required software not detected” error or have trouble installing the required packages, see the “I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine” section below.

## **Recommended documents**
[Introducing Server management tools](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)
