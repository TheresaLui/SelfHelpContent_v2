<properties
	pageTitle="Restore a database"
	description="Scoping questions to capture more details about errors encountered while trying to restore a db on SQL DB"
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688668"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-backuprestore-restore-database"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>
# scoping questions to restore a database
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
	{
            "id": "IssueType_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What kind of restore is having issues?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the restore type associated with the issue",
			"dropdownOptions": [
                {
                    "value": "PitR",
                    "text": "Point in time restore (PitR)"
                },
                {
                    "value": "GeoRestore",
                    "text": "Geo-Restore"
                },
                {
                    "value": "BACPAC",
                    "text": "Import BACPAC"
                },
                {
                    "value": "DropDB",
                    "text": "Restore Drop Server or DB"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
        },
	{
            "id": "original_db_name",
            "order": 3,
            "controlType": "textbox",
	        "visibility": "IssueType_dropdown == PitR",
            "displayLabel": "What is the name of the original DB?",
            "infoBalloonText": "Enter the original Azure SQL DB name",
            "required": false
        },
	{
            "id": "pitr_time",
            "order": 4,
            "controlType": "datetimepicker",
	        "visibility": "IssueType_dropdown == PitR",
            "displayLabel": "What was the requested restore datetime?",
            "infoBalloonText": "Enter the approximate time that you want the point in time restore for",
            "required": true
        },
	{
            "id": "georestore_server",
            "order": 5,
            "controlType": "textbox",
	        "visibility": "IssueType_dropdown == GeoRestore",
            "displayLabel": "What is the target server?",
            "infoBalloonText": "Enter the target server name where you want to geo-restore.",
            "required": false
        },
    {
            "id": "servicetier_dropdown",
            "order": 6,
            "controlType": "dropdown",
			"visibility": "IssueType_dropdown == GeoRestore",
            "displayLabel": "What is the target service tier",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select the target service tier",
			"dropdownOptions": [
                {
                    "value": "Basic",
                    "text": "Basic"
                },
                {
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "Premium",
		    "text": "Premium"
                },
                {
                    "value": "vCore General Purpose",
                    "text": "vCore General Purpose"
                },
                {
                    "value": "vCore Business Critical",
                    "text": "vCore Business Critical"
                },
                {
                    "value": "Hyperscale",
                    "text": "Hyperscale"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Dont know answer"
                }
            ],
            "required": true
        },
	{
            "id": "platform_type",
            "order": 7,
            "controlType": "dropdown",
	    "visibility": "IssueType_dropdown == BACPAC",
            "displayLabel": "What tool/method are you using to import?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select one of the following",
			"dropdownOptions": [
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
 		{
                    "value": "From blob storage via portal",
                    "text": "From blob storage via portal"
                },
		{
                    "value": "Sql Package",
                    "text": "Sql Package"
                },
                {
                    "value": "BACPAC file using PowerShell",
                    "text": "BACPAC file using PowerShell"
                },
               	{
                    "value": "dont_know_answer",
                    "text": "Dont know answer"
                }
            ],
            "required": true
        },
	{
            "id": "version_details",
            "order": 8,
            "controlType": "textbox",
	    "visibility": "platform_type == SSMS || platform_type == Sql Package",
            "displayLabel": "Please provide the version details",
            "required": false
        },
	{
            "id": "resource_type_dropdown",
            "order": 9,
            "controlType": "dropdown",
	    "visibility": "IssueType_dropdown == DropDB",
            "displayLabel": "What do you want to restore?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select from the following",
			"dropdownOptions": [
                {
                    "value": "resource group",
                    "text": "resource group"
                },
                {
                    "value": "server",
                    "text": "server"
                },
				{
                    "value": "db",
                    "text": "Database"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Dont know the answer"
                }
            ],
            "required": true
        },
	{
            "id": "target_resourcegroup_name",
     	    "order": 10,
            "visibility": "resource_type_dropdown == resource group",
            "controlType": "textbox",
            "displayLabel": "What is the resource group that was deleted?",
            "infoBalloonText": "Enter the name of the resource group that was deleted and you want to restore.",
            "required": false
        },
    {
            "id": "target_server_name",
     	    "order": 11,
            "visibility": "resource_type_dropdown == server",
            "controlType": "textbox",
            "displayLabel": "What is the server that was deleted?",
            "infoBalloonText": "Enter the name of the server that was deleted and you want to restore.",
            "required": false
        },
	{
            "id": "target_db_name",
     	    "order": 12,
            "visibility": "resource_type_dropdown == db",
            "controlType": "textbox",
            "displayLabel": "What was the database that was deleted?",
            "infoBalloonText": "Enter the name of the database that was deleted and you want to restore.",
            "required": false
        },
    {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error you are receiving. If available,please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
