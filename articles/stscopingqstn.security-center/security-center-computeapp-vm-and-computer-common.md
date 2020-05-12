<properties
    pageTitle="VMs and Computers Common Solutions"
    description="VMs and Computers Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636923,32680785"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-8ce6-4b77-a98a-dfaf9543dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# VMs and Computers Common Solutions

The VM and computer blade present VM's servers that exist under the selected subscription. When you drill down for specific VM or on-premise server, you can see the resource health with the recommendation status.

## **Recommended Steps**

If specific VM doesn't appear in this view, check the below:

1. The VM is not deleted
2. You are filtered on the correct subscription
3. For on-premise resource, check if this server sent Heartbeat to log analytics workspace in the last four days

To check the Heartbeat of the server:

1. Validate that the Server is running
2. Open log analytics
3. Select the Log analytics workspace that the VM connected to it
4. Press on the "logs" in the left menu, and write this query:

   Replace the "MyServerName" to your server name

   ```/
   Heartbeat
   | where TimeGenerated > ago(1d)
   | where Computer contains "MyServerName"
   ```

If no heartbeat was sent, use agent troubleshooting instructions:

- [Monitoring agent health issues guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)
- [Troubleshooting monitoring agent network requirements guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#troubleshooting-monitoring-agent-network-requirements-)

## **Recommended Documents**

- [Collect data about Azure Virtual Machines](https://docs.microsoft.com/azure/azure-monitor/learn/quick-collect-azurevm)
- [Monitoring agent health issues guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)
- [Troubleshooting monitoring agent network requirements guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#troubleshooting-monitoring-agent-network-requirements-)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
