<properties
	articleId="17F42952-E710-4EF4-897C-0FC07D8A9BFB"
	pageTitle="DMS service management issue - scoping questions"
	description="Scoping questions to capture migration error details"
	authors="radjaram"
	authoralias="rradjou"
	ms.author="radjaram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743193,32743194,32743219,32743220,32743221,32743222"
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>
# DMS service management issue
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "DMS Service Managemement Issue Description",
	"fileAttachmentHint": "",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },{
			"id": "sourtype_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Does the Vnet used to setup DMS allow outbound connection through port 443",
			"watermarkText": "Validating connectivity to Azure telemetry endpoint",
			"infoBalloonText": "<a href='https://docs.microsoft.com/en-us/azure/api-management/api-management-using-with-vnet#-common-network-configuration-issues'>See Azure Telemetry endpoints documented here.<a> ",
			"dropdownOptions": [
				{
					"value": "Yes",
					"text": "Yes"
				},{
					"value": "No",
					"text": "No"
				}
			],
			"required": true
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

