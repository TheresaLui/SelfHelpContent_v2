<properties
  pageTitle="I'm having issues with device management"
  description="I'm having issues with device management"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-managed-devices"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32743390"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with device management

Conditional Access App Control enables you to create policies that take into account whether a device is managed or not. To identify the state of a device, you can configure access and session policies to check for:

- Microsoft Intune Compliant devices [only available with Azure Active Directory (Azure AD)]
- Hybrid Azure AD joined devices [only available with Azure AD]
- Presence of client certificates in a trusted chain

Most users are able to resolve the following issues using the steps below:

- I'm having a problem configuring my unmanaged devices
- My device is not being recognized

## **Recommended Steps**

1. For Intune Compliant or Hybrid Azure AD joined devices, do the following:

    1. In Cloud App Security, in the menu bar, click the settings cog, select **Settings**, under **Conditional Access App Control**, select **Device identification** and verify that compliant and Hybrid Azure AD joined device are configured correctly
    1. In Azure AD, go to the relevant CA policy and under **Session**, clear **Use Conditional Access App Control**
    1. Sign in from an Intune Compliant or Hybrid Azure AD joined device
    1. Under **Monitoring** > **Sign-ins**, verify that there are sign-in activities in logs
    1. Select the relevant log entry for the device you logged into
    1. In the **Details** pane, on the **Device info** tab, verify that the device is **Managed** (Hybrid Azure AD joined) or **Compliant** (Intune compliant). If you cannot verify either state, try another log entry or ensure that your device data is configured correctly in Azure AD.
    1. If you still do not see the device information in the **Sign-ins** page, open a support ticket for Azure AD

1. For valid client certificates, do the following:
    1. In Cloud App Security, in the menu bar, click the settings cog, select **Settings**, under **Conditional Access App Control**, select **Device identification**, and upload the CA (root or intermediate) that signed the client certificate
    1. Ensure your client certificate is in .p12 or .pfx file format
    1. If **Require certificate revocation check** is enabled, verify that your client certificate contains a CRL endpoint

## **Recommended Documents**

- [Managed Device Identification](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#managed-device-identification)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
