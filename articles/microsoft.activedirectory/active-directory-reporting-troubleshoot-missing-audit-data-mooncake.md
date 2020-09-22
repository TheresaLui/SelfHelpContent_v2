<properties
    pageTitle="I can’t find actions performed in Azure Active Directory in the activity logs"
    description="I can’t find actions that haven been recently performed in Azure Active Directory in the activity logs"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    ms.author="markvi"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-reporting-troubleshoot-missing-audit-data-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I can’t find actions performed in Azure Active Directory in the activity logs

## **Recommended Steps**

Below are our latency numbers for Activity logs.

 Report           | &nbsp; |  Latency (P95) | Latency (P99)
 ---              | ----   |  ---           | ---
 Directory Audit  | &nbsp; | 2 mins         | 5 mins
 Sign-in Activity | &nbsp; | 2 mins         | 5 mins

Note: If you don't see the Audit logs even after 2 hours from performing the action, please [file a support ticket](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest).

## **Recommended Documents**

* [Azure Active Directory reporting latencies](https://docs.azure.cn/active-directory/reports-monitoring/reference-reports-latencies)