<properties
  pagetitle="Security Alerts - testing alerts self-help guide"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693250"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8e66b857-aca8-4a21-9afe-828037121f3a"
  ownershipid="Azure_Security_Security_Center" />
# Security Alerts - testing alerts self-help guide

Use the following guidance to test security alerts.

## **Recommended Steps**

### Generate sample Azure Defender alerts
You can create sample alerts in a few clicks from the security alerts page in the Azure portal in order to examine the looks, feel, descriptions of various alert types.
Please check [Generate sample Azure Defender alerts](https://docs.microsoft.com/azure/security-center/security-center-alert-validation#generate-sample-azure-defender-alerts) page for instructions.

### Testing alerts for various resources

**Test alerts for VMs**

   [Test your alert configuration (EICAR test file)](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)

   1. Enable command-line arguments auditing, using the following command: <br> 
   `reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\system\Audit" /f /v "ProcessCreationIncludeCmdLine_Enabled"`

   2. To get EICAR alerts on the Security Center portal, install the Log Analytics Agent on the resource and verify that it sends a valid heartbeat.
   3. [Monitor agent health issues troubleshooting guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide#monitoring-agent-health-issues-)


**Test alerts on Kubernetes**

   1. Connect to the Kubernetes cluster, using the following command:<br>
   `az aks get-credentials --resource-group myResourceGroup --name myAKSCluster`
   
   2. Follow instructions to [test alerts on Kubernetes](https://docs.microsoft.com/azure/security-center/security-center-alert-validation#validate-alerts-on-kubernetes-)
   

**Test alerts for Key Vault**

  [Test Azure Key Vault threat detection in Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/validating-azure-key-vault-threat-detection-in-azure-security/ba-p/1220336#M73)
    

**Test alerts for Storage ATP**
   1.	Navigate to a storage account that has Azure Defender for Storage enabled
2.	Select the **Containers** tab in the sidebar
3.	Navigate to an existing container or create a new one
4.	Upload a file to that container. Avoid uploading any file that may contain sensitive data.
5.	Right-click the uploaded file and select **Generate SAS**
6.	Select the **Generate SAS token and URL** button (no need to change any options)
7.	Copy the generated SAS URL
8.	Open the Tor browser. You can download it [here](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.torproject.org%2Fdownload%2F&data=04%7C01%7CEli.Sagie%40microsoft.com%7C507f76540eb74f596c2e08d8ac118a6f%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637448538650625099%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=nNIKvnIcHCKQhoKt3qqkHKZyj9cVfuUcp535LnyKta4%3D&reserved=0))
9.	In the Tor browser, navigate to the SAS URL
10.	You should now see/download the file uploaded in step 4.


**Test alerts for SQL ATP**

 [Create alerts for Azure SQL Managed Instance using the Azure portal](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create)


## **Recommended Documents**

* [Manage security alerts](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)
* [Create and manage alerts suppression rules](https://docs.microsoft.com/azure/security-center/alerts-suppression-rules)
* [Automate responses to alerts](https://docs.microsoft.com/azure/security-center/workflow-automation)
* [Reference list of alerts](https://docs.microsoft.com/azure/security-center/alerts-reference)
* [Generate sample Azure Defender alerts](https://docs.microsoft.com/azure/security-center/security-center-alert-validation#generate-sample-azure-defender-alerts)
* Blog: [Email Notification for alerts triggered by ATP for Azure Storage, SQL ATP and Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/email-notification-for-alerts-triggered-by-atp-for-azure-storage/ba-p/616261)

### Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
