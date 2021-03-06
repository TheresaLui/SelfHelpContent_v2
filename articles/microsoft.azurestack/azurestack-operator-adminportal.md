<properties
  pagetitle="Azure Stack Administrator Portal&#xD;"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="alexsmit,justinha,v-myoung,patricka"
  selfhelptype="Generic"
  supporttopicids="32629245,32737195,32737321,32745921"
  resourcetags=""
  productpesids="16226,17058,17057,17322"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-operator-adminportal"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Administrator Portal

To access the Azure Administrator portal, go to the Azure portal,  and sign in as an Azure Stack operator. 

## **Recommended Steps**

* For multi-node integrated systems, the portal address varies based on the region name and fully-qualified domain name (FQDN) of your Azure Stack deployment. The portal address will match this pattern: `https://adminportal.<REGION>.<FQDN>`

* Verify that the [DNS name resolution](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-dns) is working

* Access to the Administrator portal requires allowing traffic through TCP port 443. See [Azure Stack firewall integration](https://docs.microsoft.com/azure-stack/operator/azure-stack-firewall) and [Publish Azure Stack Services](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints) 

* If you can't sign in to the portal, verify that the client date and time setting is correct and not set in the past or future.

* If the portal is unavailable, and no type of patch, update, or field replacement is in progress, you can run the following command to fix the problem:

  ```
  Test-AzureStack -Repair -Include AzsPortalAPISummary
  ```

   **Caution:** You can't use this command during a component replacement or update.

## **Recommended Documents**

* [Using the administrator portal in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-portals)
