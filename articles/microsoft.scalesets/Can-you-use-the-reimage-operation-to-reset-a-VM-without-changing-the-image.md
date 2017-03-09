<properties
    pageTitle="Can you use the reimage operation to reset a VM without changing the image"
    description="Can you use the reimage operation to reset a VM without changing the image"
    service="scalesets"
    author="negat"
    displayOrder="10"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Can you use the reimage operation to reset a VM without changing the image? (that is, reset a VM to factory settings rather than to a new image)?


Yes. See: https://docs.microsoft.com/rest/api/virtualmachinescalesets/manage-all-vms-in-a-set

However, if your scale set references a platform image with version = “latest” your VM can update to a later OS image when you call reimage.

