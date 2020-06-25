<properties
    pageTitle="I don’t see the Sign-in Data streaming even though I have configured it through Azure Monitor Diagnostics"
    description="I don’t see the Sign-in Data streaming even though I have configured it through Azure Monitor Diagnostics"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    ms.author="markvi"
    displayOrder="10"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-reporting-troubleshoot-audit-logs-monitor-diagnostics-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I don’t see the Sign-in Data streaming even though I have configured it through Azure Monitor Diagnostics

## **Recommended Steps**

You configured the Azure AD Logs through Diagnostics settings (using "Export Data") in the Azure Active Directory - Activity Logs - Audit. Now you can't see the sign-ins either in Storage account or Event hub. 

Even though you can see the **SignIn** check box and select that option through the **Audit logs** - **Diagnostics Settings** blade, the sign-in logs aren't streamed to your storage account or Event hub (based on your configuration) unless you at least have one Azure AD Premium 1 license associated with your tenant. Because the **All Sign-ins** report is available only for P1 customers, you won’t be able to stream it.

Resolution: [Start a free trial for Azure AD Premium](https://www.azure.cn/pricing/1rmb-trial-full/?form-type=identityauth) and check out this feature.

## **Recommended Documents**

* [Azure Active Directory reporting latencies](https://docs.azure.cn/active-directory/reports-monitoring/reference-reports-latencies)