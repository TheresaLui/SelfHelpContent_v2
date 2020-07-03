<properties
	articleId="problemscopingques-sqlmi-migrating-to-azure-dms"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture dms issues"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637255"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":false,
   "subscriptionRequired":false,
   "title":"Database Migration Service (DMS)",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"When did the problem start?",
         "required":true
      },
      {
         "id":"issue_type",
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What kind of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue",
         "dropdownOptions":[
            {
               "value":"advisory",
               "text":"Advisory or questions"
            },
            {
               "value":"provision",
               "text":"Provisioning the DMS resource"
            },
            {
               "value":"managing",
               "text":"Managing DMS projects (creating, updating or deleting)"
            },
            {
               "value":"migrating",
               "text":"Running a DMS project"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer, another kind of issue"
            }
         ],
         "required":true
      },
      {
         "id":"problem_description",
         "order":99,
         "controlType":"multilinetextbox",
         "useAsAdditionalDetails":true,
         "displayLabel":"Details of the issue.",
         "watermarkText":"Please provide additional context for the error message you are encountering",
         "required":true
      }
   ]
}
---
