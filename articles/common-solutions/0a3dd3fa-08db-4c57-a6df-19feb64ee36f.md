<properties
  pagetitle="Azure Sentinel - Entity Behavior - Enabling UEBA on specific data soruces"
  service=""
  resource=""
  ms.author="yaronsahar"
  selfhelptype="Generic"
  supporttopicids="32786011"
  productpesids="16690"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="0a3dd3fa-08db-4c57-a6df-19feb64ee36f"
  ownershipid="Azure_Sentinel" />
# Azure Sentinel - Entity Behavior - Enabling UEBA on specific data soruces

Learn how to enable UEBA on specific sources in Azure Sentinel by following these steps.

## **Recommended Steps**

1.  Make sure to follow the [prerequisites for enabling entity pages](https://docs.microsoft.com/azure/sentinel/enable-entity-behavior-analytics#prerequisites)

2. In the navigation pane, go to **Settings** > **Entity behavior analytics**

3. Select **Select Data Sources** and check the box for the data source for which you want to enable UEBA. 
   *  If no supported data sources for UEBA are connected, go to the relevant data connectors and connect them<br>
    Note: Not all events from the selected data sources are enriched, only events that have security importance. 

4. After you enable UEBA for these data sources, wait approximately 15 minutes to see data ingested into your Azure Sentinel UEBA table<br>s:
	1. **BehaviorAnalytics** holds the enriched data 
	2. **IdentityInfo** holds a snapshot of the users' profiles
	3. **UserPeersAnalytics** holds information about the calculated user peers
	4. **UserAccessAnalytics** holds information about Azure RBAC permissions the user has

5. To search the data, use the following [enrichment reference](https://docs.microsoft.com/azure/sentinel/ueba-enrichments) 

## **Recommended Documents**

* [UEBA Concept](https://docs.microsoft.com/azure/sentinel/identify-threats-with-entity-behavior-analytics)
* [Enabling UEBA](https://docs.microsoft.com/azure/sentinel/enable-entity-behavior-analytics)
* [UEBA Enrichments](https://docs.microsoft.com/azure/sentinel/ueba-enrichments)
* [UEBA Hunting Queries](https://github.com/Azure/Azure-Sentinel/tree/master/Hunting%20Queries/BehaviorAnalytics)
