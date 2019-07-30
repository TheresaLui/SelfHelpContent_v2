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
  selfHelpType="selfhelp"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
The issue is assumed ongoing since no end time is provided. We performed a live connectivity check, using mock username/passowrd, against database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->.<!--$ServerNameSuffix-->ServerNameSuffix<!--/$ServerNameSuffix-->, and confirmed <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> is available and reachable. 
The connectivity issue that you are currently experiencing could be a symptom of network issue at your end.

**To Do's:**

1. You may also try connecting to the database using different machines to help eliminate the possibility of it being an issue due to the machine.

2. You may also try connecting to the database from a different network to help eliminate network issues.

3. You may also try using differnt clients to connect to the database to help eliminate a client-based issue.

**List of tools:**

1. Check if DNS name resolves correctly - use nslookup

2. Check if packets are not being dropped - use PsPing

3. For network packet tracing - use NetMon

Contact your network adminstrator to further investigate the issue at your end.
<!--/issueDescription-->

## **Recommended Documents**

* [Using PsPing tool](https://docs.microsoft.com/sysinternals/downloads/psping)
