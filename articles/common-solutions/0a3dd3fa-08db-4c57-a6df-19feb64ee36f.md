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

## **Recommended Steps**

1.	Make sure you followed the prerequisites for enabling entity pages described [here](https://docs.microsoft.com/azure/sentinel/enable-entity-behavior-analytics#prerequisites)

2.	In the navigation pane, go to ‘Settings’ -> ‘Settings’ -> ‘Entity behavior analytics’

3.	Click on ‘Select Data Sources’
	1.	Check the box for the data source you want to have UEBA value on top of
	2.	If no supported data sources for UEBA is connected, you can pivot to the relevant data connector to connect them

4.	Not all the events from the selected data sources is being enriched (only events that have security importance) 

5.	After you enable UEBA for these data sources, ~15 minutes you will start to see data ingested into you ‘Azure Sentinel UEBA’ tables
	1.	‘BehaviorAnalytics’ – holds the enriched data 
	2.	‘IdentityInfo’ – holds a snapshot of the users profiles
	3.	‘UserPeersAnalytics’ – hold information about the calculated user peers
	4.	‘UserAccessAnalytics’ – hold information about Azure RBAC permissions the user have

6.	You can use the following [enrichment reference](https://docs.microsoft.com/azure/sentinel/ueba-enrichments) to hunt on top of the data 

## **Recommended Documents**

* [UEBA Concept](https://docs.microsoft.com/azure/sentinel/identify-threats-with-entity-behavior-analytics)
* [Enabling UEBA](https://docs.microsoft.com/azure/sentinel/enable-entity-behavior-analytics)
* [UEBA Enrichments](https://docs.microsoft.com/azure/sentinel/ueba-enrichments)
* [UEBA Hunting Queries](https://github.com/Azure/Azure-Sentinel/tree/master/Hunting%20Queries/BehaviorAnalytics)