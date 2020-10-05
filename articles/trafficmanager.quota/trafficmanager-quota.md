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
				}
			]
		},
		{
			"id": "new_limit",
			"visibility": "quota_subtype == profileLimitChange",
			"order": 2,
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
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Describe the business requirement",
			"watermarkText": "Provide business justification for your request",
			"required": false
		},
		{
			"id": "problem_description",
			"visibility": "quota_subtype != null && quota_subtype == dont_know_answer",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Describe your quota request",
			"watermarkText": "Provide additional information about your issue, include details such as account name, type of limit, current value and new value requested.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}