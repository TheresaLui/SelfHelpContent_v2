<properties
	pageTitle="Errors when connecting to SQL MIAA instance"
	description="Errors when connecting to SQL MIAA instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743975"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="A087FFEA-D890-4AE4-BBB4-D47B3FFE63F7"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Errors when connecting to SQL MIAA instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "SQL Server - Azure Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "connection_source",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is the source of the connection?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "locally on the same node",
					"text": "locally on the same node"
				}, {
					"value": "on the same network",
					"text": "on the same network"
				}, {
					"value": "external network",
					"text": "external network"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "connection_endpoint",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What connection endpoint are you trying to use?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "external endpoint",
					"text": "external endpoint"
				}, {
					"value": "cluster endpoint",
					"text": "cluster endpoint"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "command_output",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide the output the following command:\n Use 'azdata arc sql mi list'",
			"required": false
		}, {
			"id": "error_message",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "What is the specific error message did you receive?",
			"required": false
		}, {
			"id": "issue_frequency",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Is the connectivity issue consistent or intermittent?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "consistent",
					"text": "consistent"
				}, {
					"value": "intermittent",
					"text": "intermittent"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
