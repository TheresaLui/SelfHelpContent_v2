<properties
    pageTitle="Managing firewall rules for Azure Database for PostgreSQL"  
    description="Managing firewall rules for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="230"
    selfHelpType="generic"
    supportTopicIds="32639980, 32780992"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-create-networking"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Networking

You select your preferred networking method at create. your choices are private access (VNet integration) and public access (allowed IP addresses). This networking selection cannot be changed once the server is created.

## **Recommended Steps**

* If you cannot connect after setting up a public access firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports
  * If your client does not have a static IP address, the current IP address might not be covered by the firewall rule

* If you cannot connect to your server in a virtual network, confirm that the resource you are connecting from is in the Azure virtual network or is allowed to access the virtual network. 

* There may be as much as a five minute delay for changes to the Azure Database for PostgreSQL configuration to take effect. Confirm your rule was added and re-try to connect for at least 5 minutes.

* If you receive an error while trying to create, your server may have been unavailable due to a user- or service-initiated restart. You can review the Azure Activity Log for user-initiated operations like restart or scaling. You can review Resource Health Check for service-initiated maintenance. 

* If you are having trouble using Azure CLI:

  * Make sure you are signed in to the correct Azure account using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters with valid values

* If you are deploying using ARM templates:

  * If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. 

