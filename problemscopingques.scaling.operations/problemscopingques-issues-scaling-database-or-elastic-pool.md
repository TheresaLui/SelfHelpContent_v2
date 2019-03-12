<properties
	pageTitle="Issues Scaling a Database or Elastic Pool"
	description="Issues Scaling a Database or Elastic Pool"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630431"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-scalingissues"
/>

# Issues Scaling a Database or Elastic Pool
---
{
	"resourceRequired": true,
	"title": "Issues Scaling a Database or Elastic Pool",
	"fileAttachmentHint": "",
	"formElements": [
	{
			"id": "which_server",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Test A: Please select the server containing the database you need assistance with.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [],
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/servers?api-version=2015-05-01-preview",
				"jTokenPath": "serverList",
				"textProperty": "name",
				"valueProperty": "name",
				"textPropertyRegex": null
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
			"dropdownOptions": [],
			"dynamicDropdownOptions": {
				"uri":"/subscriptions/{subscriptionId}/resourceGroups/{resourceGroup}/providers/Microsoft.Sql/servers/{which_server(resourcename)}/databases?api-version=2017-10-01-preview",
				"jTokenPath": "databaseList",
				"textProperty": "name",
				"valueProperty": "id",
				"textPropertyRegex": null
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
				},{
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
				"jTokenPath": "chosenOngoingUpdateSlo",
				"textProperty": "properties.operation",
				"valueProperty": "properties.operation",
				"textPropertyRegex": ".*"
			},
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": "ongoing_or_completed_updateslo == Currently in progress"
		},
		{
			"id": "nature_of_ongoing_problem",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What problem are you facing with this scaling operation?",
			"watermarkText": "Select the nature of your problem",
			"infoBalloonText": "In what way is the selected scaling operation causing trouble?",
			"dropdownOptions": [{
					"value": "The operation is taking longer than expected",
					"text": "The operation is taking longer than expected"
				},{
					"value": "I want to cancel the operation, but can't",
					"text": "I want to cancel the operation, but can't"
				}
			],
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": "which_ongoing_update_slo != Choose an option"
		},
		{
			"id": "problem_description",
			"order": 6,
			"controltype": "multilinetextbox",
			"displayLabel": "Any additional details that might be helpful?",
			"watermarkText": "Enter any additional details here",
			"infoBalloonText": "Enter any additional details here",
			"required": true,
			"useAsAdditionalDetails": true
		},
		{
			"id": "problem_start_time",
			"order": 7,
			"controltype": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"watermarkText": "Specify when the problem started",
			"infoBalloonText": "Specify when the problem started",
			"required": true,
			"useAsAdditionalDetails": false
		}
	]
}
---
