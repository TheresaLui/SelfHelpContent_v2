<properties
    pageTitle="How do I take an existing SSH public key and inject it into the scale set SSH layer during provisioning"
    description="How do I take an existing SSH public key and inject it into the scale set SSH layer during provisioning"
    service="scalesets"
    author="negat"
    displayOrder="28"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do I take an existing SSH public key and inject it into the scale set SSH layer during provisioning?  I would like to store the SSH Public Key values in Azure Key Vault, and then utilize them in my Resource Manager template.


If you are only providing the VMs a public ssh key, there is no reason to put the public keys in the key vault because public keys are not secret.
 
You can provide SSH public keys in plain text when you create a Linux VM.
An example can be found here:

https://github.com/Azure/azure-quickstart-templates/blob/master/101-vm-sshkey/azuredeploy.json
 
Specifically:

```json
"linuxConfiguration": {  
          "ssh": {  
            "publicKeys": [ {  
              "path": "path",
              "keyData": "publickey"
            } ]
          }
```
 
linuxConfiguration Element Name | Required | Type | Description
--- | --- | --- | --- |  ---
ssh | No | Collection | Specifies the ssh key configuration for a Linux OS.
path | Yes | String | Specifies the Linux file path that the ssh keys or certificate should be placed at.
keyData | Yes | String | Specifies a base64 encoded ssh public key.
 