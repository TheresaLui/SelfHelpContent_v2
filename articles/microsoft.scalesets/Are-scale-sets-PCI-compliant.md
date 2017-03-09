<properties
    pageTitle="Are scale sets PCI-compliant"
    description="Are scale sets PCI-compliant"
    service="scalesets"
    author="negat"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Are scale sets PCI-compliant?


Scale Sets are a thin API layer on top of the Compute Resource Provider, which is all a part of the “Compute Platform” area within the Azure Service Tree.

Therefore, from a compliance perspective, scale sets are a fundamental part of the Azure Compute Platform. As such, they share the same team, tools, processes, deployment methodology, security controls, JIT, monitoring, alerting, etc. as the Compute Resource Provider (CRP) itself.  Scale sets are PCI-compliant because Compute Resource Provider is a part of the current PCI DSS attestation:

For more information, See: [https://www.microsoft.com/TrustCenter/Compliance/PCI](https://www.microsoft.com/TrustCenter/Compliance/PCI).



