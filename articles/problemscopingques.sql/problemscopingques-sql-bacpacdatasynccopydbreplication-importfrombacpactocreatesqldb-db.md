<properties
	pageTitle="Import from BACPAC to create SQL DB"
	description="Scoping questions to capture more details about errors\issues encountered while trying Import from BACPAC to create SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630430"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="problemscopingques-sql-bacpacdatasynccopydbreplication-importfrombacpactocreatesqldb-db"
/>
# Import from BACPAC to create SQL DB
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
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
            "displayLabel": "What is this pertaining to?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select one of the following",
			"dropdownOptions": [
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
                {
                    "value": "SSDT",
                    "text": "SSDT"
                },
 		{
                    "value": "Sql Package",
                    "text": "Sql Package"
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
            "watermarkText": "Please provide the full error that you seeing or explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
