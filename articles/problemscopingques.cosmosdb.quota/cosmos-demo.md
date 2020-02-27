<properties
                pageTitle="Cosmos DB Quota"
                description="Cosmos DB Quota"
                authors="vicl"
                ms.author="vicl"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32447244"
                productPesIds="15621"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="vicl-cosmosdb-demo"
/>
# Test VICL - Cosmos DB
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
	"resourceRequired": false,
	"title": "Cosmos DB Quota VICL",
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
                    "text": "Max throughput on container",
                    "value": "maxtp"
                },
                {
                    "text": "Max Accounts per subscription",
                    "value": "maxaccts"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
		},
		{
			"id": "accountName",
			"visibility": "quotaSubType != null && quotaSubType == maxtp",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Account Name",
			"required": false,
			"dynamicDropdownOptions": {
				"dependsOn": "quotaSubType",
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.DocumentDB/databaseAccounts?api-version=2015-04-08",
                "jTokenPath": "value",
                "textProperty": "name,location",
                "textTemplate": "Name:{name}, Region:{location}",
                "valueProperty": "id",
				"valuePropertyRegex": "^*$",
				"defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            }
		},
		{
			"id": "database",
			"visibility": "accountName != null && accountName != dont_know_answer",
			"order": 3,
			"displayLabel": "Database",
			"controlType": "dropdown",
			"required": false,
			"dynamicDropdownOptions": {
				"dependsOn": "accountName",
                "uri": "{replaceWithParentValue}/apis/sql/databases?api-version=2015-04-08",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
				"valuePropertyRegex": "^*$",
				"defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            }
		},
		{
			"id": "container",
			"visibility": "database != null && database != dont_know_answer",
			"order": 4,
			"displayLabel": "Container",
			"controlType": "dropdown",
			"required": false,
			"dynamicDropdownOptions": {
				"dependsOn": "database",
                "uri": "{replaceWithParentValue}/containers?api-version=2015-04-08",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
				"valuePropertyRegex": "^*$",
				"defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            }
		},
		{
			"id": "currquota",
			"visibility": "container != null && container != dont_know_answer",
			"order": 5,
			"controlType": "textblock",
			"displayLabel": "Current Quota (RU/s)",
			"required": false,
			"dynamicTextBlockOptions": {
				"dependsOn": "container",
                "uri": "{replaceWithParentValue}/settings/throughput?api-version=2015-04-08",
                "jTokenPath": "properties",
                "textProperty": "minimumThroughput",
				"valuePropertyRegex": "^*$"
            }
		},
		{
			"id": "newquota",
			"visibility": "currquota != null && accountName != dont_know_answer && database != dont_know_answer && container != dont_know_answer",
			"order": 6,
			"controlType": "numerictextbox",
			"displayLabel": "New Quota Limit (RU/s)",
			"required": false,
			"validations": [
				{
					"type": "GreaterThan",
					"controlId": "currquota"
				},
				{
					"type": "RegExMatch",
					"value": "^[^.]*$",
					"text": "Integers only."
				}
			]
		},
		{
			"id": "newacctquota",
			"visibility": "quotaSubType != null && quotaSubType == maxaccts",
			"order": 7,
			"controlType": "numerictextbox",
			"displayLabel": "New Quota Limit",
			"required": false,
			"validations": [
				{
					"type": "GreaterThan",
					"value": 0
				},
				{
					"type": "LessThan",
					"value": 1000
				},
				{
					"type": "RegExMatch",
					"value": "^[^.]*$",
					"text": "Integers only."
				}
			]
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