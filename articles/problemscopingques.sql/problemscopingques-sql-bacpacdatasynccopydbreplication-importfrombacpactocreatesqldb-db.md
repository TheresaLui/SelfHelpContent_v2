<properties
	pageTitle="Import from BACPAC to create SQL DB"
	description="Scoping questions to capture more details about errors\issues encountered while trying Import from BACPAC to create SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630430"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-bacpacdatasynccopydbreplication-importfrombacpactocreatesqldb-db"
	ownershipId="AzureData_AzureSQLDB_ImportExport"
/>
# Import from BACPAC to create SQL DB
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
            "id": "platform_type",
            "order": 4,
            "controlType": "dropdown",
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
            "order": 5,
            "controlType": "textbox",
	    "visibility": "platform_type == SSMS || platform_type == Sql Package",
            "displayLabel": "Please provide the version details",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
