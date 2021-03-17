<properties
	  pageTitle="Full disk space"
	  description="Full disk space"
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
	  articleId="731d4234-42bf-4274-8e08-ffff133c1ff1"
	  ownershipId="Azure_Sentinel"
/>

# Full disk space

<!--issueDescription-->

During troubleshooting we have found that the Agent doesn't have sufficient disk space. <BR>
<BR>
Please delete some log files from /var/log.<BR>
<BR>
To prevent this from happening you need to reduce the log rotation to a lower number than 7 (default value) and from weekly to daily.<BR>
<BR>
Best Regards,<BR>

<!--/issueDescription-->

