<properties
	pageTitle="scoping-questions-for-sql-security-threatdetection"
	description="Scoping questions to capture more details about sql security threat detection issues."
	authors="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630457"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="0b4b3711-806d-4b40-96ea-dff92d82220f"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for sql security threat detection issues
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"sql security threat detection errors related scoping questions",
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
         "id":"IssueType_dropdown",
         "order":2,
         "controlType":"dropdown",
         "displayLabel":"What type of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"sqlinjection",
               "text":"SQL Injection notification or alert"
            },
            {
               "value":"unusuallocation",
               "text":"Access from Unusual location or data center notification or alert"
            },
            {
               "value":"unfamiliar",
               "text":"Access from unfamiliar principal or potentially harmful application alert"
            },
            {
               "value":"bruteforce",
               "text":"Brute force SQL credentials notification or alert"
            },
            {
               "value":"dont_know_answer",
               "text":"Other"
            }
         ],
         "required":true
      },
      {
         "id":"settings_dropdown",
         "order":4,
         "controlType":"dropdown",
         "displayLabel":"What Method or process used for setting up permissions and access control?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"threatARM",
               "text":"Using ARM Templates for setting up permissions or access"
            },
            {
               "value":"threatpowershell",
               "text":"Using PowerShell for setting up permissions or access"
            },
            {
               "value":"threattportal",
               "text":"Using Portal for setting up permissions or access"
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
         "order":11,
         "controlType":"multilinetextbox",
         "displayLabel":"Please describe the issue/error message you are encountering",
         "required":false
      },
      {
         "id":"resource_firewall",
         "order":40,
         "controlType":"dropdown",
         "displayLabel":"Does the resource notified having any firewal policy enabled?",
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
         "id":"subscription_administrator",
         "order":80,
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
         "id":"server_permissions",
         "order":90,
         "controlType":"multilinetextbox",
         "displayLabel":"What type of permissions granted for the resource at server level?",
         "required":false
      },
       {
         "id":"server_region",
         "order":100,
         "controlType":"textbox",
         "displayLabel":"What is the Azure SQL Server egion?",
         "required":false
      },
    {
         "id":"subscription_move",
         "order":160,
         "controlType":"dropdown",
         "displayLabel":"Was the Azure SQL Server moved from another subscription or did the subscription moved to another tenant?",
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
         "id":"browser",
         "order":170,
         "visibility": "IssueType_dropdown == threattportal",
         "controlType":"dropdown",
         "displayLabel":"If the issue only happen in Azure portal, what is the browser being used?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"chrome",
               "text":"Google Chrome"
            },
            {
               "value":"edge",
               "text":"Microsoft Edge"
            },
            {
               "value":"firefox",
               "text":"Firefox"
            },
            {
               "value":"other",
               "text":"Other"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
            }
         ],
         "required":false
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
