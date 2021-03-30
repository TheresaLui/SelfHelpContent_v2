<properties
	pageTitle="scoping-questions-for-Always Encrypted and Always Encrypted with Secure Enclaves"
	description="Scoping questions to capture more details about always encrypted and Always Encrypted with Secure Enclaves"
	authors="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32782210"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="64f06aa0-a3a0-4f5e-a201-f1bbf78555d8"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for Always Encrypted and Always Encrypted with Secure Enclaves
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Always Encrypted",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"Issue start time",
         "infoBalloonText":"Please provide the start time of the most recent occurrence of issue.",
         "required":true
      },
      {
         "id":"IssueCategory_dropdown",
         "order":2,
         "controlType":"dropdown",
         "displayLabel":"What type of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"AE",
               "text":"Always Encrypted"
            },
            {
               "value":"AESE",
               "text":"Always Encrypted with Secure Enclaves"
            },
            {
               "value":"dont_know_answer",
               "text":"Other"
            }
         ],
         "required":true
      },
      {
         "id":"IssueType_dropdown",
         "order":3,
         "visibility": "IssueType_dropdown == AESE",
         "controlType":"dropdown",
         "displayLabel":"What type of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"AESEATTURL",
               "text":"AE with Secure Enclaves using Attestation URL"
            },
            {
               "value":"dont_know_answer",
               "text":"Other"
            }
         ],
         "required":true
      },
      {
         "id":"AEServiceInformation",
         "visibility": "IssueType_dropdown == AESE",
         "order":4,
         "controlType":"multilinetextbox",
         "displayLabel":"Where is the Always Encrypted with Secure Enclaves Service running ?",
         "required":false
      },
      {
         "id":"IssueType_AEdropdown",
         "order":5,
         "visibility": "IssueType_dropdown == AE",
         "controlType":"dropdown",
         "displayLabel":"What type of issues with Always Encrypted Certificate Store?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"AESSMS",
               "text":"Using SSMS"
            },
            {
               "value":"AEADS",
               "text":"Using ADS (Azure Data Studio)"
            },
            {
               "value":"AEPWShell",
               "text":"Using PowerShell"
            },
            {
               "value":"AEPermissions",
               "text":"Removing Adimistrator permissions"
            },
            {
               "value":"dont_know_answer",
               "text":"Other"
            }
         ],
         "required":true
      },
      {
         "id":"describeissue",
         "order":6,
         "controlType":"multilinetextbox",
         "displayLabel":"Please describe the issue/error message you are facing",
         "required":false
      },
      {
         "id":"subscription_administrator",
         "order":7,
         "controlType":"dropdown",
         "displayLabel":"Do you have an administrator permission on the subscription?",
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
         "required":false
      },
      {
         "id":"server_region",
         "order":8,
         "controlType":"textbox",
         "displayLabel":"What is the Azure SQL Server region?",
         "required":false
      },
      {
         "id":"problem_description",
         "order":9,
         "controlType":"multilinetextbox",
         "displayLabel":"Additional context to help us solve your issue.",
         "required":true,
         "useAsAdditionalDetails":true,
         "watermarkText":"On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
      }
   ]
}
---
