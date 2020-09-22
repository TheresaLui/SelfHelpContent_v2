<properties
pageTitle="ExpressRoute Circuit Deprovisioning Incomplete"
description="ExpressRoute Circuit Deprovisioning Incomplete"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="seanj"
displayOrder="10"
articleId="ExpressRouteCircuitProvisioningDecomm"
diagnosticScenario="ProvisioningDecommissioningError"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Circuit Deprovisioning Incomplete
<!--issueDescription-->
We have identified a platform configuration issue for your private peering ExpressRoute connection named **<!--$CircuitName-->[CircuitName]<!--/$CircuitName-->** that uses service key: **<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**. The initial diagnosis is that the service provider has not updated the status to reflect that it has been decommissioned. See below for steps to resolve the issue.
<!--/issueDescription-->
## **Steps to resolve this issue**
**Note:** The following steps will resolve the issue by decommissioning the ExpressRoute Circuit.

1. Ask the circuit service provider to confirm when they used the Azure API to deprovision the circuit.
2. If they did not do so previously, do it now.
2. Once the circuit service provider has updated the status, you should be able to remove the circuit from your subscription.
<br>
Microsoft is continuously working to identify and resolve issues proactively. Please feel free to reach out with any questions. Again, we apologize for the inconvenience. 
