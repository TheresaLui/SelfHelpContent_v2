<properties
    pageTitle="I do not see an option for users to pass in certificates as base64 strings that most other resource providers provide"
    description="I do not see an option for users to pass in certificates as base64 strings that most other resource providers provide"
    service="scalesets"
    author="negat"
    displayOrder="40"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# I do not see an option for users to pass in certificates as base64 strings that most other resource providers provide.


You can extract the latest versioned URL within a Resource Manager template to emulate the behavior you describe. You can include the following JSON property in your Resource Manager template:

```json 
"certificateUrl": "[reference(resourceId(parameters('vaultResourceGroup'), 'Microsoft.KeyVault/vaults/secrets', parameters('vaultName'), parameters('secretName')), '2015-06-01').secretUriWithVersion]"
```
 