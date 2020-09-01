<properties
	pageTitle="Scoping questions for vNet endpoints and related issues"
	description="Scoping questions to capture more details about vNet endpoints issue."
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636832"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-security-vnet-service-endpoints"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for vNet endpoints Errors
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"vNet endpoints errors related scoping questions",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"Unavailability start time",
         "infoBalloonText":"Please provide the start time of the most recent occurrence of unavailability.",
         "required":true
      },
      {
         "id":"IssueType_dropdown",
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What kind of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"create",
               "text":"Create a new vNet Endpoint rule"
            },
            {
               "value":"update",
               "text":"Update an existing vNet Endpoint rule"
            },
            {
               "value":"delete",
               "text":"Delete a vNet Endpoint rule"
            },
	    {
               "value":"dont_know_answer",
               "text":"Don't know the answer or another type of issue"
            }
         ],
         "required":true
      },
      {
         "id":"vnet_subnet_name",
         "order":20,
         "controlType":"textbox",
         "displayLabel":"What is the name of the vNet and subnet associated with the vNet endpoint rule?",
         "infoBalloonText":"Enter the vNet and subnet name",
         "required":true
      },
      {
         "id":"tracking_id",
         "order":30,
         "controlType":"textbox",
         "displayLabel":"Do you have the tracking id or request id associated with the issue?",
         "required":false
      },
      {
         "id":"sql_endpoint_dropdown",
         "order":40,
         "controlType":"dropdown",
         "displayLabel":"Does the vNet subnet have the service endpoint Microsoft.Sql enabled?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"yes",
               "text":"Yes"
            },
            {
               "value":"no",
               "text":"No"
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
