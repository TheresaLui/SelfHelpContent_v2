<properties
  pagetitle="I have issues accessing my Key Vault from my Monitoring profile"
  description=""
  service=""
  resource=""
  ms.author="sckingho"
  selfhelptype="Generic"
  supporttopicids="32784706,32784707,32784708"
  productpesids="17412"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="edaef5e9-ee11-4dc3-bac6-c4da20760f48"
  ownershipid="AzureData_AzureSQLDB" />
# I have issues accessing my Key Vault from my Monitoring profile

When using a Key Vault to store the username and/or password for your connection strings to your SQL systems there are 3 common issues we see:

1. You don't have sufficient permissions on the Key Vault to access the Secret stored in it
2. The Key Vault Secret you are referencing in the VM Configuration does not exist in the Key Vault
3. If the Secret and Key Vault were working, but no have an error then the Secret may have been disabled

## **Recommended Steps**

1. Read through our [troubleshooting documentation](https://docs.microsoft.com//azure/azure-monitor/insights/sql-insights-troubleshoot) to help diagnose which type of Key Vault problem you are experiencing.
2. If the issue is related to improper access to the Key Vault, refer to our [onboarding documentation](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable) and the permissions needed to access the Key Vault.
3. If the issue is related to a Secret that does not exist in the Key Vault, please check the Key Vault and update your Monitoring VM configuration to use the correct name of the Secret.
4. If the issue is related to a disabled Secret in the Key Vault, either [re-enable Key Vault Secret](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets) or [create a new Secret](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets) to use for the Monitoring VM configuration..

## **Recommended Documents**

* [Troubleshoot SQL Insights](https://docs.microsoft.com//azure/azure-monitor/insights/sql-insights-troubleshoot)
* [Enable SQL Insights](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable)
* [Azure Key Vault Secret documentation](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets)