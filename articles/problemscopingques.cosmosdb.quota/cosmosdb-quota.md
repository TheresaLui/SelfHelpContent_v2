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
            "infoBalloonText": "info balloon",
            "dropdownOptions": [
                {
                    "text": "Region access",
                    "value": "enablelocation"
                },
                {
                    "text": "Accounts limit increase",
                    "value": "accountlimitincrease"
                },
                {
                    "text": "Accounts limit decrease",
                    "value": "accountlimitdecrease"
                },
                {
                    "text": "Availability Zone enablement",
                    "value": "azenablelocation"
                },
                {
                    "text": "Throughput limit increase",
                    "value": "throughputlimitincrease"
                },
                {
                    "text": "Throughput limit decrease",
                    "value": "throughputlimitdecrease"
                },
                {
                    "text": "Max number of containers increase",
                    "value": "containerlimitincrease"
                },
                {
                    "text": "Storage limit increase",
                    "value": "storagelimitincrease"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "quota_region",
            "visibility": "quota_subtype != null && (quota_subtype == enablelocation || quota_subtype ==azenablelocation)",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Location requested",
            "watermarkText":"Choose a location",
            "required": true,
            "includeInQuotaSummary": true,
            "includeInQmsPayload": false,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"displayName",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "quota_account",
            "visibility": "quota_subtype != null && (quota_subtype == accountlimitincrease || quota_subtype == accountlimitdecrease ||  quota_subtype == throughputlimitincrease ||  quota_subtype == throughputlimitdecrease ||  quota_subtype == containerlimitincrease || quota_subtype == storagelimitincrease)",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":"Account Name",
            "watermarkText":"Choose an account",
            "required": true,
            "includeInQuotaSummary": true,
            "includeInQmsPayload": false,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.DocumentDB/databaseAccounts?api-version=2020-04-01",
                "jTokenPath":"value",
                "textProperty":"name, location",
                "textTemplate":"Name:{name}, Region{location}"
                "ValueProperty":"id",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "new_limit",
            "visibility": "quota_subtype != null && quota_subtype == dbaccountlimit",
            "order": 4,
            "controlType": "numerictextbox",
            "includeInQmsPayload": true,
            "displayLabel": "New quota requested",
            "infoBalloonText": "Put the new value for the limit you are requesting here.",
            "required": true,
            "validations": [
                {
                    "type": "greaterthan",
                    "value": 0
                }
                ],
            "isNewQuotaLimit": true
        },
        {
            "id": "business_justification",
            "visibility": "quota_subtype != null && quota_subtype == enablelocation",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quota_subtype != null && quota_subtype == dont_know_answer",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
