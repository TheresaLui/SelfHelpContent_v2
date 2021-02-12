<properties
	pageTitle="Generic Issues troubleshooting guidance"
	description="Generic Issues troubleshooting guidance"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9cbc5e36-2484-4516-8b0e-5fe64e10fc24"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Generic Issues troubleshooting guidance

## Issue Description

Requests to Storage are blocked by the Storage Account Firewall. The Firewall will block any requests from Subnets or IP/s that are not explicitely whitelisted in the ACLs of the Storage Firewall.

## Symptoms

A 3rd Party application request or a Microsoft Service request fails due to AuthorizationFailure with error 403 - Forbidden.

## Troubleshooting Guidance

On this section we'll review the Storage Logs to find out more details regarding the blocked request/s.

### Review Azure Storage Front End logs

1. In [Jarvis /MDM](https://jarvis-west.dc.ad.msft.net/) access the Logs section.
2. Complete the query details. Example: <https://jarvis-west.dc.ad.msft.net/365E4FC5>
    
~~~powershell
        Namespace: Xstore
        Events: FrontEndSummaryPerfLogs
        Tenant:  <StorageCluster>
        Time range:<Time range of the issue>
        Filtering: ActivityId == <ActivityId/ResourceId>
~~~

3.  Useful information to check:
      1. **Operation**(Read/Write/Other)
      2. **RequestUrl**: has the information of the target Uri being accessed
      3. **HttpStatusCode:** For additional reference follow this [List of HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes "wikipedia:List of HTTP status codes").
      4. **Status:** reason for the failure being logged. Examples: "OperationTimedOut", "ServerBusy"
      5. **InternalStatus:** internal reason for the failure being logged. Examples: "ClientTimeoutError", ClientPartitionRequestThrottlingError.
      6. **UserAgent:** client the customer is using to perform the operation such as .NET, PowerShell, Azure CLI, etc.
      7. **ClientIP:** IP and Port of the client doing the operation.
      8. **TimeInMs:** Total time for the operation in all layers.
      9. **TotalFeTimeInMs**: Total time spent in the Azure Blob Storage Front End.
      10. **TotalTableServerTimeInMs:** Total time spent in the Azure Blob Storage Table Server.
4.  Issues related to Azure Storage Firewall blocking the requests include the following results:
    
~~~

        Status: AuthorizationFailure
        MeasurementStatus: IpAuthorizationFailure
        InternalStatus: OAuthIpAuthorizationError / IpAuthorizationError

~~~

6. If the ClientIP is showing as an IPv6, please review [**how to extract Ipv4 address from Ipv6 Service Tunnel**](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Storage_HowTo_How+to+extract+Ipv4+address+from+Ipv6+Service+Tunnel "curated:Azure_Storage_HowTo_How to extract Ipv4 address from Ipv6 Service Tunnel").
5. If the failed request doesn't have the ***IpAuthorizationError*** or ***OAuthIpAuthorizationError*** then the issue is not related to Storage Firewall and this issue needs to be investigated from an Authentication issue(SAS/Oauth/SharedKey).
7. If the errors are related to the above error messages please continue with the next subsection: **Review Azure Storage Firewall configuration**

### Review Azure Storage Firewall configuration

1.  Open Azure Support Center Resource Explorer.
2.  Search/Navigate to the involved Storage Account and select it.
3.  Locate the section "<u>Azure Storage Firewall and Virtual Networks</u>" within the Storage Account details page.
4.  Review the "<u>Allow access from</u>" property.
    1.  If the value is "<u>All networks</u>", Azure Storage Firewall is **disabled** and therefore customer shouldn't be experiencing an issue related to the Storage Firewall. 
    2.  If the value is "<u>Selected Networks</u>", Azure Storage Firewall is **enabled**.
        1.  Proceed to review the "<u>Virtual Network Rules</u>" section.
        2.  Verify that the ClientIP belongs to some of the allowed subnets or IPs. **Note:** You should have gotten the ClientIP details from the results in **Review Azure Storage Front End logs*** above.
        3.  If the ClientIP is not included in any whitelisted subnet or IP:
            * If the ClientIP is a [**Public IP**](https://en.wikipedia.org/wiki/IP_address#Public_address): for the request to be successfully allowed, the customer will need to allow the missing Client IP and/or subnet into the Storage Firewall ACLs. Further information at [Configure Azure Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
            * If the ClientIP is a [**Private IP**](https://en.wikipedia.org/wiki/Private_network#Private_IPv4_addresses): 
                * For the request to be successfully allowed, the customer will need to whitelist the Subnet where this request comes from by [Configuring Azure Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security). 
                * **IMPORTANT**: If the request comes from a Private IP not identified by the customer and not present in their VNETs/Subnets, it's possible that this request comes from another Azure Service within the same Region that is either not supported or has not been correctly configured.
