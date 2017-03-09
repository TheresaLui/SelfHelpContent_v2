<properties
    pageTitle="How do you securely ship a certificate into the VM"
    description="How do you securely ship a certificate into the VM"
    service="scalesets"
    author="negat"
    displayOrder="22"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do you securely ship a certificate into the VM?  Is there an example of provisioning a scale set to run a website where the SSL for the website is shipped securely from a certificate configuration?  The common certificate rotation operation would amount to a configuration update operation.


We support installing customer certificates directly into Windows certificate store from their key vault.

In the context of scale sets...

https://msdn.microsoft.com/library/mt589035.aspx

```json
        "secrets": [ {
	          "sourceVault": {
		              "id": "/subscriptions/{subscriptionid}/resourceGroups/myrg1/providers/Microsoft.KeyVault/vaults/mykeyvault1"
		  }
		  "vaultCertificates": [ {
		              "certificateUrl": "https://mykeyvault1.vault.azure.net/secrets/{secretname}/{secret-version}",
			      "certificateStore": "certificateStoreName"
		  } ]
        } ]
```

It supports both windows and Linux.
