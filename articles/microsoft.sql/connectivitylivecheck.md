<properties
  pageTitle="Connectivity Live Check"
  description="Connectivity Live Check"
  infoBubbleText="Found recent connectivity issue. See details on the right."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy, swbhartims"
  ms.author="subbuk, swbharti"
  displayOrder=""
  articleId="ConnectivityCheck_042F9ACD-6B75-4184-A72C-A7F68E71C9B3"
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="DiagnoseAndSolve"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
The issue is assumed ongoing since no end time is provided. We performed a live connectivity check, using mock username/password, against database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->.<!--$ServerNameSuffix-->ServerNameSuffix<!--/$ServerNameSuffix-->, and confirmed <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> is online and processing logins. 
The issue you are experiencing could be a network-related problem at your end.

**To Resolve:**

* Try connecting to the database using a different machine to help eliminate the possibility of it being a machine-specific issue.
* Or connect to the database from a different network to resolve if this is network-related.
* Or try connecting to the database from a different client.

**List of tools:**

1. Check if DNS name resolves correctly - use nslookup
2. Check if packets are not being dropped - use PsPing
3. For network packet tracing - use NetMon

Contact your network adminstrator to further investigate the issue at your end.
<!--/issueDescription-->

## **Recommended Documents**

* [Using PsPing tool](https://docs.microsoft.com/sysinternals/downloads/psping)
* [Using NetMon tool](https://www.microsoft.com/download/details.aspx?id=4865)
* [Using nslookup](https://docs.microsoft.com/windows-server/administration/windows-commands/nslookup)
