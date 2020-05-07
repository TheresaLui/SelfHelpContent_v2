<properties
    pageTitle="Azure Platform Network Failure"
    description="Virtual machine networking is not functional due to a networking platform failure."
    infoBubbleText="We have detected that your VM is inaccessible due to an Azure networking platform failure."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="PlatformNetworkFail"
    diagnosticScenario="PlatformNetworkFailure"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Virtual machine networking is not accessible due to a networking platform failure

<!--issueDescription-->
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is not accessible due to an Azure network platform failure.
<!--/issueDescription-->

## **Recommended Steps**

* Redeploy to a new host by accessing the [Redeploy blade](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/redeploy) in the Azure portal and clicking the `Redeploy` button
* Verify if you are able to connect via RDP
