<properties
    pageTitle="User gets prompted for credentials while running net use command - Encryption type error"
    description="User gets prompted for credentials while running net use command - Encryption type error"
    infoBubbleText="User gets prompted for credentials while running net use command - Encryption type error"
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
    articleId="7af24444-f9b2-4980-9988-cffc93fa3ccf"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets prompted for credentials while running net use command - Encryption type error
<!--issueDescription-->

Resolution

Dear Customer,

It seems that your computer does not have supported Kerberos encryption type(RC4-HMAC) enabled through group policy settings. This is currently resulting in authentication failures to access Azure file shares.

You (or their domain administrator) need to examine your domain group policy for "Network security configure encryption types allowed for kerberos". And make sure RC4-HMAC-MD5 is included as a value.  

You can validate the mitigation by retrying mount and running Get-AzStorageKerberosTicketStatus after the policy change.

We understand that there are concerns in the industry on whether RC4 cipher is still cryptographically secure. We recommend you to make your own assessment on whether to leverage RC4 cipher based on your security and compliance requirements. We plan to extend the Kerberos support on Azure Files with newer encryption types of AES128 and ASE256 in H1 CY2020.
<!--/issueDescription-->