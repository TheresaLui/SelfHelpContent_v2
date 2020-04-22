<properties
	pageTitle="Have I been impacted by an Information Disclosure?"
	description="Have I been impacted by an Information Disclosure?"
	infoBubbleText="Have I been impacted by an Information Disclosure?"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="asms-informationdisclosure-notimpacted"
	diagnosticScenario="YolkaNegativeInsight"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Have I been impacted by an Information Disclosure?

## We detected that information was not exposed.

Microsoft was notified of and mitigated an issue that was the result of a misconfigured network security group’s security rules which enabled an internal database used for support case analytics to be accessible to the internet.<br>

Our analysis of the support information indicates that specific personal or organizational identifiable information related to your support case was potentially visible.<br>

<!--issueDescription-->
Our internal scans have not identified that your support case data associated with your tenant or subscription was within the potentially exposed support information.<br>
<!--/issueDescription-->

We are notifying impacted customers via an email sent to Azure Active Directory (AAD) Global Admin(s), Technical Contact and or Account Admins and have notified affected subscriptions via [Service Health](https://docs.microsoft.com/azure/service-health/). If you did not receive a notification from one of these channels, then you are not affected by this issue.<br>

If you are unsure, we recommend confirming with your **Global Admin** or **Tenant Contact** on your Tenant, or **Account Admin** on this subscription if they have been notified.<br>

We are committed to the privacy and security of your data and have taken the appropriate steps to promptly investigate and mitigate this issue.<br>

### Additional Information:
* [For more information regarding Microsoft Privacy Policy](https://privacy.microsoft.com)
