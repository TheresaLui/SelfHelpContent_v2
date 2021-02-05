<properties
  pagetitle="I can't see my activities in the activity log or my activities have missing/inaccurate information&#xD;"
  service="microsoft.mcas"
  resource=""
  ms.author="shsagir,nagrand"
  selfhelptype="Generic"
  supporttopicids="32728980"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-missing-activities"
  ownershipid="CloudAppSecurity_API" />
# I can't see my activities in the activity log or my activities have missing/inaccurate information

Most users are able to resolve activity issues using the steps below.

## **Recommended Steps**

1. Determine whether you're using a *scoped deployment* to filter out activities performed by members of certain user groups. Review [How to include or exclude user groups in Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/scoped-deployment#include-or-exclude-user-groups).
1. Make sure that you enabled auditing in Office 365: [How to connect Office 365 to Cloud App security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security#how-to-connect-office-365-to-cloud-app-security)
1. Check that the app connector is in a healthy state. In Cloud App Security, go to **Settings** > **App connectors**.
1. If your activities are missing or delayed in Cloud App Security, do the following:
    1. Check the [current status of Microsoft Cloud App Security](https://status.cloudappsecurity.com/). Look for ongoing maintenance or issues affecting your tenant that may result in missing or delayed activities.
    1. Check if the activities exist in the audit log of the connected app.

        For example:

        - To check the audit log of Office 365, go to [Unified Audit logs](https://protection.office.com/unifiedauditlog)
        - To check the audit log of Azure AD sign-ins, go to **Azure Active Directory** > **Sign-ins**
		
		**NOTE**: For Azure AD sign-in activities, Cloud App Security only surfaces interactive sign-in activities and sign-in activities from legacy protocols, such as ActiveSync. View noninteractive sign-in activities in the Azure AD sign-ins audit log.
1. For Azure AD Identity Protection alerts (i.e. Risky sign-in/Leaked Credentials alerts), you might see Azure AD Identity alerts without logins activities related to it.
   The reason for that is that Cloud App Security consumes only interactive logins from Azure AD.
   For further investigation of alerts that doesn't contain logins, we suggest to continue the investigation through Azure AD portal
1. If your activities are missing information or show incorrect values (i.e., username, IP address, and so on) in Cloud App Security, compare them with corresponding activities in the audit log of the connected app. If the information matches, open a ticket with the support team for the app which logged the event.
1. If you want to see the list of activities we support for an app, in Cloud App Security, on the **Activity log** page, filter by *app* and *activity type* to see the list of supported activities for the app.

## **Recommended Documents**

* [Scoped deployment](https://docs.microsoft.com/cloud-app-security/scoped-deployment)
* [User groups](https://docs.microsoft.com/cloud-app-security/user-groups)
* [Investigating activities](https://docs.microsoft.com/cloud-app-security/activity-filters)
* [Connecting Office 365](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security)
* [Troubleshooting app connector error messages](https://docs.microsoft.com/cloud-app-security/troubleshooting-api-connectors-using-error-messages)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.