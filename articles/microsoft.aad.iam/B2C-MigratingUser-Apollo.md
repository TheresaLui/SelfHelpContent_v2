<properties
  pagetitle="Migrate User"
  description="Content on how to handle migrating users issues"
  ms.author="nishring"
  selfhelptype="apollo"
  supporttopicids="0bd7d616-07bb-6bec-96c9-3c2e23e3c8b5"
  resourcetags=""
  productpesids="16580"
  cloudenvironments="public"
  articleid="cecddd38-c44d-453b-b1ac-ea7475844d35"
  ownershipid="AzureIdentity_B2C"
  resourcerequired="false" 
/>

# Business to Consumer (B2C)

## Migrate users to Azure AD B2C

Learn how to migrate users to Azure AD B2C by using the following video tutorials and documents.

:::Section Solution:::

### Recommended steps

1. If you're using Azure Active Directory: in the Active Directory portal, in the relevant Conditional Access policy, under **Session**, make sure that **Use Conditional Access App Control** is selected.
    - If you're not using a custom Cloud App Security policy, in the drop-down list box, select **Monitor Only** or **Block Downloads**.
    - Otherwise, in the drop-down list box, select **Use Custom Policy**, and in Cloud App Security, create granular access or session control policies, such as block upload, copy/paste/print, or block downloads, based on content inspection.
1. If you're using a third-party Identity provider, make sure to onboard the app first.
    - In Cloud App Security, browse to **Investigate** > **Connected apps** > **Conditional Access App Control apps**, and click the plus sign to start the process.
1. If you're trying to create a session policy and see a "No apps onboarded" error message:
    - Verify that the app appears on the **Conditional Access App Control apps** page.
    - If the app does not appear, log in to the app.
    - If the app still does not appear, continue with opening the ticket.

If you're still experiencing the issue or your issue is not listed, our [Troubleshooting guide for access and session controls](https://docs.microsoft.com/cloud-app-security/troubleshooting-proxy), videos, and resources can help you.

### How-to videos

<videoGroup>
    <video>
        <src>https://www.youtube.com/watch?v=DyC0eV_pMhs</src>
        <title>How to configure real-time monitoring and control</title>
    </video>
    <video>
        <src>https://www.youtube.com/watch?v=vD9C9jwDuv4</src>
        <title>How to configure real-time labeling and protection of sensitive files</title>
    </video>
    <video>
        <src>https://www.youtube.com/watch?v=nGg2XyQWJ4o</src>
        <title>How to configure a policy to block uploads in real time</title>
    </video>
</videoGroup>

### More resources

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Access policies](https://docs.microsoft.com/cloud-app-security/access-policy-aad)
- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)
- [Tutorial: How to block downloads of sensitive information](https://docs.microsoft.com/cloud-app-security/use-case-proxy-block-session-aad)
