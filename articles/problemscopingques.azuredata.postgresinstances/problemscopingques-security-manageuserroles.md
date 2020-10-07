<properties
	pageTitle="Security - Manage Users and Roles"
	description="Security - Manage Users and Roles"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747933"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="31f87314-8e75-441d-913c-a114612a57f4"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Security - Manage Users and Roles
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Security - Manage Users and Roles",
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
			"id": "readwrite",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What operation are you trying to do?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Create user/role",
					"text": "Create user/role"
				}, {
					"value": "Manage user/role",
					"text": "Manage user/role"
				}, {
					"value": "Propagate user/role",
					"text": "Propagate user/role"
				}, {
					"value": "Delete user/role",
					"text": "Delete user/role"
				}, {
					"value": "Set permissions",
					"text": "Set permissions"
				}, {
					"value": "Reset Postgres admin User password",
					"text": "Reset Postgres admin User password"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
