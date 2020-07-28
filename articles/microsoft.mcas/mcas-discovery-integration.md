<properties
  pageTitle="I'm having issues around Discovery integrations (Zscaler, iboss, Corrata)"
  description="I'm having issues around Discovery integrations (Zscaler, iboss, Corrata)"
  infoBubbleText=""
  service="microsoft.Cloud App Security"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-discovery-integration"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32729007"
  resourceTags=""
  productPesIds="16031"
 ownershipId="CloudAppSecurity_Discovery"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues around Discovery integrations (Zscaler, iboss, Corrata)

Most users are able to resolve discovery integration issues using the steps below.

## **Recommended Steps**

**For Zscaler integration issues**

Use the steps in [Integrate Cloud App Security with Zscaler](https://docs.microsoft.com/cloud-app-security/zscaler-integration) to verify that the Zscaler integration is correctly configured.

If no discovered apps are available, do the following:

1. In Cloud App Security, verify that:

    1. The data source name is **NSS**
    1. The Cloud App Security API token which is used by Zscaler is active (go to **Settings** > **Security extensions** > **API tokens**)

1. In Zscaler, verify that all statuses are valid (go to **Administration** > **Partner Integrations** > **Microsoft Cloud App Security**)

If apps are not being blocked, do the following:

1. In Cloud App Security, in the Cloud App Catalog, verify that at least one app has been marked as **Unsanctioned**
1. In the Zscaler portal, go to **Administration** > **Access Control** > **URL categories**
1. Under **User-Defined**, verify that **MCAS Unsanctioned Apps** exists and that custom URLs are defined

If you cannot see any discovered data or completed parsed tasks in the governance log:

- In Zscaler, verify that the NSS server allows the following [domains](https://docs.microsoft.com/cloud-app-security/network-requirements#log-collector)

**For iboss integration issues**

Use the steps in [Integrate Cloud App Security with iboss](https://docs.microsoft.com/cloud-app-security/iboss-integration) to verify that the iboss integration is correctly configured.

**For Corrata integration issues**

Use the steps in [Integrate Cloud App Security with Corrata](https://docs.microsoft.com/cloud-app-security/corrata-integration) to verify that the Corrata integration is correctly configured.

## **Recommended Documents**

- [Zscaler integration and troubleshooting guide](https://help.zscaler.com/zia/configuring-mcas-integration)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
