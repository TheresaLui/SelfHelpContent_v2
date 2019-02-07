<properties
	articleId="problemscopingques-scalingissues"
	pageTitle="Issues Scaling a Database or Elastic Pool"
	description="Issues Scaling a Database or Elastic Pool"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="01"
	productPesIds="02"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Issues Scaling a Database or Elastic Pool
---
{
	"resourceRequired": true,
	"title": "Issues Scaling a Database or Elastic Pool",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "which_server",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select which server contains the database you need assistance with.",
			"watermarkText": "Choose an option",
			"infoBalloonText": "This is a list of all of your associated servers.",
			"dropdownOptions": [],
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/servers?api-version=2015-05-01-preview",
				"jTokenPath": "serverList",
				"textProperty": "name",
				"valueProperty": "name",
				"textPropertyRegex": ".*"
			},
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "which_database",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Please select the database you're having trouble with:",
			"watermarkText": "Which database are you having trouble scaling?",
			"infoBalloonText": "On which database are you having difficulties with a scaling operation?",
			"dropdownOptions": [],
			"dynamicDropdownOptions": {
				"uri":/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Sql/servers/{which_server}/databases?api-version=2017-10-01-preview",
				"jTokenPath": "databaseList",
				"textProperty": "name",
				"valueProperty": "name",
				"textPropertyRegex": ".*"
			},
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "ongoing_or_completed_updateslo",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Do you need assistance with a currently in-progress scaling operation, or an operation that already completed?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "Is the scaling operation you need help with still in progress, or has it concluded?",
			"dropdownOptions": [{
					"value": "Currently in progress",
					"text": "Currently in progress"
				}, {
					"value": "Already completed",
					"text": "Already completed"
				}
			],
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": "which_database != Which database are you having trouble scaling?"
		},
		{
			"id": "which_ongoing_update_slo",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Please select which scaling operation you need assistance with.",
			"watermarkText": "Choose an option",
			"infoBalloonText": "This is a list of all of your ongoing scaling operations",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Sql/servers/{serverName}/databases/{databaseName}/operations?api-version=2017-10-01-preview",
				"jTokenPath": "JtokenPath",
				"textProperty": "textProperty",
				"valueProperty": "valueProperty",
				"textPropertyRegex": "regex"
			},
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": "ongoing_or_completed_updateslo == Currently in progress"
		}
  	]
}
---
