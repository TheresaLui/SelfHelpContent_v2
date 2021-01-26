<properties
  pagetitle="Azure Sentinel - Azure Sentinel management - Removing Azure Sentinel"
  service=""
  resource=""
  ms.author="yaronsahar"
  selfhelptype="Generic"
  supporttopicids="32785991"
  productpesids="16690"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="60cac1e8-ef9b-4157-a03d-f5ea6be46bfd"
  ownershipid="Azure_Sentinel" />
# Azure Sentinel - Azure Sentinel management - Removing Azure Sentinel

## **Recommended Steps**

1. If you remove the solution, your subscription will continue to be registered with the Azure Sentinel resource provider.
   You can remove it manually.

2. Within the first 48 hours after offboarding, the data and analytic rules (including real-time automation configuration) will no longer be accessible or queryable in Azure Sentinel.
   After 30 days these resources are removed:
   Incidents (including investigation metadata), Analytic rules and Bookmarks.

2. Your playbooks, saved workbooks, saved hunting queries, and notebooks are not removed. Some may break due to the removed data. You can remove those manually.

## **Recommended Documents**

* [Remove Azure Sentinel from your workspace](https://docs.microsoft.com/azure/sentinel/offboard)