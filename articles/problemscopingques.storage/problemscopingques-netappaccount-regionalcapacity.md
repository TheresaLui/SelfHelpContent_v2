<properties
	articleId="bffc5036-209f-4b05-9c91-4a57c0af12e2"
	pageTitle="Requesting additional capacity"
	description="Requesting additional capacity"
	authors="b-aragus"
	ms.author="b-aragus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637708"
	productPesIds="15621"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Requesting additional capacity
---
{
    "subscriptionRequired": true,
    "resourceRequired":false,
    "title": "Request regional capacity quota",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "0.0",
    "formElements": [
        {
            "id": "quota_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota type",
            "required": true,
            "infoBalloonText": "Select the quota type that you want to change",
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
			]
        },
        {
            "id": "quota_region",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Location requested",
            "watermarkText":"Choose a location",
            "required": true,
            "includeInQuotaSummary": true,
            "infoBalloonText": "Select the region that the quota limit change will affect",
            "dynamicDropdownOptions": {
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
            "displayLabel": "Enter value for new limit",
            "watermarkText": "",
            "required": true,
            "isNewQuotaLimit": true,
            "infoBallonText": "Enter the new limit for the quota type"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
