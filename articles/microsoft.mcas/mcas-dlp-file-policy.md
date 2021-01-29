<properties
  pagetitle="I'm having a problem with DLP and file policies&#xD;"
  service="microsoft.mcas"
  resource=""
  ms.author="shsagir,nagrand"
  selfhelptype="Generic"
  supporttopicids="32728974"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-dlp-file-policy"
  ownershipid="CloudAppSecurity_DataProtection" />
# I'm having a problem with DLP and file policies

Most users are able to resolve DLP and file policy questions using the information below.

## **Recommended Steps**

*  **You share files, but the domain isn't detected**<br>
    This can occur if you share files with external users using a group and the **Collaborators** filter is set to **Any from domain**. With this setting, domains are not detected for members of a group; they are only detected by users who have direct permissions on the file.

* **Your sensitive types in the data classification service aren't matching as expected** <br>
   Review the conditions of each [sensitivity type](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions). In the Advanced settings, verify that match accuracy and instance counts are configured correctly for each sensitive type.

* **You are unable to investigate and control files**<br>
   Verify that file monitoring is enabled. In Cloud App Security, select **Settings** > **Files**, and then **Enable file monitoring**.
   
* **You cannot see Office 365 files (including SharePoint Online and OneDrive)**<br>
    In Cloud App Security, in the **Office 365 connector** settings, verify that you have enabled **Office 365 files** and **Office 365 activities** as described on [How to connect Office 365 to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security#how-to-connect-office-365-to-cloud-app-security).

**Note:** If you don't access the **Files** page for more than 60 days and have no active file policies, file monitoring will be automatically disabled.

## **Recommended Documents**

- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)
- [File policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies)
- [Sensitive information type entity definitions](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
