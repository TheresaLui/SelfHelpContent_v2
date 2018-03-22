<properties
pageTitle="Password Expired"
description="Administrator account password expired"
infoBubbleText="Built-in Administrator account has issues"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="vmhealthsignal_e78569b2-cde5-488b-acc4-c79a307c12c9"
diagnosticScenario="Admini password expired"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# Built-in Administrator account has issues
<!--issueDescription-->
Built-in Administrator account password has expired
<!--/issueDescription-->

## **Customer Ready Mitigation Steps**

The password of the built-in administrator account has expired so RDP access using this account is unavailable.

Below are articles with detailed steps to reset the password through Azure Portal/PowerShell:
* [Reset RDP password](https://docs.microsoft.com/azure/virtual-machines/windows/reset-rdp)
* [Reset local password without Azure Guest agent](https://docs.microsoft.com/azure/virtual-machines/windows/reset-local-password-without-agent)


## **Internal**

Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/Basic_Workflow/VM_Responding_Bucket/Password_Reset_Bucket)
