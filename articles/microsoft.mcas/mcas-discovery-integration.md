<properties
  pagetitle="I'm having issues around Discovery integrations (Zscaler, iboss, Corrata)&#xD;"
  service="microsoft.cloud app security"
  resource=""
  ms.author="shsagir,nagrand"
  selfhelptype="Generic"
  supporttopicids="32729007"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-discovery-integration"
  ownershipid="CloudAppSecurity_Discovery" />
# Issues with Discovery integrations (Zscaler, iboss, Corrata)

Refer to the section that best describes your integration issue.


## **Zscaler integration issues**

1. Verify that the Zscaler integration is correctly configured. Follow steps in [Integrate Cloud App Security with Zscaler](https://docs.microsoft.com/cloud-app-security/zscaler-integration).

1. If no discovered apps are available, in Cloud App Security, verify that:

   * The data source name is **NSS**
   * The Cloud App Security API token used by Zscaler is active: Go to **Settings** > **Security extensions** > **API tokens**.

1. In Zscaler, verify that all statuses are valid: Go to **Administration** > **Partner Integrations** > **Microsoft Cloud App Security**.

1. If no apps are blocked, do the following:

     1. In Cloud App Security, in the Cloud App Catalog, verify that at least one app is marked as **Unsanctioned**
     1. In the Zscaler portal, go to **Administration** > **Access Control** > **URL categories**
     1. Under **User-Defined**, verify that **MCAS Unsanctioned Apps** exists and that custom URLs are defined

1. If the governance log contains no discovered data or completed parsed tasks, in Zscaler, verify that the NSS server allows the following [domains](https://docs.microsoft.com/cloud-app-security/network-requirements#log-collector)

   **NOTE**: By default, Zscaler integration supports connecting one NSS server to Cloud App Security. To connect additional NSS servers, open a ticket with Zscaler support.
<br><br>

## **iboss integration issues**

Verify that the iboss integration is correctly configured. Follow steps in [Integrate Cloud App Security with iboss](https://docs.microsoft.com/cloud-app-security/iboss-integration).
<br><br>


## **Corrata integration issues**

Verify that the Corrata integration is correctly configured. Follow steps in [Integrate Cloud App Security with Corrata](https://docs.microsoft.com/cloud-app-security/corrata-integration).
<br><br>


## **Recommended Documents**
- [Zscaler integration and troubleshooting guide](https://help.zscaler.com/zia/configuring-mcas-integration)
<br>
If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
