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

##### From the Serial Console:

* Execute the following set of commands in the given order to reset the permission levels on the MachineKey folder and the RSA files to default. This folder is used to store certificate key pairs for the system and its users:

  ```takeown /f "C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys" /a /r```<br>
  ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "NT AUTHORITY\System:(F)"```<br>
  ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "NT AUTHORITY\NETWORK SERVICE:(R)"```<br>
  ```icacls C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys /t /c /grant "BUILTIN\Administrators:(F)"```<br>
  ```Restart-Service TermService -Force```

* Now ensure that the self-signed certificate is renewed by executing the below commands in the given order:

  ```Import-Module PKI```<br>
  ```Set-Location Cert:\LocalMachine```<br>
  ```$RdpCertThumbprint = 'Cert:\LocalMachine\Remote Desktop\'+((Get-ChildItem -Path 'Cert:\LocalMachine\Remote Desktop\').thumbprint)```<br>
  ```Remove-Item -Path $RdpCertThumbprint```<br>
  ```Stop-Service -Name "SessionEnv"```<br>
  ```Start-Service -Name "SessionEnv"```<br>
