<properties
    pageTitle="Self signed certificate example"
    description="Self signed certificate example"
    service="scalesets"
    author="negat"
    displayOrder="25"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Self signed certificate example:

#### Create a self-signed Cert in a KeyVault
One way to create a self-signed cert in a KeyVault is to use the instructions from this Service Fabric article here: https://azure.microsoft.com/documentation/articles/service-fabric-cluster-security/
The powershell commands:
```powershell
Import-Module "C:\Users\mikhegn\Downloads\Service-Fabric-master\Scripts\ServiceFabricRPHelpers\ServiceFabricRPHelpers.psm1"
Login-AzureRmAccount
Invoke-AddCertToKeyVault -SubscriptionId <Your SubID> -ResourceGroupName KeyVault -Location westus -VaultName MikhegnVault -CertificateName VMSSCert -Password VmssCert -CreateSelfSignedCertificate -DnsName vmss.mikhegn.azure.com -OutputPath c:\users\mikhegn\desktop\
The preceding command gives you the input for the Resource Manager template.
#### Change Resource Manager Template
Add this property to the "virtualMachineProfile” as part of the scale set Resource:
```json 
"osProfile": {
            "computerNamePrefix": "[variables('namingInfix')]",
            "adminUsername": "[parameters('adminUsername')]",
            "adminPassword": "[parameters('adminPassword')]",
            "secrets": [
              {
                "sourceVault": {
                  "id": "[resourceId('KeyVault', 'Microsoft.KeyVault/vaults', 'MikhegnVault')]"
                },
                "vaultCertificates": [
                  {
                    "certificateUrl": "https://mikhegnvault.vault.azure.net:443/secrets/VMSSCert/20709ca8faee4abb84bc6f4611b088a4",
                    "certificateStore": "My"
                  }
                ]
              }
            ]
          }