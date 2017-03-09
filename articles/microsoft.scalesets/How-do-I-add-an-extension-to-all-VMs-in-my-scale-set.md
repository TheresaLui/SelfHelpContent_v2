<properties
    pageTitle="How do I add an extension to all VMs in my scale set"
    description="How do I add an extension to all VMs in my scale set"
    service="scalesets"
    author="negat"
    displayOrder="47"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do I add an extension to all VMs in my scale set?

 - If update policy is set to automatic, redeploying the template with the new extension properties updates every VM.
- If update policy is set to manual, you must update the extension with manual mode, then do a manualUpdate on all instances.