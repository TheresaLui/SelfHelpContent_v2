<properties
	pageTitle="scoping-questions-for-sql-security-auditing"
	description="Scoping questions to capture more details about sql security auditing issues."
	authors="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630407"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="42c59ec5-c7f6-4728-a572-56725da5834a"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for sql security auditing issues
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"sql security auditing errors related scoping questions",
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
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What type of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"auditenable",
               "text":"Enable or Create Auditing"
            },
            {
               "value":"auditconfigure",
               "text":"Save or Edit Audit configuration"
            },
            {
               "value":"auditsettings",
               "text":"Error while setting up Audit"
            },
            {
               "value":"auditalert",
               "text":"Audit Alerts related issue"
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
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What type of audit configuration for storing logs?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"auditloganalytics",
               "text":"Using Azure log Analytics for storing"
            },
            {
               "value":"auditstorageaccnt",
               "text":"Using Azure Storage Account for storing"
            },
            {
               "value":"auditeventhub",
               "text":"Using Azure Event hub for storing"
            },
            {
               "value":"auditthirdparty",
               "text":"Using Third Party apps for storing"
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
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What Method or process used for setting up auditing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue you are facing",
         "dropdownOptions":[
            {
               "value":"auditARM",
               "text":"Using ARM Templates for setting up Auditing"
            },
            {
               "value":"auditpowershell",
               "text":"Using PowerShell for setting up auditing"
            },
            {
               "value":"auditportal",
               "text":"Using Portal for setting up audiring"
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
         "id":"auditlogs",
         "order":20,
         "controlType":"textbox",
         "displayLabel":"What is the name of the Azure Storage account, log analytics or Event hub storing logs?",
         "infoBalloonText":"Enter the audit log sent to ",
         "required":false
      },
      {
         "id":"auditlog_permissions",
         "order":30,
         "controlType":"multilinetextbox",
         "displayLabel":"What are the permissions granted or available for the audit log storing location?",
         "infoBalloonText":"You can found the permissions on the 'Access control (IAM)' section in the resource blade on the Azure portal",
         "required":false
      },
      {
         "id":"auditlog_firewall",
         "order":40,
         "controlType":"dropdown",
         "displayLabel":"Does the resource storing logs have a firewall policies?",
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
         "displayLabel":"What type of permissions granted for the resource storing audit logs?",
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
         "id":"auditlog_region_server",
         "order":120,
         "visibility": "IssueType_dropdown == AEAKV ",
         "controlType":"dropdown",
         "displayLabel":"Is the Audit log stored in the same region as the Azure SQL Server?",
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
         "id":"AKV_subscription_server",
         "order":130,
         "controlType":"dropdown",
         "displayLabel":"Is the Audit log stored in the same subscription as the Azure SQL Server?",
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
         "id":"auditlog_access",
         "order":140,
         "controlType":"dropdown",
         "displayLabel":"Do you have access to the Audit logs?",
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
         "visibility": "IssueType_dropdown == auditportal",
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
