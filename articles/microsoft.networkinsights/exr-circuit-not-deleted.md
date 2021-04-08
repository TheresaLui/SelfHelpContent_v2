<properties
    pageTitle="Express Route Circuit can't be deleted"
    description="Express Route Circuit can't be deleted"
    infoBubbleText="Need more information about this issue? See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="CircuitNotDeleted"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds="32627989, 32627990, 32627991, 32627992, 32627993, 32675801"
    resourceTags=""
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureExpressRoute"
/>

# Express Route Circuit can't be deleted
<!--issueDescription-->
We have identified a recent failed attempt to delete your ExpressRoute circuit **[Azure resource name]**. ExpressRoute facilitates connectivity to private resources deployed within an Azure virtual network via private peering or to online Microsoft resources deployed with a public IP address via Microsoft peering. To delete an ExpressRoute circuit, any reference resources (such as Route Filters or connections) must be deleted and any peering must be deprovisioned.
<!--/issueDescription-->

## **Recommended Steps**

- Delete any route filters associated with the target ExpressRoute circuit
- Delete any connection objects between the target ExpressRoute circuit and any virtual network gateways
- Deprovision private peering
- Deprovision Microsoft peering
- If you're using the ExpressRoute partner model, the ExpressRoute partner must deprovision the connection on their end and update the circuit status. Please work directly with your ExpressRoute partner to complete this step.
