<properties
    pageTitle="How do I get property information for each VM without having to make multiple calls"
    description="How do I get property information for each VM without having to make multiple calls"
    service="scalesets"
    author="negat"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do I get property information for each VM without having to make multiple calls? For example: getting the Fault Domain for each VM in my 100 scale set?


You can call ListVMInstanceViews by:

`/subscriptions/<subscription_id>/resourceGroups/<resource_group_name>/providers/Microsoft.Compute/virtualMachineScaleSets/<scaleset_name>/virtualMachines?$expand=instanceView&$select=instanceView`
