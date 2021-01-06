<properties
    pageTitle="TLS 1.2 Upgrade Documents - No TLS &lt; 1.2 but has override"
    description="RCA - Documents recommended to for information on upgrading to using TLS 1.2"
    infoBubbleText="The customer is recommended to upgrade to using TLS 1.2"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="tomrlake"
    ms.author="tolake"
    articleId="cosmosdb-tls12-upgrade-no-current-with-override-and-no-old-rca"
    diagnosticScenario="CosmosDBTLS12Insight"
    selfHelpType="rca"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# TLS 1.2 Upgrade Document

We have determined that you have not used TLS that is earlier than 1.2 in the last 14 days, but you have an override to allow for these non-secure versions of TLS.

## Documents on why to switch to TLS 1.2:

* [Preparing for TLS 1.2 in Microsoft Azure](https://azure.microsoft.com/updates/azuretls12/)

  Microsoft Azure recommends that all users complete migration towards solutions that support transport layer security (TLS) 1.2 and that you make sure that TLS 1.2 is used by default.

  All Azure services fully support TLS 1.2 and services where users who use only TLS 1.2 have made a switch to accept only TLS 1.2 traffic. Services that currently accept TLS 1.0/1.1 traffic will continue supporting these protocol versions until further notice to ensure compatibility with existing applications. Although TLS 1.0 implementation has no known security vulnerabilities, it’s important to account for potential future protocol downgrade attacks and other TLS vulnerabilities. We continue to monitor the security landscape and will reevaluate its position as needed.

  We understand that the security of your data is important, and we're committed to transparency about changes that may affect your use of TLS with Azure services.

* [TLS 1.2 enforcement on Azure Cosmos DB](https://devblogs.microsoft.com/cosmosdb/tls-1-2-enforcement/)

  Microsoft Azure recommends all customers complete migration towards solutions that support transport layer security (TLS) 1.2 and make sure that TLS 1.2 is used by default.

  Azure Cosmos DB already supports TLS 1.2. To ensure our customers are covered with the best level of security, TLS 1.2 will be enforced by default starting July 29th, 2020 on:

  * New accounts
  * Existing accounts where our records show that client connections use TLS 1.2 exclusively

  This means that any client request that uses a TLS version lower than 1.2 will be actively rejected on the preceding accounts.

* [Enabling TLS 1.2 with the Windows registry](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/manage-ssl-protocols-in-ad-fs#enable-and-disable-tls-12)

  ### Enable and Disable TLS 1.2
  Use the registry keys and their values from the link above to enable and disable TLS 1.2.

## More information based on SDK used:

* [.NET Framework](https://docs.microsoft.com/dotnet/framework/network-programming/tls)

  ### Transport Layer Security (TLS) best practices with the .NET Framework

  The Transport Layer Security (TLS) protocol is an industry standard designed to help protect the privacy of information communicated over the internet. TLS 1.2 is a standard that provides security improvements over previous versions. TLS 1.2 will eventually be replaced by the newest released standard, TLS 1.3, which is faster and has improved security. The article in the link above presents recommendations to secure .NET Framework applications that use the TLS protocol.

  To ensure .NET Framework applications remain secure, the TLS version should not be hardcoded. .NET Framework applications should use the TLS version the operating system (OS) supports.

* [Java](https://www.java.com/en/configure_crypto.html)

  ### Additional information on Oracle's JDK and JRE Cryptographic Algorithms
  This page contains additional information and/or instructions for testing and/or reverting changes to Oracle's JDK and JRE announced on the [Oracle JRE and JDK Cryptographic Roadmap](https://www.java.com/en/jre-jdk-cryptoroadmap.html)

  We don't recommend reverting changes. Instructions for reverting changes are provided as a temporary workaround, in controlled environments, until the system can be updated to comply with the new security standards.

* [Python](http://pyfound.blogspot.com/2017/01/time-to-upgrade-your-python-tls-v12.html)

  ### Time To Upgrade Your Python: TLS v1.2 Will Soon Be Mandatory
  If you're using an older Python without the most secure TLS implementation, it's time to upgrade. Otherwise, you may not be able to "pip install" packages from PyPI.

* [Node.js](https://nodejs.org/api/tls.html)

  ### TLS (SSL)
  Stability: 2 - Stable<br>
  Source Code: lib/tls.js

  The tls module provides an implementation of the Transport Layer Security (TLS) and Secure Socket Layer (SSL) protocols that is built on top of OpenSSL. The module can be accessed by running the following command:

  ```const tls = require('tls');```
