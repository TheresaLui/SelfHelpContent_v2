<properties
	pageTitle="Enclave attestation - Endpoint not reachable error"
	description="Enclave attestation - Endpoint not reachable error"
	infoBubbleText="Attestation endpoint is not reachable while connecting to the secure enclave server."
	service="microsoft.sql"
	resource="servers"
	authors="vidit-msft"
	ms.author="viditgupta"
	displayOrder=""
	articleId="enclaveAttestationEndpointError_ACE321DC-FA80-4FDB-B917-603543D78A45"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="32630405, 32630429, 32630438, 32637230"
	resourceTags=""
	productPesIds="13491, 16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Attestation url not reachable for the secure enclaves server

## We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and 
it seems the attestation endpoint is not reachable while connecting to your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->**. To resolve this issue, follow the recommended steps.
<!--/issueDescription-->

## **Attestation Process**
Before a client driver submits a T-SQL statement to Azure SQL logical server for execution, the driver triggers the following enclave attestation workflow using Microsoft Azure Attestation.
1.  The client driver passes the attestation URL, specified in the database connection, to the Azure SQL logical server.
2.  The Azure SQL logical server collects the evidence about the enclave, its hosting environment, and the code running inside the enclave. The server then sends an attestation request to the attestation provider, referenced in the attestation URL.
3.  The attestation provider validates the evidence against the configured policy and issues an attestation token to the Azure SQL logical server. The attestation provider signs the attestation token with its private key.
4.  The Azure SQL logical server sends the attestation token to the client driver.
5.  The client contacts the attestation provider at the specified attestation URL to retrieve its public key. It then verifies the signature in the attestation token.

## **Recommended Steps**

Your Azure SQL logical server is unable to connect to the attestation provider in Azure Attestation (step 2 of the above workflow), specified in the attestation URL. <br>
The likely causes include:
- The attestation URL is incorrect or incomplete. For more information, see [Determine the attestation URL for your attestation policy](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-enclaves-configure-attestation#determine-the-attestation-url-for-your-attestation-policy).
- The attestation provider has been accidentally deleted.
- The firewall was configured for the attestation provider, but it doesn't allow access to Microsoft services.
- An intermittent network error causes the attestation provider to be unavailable.

## **Recommended Documents**

* [Guidelines for setting up Always Encrypted with secure enclaves](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-with-secure-enclaves-landing)
* [Troubleshoot common issues for Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves-troubleshooting)
