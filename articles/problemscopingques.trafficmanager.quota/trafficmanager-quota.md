<properties
    pageTitle="Traffic Manager Quota"
    description="Traffic Manager Quota"
    authors="anchou"
    ms.author="anchou"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32447253"
    productPesIds="15621"
    cloudEnvironments="public, fairfax, mooncake, blackforest, usnat, ussec"
    schemaVersion="1"
    articleId="trafficmanager-quota"
    ownershipId="CloudNet_TrafficManager"
/>
# TrafficManager Quota Questions
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
	"resourceRequired": false,
	"title": "Traffic Manager Quota",
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
					"text": "Max Profile Quota per subscription",
					"value": "profileLimitChange"
				},
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
			]
		},
		{
            "id": "quota_region",
			"visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Region",
			"infoBalloonText": "It is always global for Traffic Manager.",
            "watermarkText":"Global",
            "required": false,
            "includeInQuotaSummary": false,
			"dropdownOptions": [
				{
					"text": "Global",
					"value": "Global"
				},
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
			]
        },
		{
			"id": "new_limit",
			"visibility": "quota_subtype == profileLimitChange",
			"order": 3,
			"controlType": "numerictextbox",
			"displayLabel": "New quota requested",
			"infoBalloonText": "Put the new value for the limit you are requesting here.",
			"required": true,
			"validations": [
				{
					"type": "greaterthan",
					"value": 200
				},
				{
					"type": "lessthan",
					"value": 1000
				}
			],
			"isNewQuotaLimit": true
		},
		{
			"id": "business_justification",
			"visibility": "quota_subtype != null && quota_subtype != dont_know_answer",
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
			"watermarkText": "Provide additional information about your issue, include details such as account name, type of limit, current value and new value requested.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---