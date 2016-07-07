<properties
	pageTitle="I can’t connect to a server"
	description="I can't connect to a Server management node"
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

* Make sure the Health status on the Gateway blade is displayed as “OK”. If not, see the “I can’t connect to a gateway” section in the Gateway blade’s Troubleshoot menu.
* If you are trying to connect to a non-domain-joined workgroup machine, run this command as an administrator on the gateway machine:<br>
winrm set winrm/config/client @{ TrustedHosts="<<IP address>>" }<br>
<<IP address>> should be the IP address of the workgroup machine you are trying to connect to.
Also, when creating a Server management tools connection to the workgroup machine, use the machine’s IP address as the computer name.
* In order to connect using the local Administrator account, you will need to enable this policy on the target machine by running the following command in an administrator session on the target machine:
REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1
* In order to connect to a workgroup machine which is not on the same subnet as the gateway, make sure the firewall port for WinRM (TCP 5985) allows inbound traffic on the target machine. You can run the following command in an administrator session on the target machine to create this firewall rule:<br>
NETSH advfirewall firewall add rule name="WinRM 5985" protocol=TCP dir=in localport=5985 action=allow
* If you get a “CANNOT CONNECT” error when entering credentials in the “Manage as” popup dialog box, make sure the credentials are correct and the user is a member of the target server’s local Administrators group. In some cases, WinRM also requires that the user additionally be a member of the Remote Management Users group.
* TODO: Add section for gateway/server time mismatch
* When configuring a connection to a Windows Server 2012 or 2012 R2 machine, if you get a “Required software not detected” error or have trouble installing the required packages, see the “I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine” section below.

## **Recommended documents**
[Introducing Server management tools](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)
