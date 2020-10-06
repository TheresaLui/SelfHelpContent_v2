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
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Cosmos DB",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "1.0",
    "formElements": [
        {
            "id": "quota_subtype",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota type",
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "includeInQuotaSummary": true,
            "infoBalloonText": "Quota type",
            "dropdownOptions": [
                {
                    "text": "Region access",
                    "value": "enableLocation"
                },
                {
                    "text": "Database accounts per subscription",
                    "value": "accountLimitChange"
                },
                {
                    "text": "Throughput on container",
                    "value": "throughputLimitChange"
                },
                {
                    "text": "Storage limit for container",
                    "value": "storageLimitIncrease"
                }
                {
                     "text": "Other quota types",
                    "value": "otherQuotas"
                }
            ]
        },
        {
            "id": "quota_othersubtype",
            "visibility": "quota_subtype == otherQuotas"
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Other quota type",
            "watermarkText": "Select the type of quota",
            "required": "true",
            "filter": false,
            "includeInQuotaSummary": true,
            "infoBalloonText": "Other quota types",
            "dropdownOptions": [
                {
                    "text": "Containers for shared database throughput",
                    "value": "containerLimitIncrease"
                }, 
                {
                    "text": "RUs per database (shared)",
                    "value": "ruDatabaseShared"
                },
                {
                    "text": "Partitions per account",
                    "value": "partitionAccount"
                },
                {
                    "text": "Partition size",
                    "value": "partitionSize"
                },
                {
                    "text": "Number of regional failover",
                    "value": "regionalFailovers"
                },
                {
                     "text": "Partition key size",
                    "value": "partitionKeySize"
                },
                {
                     "text": "Stored procedures per container",
                    "value": "storeProcedureContainer"
                },
                {
                     "text": "UDFs per container",
                    "value": "udfsContainer"
                },
                {
                     "text": "Number of unique keys per container",
                    "value": "uniqueKeysContainer"
                },
                {
                     "text": "Number of paths per unique key constraint",
                    "value": "pathsUniqueKey"
                },
                {
                     "text": "Number of paths in indexing policy",
                    "value": "pathsIndexPolicy"
                },
                {
                     "text": "JOINs per query",
                    "value": "joinsQuery"
                },
                {
                     "text": "UDFs per query",
                    "value": "udfsQuery"
                },
                {
                     "text": "Resource token expiry time",
                    "value": "tokenExpiryTime"
                }
            ]
        },
        {
            "id": "quota_account",
            "visibility": "quota_subtype != enableLocation &&  quota_subtype != accountLimitChange || quota_othersubtype != null ",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":"Account Name",
            "watermarkText":"Choose an account",
            "required": true,
            "includeInQuotaSummary": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.DocumentDB/databaseAccounts?api-version=2020-04-01",
                "jTokenPath":"value",
                "textProperty":"name, location",
                "textTemplate":"{name}",
                "ValueProperty":"id",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "quota_region",
            "visibility": "quota_subtype == enableLocation || quota_subtype == throughputLimitChange  || quota_subtype ==storageLimitIncrease",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel":"Location requested",
            "watermarkText":"Choose a location",
            "required": true,
            "includeInQuotaSummary": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"name",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "unit_measureUnits",
            "order": 5,
            "visibility": "quota_subtype == throughputLimitChange ||  quota_subtype == containerLimitIncrease || quota_othersubtype == containerLimitIncrease || quota_othersubtype == ruDatabaseShared || quota_othersubtype == partitionAccount || quota_othersubtype == regionalFailovers || quota_othersubtype == storeProcedureContainer || quota_othersubtype == udfsContainer || quota_othersubtype == uniqueKeysContainer || quota_othersubtype == pathsUniqueKey || quota_othersubtype == pathsIndexPolicy || quota_othersubtype == joinsQuery || quota_othersubtype == udfsQuery ",
            "controlType: "textBlock",
            "text": "Please enter limit values using Units as your unit of measure"
        },
        {
            "id": "gigabytes_measureUnits",
            "order": 6,
            "visibility": "quota_subtype == storageLimitIncrease || quota_othersubtype == partitionSize ",
            "controlType: "textBlock",
            "text": "Please enter limit values using GigaBytes (GB) as your unit of measure"
        },
        {
            "id": "bytes_measureUnits",
            "order": 7,
            "visibility": "quota_othersubtype == partitionKeySize",
            "controlType: "textBlock",
            "text": "Please enter limit values using Bytes (b) as your unit of measure"
        },
        {
            "id": "minutes_measureUnits",
            "order": 8,
            "visibility": "quota_othersubtype == tokenExpiryTime",
            "controlType: "textBlock",
            "text": "Please enter limit values using minutes (mm) as your unit of measure"
        },
        {
            "id": "current_limit",
            "visibility": "quota_subtype == accountLimitChange ||  quota_subtype == throughputLimitChange ||  quota_subtype == containerLimitIncrease || quota_subtype == storageLimitIncrease",
            "order": 9,
            "controlType": "numerictextbox",
            "displayLabel": "Current Limit",
            "infoBalloonText": "Put the current limit value here.",
            "required": false,
            "validations": [
                {
                    "type": "greaterthan",
                    "value": -1
                }
                ],
            "isNewQuotaLimit": false
        },
        {
            "id": "new_limit",
            "visibility": "quota_subtype == accountLimitChange ||  quota_subtype == throughputLimitChange ||  quota_subtype == containerLimitIncrease || quota_subtype == storageLimitIncrease",
            "order": 10,
            "controlType": "numerictextbox",
            "displayLabel": "New quota requested",
            "infoBalloonText": "Put the new value for the limit you are requesting here.",
            "required": true,
            "validations": [
                {
                    "type": "greaterthan",
                    "controlId": current_limit
                }
                ],
            "isNewQuotaLimit": true
        },
        {
            "id": "business_justification",
            "visibility": "quota_subtype != null && quota_subtype != dont_know_answer",
            "order": 11,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quota_subtype != null && quota_subtype == dont_know_answer",
            "order": 12,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue, include details such as account name, type of limit, current value and new value requested.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
