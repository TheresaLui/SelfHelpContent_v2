<properties
pageTitle="VM Health Signal"
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


# Built-in Administrator account is disabled

<!--issueDescription-->
The account you are using to for RDP connection, is currently disabled.
<!--/issueDescription-->

Please note, if the Client OS machines is migrated from OnPrem or deployed from gallery, the built-in administrator account is sometimes not enabled by default in the image.

Push the following script using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript) to enable the user account:

 ```
$adminAccount = Get-WmiObject Win32_UserAccount -filter "LocalAccount=True" | ? {$_.SID -Like "S-1-5-21-*-500"}
if($adminAccount.Disabled)
{
    $adminAccount.Disabled = $false
    $adminAccount.Put()
}
 ```
