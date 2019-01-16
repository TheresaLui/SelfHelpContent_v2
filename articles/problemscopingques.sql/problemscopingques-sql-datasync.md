<properties
	articleId="problemscopingques-sql-datasync"
	pageTitle="SQL Data Sync"
	description="Scoping questions to capture sync group name"
	authors="vitomaz-msft"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630455"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
/>
# SQL Data Sync
---
{
	"resourceRequired": true,
	"title": "SQL Data Sync",
	"fileAttachmentHint": "",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },{
			"id": "sync_group_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Sync group name?",
            "watermarkText": "Sync group name",
            "infoBalloonText": "Name of the Sync Group facing the issue (if applicable)",
			"required": false,
			"useAsAdditionalDetails": false
		},{
			"id": "sync_group_name2",
			"order": 3,
			"controlType": "dropdown",
            "displayLabel": "Please select the sync group you are experiencing issues with",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "{resourceInstanceId}/syncGroups?api-version=2015-05-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "syncDatabaseId",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of sync groups",
                    "text": "Unable to get the list of sync groups"
                }
            ],
            "required": false
		},{
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	]
}
---