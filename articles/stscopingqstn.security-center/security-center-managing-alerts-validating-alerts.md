<properties
  pagetitle="Security Alerts validation self-help guide&#xD;"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693250"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8e66b857-aca8-4a21-9afe-828037121f3a"
  ownershipid="Azure_Security_Security_Center" />
# Security Alerts validation self-help guide

Use the following guidance to validate security alerts.


## **Recommended Steps**

### Validate alerts for VMs

* [Validate your alert configuration (EICAR test file)](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)

1. Enable command-line arguments auditing, using the following command: <br> 
   `reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\system\Audit" /f /v "ProcessCreationIncludeCmdLine_Enabled"`

2. To get EICAR alerts on the Security Center portal, install the Log Analytics Agent on the resource and verify that it sends a valid heartbeat.
3. [Monitoring agent health issues troubleshooting](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)

### Validate alerts on Kubernetes

1. Connect to the Kubernetes cluster, using the following command:<br>
   `az aks get-credentials --resource-group myResourceGroup --name myAKSCluster`
   
2. [Validate alerts on Kubernetes](https://docs.microsoft.com/azure/security-center/security-center-alert-validation#validate-alerts-on-kubernetes-)

### Validate alerts for Key Vault

* [Validate Azure Key Vault Threat Detection in Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/validating-azure-key-vault-threat-detection-in-azure-security/ba-p/1220336#M73)

### Validate alerts for Storage ATP

* Coming soon.  
Ask your Support Engineer for updates.

### Validate alerts for SQL ATP

* [Create alerts for Azure SQL Managed Instance using the Azure portal](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create)

## **Recommended Documents**

* [Manage security alerts](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)
* [Create and manage alerts suppression rules](https://docs.microsoft.com/azure/security-center/alerts-suppression-rules)
* [Automate responses to alerts](https://docs.microsoft.com/azure/security-center/workflow-automation)
* [Reference list of alerts](https://docs.microsoft.com/azure/security-center/alerts-reference)
* Blog: [Email Notification for alerts triggered by ATP for Azure Storage, SQL ATP and Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/email-notification-for-alerts-triggered-by-atp-for-azure-storage/ba-p/616261)

### Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
