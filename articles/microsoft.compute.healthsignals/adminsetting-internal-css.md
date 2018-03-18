<properties
pageTitle="Admin Account Disabled"
description="Administrator Setting"
infoBubbleText="Administrator"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_2fd10e1f-f50f-4087-8269-ae7bbfb34489"
diagnosticScenario="Administrator Setting"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# Built-in Administrator account has issues
<!--issueDescription-->
Built-in Administrator account is disabled
<!--/issueDescription-->

## **Customer Ready RCA**

The user account being used for the RDP connection is currently disabled.

In a few cases w.r.t VMs migrated from On-prem or created specialized disks, the built-in administrator account is sometimes disabled.

Push the following script using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript) to enable the user account:

 ```
$adminAccount = Get-WmiObject Win32_UserAccount -filter "LocalAccount=True" | ? {$_.SID -Like "S-1-5-21-*-500"}
if($adminAccount.Disabled)
{
    $adminAccount.Disabled = $false
    $adminAccount.Put()
}
 ```
