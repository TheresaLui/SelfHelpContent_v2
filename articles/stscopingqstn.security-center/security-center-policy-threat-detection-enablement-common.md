<properties
  pagetitle="Threat Detection Enable Common Solutions"
  description="Threat Detection Enable Common Solutions"
  service=""
  resource=""
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32788563"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="i15f057d-8ce6-4b77-a98a-dfaf3843dc2f"
  ownershipid="Azure_Security_Security_Center" />
# Threat Detection Enable Common Solutions

## **Recommended Steps**

### **Step 1 : Allow Microsoft Cloud App Security to access your data**

Azure Security Center partners with Microsoft Cloud App Security to bring you alerts based on user and entity behavioral analytics (UEBA) for your Azure resources and users (Azure Activity). These alerts detect anomalies in user behavior and are based on user and entity behavioral analytics and machine learning (ML) so that you can immediately run advanced threat detection across your subscriptions' activities. Because they are automatically enabled, the new anomaly detections provide immediate results by providing immediate detections, targeting numerous behavioral anomalies across the users and resources associated with your subscription. In addition, these alerts leverage additional data that already exists in the Microsoft Cloud App Security detection engine, to help you speed up the investigation process and contain ongoing threats.

### **Step 2 : Disabling threat detection alerts**

1. In the Security Center blade, select **Security policy**, click **Edit settings** for the subscription that you want to change
2. Click **Threat detection**
3. Under **Enable integrations**, clear **Allow Microsoft Cloud App Security to access my data**, then click **Save**

### **Step 3 : Allow Microsoft Defender for Endpoint to access your data**

Azure Security Center is extending its Cloud Workload Protection Platforms offering by integrating with [Microsoft Defender for Endpoint](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp). This change brings comprehensive Endpoint Detection and Response (EDR) capabilities.

These capabilities are now available in Azure Security Center:

- Automated onboarding: The Microsoft Defender for Endpoint sensor is automatically enabled for Windows servers that are onboarded to Azure Security Center
- Single pane of glass: The Azure Security Center console displays Microsoft Defender for Endpoint alerts
- Detailed machine investigation: Azure Security Center customers can access Microsoft Defender for Endpoint console to perform a detailed investigation to uncover the scope of a breach

To onboard servers to Security Center, select **Go to Azure Security Center** to onboard servers from the Microsoft Defender for Endpoint server onboarding.

1. In the Onboarding blade, select or create a workspace in which to store the data
2. If you can't see your workspace, it may be due to lack of permissions. Make sure that your workspace is Azure Defender enabled. For more information, see [Enable Azure Defender](https://docs.microsoft.com/azure/security-center/security-center-pricing).
3. Select **Add servers** to view instructions on how to install the Microsoft Monitoring Agent
4. After onboarding, you can monitor the machines under **Compute and apps**

## **Recommended Documents**

- [UEBA for Azure resources and users](https://docs.microsoft.com/azure/security-center/security-center-ueba-mcas)
- [Disabling threat detection alerts](https://docs.microsoft.com/azure/security-center/security-center-ueba-mcas#disabling-threat-detection-alerts)
- [Protect your endpoints with Security Center's integrated with Microsoft Defender for Endpoint](https://docs.microsoft.com/azure/security-center/security-center-wdatp)
- [Onboarding servers to Security Center](https://docs.microsoft.com/azure/security-center/security-center-wdatp#onboarding-servers-to-security-center)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
