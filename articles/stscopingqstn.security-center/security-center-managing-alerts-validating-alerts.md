<properties
  pagetitle="Security Alerts validation self-help guide"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693250"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8e66b857-aca8-4a21-9afe-828037121f3a"
  ownershipid="Azure_Security_Security_Center" />
# Security Alerts validation self-help guide

## **Recommended Steps**

### Validate alerts for VMs

* [Validate your alert configuration (EICAR test file)](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)

1. You need to enable command-line arguments auditing. To enable it, use the command `reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\system\Audit" /f /v "ProcessCreationIncludeCmdLine_Enabled"`
2. In order for EICAR alert to show on the Security Center portal make sure the resource have the monitoring agent (a.k.a Log Analytics Agent) is installed and sending valid heartbeat
3. [Monitoring agent health issues troubleshooting](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)

### Validate alerts on Kubernetes

1. Connect to the Kubernetes cluster: `az aks get-credentials --resource-group myResourceGroup --name myAKSCluster`
2. [Validate alerts on Kubernetes](https://docs.microsoft.com/azure/security-center/security-center-alert-validation#validate-alerts-on-kubernetes-)

### Validate alerts for Key Vault

* [Validating Azure Key Vault Threat Detection in Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/validating-azure-key-vault-threat-detection-in-azure-security/ba-p/1220336#M73)

### Validate alerts for Storage ATP

* [Validating ATP for Azure Storage Detections in Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/validating-atp-for-azure-storage-detections-in-azure-security/ba-p/1068131)

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
