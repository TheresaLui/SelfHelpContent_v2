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
         "id":"dms_region",
         "order":20,
         "controlType":"textbox",
         "visibility":"issue_type == provision",
         "displayLabel":"In what Azure region are you trying to provision DMS?",
         "required":false
      },
      {
         "id":"service_mode",
         "order":21,
         "controlType":"dropdown",
         "visibility":"issue_type == provision",
         "displayLabel":"What is the service mode being selected?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"azure",
               "text":"Azure"
            },
            {
               "value":"hybrid",
               "text":"Hybrid"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer, any of them"
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
