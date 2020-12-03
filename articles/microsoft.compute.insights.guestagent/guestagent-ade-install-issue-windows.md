<properties
    pageTitle="Azure Disk Encryption Extension and VM Agent Installation Issue"
    description="Resolve installation issues with VM AGent and Azure Disk Encryption extension on Windows VMs"
    infoBubbleText="Resolve GuestAgent ADE Installation Issue"
	service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS,timbasham"
    ms.author="mnanda,tibasham"
    displayOrder=""
    articleId="GuestAgent-ADE-Install-Issue-Insight"
    diagnosticScenario="Resolve VM Agent and ADE installation Issue"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745,16080"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM Deployment Template with Disk Encryption has failed

<!--issueDescription-->
We detected that a recent deployment failure for <!--$vmname-->[vmname]<!--/$vmname--> was due to a known issue. Creation of the VM will succeed but Azure Disk Encryption (ADE) will show a failure.

In this scenario, the VM creation will succeed, but the installation of the VM Agent, as well as enabling ADE, will show as failed. This failure occurs because the ADE installation initiates a reboot that interrupts the VM Agent installation.
<!--/issueDescription-->

## **Recommended Steps**

Follow the steps below to remediate the issue, before opening a support ticket.

The workaround for this issue involves completing the VM Agent installation before the ADE installation restarts the VM by adding another extension to the template and making the ADE extension depend on that extension using the [dependsOn](https://docs.microsoft.com/azure/azure-resource-manager/templates/define-resource-dependency) element. 

### If you are installing any other extensions as part of your deployment
Add the [dependsOn](https://docs.microsoft.com/azure/azure-resource-manager/templates/define-resource-dependency) element to your ADE block and reference any one of these extensions. 

### If you are not installing any other extensions as part of your deployment
You can use the [Custom Script Extension (CSE)](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-windows#extension-schema) with a script or command that echoes `$null`. Add the [dependsOn](https://docs.microsoft.com/azure/azure-resource-manager/templates/define-resource-dependency) element to your ADE block and reference your CSE.

In the below example CSE is added executing `{$null}`, and ADE depends on CSE.

```
{
    "type": "Microsoft.Compute/virtualMachines/extensions",
    "name": "[concat(parameters('vmName'), '/CustomScriptExtension')]",
    "apiVersion": "2020-06-01",
    "location": "[parameters('location')]",
    "dependsOn": [
        "[resourceId('Microsoft.Compute/virtualMachines/', parameters('vmName'))]"
    ],
    "properties": {
        "publisher": "Microsoft.Compute",
        "type": "CustomScriptExtension",
        "typeHandlerVersion": "1.10",
        "autoUpgradeMinorVersion": true,
        "settings": {
            "commandToExecute": "PowerShell -ExecutionPolicy Bypass -NonInteractive -NoProfile -NoLogo -Command \"& {$null}\""
        }
    }
},
{
    "type": "Microsoft.Compute/virtualMachines/extensions",
    "name": "[concat(parameters('vmName'), '/AzureDiskEncryption')]",
    "apiVersion": "2020-06-01",
    "location": "[parameters('location')]",
    "dependsOn": [
        "[concat('Microsoft.Compute/virtualMachines/', variables('vmName'),'/extensions/CustomScriptExtension')]"
    ],
    "properties": {
        "publisher": "Microsoft.Azure.Security",
        "type": "AzureDiskEncryption",
        "typeHandlerVersion": "2.2",
        "autoUpgradeMinorVersion": true,
        "settings": {
            "EncryptionOperation": "[variables('encryptionOperation')]",
            "KeyEncryptionAlgorithm": "[variables('KeyEncryptionAlgorithm')]",
            "KeyVaultURL": "[variables('KeyVaultURL')]",
            "KeyEncryptionKeyURL": "[variables('KeyEncryptionKeyURL')]",
            "KeyVaultResourceId": "[variables('KeyVaultResourceId')]",
            "KekVaultResourceId": "[variables('KeyVaultResourceId')]",
            "VolumeType": "[variables('VolumeType')]"
        }
    }
}
```
