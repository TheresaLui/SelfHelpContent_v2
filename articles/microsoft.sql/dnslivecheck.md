<properties
  pageTitle="Resolve issues connecting to SQL Database"
  description="Resolve issues connecting to SQL Database"
  infoBubbleText="Found recent connectivity issue. See details on the right."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy, swbhartims"
  ms.author="subbuk, swbharti"
  displayOrder=""
  articleId="DnsLiveCheck_5A769A5F-883A-4E9D-A336-DF22A8A32E07"
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="rca"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We performed a DNS resolution against server <!--$ServerName-->ServerName<!--/$ServerName-->.<!--$ServerNameSuffix-->ServerNameSuffix<!--/$ServerNameSuffix--> which failed to resolve to a valid IP address. This indicates that the DNS is unavailable. Please open a support ticket with us to debug this issue further.

<!--/issueDescription-->

## **Recommended Documents**
* [Testing DNS resolution](https://docs.microsoft.com/powershell/module/dnsclient/resolve-dnsname?view=winserver2012r2-ps)
