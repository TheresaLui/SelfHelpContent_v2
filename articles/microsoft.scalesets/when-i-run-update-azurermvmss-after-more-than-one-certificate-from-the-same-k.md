<properties
    pageTitle="When I run Update-AzureRmVmss after more than one certificate from the same KeyVault"
    description="When I run Update-AzureRmVmss after more than one certificate from the same KeyVault"
    service="scalesets"
    author="negat"
    displayOrder="29"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# When I run Update-AzureRmVmss after more than one certificate from the same KeyVault, I get the following error:

 
Update-AzureRmVmss: List secrets contains repeated instances of /subscriptions/<my-subscription-id>/resourceGroups/internal-rg-dev/providers/Microsoft.KeyVault/vaults/internal-keyvault-dev, which is disallowed. Why can’t I add two certificates from the same KeyVault?
 
This behavior can happen if you're trying to add the same vault twice instead of a new vaultCertificate for the existing sourceVault. The Add-AzureRmVmssSecret does not work correctly for adding additional secrets.
 
If you want to add more secrets from the same key vault, you should update the list $vmss.properties.osProfile.secrets[0].vaultCertificates
 
You can see the expected input structure here:
https://msdn.microsoft.com/library/azure/mt589035.aspx
 
You need to find the secret in the scale set object that has the same containing key vault. Then you must add your certificate reference (the URL along with the secret store name) into the list associated with the vault.

Note: removing certificates from VMs through the scale set APIs is not currently supported.
 
New VMs will not have the old cert, but ones that had the cert already deployed will still have the old certificate.
 