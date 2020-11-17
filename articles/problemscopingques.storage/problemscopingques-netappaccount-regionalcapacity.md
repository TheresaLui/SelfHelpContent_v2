<properties
	articleId="problemscopingques-netappaccount-regionalcapacity"
	pageTitle="Requesting additional capacity"
	description="Requesting additional capacity"
	authors="b-aragus"
	ms.author="b-aragus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777926"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
    articleId="AzureNetApp_regional_quota"
	ownershipId="AzureNetAppFiles"
/>
# Requesting additional capacity
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Request regional capacity quota",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "quota_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota type",
            "required": true,
            "dropdownOptions": [
				{
                    "value": "tib_per_subscription",
                    "text": "Tibs per subscription"
                },
                {
                    "value": "accounts_per_subscription",
                    "text": "Accounts per subscription"
                },
				{
                    "value": "pools_per_account",
                    "text": "Pools per account"
                },
				{
                    "value": "volumes_per_pool",
                    "text": "Volumes per pool"
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
            "id": "quota_value",
            "order": 3,
            "controlType": "numerictextbox",
            "displayLabel": "Enter value",
            "watermarkText": "",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
