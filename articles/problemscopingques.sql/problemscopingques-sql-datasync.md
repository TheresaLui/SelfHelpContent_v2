<properties
	articleId="problemscopingques-sql-datasync"
	pageTitle="SQL Data Sync"
	description="Scoping questions to capture sync group name"
	authors="vitomaz-msft"
	authoralias="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32574329"
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
            "id": "problem_start_time", //This is a required value
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
            "id": "problem_description", //This is a required value
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