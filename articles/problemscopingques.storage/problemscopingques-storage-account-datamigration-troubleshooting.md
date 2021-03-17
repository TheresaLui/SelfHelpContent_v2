<properties
	pageTitle="Troubleshooting migration issue"
	description="Troubleshooting migration issue"
	authors="kartikshah9"
	ms.author="kashah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743317"
	productPesIds="15629"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest,usnat,ussec"
	schemaVersion="1"
	articleId="0f76c1ac-ed33-475d-a413-5e6a7398186a"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshooting migration issue
---
{
	"$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Troubleshooting migration issue",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to troubleshoot a data migration issue?",
        "description": "Our Azure Data Migration Troubleshooter can help you troubleshoot the data migration issue for your specific scenario. Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our troubleshooter did not find any issue for your migration. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a solution."
    },
    "formElements": [
	{
		"id": "account_migration_scenario",
		"order": 1,
		"controlType": "dropdown",
		"displayLabel": "Which scenario did you have issue with",
		"dropdownOptions": [
			{
				"value": "move_account_to_new_subId",
				"text": "Move storage account to another subscription"
			},
			{
				"value": "move_account_to_new_rg",
				"text": "Move storage account to another resource group"
			},
			{
				"value": "move_account_to_new_region",
				"text": "Move storage account to another region"
			},
			{
				"value": "migrate_classic_account_to_arm",
				"text": "Migrate classic storage account to ARM"
			},
			{
				"value": "upgrade_gpv1_account_to_gpv2",
				"text": "Upgrade GPV1 storage account to GPV2"
			},
			{
				"value": "dont_know_answer",
				"text": "Don't know or not listed above"
			}
		],
		"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "storage_account_from",
		"order": 2,
		"controlType": "dropdown",
		"displayLabel": "Source storage account",
		"watermarkText": "Select the storage account to migrate",
		"dynamicDropdownOptions": {
			"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
			"jTokenPath": "value",
			"textProperty": "id",
			"valueProperty": "id",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "From a different subscription, external source or not applicable"
			}
		},
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
    },
	{
		"id": "storage_account_from_other",
		"visibility": "storage_account_from == dont_know_answer",
		"order": 3,
		"controlType": "textbox",
		"displayLabel": "Source storage account name",
		"watermarkText": "Enter storage account name",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "destination_subId",
		"visibility": "account_migration_scenario == move_account_to_new_subId",
		"order": 4,
		"controlType": "textbox",
		"displayLabel": "Destination subscription id",
		"watermarkText": "Enter the destination subscription id",
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_start_time",
		"order": 5,
		"controlType": "datetimepicker",
		"displayLabel": "Approximate start time of the most recent occurrence",
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_description",
		"order": 6,
		"controlType": "multilinetextbox",
		"displayLabel": "Details",
		"watermarkText": "Provide additional information about your issue",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
				"text": "Issue description."
			}, {
				"text": "Provide additional information about your issue"
			}
		]
	}]
}
---