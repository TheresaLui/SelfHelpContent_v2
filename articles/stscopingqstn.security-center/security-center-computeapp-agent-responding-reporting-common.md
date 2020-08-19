<properties
    pageTitle="Agent not responding or not reporting"
    description="Agent not responding or not reporting"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636840,32636856"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15r058d-1uj6-4b77-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Agent Not Responding or Not Reporting

Windows or Linux IaaS VMs qualify for automatic provisioning of the Microsoft Monitoring Agent installation if:

- The Microsoft Monitoring Agent extension is not currently installed on the VM
- The VM is in running state
- The Windows or Linux Azure Virtual Machine Agent is installed
- The VM is not used as an appliance such as web application firewall or next generation firewall

To be able to check if the agent (direct\MMA\SCOM) is reporting correctly, you can run Log analytics.

## **Recommended Steps**

Query to check the Heartbeat of the VM:

1. Validate that the VM is ruining
2. Open log analytics
3. Select the Log analytics workspace that the VM connected to it
4. Press on the "logs" in the left menu, and write this query:

   ```/
   Heartbeat
   | where TimeGenerated > ago(1d)
   | where Computer contains "MyVMName"
   ```

   In this example, replace the "MyVMName" to your VM name.

If you are not getting any results, it means that the agent is not able to communicate and send data to the workspace. For more information, refer the following articles:

- [Monitoring agent health issues](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)
- [Troubleshooting monitoring agent network requirements](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#troubleshooting-monitoring-agent-network-requirements-)

## **Recommended Documents**

- [Collect data about Azure Virtual Machines](https://docs.microsoft.com/azure/azure-monitor/learn/quick-collect-azurevm)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)