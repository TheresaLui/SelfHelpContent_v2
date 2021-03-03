<properties
	pageTitle="Scoping questions for Data Discovery and Classification and related issues"
	description="Scoping questions to capture more details about Data Discovery and Classification issues."
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630416"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-security-data-discovery"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for Data Discovery and Classification Errors
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Data Discovery and Classification errors related scoping questions",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"When did you face the issue",
         "required":true
      },
      {
         "id":"issuetype_dropdown",
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What kind of support is being requested?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"questions",
               "text":"Questions about Data Discovery and Classification"
            },
            {
               "value":"failing",
               "text":"Data Discovery failing to run"
            },
            {
               "value":"view",
               "text":"Not able to view or export data"
            },
	          {
               "value":"recommendations",
               "text":"Not able to accept or dismiss recommendations"
            },
            {
               "value":"manual",
               "text":"Not able to do manual classifications"
            },
            {
               "value":"config",
               "text":"Not able to configure Advanced Data Security"
            },
            {
               "value":"permissions",
               "text":"Don't have permissions"
            },
	          {
               "value":"dont_know_answer",
               "text":"Don't know the answer or another type of issue"
            }
         ],
         "required":true
      },
      {
         "id":"permissions",
         "order":20,
         "controlType":"multilinetextbox",
         "visibility": "issuetype_dropdown == permissions",
         "displayLabel":"What are the user permissions?",
         "required":false
      },
      {
         "id":"interface_used",
         "order":30,
         "controlType":"multiselectdropdown",
         "displayLabel":"What was the interface(s) used?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"portal",
               "text":"Azure Portal"
            },
            {
               "value":"tsql",
               "text":"T-Sql"
            },
            {
               "value":"rest",
               "text":"REST API"
            },
	          {
               "value":"ps",
               "text":"PowerShell"
            },
	          {
               "value":"dont_know_answer",
               "text":"Don't know the answer or another interface"
            }
         ],
         "required":true
      },
      {
         "id":"problem_description",
         "order":999,
         "controlType":"multilinetextbox",
         "displayLabel":"Additional context to help us solve your issue.",
         "required":true,
         "useAsAdditionalDetails":true,
         "watermarkText":"On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
      }
   ]
}
---
