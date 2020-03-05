<properties
                pageTitle="MySql-Quota-Enable-Region"
                description="MySql-Quota-Enable-Region"
                authors="ambrahma"
                ms.author="ambrahma"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32684016"
                productPesIds="15621"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="AzureData_AzureDatabaseforMySQL"
/>
# Test ambrahma - MySql Quota Enable Region
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
	"resourceRequired": false,
	"title": "MySql-Quota",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "quotaSubType",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota Sub-type",
			"watermarkText": "Choose an option",
			"required": "true",
            "dropdownOptions": [
                {
                    "text": "Enable region",
                    "value": "enableregion"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
		},
		{
			"id": "location",
			"visibility": "quotaSubType != null && quotaSubType == enableregion",
			"order": 2,
			"controlType": "dropdown",
            "displayLabel":"REQUIRED: Please choose the region in which you want to have MySql Server",
            "watermarkText":"Choose a region",
			"required": true,
			"infoBalloonText": "Please select the region in your Azure subscription for which you want to submit quota request to enable the same.",
			"dynamicDropdownOptions": {
				"dependsOn": "quotaSubType",
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"displayName",
				"valuePropertyRegex": ".*",
				"defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            }
		},
        {
            "id": "problem_description",
			"visibility": "quotaSubType == dont_know_answer",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "required": false,
            "useAsAdditionalDetails": true
        }
	]
}
---