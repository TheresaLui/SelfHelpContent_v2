<properties
	  pageTitle="Check if the delay exist on the source app audit logs as well"
	  description="Check if the delay exist on the source app audit logs as well"
      service="Microsoft.Security"
      resource="Microsoft.Security/alerts"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="40e64c6c-da46-42bb-ab2b-6c3600f8b545"
	  ownershipId="CloudAppSecurity_API"
/>

# Check if the delay exist on the source app audit logs as well

1. Ask the customer to check the audit logs of the source app, and see if the delay in the auditing of the activities in the audit log of the source app (for example, O365 SCC audit logs).
2. NOTE: for O365 apps SLA, please see [Search Audit Log](https://docs.microsoft.com/en-us/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance?view=o365-worldwide). If the delay is within the SLA, then it's expected.
3. NOTE 2: For AAD logins SLA, please see [AAD Logins](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-sign-ins). If the delay is within the SLA, then it's expected.
