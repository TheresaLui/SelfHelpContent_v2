<properties
    pageTitle="I can’t connect to a server"
    description="I can't connect to a Server management tools node"
    service="microsoft.servermanagement"
    resource="nodes"
    authors="daniellee-msft"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# I can’t connect to a server

## **Recommended steps**

To resolve common issues, try one or more of the following methods.

* Is the gateway’s health status displayed as “OK”?<br>
On the Server management tools connection blade, go to the Overview menu, check the Gateway name in the Essentials section and make sure it shows “OK”. If not, click on the Gateway name to open the Gateway blade and see details on the error. You can also find solutions to common gateway issues in the “Diagnose and solve problems” menu on the Gateway blade.
* Is the target server a workgroup (non-domain joined) machine?<br>
If yes, you will need to add the target server to the Trusted Hosts list on the gateway machine. On the gateway machine, run the following command in PowerShell or Command Prompt as Administrator. `TargetMachineNameOrAddress` should be the NetBIOS name, FQDN or IP address (IPv4 or IPv6) that you’ve used when creating the Server management tools connection in Azure (which is also the name displayed at the top of the blade). You can also add multiple machines by separating them with commas.<br>
**Command Prompt:** `winrm set winrm/config/client @{TrustedHosts=”TargetMachineNameOrAddress”}`<br>
**PowerShell:** `winrm set winrm/config/client '@{TrustedHosts="TargetMachineNameOrAddress"}'`<br>
**NOTE:** The commands above will replace any existing list of trusted hosts with the host(s) you specify in the command. You can use the following command in PowerShell with the `Concatenate` parameter to add a computer name to an existing list of trusted hosts.<br>
`Set-Item wsman:\localhost\Client\TrustedHosts TargetMachineNameOrAddress –Concatenate`
* Are you connecting with a local user account?<br>
When entering credentials in the server connection’s “Manage as” dialog box, you can use a local or domain account that is a member of the local administrators group on the target server. When using a local user account that is not the built-in administrator account, you will need to enable the policy on the target machine by running the following command in PowerShell or Command Prompt as Administrator on the target machine.<br>
`REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1`
* Are you connecting to a workgroup machine on a different subnet?<br>
In order to connect to a workgroup machine which is not on the same subnet as the gateway, make sure the firewall port for WinRM (TCP 5985) allows inbound traffic on the target machine. You can run the following command in PowerShell or Command Prompt as Administrator on the target machine to create this firewall rule:<br>
`NETSH advfirewall firewall add rule name=”WinRM 5985” protocol=TCP dir=in localport=5985 action=allow`
* “CANNOT CONNECT” error when connecting to a server<br>
If you get a “CANNOT CONNECT” error when entering credentials in the “Manage as” popup dialog box, make sure the credentials are correct and the user is a member of the target server’s local administrators group. In some cases, WinRM also requires that the user additionally be a member of the Remote Management Users group.
* Are you having a problem only when connecting to a Windows Server 2012 or 2012 R2 machine?<br>
If you can connect to a Windows Server 2016 machine, but not to a 2012 or 2012 R2 machine, also check the “I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine” section below.