<properties
pageTitle="VM connectivity affected due to network stack initialization issue after live migration"
description="VM connectivity affected due to network stack initialization issue after live migration"
infoBubbleText="Connectivity issues detected with VM. See details on the right"
service="microsoft.compute"
resource="virtualmachines"
authors="rkrir"
ms.author="krisragh"
displayOrder="1"
articleId="NetworkDatapathLiveMigrationSerializationError"
diagnosticScenario="NetworkDatapathLiveMigrationSerializationError"
selfHelpType="resource"
supportTopicIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# We ran diagnostics on your VM and found an issue

We identified that a live migration was performed on the VM <!--$VMName-->[VMName]<!--/$VMName--> by Azure. After the live migration, the network stack for the VM failed to initialize as expected, at approximately <!--$FailureTimestamp-->[FailureTimestamp]<!--/$FailureTimestamp-->. This prevented connectivity to the VM from outside the virtual network topology. A fix for this bug was already being deployed to production and is expected to complete in ~4 weeks.

## **Recommended Steps**

Redeploying affected VMs (instructions available for [Linux](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux) and [Windows](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)) mitigates the issue.

We sincerely apologize for the inconvenience. We are continuously taking steps to help ensure such incidents do not occur in the future. In this case, this includes a fix for the code bug being tested and applied to all affected Azure regions, and a review of auto-detection and auto-mitigation logic to address this issue before customers experience impact.

## **Recommended Documents**

* [Live migrations](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-and-updates#live-migration)
