<properties
  pagetitle="Issues accessing Key Vault from monitoring profile"
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
# Issues accessing Key Vault from monitoring profile

In SQL insights (preview), Azure Key Vault is used to store the secrets for your SQL connection strings. When using Key Vault with SQL insights, there are 4 common issues:

- The user creating the monitoring profile does not have permissions to access secrets in the Key Vault
- The wrong Key Vault is specified in the monitoring configuration
- The secret specified in the monitoring configuration does not exist in the Key Vault
- The secret has been disabled or has expired

## **Recommended Steps**

- Verify that you have the required permissions to access secrets in the Key Vault by using our [onboarding documentation](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable) 
- Verify that the Key Vault specified in your monitoring configuration is correct. If not, [update your monitoring configuration](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#create-sql-monitoring-profile).
- Verify that all secrets specified in your monitoring configuration exist in the Key Vault. If not, [create a new secret](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-portal) and [update your monitoring configuration](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#create-sql-monitoring-profile).
- Verify that all secrets specified in your monitoring configuration are enabled and not expired. If not, [re-enable your Key Vault secret](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets) and [update your monitoring configuration](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#create-sql-monitoring-profile).

## **Recommended Documents**

- [Troubleshoot SQL insights](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-troubleshoot)
- [Enable SQL insights](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable)
- [About Azure Key Vault secrets](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets)
