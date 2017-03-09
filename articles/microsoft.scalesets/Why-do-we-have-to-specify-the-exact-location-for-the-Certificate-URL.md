<properties
    pageTitle="Why do we have to specify the exact location for the Certificate URL"
    description="Why do we have to specify the exact location for the Certificate URL"
    service="scalesets"
    author="negat"
    displayOrder="37"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Why do we have to specify the exact location for the Certificate URL, as referenced here: per https://azure.microsoft.com/documentation/articles/service-fabric-cluster-security/, 

https://<name of the vault>.vault.azure.net:443/secrets/<exact location>
 
Per KeyVault documentation, the get-secret REST API should return the latest version of the secret if version is not specified:
 
Method | URL
--- | ---
GET | https://mykeyvault.vault.azure.net/secrets/{secret-name}/{secret-version}?api-version={api-version}

Replace {secret-name} with the name and {secret-version} with the version of the secret you want to retrieve. Secret version may be excluded in which case the current version is retrieved.
  