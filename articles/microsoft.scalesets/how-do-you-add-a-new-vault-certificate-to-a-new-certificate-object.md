<properties
    pageTitle="How do you add a new vault certificate to a new certificate object"
    description="How do you add a new vault certificate to a new certificate object"
    service="scalesets"
    author="negat"
    displayOrder="34"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do you add a new vault certificate to a new certificate object?


If you want to add a vault certificate to existing secret, which should be the only one secret object, you can do it as in the following powershell example:
 
```powershell
$newVaultCertificate = New-AzureRmVmssVaultCertificateConfig -CertificateStore MY -CertificateUrl https://sansunallapps1.vault.azure.net:443/secrets/dg-private-enc/55fa0332edc44a84ad655298905f1809
 
$vmss.VirtualMachineProfile.OsProfile.Secrets[0].VaultCertificates.Add($newVaultCertificate)
 
Update-AzureRmVmss -VirtualMachineScaleSet $vmss -ResourceGroup $rg -Name $vmssName
```
 