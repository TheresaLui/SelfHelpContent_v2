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
If you are trying to connect to a workgroup machine, run the following command as an administrator on the gateway machine. **TargetMachineIPAddress** should be the IP address of the workgroup machine you are connecting to. Also, when creating a Server management tools connection to the workgroup machine, use the machine’s IP address as the computer name.
**winrm set winrm/config/client @{ TrustedHosts="TargetMachineIPAddress" }**
* Logging on with a local Administrator account<br>
When entering credentials in the server connection's "Manage as" dialog box, in order to use a local Administrator account, you will need to enable this policy on the target machine by running the following command in an administrator session on the target machine:<br>
**REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1**
* Connecting to a workgroup machine on a different subnet<br>
In order to connect to a workgroup machine which is not on the same subnet as the gateway, make sure the firewall port for WinRM (TCP 5985) allows inbound traffic on the target machine. You can run the following command in an administrator session on the target machine to create this firewall rule:<br>
**NETSH advfirewall firewall add rule name="WinRM 5985" protocol=TCP dir=in localport=5985 action=allow**
* "CANNOT CONNECT" error when connecting to a server<br>
If you get a “CANNOT CONNECT” error when entering credentials in the “Manage as” popup dialog box, make sure the credentials are correct and the user is a member of the target server’s local Administrators group. In some cases, WinRM also requires that the user additionally be a member of the Remote Management Users group.
* TODO: Add section for gateway/server time mismatch
* Connecting to a Windows Server 2012 or 2012 R2 machine<br>
When configuring a connection to a Windows Server 2012 or 2012 R2 machine, if you get a “Required software not detected” error or have trouble installing the required packages, see the “I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine” section below.

## **Recommended documents**
[Introducing Server management tools](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)
