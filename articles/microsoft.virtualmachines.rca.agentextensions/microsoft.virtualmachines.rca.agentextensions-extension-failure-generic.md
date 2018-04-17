<properties
pageTitle="Extension Execution Failure"
description="Extension Execution Failure"
infoBubbleText="Extension Execution Failure"
service="microsoft.compute"
resource="virtualmachines"
authors="scottAzure"
displayOrder=""
articleId="extension_failederror_generic"
diagnosticScenario="Extension Execution Failure"
selfHelpType="diagnostics"
supportTopicIds="32411845"
resourceTags=""
productPesIds="14749,15797,15571"
cloudEnvironments="public"
/>

# An extension reported a failure
<!--issueDescription-->
We have detected that **<!--$extensionname-->Extension Name<!--/$extensionname-->**   installed for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** has failed with the following status: **<!--$statuscode-->Status Code<!--/$statuscode-->**.

> <!--$errormessage-->Error Message!--/$errormessage-->

<!--/issueDescription-->

The installed version of the agent is below the required minimum version for the VM to run in Azure. Please upgrade the agent version installed on this virtual machine. Microsoft also recommends updating any custom images that may be used in future deployments to avoid this issue.<br>

For additional information regarding extensions and how to troubleshoot:<br>
* [Windows extensions overview and troubleshooting ](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-features)<br>
* [Linux extensions overview and troubleshooting ](https://docs.microsoft.com/azure/virtual-machines/linux/extensions-features)<br>
