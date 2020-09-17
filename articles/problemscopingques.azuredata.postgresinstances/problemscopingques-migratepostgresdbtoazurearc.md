<properties
	pageTitle="Migrate a Postgres database into Arc"
	description="Migrate a Postgres database into Arc"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747910"
	productPesIds="17124"
	cloudEnvironments="Public"
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
			"id": "objective",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What are you trying to achieve?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Migrate data into your Azure Arc enabled Postgres Hyperscale server group",
					"text": "Migrate data into your Azure Arc enabled Postgres Hyperscale server group"
				}, {
					"value": "Optimize Azure Arc enabled Postgres Hyperscale after getting data in it",
					"text": "Optimize Azure Arc enabled Postgres Hyperscale after getting data in it"
				}, {
					"value": "Other",
					"text": "Other"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "migration_methodology",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "What methodology are you using to migrate data into Arc?",
			"required": false
		}, {
			"id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
