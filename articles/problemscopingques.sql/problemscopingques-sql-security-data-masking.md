<properties
	pageTitle="Scoping questions for Data Masking and related issues"
	description="Scoping questions to capture more details about Data Masking issues."
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630417"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-security-data-masking"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for Data Masking Errors
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Data Masking errors related scoping questions",
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
               "text":"Questions about Data Masking"
            },
            {
               "value":"cud_operations",
               "text":"Create, alter or drop data masked columns"
            },
            {
               "value":"permissions",
               "text":"Grant or Remove permissions to view masked data"
            },
            {
               "value":"view",
               "text":"User can view masked data when he shouldn't or vice-versa"
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
         "visibility": "issuetype_dropdown == cud_operations && issuetype_dropdown == permissions",
         "displayLabel":"What are the user permissions?",
         "required":false
      },
      {
         "id":"interface_used",
         "order":30,
         "controlType":"multiselectdropdown",
         "visibility": "issuetype_dropdown == cud_operations && issuetype_dropdown == permissions",
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
         "id":"mask_function",
         "order":40,
         "controlType":"dropdown",
         "visibility": "issuetype_dropdown == cud_operations",
         "displayLabel":"What was the masking function being used?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"default",
               "text":"Default"
            },
            {
               "value":"credit",
               "text":"Credit Card"
            },
            {
               "value":"email",
               "text":"Email"
            },
	          {
               "value":"random",
               "text":"Random Number"
            },
            {
               "value":"custom",
               "text":"Custom text"
            },
	          {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
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
