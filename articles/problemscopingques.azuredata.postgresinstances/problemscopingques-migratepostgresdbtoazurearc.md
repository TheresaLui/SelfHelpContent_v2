<properties
	pageTitle="Migrate a Postgres database into Arc"
	description="Migrate a Postgres database into Arc"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747910"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="cdb6b80c-15f1-4d1d-bd1e-a41c896106db"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Migrate a Postgres database into Arc
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Migrate a Postgres database into Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "error_message",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "If an error was displayed, what was the error message?",
            "required": false
		}, {
			"id": "migration_methodology",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What methodology are you using to migrate data into Arc?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Backup/restore",
					"text": "Backup/restore"
				}, {
					"value": "Replication",
					"text": "Replication"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "postgres_version",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "What version of Postgres are you trying to migrate from?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "11",
					"text": "11"
				}, {
					"value": "12",
					"text": "12"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "system_host",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What system hosts the database you are trying to migrate from? (On-Premises, Other Cloud vendor)",
            "required": false
		}, {
			"id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
