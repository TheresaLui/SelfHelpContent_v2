<properties
         pageTitle="Scoping questions for SAP HANA backup performance"
         description="Scoping questions for SAP HANA backup performance"
         authors="akanase-ot"
         ms.author="akkanase"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32690766"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="f2bf8fdc-5f56-486d-9f2a-8770371e3d8d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Scoping questions for SAP Hana backup performance
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "SAP HANA backup performance",
	"fileAttachmentHint": "",
	"diagnosticCard": {
		"title": "SAP HANA backup performance",
		"description": "These diagnostics will check for errors.",
		"insightNotAvailableText": "We didn't find any problems"
	},
	"formElements": [{
			"id": "machine_name",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Which machine is experiencing the problem?",
			"watermarkText": "Select the virtual machine running SAP HANA",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
				"jTokenPath": "value",
				"textProperty": "name",
				"valueProperty": "id",
				"textPropertyRegex": ".*",
				"defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "Other or none of the above"
				}
			},
			"required": false
		},
		{
			"id": "database_Name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Provide the name(s) of the databases whose backup is slow?",
			"watermarkText": "Enter database name(s) comma separated",
			"required": false
		},
		{
			"id": "backup_Type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which backup is taking longer than expected?",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Full backup",
					"text": "Full backup"
				},
				{
					"value": "Log backup",
					"text": "Log backup"
				},
				{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": false,
			"diagnosticInputRequiredClients": "Portal"
		},
		{
			"id": "jobID_Name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Enter the long running job activity ID:",
			"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
			"required": false
		},
		{
			"id": "job_Running_Time",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Since how long the job is running?",
			"watermarkText": "Enter time in hours ex. 18hrs",
			"required": false
		},
		{
			"id": "problem_start_time",
			"order": 6,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 7,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Additional details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"hints": []
		}
	],
	"$schema": "SelfHelpContent"
}
---
