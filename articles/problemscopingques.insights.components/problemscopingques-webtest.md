<properties
	articleId="problemscopingques-webtest"
	pageTitle="Availability Test"
	description="Availability Test"
	authors="debugthings"
	authoralias="jamdavi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32422336"
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Metrics Alert (Classic)
---
{
	"resourceRequired": true,
	"title": "Availability Tests",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "classic_alert_id",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the affected Availability Tests resource name.",
			"watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.insights/components/{resourcename}/webtests?noLargeObjects=true&skipConfig=true&api-version=2015-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
			"dropdownOptions": [{
					"value": "Unable to get the list of availability tests for this resource",
					"text": "Unable to get the list of availability tests for this resource"
				}],
			"required": false
		}, {
			"id": "availability_test_reason",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is the primary issue with this availability test?",
			"dropdownOptions": [
				{
					"value": "Automation: Issues with REST API or Azure command line interface (CLI)",
					"text": "Automation: Issues with REST API or Azure command line interface (CLI)"
				}, {
					"value": "Configuration: Creating, editing or deleting availability tests",
					"text": "Configuration: Creating, editing or deleting availability tests"
				}, {
					"value": "Configuration: Issues with Azure resource manager (ARM) templates",
					"text": "Configuration: Issues with Azure resource manager (ARM) templates"
				}, {
					"value": "Detection: Availability test consistently shows error across one or more specific regions",
					"text": "Detection: Availability test consistently shows error across one or more specific regions"
				}, {
					"value": "Detection: Availability test shows exception message in results",
					"text": "Detection: Availability test shows exception message in results"
				}, {
					"value": "General: Cannot view or find availability test",
					"text": "General: Cannot view or find availability test"
				}, {
					"value": "General: Other issues",
					"text": "General: Other issues"
				}],
			"required": true
		}, {
			"id": "affected_region",
			"order": 3,
			"controlType": "multiselectdropdown",
			"visibility": "availability_test_reason == Detection: Availability test consistently shows error across one or more specific regions",
			"displayLabel": "Please select the region(s) showing the error.",
			"dropdownOptions": [
				{
					"value": "Australia East",
					"text": "Australia East"
				}, {
					"value": "Brazil South",
					"text": "Brazil South"
				}, {
					"value": "Central US",
					"text": "Central US"
				}, {
					"value": "East Asia",
					"text": "East Asia"
				}, {
					"value": "East US",
					"text": "East US"
				}, {
					"value": "France Central",
					"text": "France Central"
				}, {
					"value": "France South",
					"text": "France South"
				}, {
					"value": "Japan East",
					"text": "Japan East"
				}, {
					"value": "North Central US",
					"text": "North Central US"
				}, {
					"value": "North Europe",
					"text": "North Europe"
				}, {
					"value": "South Central US",
					"text": "South Central US"
				}, {
					"value": "Southeast Asia",
					"text": "Southeast Asia"
				}, {
					"value": "UK South",
					"text": "UK South"
				}, {
					"value": "UK West",
					"text": "UK West"
				}, {
					"value": "West Europe",
					"text": "West Europe"
				}, {
					"value": "West US",
					"text": "West US"
				}
			],
			"required": true
		},{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": true,
			"watermarkText": "Please provide: a detailed scenario of the error condition, troubleshooting done so far, log files, timestamp, screenshots and any other relevant information.",
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Expected behavior, actual behavior"
				}, {
					"text": "Troubleshooting done so far"
				}, {
					"text": "Log Files, downloaded webtest results"
				}, {
					"text": "Timestamps"
				}, {
					"text": "Screenshots"
				}
			]
		}
	]
}
---