<properties
    pageTitle="Is there a way to specify an SSH key pair that I want to use for SSH authentication with a Linux scale set from a Resource Manager template"
    description="Is there a way to specify an SSH key pair that I want to use for SSH authentication with a Linux scale set from a Resource Manager template"
    service="scalesets"
    author="negat"
    displayOrder="26"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Is there a way to specify an SSH key pair that I want to use for SSH authentication with a Linux scale set from a Resource Manager template?  


The REST API for the osProfile looks similar to the ordinary VM case:
 
https://msdn.microsoft.com/library/azure/mt589035.aspx#linuxconfiguration
 
Include an `osProfile` in your template like the following example:

```json 
"osProfile": {
          "computerName": "[variables('vmName')]",
          "adminUsername": "[parameters('adminUserName')]",
          "linuxConfiguration": {
            "disablePasswordAuthentication": "true",
            "ssh": {
              "publicKeys": [
                {
                  "path": "[variables('sshKeyPath')]",
                  "keyData": "[parameters('sshKeyData')]"
                }
              ]
            }
          }
        }
```
 
This JSON block is used in the following quickstart template:
 
https://github.com/Azure/azure-quickstart-templates/blob/master/101-vm-sshkey/azuredeploy.json
 
Also look at the OS Profile on this template:
 
https://github.com/ExchMaster/gadgetron/blob/master/Gadgetron/Templates/grelayhost.json
