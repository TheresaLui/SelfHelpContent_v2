<properties
  pagetitle="Administration and Security/Synapse Workspace - Customer Managed Keys"
  service="microsoft.synapse"
  resource="workspaces"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32783928"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-cs-administrationandsecurity-synapseworkspacecustomermanagedkeys.md"
  ownershipid="AzureData_SynapseAnalytics" />
  
# Administration and Security/Synapse Workspace - Customer Managed Keys

Use the following steps when the error message, "Workspace activation failed. Click here to retry activation or contact support" occurs during workspace activation.

## Recommended Steps

- Verify whether the key used for encryption meets the requirements for Synapse Workspaces
- Synapse Workspaces support RSA keys with 2048 and 3072 byte-sized keys, and do not support the use of Elliptic-Curve Cryptography (ECC) keys for encryption.
- If the Workspace was created using an unsupported key size or algorithm, the workspace must be recreated using a supported key. Double encryption configuration cannot be changed after the workspace is created.
- More information can be found in [Azure Synapse encryption](https://docs.microsoft.com/azure/synapse-analytics/security/workspaces-encryption#azure-synapse-encryption)

## Recommended Documents

* [Encryption for Azure Synapse Analytics workspaces](https://docs.microsoft.com/azure/synapse-analytics/security/workspaces-encryption)
* [Security baseline](https://docs.microsoft.com/azure/synapse-analytics/security-baseline)
