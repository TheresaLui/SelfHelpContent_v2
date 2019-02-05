<properties
	pageTitle="Issues Scaling a Database or Elastic Pool"
	description="Issues Scaling a Database or Elastic Pool"
	authors="Johirsch"
	ms.author="Johirsch"
	supportTopicIds="32630431"
	productPesIds="13491"
	selfHelpType="problemScopingQuestions"
	articleId="problemscopingques-scalingissues"
	cloudEnvironments="public"
	schemaVersion=1
/>

#Issues Scaling a Database or Elastic Pool

{
	"resourceRequired": true,
	"title": "Issues Scaling a Database or Elastic Pool"
	"formElements": [{
			"id": "server_name_entry",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Enter server name:",
			"watermarkText": "Which server are you having trouble with?",
			"infoBalloonText": "On which server are you having difficulties scaling a database?",
			"required": true,
			"useAsAdditionalDetails": false
		},
		{
			"id": "database_name_entry",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Enter database name:",
			"watermarkText": "Which database are you having trouble scaling?",
			"infoBalloonText": "On which database are you having difficulties with a scaling operation?",
			"required": true,
			"useAsAdditionalDetails": false
		},
		{
			"id": "ongoing_or_completed_updateslo",
			"order": 3,
			"controlType": "dropdownOptions",
			"displayLabel": "Do you need assistance with a currently in-progress scaling operation, or an operation that already completed?",
			"watermarktext": "Choose an option",
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
			"visibility": "server_name_entry != Which server are you having trouble with? && database_name_entry != Which database are you having trouble scaling?"
		},
		{
			"id": "which_ongoing_update_slo",
			"order": 4,
			"controlType": "dropdownOptions",
			"displayLabel": "Please select which scaling operation you need assistance with."
			"watermarktext": "Choose an option",
			"infoBalloonText": "This is a list of all of your ongoing scaling operations"
			"dropdownOptions": []
			"dynamicDropdownOptions": {
				"uri": "",
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
