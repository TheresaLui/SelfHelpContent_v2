<properties
  pagetitle="Threat Detection self help guide&#xD;"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32788559"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="920335e4-8548-4e24-9a8e-c232ab6a636c"
  ownershipid="Azure_Security_Security_Center" />
# Threat Detection self help guide

## **Recommended Steps**

### Allow Microsoft Defender for Endpoint to access your data

Onboarding to "Microsoft Defender for Endpoint" previously known as "Microsoft Defender Advanced Threat Protection" (MDATP): Azure Security Center is extending its Cloud Workload Protection Platforms offering by integrating with [Microsoft Defender for Endpoint](https://www.microsoft.com/microsoft-365/security/endpoint-defender).

These capabilities are available for Azure Defender (Security Center Standard pricing tier) customers at no extra charge:

- Automated onboarding: The Microsoft Defender for Endpoint sensor is automatically enabled for Windows servers that are onboarded to Azure Defender
- Single pane of glass: The Azure Defender console displays Microsoft Defender for Endpoint alerts
- Detailed machine investigation: Azure Defender customers can access Microsoft Defender for Endpoint console to perform a detailed investigation to uncover the scope of a breach

To onboard servers to Security Center:

1. Make sure that the subscription has Azure Defender enabled (previously known as Security Center standard pricing tier)
1. Make sure that in Pricing & Settings -> Threat detection -> Enable integrations are checked:
- Allow Microsoft Cloud App Security to access my data
- Allow Microsoft Defender for Endpoint to access my data  
**Note:** Both of the above are selected by default
2. Make sure all required workspaces under the subscription, both default and user workspaces, are [Azure defender enabled](https://docs.microsoft.com/azure/security-center/security-center-pricing#enable-azure-defender)
3. To verify that the workspace is eligible check that 'Security' solution is enabled on that workspace
4. Onboarding for the first time can take up to 48 hours

### Allow Microsoft Cloud App Security to access your data

Azure Security Center partners with Microsoft Cloud App Security to bring you alerts based on user and entity behavioral analytic (UEBA) for your Azure resources and users (Azure Activity). These alerts detect anomalies in user behavior and are based on user and entity behavioral analytic and machine learning (ML) so that you can immediately run advanced threat detection across your subscriptions' activities. Because they are automatically enabled, the new anomaly detection provide immediate results by providing immediate detection, targeting numerous behavioral anomalies across the users and resources associated with your subscription. In addition, these alerts leverage additional data that already exists in the Microsoft Cloud App Security detection engine, to help you speed up the investigation process and contain ongoing threats.

### Disabling threat detection alerts

1. In Security Center portal go to Pricing & Settings -> Threat detection 
2. Un-check the required checkbox
3. Click **Save**

## **Recommended Documents**

- [Microsoft Defender Advanced Threat Protection with Azure Defender](https://docs.microsoft.com/azure/security-center/security-center-wdatp)
- [Microsoft Defender for Endpoint](https://www.microsoft.com/microsoft-365/security/endpoint-defender).
- [Microsoft Cloud App Security documentation](https://docs.microsoft.com/cloud-app-security/)

### Troubleshooting
* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ
* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)