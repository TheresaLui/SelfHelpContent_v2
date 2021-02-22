<properties
	pageTitle="Enclave attestation - Sgx Not Loaded"
	description="Enclave attestation - Sgx Not Loaded"
	infoBubbleText="Unable to verify if the server loaded SGX enclave for Always Encrypted."
	service="microsoft.sql"
	resource="servers"
	authors="vidit-msft"
	ms.author="viditgupta"
	displayOrder=""
	articleId="enclaveAttestationSgxNotLoaded_3EE66051-C3C2-4A15-A635-3D086446AA1B"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="32630405, 32630429, 32630438, 32637230"
	resourceTags=""
	productPesIds="13491, 16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Server did not load SGX enclave correctly

## We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and 
it seems the SGX enclave is not loaded correctly on your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->**. To resolve this issue, follow the recommended steps.
<!--/issueDescription-->

## **Attestation Process**

Before a client driver submits a T-SQL statement to Azure SQL logical server for execution, the driver triggers the following enclave attestation workflow using Microsoft Azure Attestation.
1.  The client driver passes the attestation URL, specified in the database connection, to the Azure SQL logical server.
2.  The Azure SQL logical server collects the evidence about the enclave, its hosting environment, and the code running inside the enclave. The server then sends an attestation request to the attestation provider, referenced in the attestation URL.
3.  The attestation provider validates the evidence against the configured policy and issues an attestation token to the Azure SQL logical server. The attestation provider signs the attestation token with its private key.
4.  The Azure SQL logical server sends the attestation token to the client driver.
5.  The client contacts the attestation provider at the specified attestation URL to retrieve its public key, and then it verifies the signature in the attestation token.

## **Recommended Steps**

Validate if the SGX enclave is loaded correctly on **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** by running the following query in SSMS:

`select * from sys.dm_column_encryption_enclave`


- If the query returns a row and size of **current_memory_size_kb > 0**, the SGX enclave is loaded correctly.

- If enclave fails to load due to some reason, contact **Customer Support**.

## **Recommended Documents**

* [Guidelines for configuring and setting up Always Encrypted with secure enclaves](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-with-secure-enclaves-landing)
* [Troubleshoot common issues for Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves-troubleshooting)
