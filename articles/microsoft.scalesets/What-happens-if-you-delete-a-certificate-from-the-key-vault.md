<properties
    pageTitle="What happens if you delete a certificate from the key vault"
    description="What happens if you delete a certificate from the key vault"
    service="scalesets"
    author="negat"
    displayOrder="36"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# What happens if you delete a certificate from the key vault?


If the secret is deleted in the key vault, and you stop deallocate all your VMs then start them again, you will encounter a failure. This failure is due to CRP needing to retrieve the secrets from Key Vault but not being able to. In this scenario, you can delete the certificates from the scale set model. 

The CRP component does not persist any customer secrets. If you stop deallocate all VMs in the scale set, then the cache is deleted. In this scenario, secrets are retrieved from key vault.

This issue is not hit on scale-out because there is a cached copy of the secret in fabric (at least in the single fabric tenant model).
 