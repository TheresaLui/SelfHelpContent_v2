<properties
    pageTitle="RDPCert Expired"
    description="RDP certificate has expired"
    infoBubbleText="RDP certificate has expired"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani,timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="vmhealthsignal_5352ed8a-1807-4c31-a00d-184b641b18dd"
    diagnosticScenario="RDPCert Expired"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# RDP certificate has expired

<!--issueDescription-->
We have investigated and detected that the self-signed certificate associated with the RDP listener on your VM has expired, preventing connectivity to the VM via RDP.
<!--/issueDescription-->

## **Recommended Steps**

* To restore connectivity to the VM via RDP, please try the below steps via PowerShell using the [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/serialConsole)
* If you’re unfamiliar with the serial console or would like additional information, please refer to our [user guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)

### From the Serial Console

* Execute the following set of commands in the given order to reset the permission levels on the MachineKey folder and the RSA files to default. This folder is used to store certificate key pairs for the system and its users.
* Take ownership of the folder and its sub-directories: `takeown /f "C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys" /a /r`
* Backup the current access control lists: 

 	* ```md C:\BackupACLs```
	* ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /save C:\BackupACLs\machinekeys_before.txt /t /c```

* Add the system default ACLs to the MahcineKeys folder:

	* ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "NT AUTHORITY\System:(F)"```
	* ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "NT AUTHORITY\NETWORK SERVICE:(R)"```
	* ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "BUILTIN\Administrators:(F)"```

* Restart the Terminal Service to all the certificate renewal: `Restart-Service TermService -Force`

* If RDP is still now working, ensure that the self-signed certificate is renewed by executing the below commands in the given order:

  1. `Import-Module PKI`
  2. `Set-Location Cert:\LocalMachine`
  3. `$RdpCertThumbprint = 'Cert:\LocalMachine\Remote Desktop\'+((Get-ChildItem -Path 'Cert:\LocalMachine\Remote Desktop\').thumbprint)`
  4. `Remove-Item -Path $RdpCertThumbprint`
  5. `Stop-Service -Name "SessionEnv"`
  6. `Start-Service -Name "SessionEnv"`
  
