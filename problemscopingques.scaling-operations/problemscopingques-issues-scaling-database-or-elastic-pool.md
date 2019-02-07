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
		}
  	]
}
---
