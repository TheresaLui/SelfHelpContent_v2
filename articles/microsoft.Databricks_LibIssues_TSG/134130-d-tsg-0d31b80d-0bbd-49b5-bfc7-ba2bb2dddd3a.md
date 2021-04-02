<properties
 pageTitle="Library resolution is stuck in cluster UI"
 description="Library resolution is stuck in cluster UI"
 service="Microsoft.Databricks"
 resource="Microsoft.Databricks/workspaces"
 authors="AzureData_AzureDatabricks"
 ms.author="AzureData_AzureDatabricks"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="0d31b80d-0bbd-49b5-bfc7-ba2bb2dddd3a"
 ownershipId="AzureData_AzureDatabricks"
/>

# Library resolution is stuck in cluster UI

### Symptom

The library resolution (for all types) is stuck in the cluster UI (rotates forever) and commands are slow to get started. The equivalent pip install commands work fine from notebook though it is slow.

### Troubleshooting

- Verify if you can run equivalent `%sh pip install <library>`
- Check if subnet CIDR range is outside private CIDR range

### Solution

This can happen if the used subnet CIDR range is outside private address space.

### Next Steps

If issue persists, involve SME on Ava and file a Databricks SF ticket if needed.
