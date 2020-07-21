<properties
    pageTitle="PostgreSQL-Quota"
    description="PostgreSQL-Quota"
    authors="ambrahma"
    ms.author="ambrahma"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684017"
    productPesIds="15621"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-orcas-quota-postgresql"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# PostgreSQL Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "PostgreSQL-Quota",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "0.0",
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
            "dropdownOptions": [
                {
                    "text": "Region access",
                    "value": "enablelocation"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "quota_region",
            "visibility": "quota_subtype != null && quota_subtype == enablelocation",
            "order": 2,
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
            "id": "capacity_requested",
            "visibility": "quota_subtype != null && quota_subtype == enablelocation",
            "order": 3,
            "controlType": "numerictextbox",
            "isNewQuotaLimit": true,
            "includeInQmsPayload": true,
            "displayLabel": "Capacity requested (in VCores)",
            "infoBalloonText": "<a href='https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers'>Learn more</a>.",
            "required": true,
            "validations": [
                            {
                             "type": "greaterthan",
                             "value": 0
                            }
                           ]
        },
        {
            "id": "business_justification",
            "visibility": "quota_subtype != null && quota_subtype == enablelocation",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quota_subtype != null && quota_subtype == dont_know_answer",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---