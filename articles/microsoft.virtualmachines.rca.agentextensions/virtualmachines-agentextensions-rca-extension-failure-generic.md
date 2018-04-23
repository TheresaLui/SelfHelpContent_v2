<properties
pageTitle="Extension Execution Failure Error"
description="Extension Execution Failure Error"
infoBubbleText="Extension Execution Failure Error"
service="microsoft.compute"
resource="virtualmachines"
authors="scottAzure"
displayOrder=""
articleId="extension_failederror_generic"
diagnosticScenario="agentextensions"
selfHelpType="diagnostics"
supportTopicIds="32411845"
resourceTags=""
productPesIds="14749,15797,15571"
cloudEnvironments="public"
/>

# An extension reported a failure
<!--issueDescription-->
We have detected that **<!--$extensionname-->Extension Name<!--/$extensionname-->**   installed for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** has failed with the following status: **<!--$statuscode-->Status Code<!--/$statuscode-->**.

<!--$errormessage-->Error Message<!--/$errormessage-->
<!--/issueDescription-->

The extension has encountered an error and is displayed above.

For internal troubleshooting guidance, [Click here](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Deploy_a_new_VM/Guest_Agent_and_Extensions_Workflow)

For additional information regarding extensions and how to troubleshoot:<br>
* [Windows extensions overview and troubleshooting ](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-features)<br>
* [Linux extensions overview and troubleshooting ](https://docs.microsoft.com/azure/virtual-machines/linux/extensions-features)
