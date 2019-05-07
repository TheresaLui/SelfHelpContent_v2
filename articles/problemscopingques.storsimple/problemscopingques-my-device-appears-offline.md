<properties
	articleId="75ad0b3e-9e52-4741-8f51-990cd5049a21"
	pageTitle="Scoping my device appears offline"
	description="My device appears offline Scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630504"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# My Device appears offline on the portal
---
{
	"resourceRequired": true,
	"title": "My device appears offline",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "changes_updates",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Were there any changes/updates made on the network?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		}, {
			"id": "url_requirement",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Is URL "https://login.windows.net" for public cloud or "https://login.microsoftonline.us" for US Government cloud whitelisted in the firewall?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},{
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Include output."
				}, {
					"text": "Output of "invoke-hcsdiagnostics -scope network" will assist in troubleshooting the issue."
				}
			]
		},
	]
}
---
