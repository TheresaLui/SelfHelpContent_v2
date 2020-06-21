<properties
    pageTitle="Unable to mount - User is not able to retrieve the Kerberos ticket"
    description="Unable to mount - User is not able to retrieve the Kerberos ticket"
    infoBubbleText="Unable to mount - User is not able to retrieve the Kerberos ticket"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="8409904d-948f-471c-8f46-111280edad4a"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - User is not able to retrieve the Kerberos ticket
<!--issueDescription-->
In order for AD Auth to work properly, we need a valid Kerberos ticket to connect to the storage account. The customers may run into issue with CheckGetKerberosTicket step if their domain group policy does not have supported Kerberos encryption type enabled.
<!--/issueDescription-->

## **Recommended Steps**

1. The customer (or their domain administrator) needs to examine their domain group policy for:

   https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/network-security-configure-encryption-types-allowed-for-kerberos

2. And make sure RC4_HMAC_MD5 is included as a value.  They may be wary about reverting to a weaker encryption type, below section has customer communication regarding that.

3. Once the group policy changes have been made, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 

4. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.

**Customer Ready Message**

Dear Customer,

It seems that your computer does not have supported Kerberos encryption type(RC4-HMAC) enabled through group policy settings. This is currently resulting in authentication failures to access Azure file shares.

You (or their domain administrator) need to examine your domain group policy for "Network security configure encryption types allowed for kerberos". And make sure RC4-HMAC-MD5 is included as a value.  

You can validate the mitigation by retrying mount and running Get-AzStorageKerberosTicketStatus after the policy change.

We understand that there are concerns in the industry on whether RC4 cipher is still cryptographically secure. We recommend you to make your own assessment on whether to leverage RC4 cipher based on your security and compliance requirements. We plan to extend the Kerberos support on Azure Files with newer encryption types of AES128 and ASE256 in H2 CY 2020.
