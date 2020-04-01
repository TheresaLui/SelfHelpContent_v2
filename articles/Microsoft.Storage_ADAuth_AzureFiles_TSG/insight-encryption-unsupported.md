<properties
    pageTitle="Customer does not have RC4-HMAC Encryption type enabled on their computer."
    description="Customer does not have RC4-HMAC Encryption type enabled on their computer."
    infoBubbleText="Customer does not have RC4-HMAC Encryption type enabled on their computer."
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="2be2c421-288e-4c22-81d2-a8589775310d"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>


# Customer does not have RC4-HMAC Encryption type enabled on their computer.
<!--issueDescription-->

Resolution/Workaround

Dear Customer,

It seems that your computer does not have supported Kerberos encryption type(RC4-HMAC) enabled through group policy settings. This is currently resulting in authentication failures to access Azure file shares.

You (or their domain administrator) need to examine their domain group policy for:

https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/network-security-configure-encryption-types-allowed-for-kerberos

And make sure RC4_HMAC_MD5 is included as a value.  

![EncryptionSetting.gif](Screenshots\EncryptionSetting.gif)

You can validate the mitigation by retrying mount and running **Get-AzStorageKerberosTicketStatus** after the policy change.

We understand that there are concerns in the industry on whether RC4 cipher is still cryptographically secure. We recommend you to make your own assessment on whether to leverage RC4 cipher based on your security and compliance requirements. We plan to extend the Kerberos support on Azure Files with newer encryption types of AES128 and ASE256 in H1 CY2020.
<!--/issueDescription-->