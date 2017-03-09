<properties
    pageTitle="Why does certificate version have to be specified when using key vault"
    description="Why does certificate version have to be specified when using key vault"
    service="scalesets"
    author="negat"
    displayOrder="38"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Why does certificate version have to be specified when using key vault?


The reason for this requirement is to make it clear to the user what certificate is deployed on their VMs.

If you create a VM then update your secret in the key vault, that new certificate will not be downloaded to your VMs. But your VMs will appear to reference it, and new VMs will get the new secret. To avoid this confusion, it is required that you reference an explicit secret version.
