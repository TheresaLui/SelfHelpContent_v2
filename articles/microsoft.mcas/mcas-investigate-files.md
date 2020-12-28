<properties
  pagetitle="I need help investigating files&#xD;"
  service="microsoft.mcas"
  resource=""
  ms.author="shsagir,nagrand"
  selfhelptype="Generic"
  supporttopicids="32728982"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-investigate-files"
  ownershipid="CloudAppSecurity_DataProtection" />
# I need help investigating files

Most users are able to file investigation questions using the information below.

## **Recommended Steps**

*  **You can't see Amazon Web Services (AWS) files** <br>
   This is expected behavior. Only AWS bucket-level permissions are supported; Cloud App Security doesn't have visibility into the files contained in the buckets.
   
* **You cant see Office 365 files (including SharePoint Online and OneDrive)** <br>
   In Cloud App Security, in the **Office 365 connector** settings, verify that you have enabled **Office 365 files** and **Office 365 activities** as described on [How to connect Office 365 to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security#how-to-connect-office-365-to-cloud-app-security).
   
* **You can't export more than 5000 results in the Microsoft Cloud App Security portal**<br>
   This is expected behavior as the portal is limited to 5000 results. To export more than 5000 results, use the [Cloud App Security REST API](https://docs.microsoft.com/cloud-app-security/api-alerts-list).

## **Recommended Documents**

- [Investigate files](https://docs.microsoft.com/cloud-app-security/file-filters)
- [Connected apps](https://docs.microsoft.com/cloud-app-security/enable-instant-visibility-protection-and-governance-actions-for-your-apps)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
