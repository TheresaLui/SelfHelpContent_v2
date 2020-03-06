<properties
    pageTitle="MySQL-Quota"
    description="MySQL-Quota"
    authors="ambrahma"
    ms.author="ambrahma"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684016"
    productPesIds="15621"
    cloudEnvironments="Public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-orcas-quota-mysql"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# MySQL Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "MySQL-Quota",
    "fileAttachmentHint": "Please upload your file to support your request",
    "formElements": [
        {
            "id": "quotaSubType",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota Sub-type",
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "dropdownOptions": [
                {
                    "text": "MySQL region enable",
                    "value": "enableregion"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "location",
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Please choose the region in which you want to have MySQL Server",
            "watermarkText":"Choose a region",
            "required": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quotaSubType",
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
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
            "order": 3,
            "controlType": "numerictextbox",
            "displayLabel": "Please provide specific capacity for your request",
            "watermarkText": "For example, 30 General purpose vCores",
            "required": true
        }, {
			"id": "learn_more_text",
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
			"order": 4,
			"controlType": "infoblock",
			"content": "<a href='https://go.microsoft.com/fwlink/?linkid=867609'>Learn more</a> about vCore capacity."
		},
        {
            "id": "business_justification",
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quotaSubType != null && quotaSubType == dont_know_answer",
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