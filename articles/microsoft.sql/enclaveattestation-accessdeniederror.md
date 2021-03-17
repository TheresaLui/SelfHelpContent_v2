<properties
	pageTitle="Enclave attestation - Access Denied error"
	description="Enclave attestation - Access Denied error"
	infoBubbleText="Access denied for the attestation tenant of secure enclave server with Always Encrypted"
	service="microsoft.sql"
	resource="servers"
	authors="vidit-msft"
	ms.author="viditgupta"
	displayOrder=""
	articleId="enclaveAttestationAccessDeniedError_B459C5D0-A82D-4669-A60D-52188F54D91B"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="32630405, 32630429, 32630438, 32637230"
	resourceTags=""
	productPesIds="13491, 16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Access denied on the Attestation tenant

## We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and 
it seems like you are facing an access denied error for the attestation tenant on your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->**. 

This error is probably due to an issue with the RBAC (Role Based Access Control) permission. To resolve this issue, follow the recommended steps.
<!--/issueDescription-->

## **Attestation Process**

Before a client driver submits a T-SQL statement to Azure SQL logical server for execution, the driver triggers the following enclave attestation workflow using Microsoft Azure Attestation.
1.  The client driver passes the attestation URL, specified in the database connection, to the Azure SQL logical server.
2.  The Azure SQL logical server collects the evidence about the enclave, its hosting environment, and the code running inside the enclave. The server then sends an attestation request to the attestation provider, referenced in the attestation URL.
3.  The attestation provider validates the evidence against the configured policy and issues an attestation token to the Azure SQL logical server. The attestation provider signs the attestation token with its private key.
4.  The Azure SQL logical server sends the attestation token to the client driver.
5.  The client contacts the attestation provider at the specified attestation URL to retrieve its public key. It then verifies the signature in the attestation token.

## **Recommended Steps**

- Your Azure SQL logical server is not authorized to send attestation requests to the attestation provider. Make sure the administrator of your attestation provider has added the database server to the Attestation Reader role. For more information, see [Grant your Azure SQL database server access to your attestation provider](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-enclaves-configure-attestation#grant-your-azure-sql-database-server-access-to-your-attestation-provider).

## **Recommended Documents**

* [Guidelines for setting up Always Encrypted with secure enclaves](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-with-secure-enclaves-landing)
* [Troubleshoot common issues for Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves-troubleshooting)
