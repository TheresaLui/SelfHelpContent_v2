<properties
	pageTitle="Synchronizing AD to Azure AD/SQL-related installation and sync issues"
	description="Synchronizing AD to Azure AD/SQL-related installation and sync issues"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cychua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32565592"
	resourceTags=""
	productPesIds="14785,16578"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="08378581-7bc3-42c3-b45d-63468638d316"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Synchronizing AD to Azure AD/SQL-related installation and sync issues

## **Recommended steps**
1. If you are using **LocalDB** as the database for Azure AD Connect and has reached its **10-GB limit**, the Synchronization Service can no longer operate correctly. You can temporarily recover the service by deleting run history data to reclaim DB space. For more information, refer to article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).

2. If you wish to upgrade the LocalDB of an existing Azure AD Connect deployment with full version of SQL, you must deploy a new Azure AD Connect server with the full version of SQL. It is recommended that you do a swing migration where the new Azure AD Connect server (with SQL DB) is deployed as a staging server, next to the existing Azure AD Connect server (with LocalDB).

## **Recommended documents**
* [Prerequisites for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-prerequisites)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
