<properties
    pageTitle="Follow SQL DB Advisor recommendations"
    description="Follow SQL DB Advisor recommendations"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="a1f91337-c953-4791-9517-f170de60bf35_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudES_AzureAdvisor"
/>
# Follow SQL DB Advisor recommendations
---
{
  "recommendationOfferingId": "1c017867-b3d9-4798-979e-9693c49579f8",
  "recommendationOfferingName": "Azure SQL Database",
  "$schema": "AdvisorRecommendation",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationTypeId": "a1f91337-c953-4791-9517-f170de60bf35",
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/servers/databases",
  "recommendationFriendlyName": "SQLDBAdvisor",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/aa_sqldbadvisorrec_learnmore",
  "description": "Follow SQL DB Advisor recommendations",
  "longDescription": "Improve the performance of your SQL database. Follow the recommendations from SQL DB Advisor.",
  "potentialBenefits": "Improved database performance",
  "actions": [
    {
      "actionId": "18c1ceec-2171-486c-ab89-8205f804340f",
      "actionType": "Document",
      "description": "Improve database performance with SQL DB Advisor",
      "documentLink": "https://aka.ms/aa_sqldbadvisorrec_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "bae53d35-0888-4af8-b06b-d98ffa6acf8f",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DatabaseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "SQL DB Advisor recommendations",
  "additionalColumns": [],
  "onDemand": true,
  "legacyRecommender": {
    "className": "Microsoft.Azure.Advisor.Common.Recommenders.SqlAdvisorDatabaseIntegration",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  },
  "tip": "You can improve the performance of your SQL Azure databases."
}
---
