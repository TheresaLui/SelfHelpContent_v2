<properties
	pageTitle="CycleCloud issues in general"
	description="CycleCloud issues in general"
	ms.author="cargonz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745218,32745226,32745225,32745224,32745223,32745222,32745228,32745221,32745220,32745219"
	productPesIds="16478"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-general"
	ownershipId="Compute_AzureCycleCloud"
/>
# Useful Title
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
	"title": "CycleCloud issues in general",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "CycleCloud_version",
			"order": 1,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "What version of CycleCloud are you using?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "8.1",
					"text": "8.1"
				}, {
					"value": "8.0",
					"text": "8.0"
				}, {
					"value": "7.9",
					"text": "7.9"
				}, {
					"value": "7.8",
					"text": "7.8"
				}, {
					"value": "7.7",
					"text": "7.7"
				}, {
					"value": "7.6",
					"text": "7.6"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		}, {
			"id": "scheduler_selected",
			"order": 2,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "What scheduler have you selected?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "SLURM",
					"text": "SLURM"
				}, {
					"value": "PBS",
					"text": "PBS"
				}, {
					"value": "GridEngine",
					"text": "GridEngine"
				}, {
					"value": "LSF",
					"text": "LSF"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		}, {
			"id": "image_info",
			"order": 3,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Are you using a custom image or a platform image?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "custom_image",
					"text": "Using a custom image"
				}, {
					"value": "platform_image",
					"text": "Using a platform image"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		},
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
        "id": "problem_description",
        "order": 5,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "useAsAdditionalDetails": true,
        "required": true
    }
	]
}
---
