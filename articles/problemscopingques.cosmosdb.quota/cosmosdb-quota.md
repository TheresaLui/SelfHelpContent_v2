<properties
    pageTitle="Cosmos DB Quotas"
    description="Cosmos DB Quota"
    authors="hecepeda"
    ms.author="hecepeda"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32447244"
    productPesIds="15621"
    cloudEnvironments="public,fairfax,usnat,ussec"
    schemaVersion="1"
    articleId="cosmosdb-quota"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Cosmos DB
---
{
   "$schema":"SelfHelpContent",
   "subscriptionRequired":true,
   "resourceRequired":false,
   "title":"Cosmos DB",
   "fileAttachmentHint":"",
   "quotaRequestVersion":"1.0",
   "formElements":[
      {
         "id":"quota_subtype",
         "order":1,
         "controlType":"dropdown",
         "infoBalloonText":"Quota Type",
         "displayLabel":"Quota type",
         "watermarkText":"Choose an option",
         "required":true,
         "filter":false,
         "includeInQuotaSummary":true,
         "dropdownOptions":[
            {
               "text":"Region access",
               "value":"enableLocation"
            },
            {
               "text":"Database accounts per subscription",
               "value":"accountLimitChange"
            },
            {
               "text":"Throughput on container",
               "value":"throughputLimitChange"
            },
            {
               "text":"Storage limit for container",
               "value":"storageLimitIncrease"
            },
            {
               "text":"Shared database throughput",
               "value":"ruDatabaseShared"
            },
            {
               "text":"Remove limit on number of containers for Shared database throughput",
               "value":"containerLimitIncrease"
            },
            {
               "text":"Other quota types",
               "value":"otherQuotas"
            }
         ]
      },
      {
         "id":"quota_othersubtype",
         "visibility":"quota_subtype == otherQuotas",
         "order":2,
         "controlType":"dropdown",
         "displayLabel":"Other quota type",
         "watermarkText":"Select the type of quota",
         "required":true,
         "filter":false,
         "includeInQuotaSummary":true,
         "infoBalloonText":"Other quota types",
         "dropdownOptions":[
            {
               "text":"Number of regional failover",
               "value":"regionalFailovers"
            },
            {
               "text":"Stored procedures per container",
               "value":"storeProcedureContainer"
            },
            {
               "text":"UDFs per container",
               "value":"udfsContainer"
            },
            {
               "text":"Number of unique keys per container",
               "value":"uniqueKeysContainer"
            },
            {
               "text":"Number of paths per unique key constraint",
               "value":"pathsUniqueKey"
            },
            {
               "text":"Number of paths in indexing policy",
               "value":"pathsIndexPolicy"
            },
            {
               "text":"JOINs per query",
               "value":"joinsQuery"
            },
            {
               "text":"UDFs per query",
               "value":"udfsQuery"
            },
            {
               "text":"Resource token expiry time",
               "value":"tokenExpiryTime"
            }
         ]
      },
      {
         "id":"quota_othersubtype_account",
         "visibility":"quota_othersubtype != null",
         "order":3,
         "controlType":"dropdown",
         "displayLabel":"Account Name",
         "watermarkText":"Choose an account",
         "required":true,
         "includeInQuotaSummary":true,
         "dynamicDropdownOptions":{
            "dependsOn":"quota_subtype",
            "uri":"/subscriptions/{subscriptionId}/providers/Microsoft.DocumentDB/databaseAccounts?api-version=2020-04-01",
            "jTokenPath":"value",
            "textProperty":"name, location",
            "textTemplate":"{name}",
            "ValueProperty":"id",
            "valuePropertyRegex":".*",
            "defaultDropdownOptions":{
               "value":"dont_know_answer",
               "text":"Other"
            }
         }
      },
      {
         "id":"quota_subtype_account",
         "visibility":"quota_subtype == throughputLimitChange || quota_subtype == ruDatabaseShared || quota_subtype == containerLimitIncrease",
         "order":4,
         "controlType":"dropdown",
         "displayLabel":"Account Name",
         "watermarkText":"Choose an account",
         "required":true,
         "includeInQuotaSummary":true,
         "dynamicDropdownOptions":{
            "dependsOn":"quota_subtype",
            "uri":"/subscriptions/{subscriptionId}/providers/Microsoft.DocumentDB/databaseAccounts?api-version=2020-04-01",
            "jTokenPath":"value",
            "textProperty":"name, location",
            "textTemplate":"{name}",
            "ValueProperty":"id",
            "valuePropertyRegex":".*",
            "defaultDropdownOptions":{
               "value":"dont_know_answer",
               "text":"Other"
            }
         }
      },
      {
         "id":"quota_region",
         "visibility":"quota_subtype == enableLocation || quota_subtype == storageLimitIncrease",
         "order":5,
         "controlType":"dropdown",
         "displayLabel":"Location requested",
         "watermarkText":"Choose a location",
         "required":true,
         "includeInQuotaSummary":true,
         "dynamicDropdownOptions":{
            "dependsOn":"quota_subtype",
            "uri":"/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
            "jTokenPath":"value",
            "textProperty":"displayName",
            "ValueProperty":"name",
            "valuePropertyRegex":".*",
            "defaultDropdownOptions":{
               "value":"dont_know_answer",
               "text":"Other"
            }
         }
      },
      {
         "id":"unit_measureUnits",
         "order":6,
         "visibility":"quota_subtype == accountLimitChange || quota_subtype == throughputLimitChange || quota_subtype == ruDatabaseShared",
         "controlType":"textBlock",
         "displayLabel":"Please enter limit values using Units as your unit of measure"
      },
      {
         "id":"unit_measureUnits_othersubtype",
         "order":7,
         "visibility":"quota_othersubtype != tokenExpiryTime",
         "controlType":"textBlock",
         "displayLabel":"Please enter limit values using Units as your unit of measure"
      },
      {
         "id":"gigabytes_measureUnits",
         "order":8,
         "visibility":"quota_subtype == storageLimitIncrease",
         "controlType":"textBlock",
         "displayLabel":"Enter limit values using GigaBytes (GB) as your unit of measure"
      },
      {
         "id":"minutes_measureUnits",
         "order":9,
         "visibility":"quota_othersubtype == tokenExpiryTime",
         "controlType":"textBlock",
         "displayLabel":"Enter limit values using minutes (mm) as your unit of measure"
      },
      {
         "id":"current_limit",
         "visibility":"quota_subtype != enableLocation && quota_subtype != containerLimitIncrease",
         "order":10,
         "controlType":"numerictextbox",
         "displayLabel":"Current Limit",
         "infoBalloonText":"Put the current limit value here.",
         "required":false,
         "validations":[
            {
               "type":"greaterthan",
               "value":-1
            }
         ],
         "isNewQuotaLimit":false
      },
      {
         "id":"new_limit",
         "visibility":"quota_subtype != enableLocation && quota_subtype != containerLimitIncrease",
         "order":11,
         "controlType":"numerictextbox",
         "displayLabel":"New quota requested",
         "infoBalloonText":"Put the new value for the limit you are requesting here.",
         "required":true,
         "validations":[
            {
               "type":"greaterthan",
               "controlId":"current_limit"
            }
         ],
         "isNewQuotaLimit":true
      },
      {
         "id":"business_justification",
         "visibility":"quota_subtype != null",
         "order":12,
         "controlType":"multilinetextbox",
         "displayLabel":"Describe the business requirement",
         "watermarkText":"Provide business justification for your request",
         "required":false,
         "useAsAdditionalDetails": true
      }
   ]
}
---
