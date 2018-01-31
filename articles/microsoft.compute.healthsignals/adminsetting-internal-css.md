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

# Guest VM Health Signal Insight
<!--issueDescription-->
## **Built-in Administrator account has issues**
Built-in Administrator account is disabled
<!--/issueDescription-->

## **Recommended Steps - Internal**
**Administrator account is disabled**

The account customer is trying to use on the RDP connection, is currently disabled.

Please note, if the Client OS machines is migrated from OnPrem or deployed from gallery, the built-in administrator account is not enabled by default in the image. Windows Client VL/CSP Customers who bring their own VHDs to Azure will face this issue.  

Please refer to the steps in the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can’t_RDP-SSH/TSG/VM_Responding_Bucket/The_user_account_is_currently_disabled_and_cannot_be_used) to enable the local account.  
