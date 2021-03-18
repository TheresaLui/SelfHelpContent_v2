<properties
  pagetitle="I would like to get more information on an alert&#xD;"
  service="microsoft.mcas"
  resource=""
  ms.author="nagrand"
  selfhelptype="Generic"
  supporttopicids="32729000"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-information-anomaly-alerts"
  ownershipid="CloudAppSecurity_DataScience" />
# I would like to get more information on an alert

Most users are able to get additional information on their alerts using the steps below.

## **Recommended Steps**

1. For any delayed/missing alerts, check if there's a known incident on the [Microsoft Cloud App Security status page](https://status.cloudappsecurity.com/)
2. For Azure Active Directory (Azure AD) Identity Protection alerts (for example, Risky sign-in/Leaked Credentials alerts):
	* The default severity for Leaked credentials alerts is **Low**, meaning that Cloud App Security will receive alerts of all severities (low, medium, and high)
	* The default severity for Risky sign-in alerts is **High**, meaning that Cloud App Security will receive only high severity alerts
	
	**NOTE:** Severities can be modified by editing the relevant policies within Cloud App Security (**Control** > **Policies**).

	* If you see Azure AD Identity Protection alerts without related sign-in activities: Because Cloud App Security consumes only interactive logins from Azure AD, this may result in some alerts not showing related activities. You can investigate activities related to these kinds of alerts in the Azure AD portal.
    * If you want to configure email notifications: You can configure the email notifications for Azure AD Identity Protection alerts in the [Azure AD Identity portal](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications).

        **NOTE:** Cloud App Security doesn't support sending Azure AD Identity Protection alerts as email notifications.

3. For anomaly alerts:

    * Use the [Investigate anomaly detection alerts tutorial](https://docs.microsoft.com/cloud-app-security/investigate-anomaly-alerts) (Impossible Travel, Ransomware activity, Infrequent country, and so on) for investigation steps, alerts details, guidelines, and remediation steps.
    * You can [tune the Impossible travel](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy#tune-anomaly-detection-policies) policy:
        * By using the sensitivity slider to affect the suppression type
        * By scoping the successful/non-legacy failed logins 
        * By configuring [IP ranges as **Corporate**](https://docs.microsoft.com/cloud-app-security/ip-tags)

**NOTE:** For more information about the activities that triggered an alert, we recommend opening a ticket with the respective app (for example: Exchange Online, Azure Ad, and so on).

## **Recommended Documents**

- [Azure AD Identity Protection Policies](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-risks)
- [Detect suspicious user activity with UEBA](https://docs.microsoft.com/cloud-app-security/tutorial-suspicious-activity)
- [Investigate risky users](https://docs.microsoft.com/cloud-app-security/tutorial-ueba)
- [Investigate risky OAuth apps](https://docs.microsoft.com/cloud-app-security/investigate-risky-oauth)

If you're still experiencing the issue after reviewing the documentation and configuration, continue with opening the support ticket.
