<properties
    pageTitle="Threat Detection Enable Common Solutions"
    description="Threat Detection Enable Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680784"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="i15f057d-8ce6-4b77-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Threat Detection Enable Common Solutions

## **Recommended Steps**

### **Step 1 : Allow Microsoft Cloud App Security to access your data**

Azure Security Center partners with Microsoft Cloud App Security to bring you alerts based on user and entity behavioral analytics (UEBA) for your Azure resources and users (Azure Activity). These alerts detect anomalies in user behavior and are based on user and entity behavioral analytics and machine learning (ML) so that you can immediately run advanced threat detection across your subscriptions' activities. Because they are automatically enabled, the new anomaly detections provide immediate results by providing immediate detections, targeting numerous behavioral anomalies across the users and resources associated with your subscription. In addition, these alerts leverage additional data that already exists in the Microsoft Cloud App Security detection engine, to help you speed up the investigation process and contain ongoing threats.

### **Step 2 : Disabling threat detection alerts**

1. In the Security Center blade, select **Security policy**, click **Edit settings** for the subscription that you want to change
2. Click **Threat detection**
3. Under **Enable integrations**, clear **Allow Microsoft Cloud App Security to access my data**, then click **Save**

### **Step 3 : Allow Windows Defender ATP to access your data**

Azure Security Center is extending its Cloud Workload Protection Platforms offering by integrating with [Windows Defender Advanced Threat Protection](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp) (ATP). This change brings comprehensive Endpoint Detection and Response (EDR) capabilities.

These capabilities are now available in Azure Security Center:

- Automated onboarding: The Windows Defender ATP sensor is automatically enabled for Windows servers that are onboarded to Azure Security Center
- Single pane of glass: The Azure Security Center console displays Windows Defender ATP alerts
- Detailed machine investigation: Azure Security Center customers can access Windows Defender ATP console to perform a detailed investigation to uncover the scope of a breach

To onboard servers to Security Center, click Go to Azure Security Center to onboard servers from the Windows Defender ATP server onboarding.

1. In the Onboarding blade, select or create a workspace in which to store the data
2. If you can't see your workspace, it may be due to lack of permissions, make sure your workspace is set to Azure Security Standard tier. For more information, see [Upgrade to Security Center's Standard tier for enhanced security](https://docs.microsoft.com/azure/security-center/security-center-pricing)
3. Select **Add servers** to view instructions on how to install the Microsoft Monitoring Agent
4. After onboarding, you can monitor the machines under **Compute and apps**

## **Recommended Documents**

- [UEBA for Azure resources and users](https://docs.microsoft.com/azure/security-center/security-center-ueba-mcas)
- [Disabling threat detection alerts](https://docs.microsoft.com/azure/security-center/security-center-ueba-mcas#disabling-threat-detection-alerts)
- [Windows Defender Advanced Threat Protection with Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-wdatp)
- [Onboarding servers to Security Center](https://docs.microsoft.com/azure/security-center/security-center-wdatp#onboarding-servers-to-security-center)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
