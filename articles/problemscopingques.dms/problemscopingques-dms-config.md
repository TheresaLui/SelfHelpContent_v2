<properties
	articleId="0C42E85E-E838-4C5F-A4F3-4843C79D0A9E"
	pageTitle="DMS Migration Error - scoping questions"
	description="Scoping questions to capture migration error details"
	authors="radjaram"
	authoralias="rradjou"
	ms.author="radjaram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743195,32743201,32743207,32743213,32743196,32743202,32743208,32743214,32743197,32743203,32743209,32743215,32743198,32743204,32743210,32743216,32743199,32743205,32743211,32743217,32743200,32743206,32743212,32743218"
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>
# Failure when running a database migration using DMS
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "DMS Migration Issue Description",
	"fileAttachmentHint": "",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },{
			"id": "sourcetype_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Where is your source server hosted?",
			"watermarkText": "Select type of your source server",
			"infoBalloonText": "If your source type is not in the list, choose Other",
			"dropdownOptions": [
				{
					"value": "On-Premise",
					"text": "On-Premise"
				},{
					"value": "Azure-VM",
					"text": "Azure VM"
				},{
					"value": "AWS",
					"text": "AWS"
				},{
					"value": "dont_know_answer",
					"text": "Other"
				}
			],
			"required": true
		},{
			"id":"SourceServer",
			"order":100,
			"controlType":"multilinetextbox",
			"displayLabel":"Please provide exact string used in the source server-name fields in the project/task creation",
			"required":false,
			"watermarkText":"This is needed to validate if there is a formatting issue in the IP address or FQDN in the configuration"
		},{
			"id":"problem_description",
			"order":1000,
			"controlType":"multilinetextbox",
			"displayLabel":"Please provide additional context for the error message you are encountering.",
			"required":true,
			"useAsAdditionalDetails":true,
			"watermarkText":"Please provide the detailed symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information"
		}
	]
}
---

