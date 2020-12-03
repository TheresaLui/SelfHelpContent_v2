<properties
	pageTitle="scoping-questions-for-always-encrypted with secure enclaves"
	description="Scoping questions to capture more details about always encrypted, secure enclaves."
	authors="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32782210"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="4c2f22d0-06a1-44c7-85f5-297b5c6291ee"
	ownershipId="AzureData_AzureSQLDB_Security"
/>
# Scoping questions for Always Encrypted, Secure Enclaves
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Always Encrypted with Secure Enclaves",
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
               "value":"AESE",
               "text":"Always Encrypted with Security Enclaves"
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
         "displayLabel":"Please describe the issue/error message you are facing",
         "required":false
      },
      {
         "id":"Issue_Type",
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
         "id":"server_region",
         "order":100,
         "controlType":"textbox",
         "displayLabel":"What is the Azure SQL Server egion?",
         "required":false
      },
      {
         "id":"akv_region",
         "order":110,
         "visibility": "IssueType_dropdown == AEAKV",
         "controlType":"textbox",
         "displayLabel":"What is the Azure Key Vault region?",
         "required":false
      },
      {
         "id":"akv_region_server",
         "order":120,
         "visibility": "IssueType_dropdown == AEAKV ",
         "controlType":"dropdown",
         "displayLabel":"Is the Azure Key Vault in the same region as the Azure SQL Server?",
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
         "visibility": "IssueType_dropdown == AEAKV ",
         "controlType":"dropdown",
         "displayLabel":"Is the Azure Key Vault in the same subscription as the Azure SQL Server?",
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
         "id":"AKV_access",
         "order":140,
         "visibility": "IssueType_dropdown == AEAKV",
         "controlType":"dropdown",
         "displayLabel":"Do you have access to the Azure KeyVault?",
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
