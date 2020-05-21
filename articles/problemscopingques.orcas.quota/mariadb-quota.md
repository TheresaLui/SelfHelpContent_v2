<properties
    pageTitle="MariaDB-Quota"
    description="MariaDB-Quota"
    authors="ambrahma"
    ms.author="ambrahma"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684015"
    productPesIds="15621"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-orcas-quota-mariadb"
    ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# MariaDB Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "MariaDB-Quota",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "quotaType",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota type",
            "watermarkText": null,
            "required": "true",
            "filter": false,
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
            "id": "location_requested",
            "visibility": "quotaType != null && quotaType == enablelocation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Location requested",
            "watermarkText":"Choose a location",
            "required": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quotaType",
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
            "id": "capacity_requested",
            "visibility": "quotaType != null && quotaType == enablelocation",
            "order": 3,
            "controlType": "numerictextbox",
            "displayLabel": "Capacity requested (in VCores)",
            "infoBalloonText": "<a href='https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers'>Learn more</a>.",
            "required": true
        },
        {
            "id": "business_justification",
            "visibility": "quotaType != null && quotaType == enablelocation",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quotaType != null && quotaType == dont_know_answer",
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