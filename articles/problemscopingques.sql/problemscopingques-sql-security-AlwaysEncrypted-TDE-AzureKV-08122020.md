<properties
	pageTitle="Scoping questions for Always Encrypted, TDE and Azure Key Vault"
	description="Scoping questions to capture more details aboutAlways Encrypted, TDE and Azure Key Vault issue."
	authors="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630405"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="4c2f22d0-06a1-44c7-85f5-297b5c6291ee"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for Always Encrypted, TDE and Azure Key Vault Errors
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Always Encrypted, TDE and Azure Key Vault errors related scoping questions",
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
               "value":"AECERTStore",
               "text":"Always Encrypted with Certificate Store"
            },
            {
               "value":"AEAKV",
               "text":"Always Encrypted with Azure Key Vault"
            },
            {
               "value":"TDE",
               "text":"Transparent Data Encryption"
            },
            {
               "value":"TDEBYOK",
               "text":"TDE with Bring Your Own Key"
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
         "id":"Azure_KeyVault",
         "order":20,
         "controlType":"textbox",
         "displayLabel":"What is the name of the Azure Key Vault being used?",
         "infoBalloonText":"Enter the Azure Key Vault name",
         "required":false
      },
      {
         "id":"AzureKeyVault_permissions",
         "order":30,
         "controlType":"multilinetextbox",
         "displayLabel":"What are the permissions granted or available for the Azure KeyVault?",
         "infoBalloonText":"You can found the permissions on the 'Access control (IAM)' section in the storage blade on the Azure portal",
         "required":false
      },
      {
         "id":"AzureKeyVault_fw",
         "order":40,
         "controlType":"dropdown",
         "displayLabel":"Does the Azure KeyVault have a firewall?",
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
         "id":"storage_kind",
         "order":50,
         "visibility": "IssueType_dropdown == AECERTStore",
         "controlType":"dropdown",
         "displayLabel":"What type of Always Encryption you are trying ?",
         "infoBalloonText":"Describe the action of Always Encryption trying to perform",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"AESSMS",
               "text":"SSMS to create Always Encrypted Keys)"
            },
            {
               "value":"AECMK",
               "text":"Column Master Key (CMK)"
            },
            {
               "value":"AECEK",
               "text":"Column Encryption Key (CEK)"
            },
            {
               "value":"AEDBTBL",
               "text":"Database table and encrypt columns."
            },
            {
               "value":"AEAPP",
               "text":"Create an Application that Encrypt Columns"
            }
         ],
         "required":false
      },
      {
         "id":"storage_performance",
         "order":60,
         "visibility": "IssueType_dropdown == AEAKV ",
         "controlType":"dropdown",
         "displayLabel":"What type of Always Encryption you are trying ?",
         "infoBalloonText":"Describe the action of Always Encryption trying to perform",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"AESSMS",
               "text":"SSMS to create Always Encrypted Keys)"
            },
            {
               "value":"AECMK",
               "text":"Column Master Key (CMK)"
            },
            {
               "value":"AECEK",
               "text":"Column Encryption Key (CEK)"
            },
            {
               "value":"AEDBTBL",
               "text":"Database table and encrypt columns."
            },
            {
               "value":"AEAPP",
               "text":"Create an Application that Encrypt Columns"
            }
         ],
         "required":false
      },
     {
         "id":"subscription_administrator",
         "order":80,
         "visibility": "IssueType_dropdown == save_setting",
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
         "displayLabel":"What type of permissions granted for the Azure Key Vault?",
         "required":false
      },
       {
         "id":"server_region",
         "order":100,
         "controlType":"textbox",
         "displayLabel":"What is the Azure Key Vault region?",
         "required":false
      },
      {
         "id":"storage_region",
         "order":110,
         "visibility": "IssueType_dropdown == save_setting",
         "controlType":"textbox",
         "displayLabel":"What is the storage account region?",
         "required":false
      },
      {
         "id":"storage_region_server",
         "order":120,
         "visibility": "IssueType_dropdown == save_setting ",
         "controlType":"dropdown",
         "displayLabel":"Is the storage account in the same region as the Azure SQL Server?",
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
         "id":"storage_subscription_server",
         "order":130,
         "visibility": "IssueType_dropdown == save_setting ",
         "controlType":"dropdown",
         "displayLabel":"Is the storage account in the same subscription as the Azure SQL Server?",
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
         "id":"storage_access",
         "order":140,
         "visibility": "IssueType_dropdown == view",
         "controlType":"dropdown",
         "displayLabel":"Do you have access to the Storage Account?",
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
         "id":"portal_scan_result",
         "order":150,
         "visibility": "IssueType_dropdown == view",
         "controlType":"dropdown",
         "displayLabel":"Can you view Vulnerability Assessment results by accessing it from the portal?",
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
         "visibility": "IssueType_dropdown == view",
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
         "visibility": "IssueType_dropdown == view",
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
         "id":"change_storage",
         "order":180,
         "visibility": "IssueType_dropdown == failed_export",
         "controlType":"dropdown",
         "displayLabel":"Did you change a storage account for this server in the Vulnerability Assessment setting?",
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
         "id":"baseline_rules_ids",
         "order":190,
         "visibility": "IssueType_dropdown == baseline",
         "controlType":"textbox",
         "displayLabel":"What are the rule ids that this issue is relevant to?",
         "required":false
      },
       {
         "id":"baseline_set_failed",
         "order":200,
         "visibility": "IssueType_dropdown == baseline",
         "controlType":"dropdown",
         "displayLabel":"Did you set a baseline and the rule still failed?",
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
               "value":"not_relevant",
               "text":"Not relevant"
            }
         ],
         "required":false
      },
      {
         "id":"scan_issue_type",
         "order":210,
         "visibility": "IssueType_dropdown == scan",
         "controlType":"dropdown",
         "displayLabel":"What is the type of scan that you has an issue with",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"manual_scan",
               "text":"Manual scan"
            },
            {
               "value":"recurring_scan",
               "text":"Recurring scan"
            },
            {
               "value":"both",
               "text":"Both"
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
