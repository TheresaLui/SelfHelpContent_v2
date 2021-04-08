<properties
  pagetitle="Connect monitoring machine to SQL"
  description=""
  service=""
  resource=""
  ms.author="sckingho"
  selfhelptype="Generic"
  supporttopicids="32784715,32784716,32784717"
  productpesids="17412"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="ae6a42a4-33ed-4f44-bf3f-c06fbd74dba3"
  ownershipid="AzureData_AzureSQLDB" />
# Connect monitoring machine to SQL

A status of **Not collecting** or **Collecting with errors** will appear if your monitoring machine is unable to establish a connection to one or more of your SQL instances. Follow the steps below to resolve this issue.

## **Recommended Steps**

1. Navigate to [SQL insights (preview)](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/sqlWorkloadInsights) in the Azure Portal 
2. Select the **monitoring profile** of interest
3. Select the **Manage profile** tab to see the status for each of the monitoring machines associated with the profile
    - A status of **Not collecting** means we have not seen any data for this monitoring profile for the last 10 minutes
    - A status of **Collecting with errors** means we do see some data for this monitoring profile, but we also see errors. This suggests that connection strings for some SQL instances are correct, but connection strings for other SQL instances are incorrect
4. Select the **Not collecting** or **Collecting with errors** link in the status column to navigate to the **Collection logs** page
5. Observe the displayed errors and perform any suggested solutions shown in the **Actions** column
6. See the list below for further suggestions

## Common Errors and Solutions

* If the monitoring profile is incorrectly configured, try [recreating your monitoring profile
](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#create-sql-monitoring-profile) with default settings)
* If a firewall or virtual network is preventing your monitoring machine from accessing your SQL instances, see [Configure network settings](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#configure-network-settings)
* If the monitoring user has not been created or has insufficient permissions, see [Create monitoring user](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#create-monitoring-user)
* If the connection string is malformed. try [deleting and reentering all connection strings](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-enable#add-connection-strings)
* The username or password for the monitoring user is incorrect

For additional solutions, see our [troubleshooting documentation](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-troubleshoot).

## **Recommended Documents**

- [Enable SQL insights](https://docs.microsoft.com//azure/azure-monitor/insights/sql-insights-enable)
- [Troubleshoot SQL insights](https://docs.microsoft.com/azure/azure-monitor/insights/sql-insights-troubleshoot)
