<properties
	pageTitle="Export from SQL DB to BACPAC"
	description="Scoping questions to capture more details about errors\issues encountered while trying Export from SQL DB to BACPAC"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630420"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problem-scopingques-sql-bacpacdatasynccopydbreplication-exportfromsqldbtobacpac-db"
	ownershipId="AzureData_AzureSQLDB_ImportExport"
/>
# Export from SQL DB to BACPAC
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
            "displayLabel": "What tool or method are you using to export?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select one of the following",
			"dropdownOptions": [
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
 		{
                    "value": "Sql package",
                    "text": "Sql package"
                },
		{
                    "value": "SQL DB Export Service",
                    "text": "SQL DB Export Service"
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
	    "visibility": "platform_type == SSMS || platform_type == Sql package ",
            "controlType": "textbox",
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
