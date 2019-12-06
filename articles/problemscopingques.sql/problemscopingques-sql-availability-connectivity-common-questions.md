<properties
	pageTitle="Scoping Questions for Azure Active Directory (AAD) authentication"
	description="Scoping questions to capture more details about Azure Active Directory (AAD) authentication issue."
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa,swbhartims,vimahadi,subbuk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630414, 32630460"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="217152B3-3A59-4441-8B67-B20B2DE5CD95"
/>

# Scoping questions for Configure or use Azure Active Directory (AAD) authentication
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Azure Active Directory (AAD) authentication scoping questions",
  "fileAttachmentHint": "",
  "diagnosticCard": {
    "title": "Azure Active Directory (AAD) authentication scoping questions",
    "description": "Scoping questions to capture more details about Azure Active Directory (AAD) authentication issue.",
    "insightNotAvailableText": "We did not find any issues with your AAD configuration."
  },
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Start Time of the AAD Issue",
      "infoBalloonText": "Please provide the start time of the most recent occurrence of AAD Issue.",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional context to help us solve your issue.",
      "required": true,
      "useAsAdditionalDetails": true,
      "watermarkText": "On the basics tab, please ensure that you have selected a server, database or an elastic pool in the resource dropdown. This will let us know the resource that you need assistance with. Please provide any additional details that may help us troubleshoot your issue."
    },
    {
      "id": "aad_issue_type",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "Choose an option that best describes your AAD issue.",
      "required": true,
      "watermarkText": "Common AAD issue categories",
      "infoBalloonText": "AAD Issue category",
      "dropdownOptions": [
        {
          "text": "Logging using AAD",
          "value": "AADLogin"
        },
        {
          "text": "Creating new AAD Users",
          "value": "AADCreateUser"
        },
        {
          "text": "Setting up AAD administrator",
          "value": "AADSetupAdmin"
        },
        {
          "text": "Other AAD issues",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "sqlexception_received_on_client",
      "order": 2000,
      "controlType": "multilinetextbox",
      "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
      "required": true,
      "visibility": "aad_issue_type == AADLogin || aad_issue_type == AADCreateUser || aad_issue_type == dont_know_answer",
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "aad_login_conditional_errors",
      "order": 2100,
      "controlType": "textbox",
      "displayLabel": "Are the login failures conditional? Ex. Only from certain IPs or only when using username and password, or when using Single Sign On (SSO) or when using Multi Factor Authentication (MFA)",
      "infoBalloonText": "Please describe the circumstances in which you are facing login errors.",
      "required": true,
      "visibility": "aad_issue_type == AADLogin",
      "diagnosticInputRequiredClients": "Portal",
      "content": null,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "aad_login_aid",
      "order": 2500,
      "controlType": "textbox",
      "displayLabel": "Please enter your Application Id (AppId)",
      "infoBalloonText": "Please enter your Application Id if you know it.",
      "required": false,
      "visibility": "aad_issue_type == AADLogin",
      "content": null,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "aad_user_type_login",
      "order": 3000,
      "controlType": "dropdown",
      "displayLabel": "Choose the type of AAD user that is trying to login",
      "required": true,
      "watermarkText": "AAD User Types",
      "infoBalloonText": "AAD User Types",
      "dropdownOptions": [
        {
          "text": "Service Principal",
          "value": "AADUserServicePrincipal"
        },
        {
          "text": "Outlook / Office 365 Group",
          "value": "AADUserOutlookOffice365Group"
        },
        {
          "text": "Guest User",
          "value": "AADUserGuest"
        },
        {
          "text": "Native User",
          "value": "AADUserNative"
        },
        {
          "text": "Other",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADLogin"
    },
    {
      "id": "aad_user_type_create",
      "order": 3100,
      "controlType": "dropdown",
      "displayLabel": "Choose the type of AAD user that you are creating",
      "required": true,
      "watermarkText": "AAD User Types",
      "infoBalloonText": "AAD User Types",
      "dropdownOptions": [
        {
          "text": "Service Principal",
          "value": "AADUserServicePrincipal"
        },
        {
          "text": "Outlook / Office 365 Group",
          "value": "AADUserOutlookOffice365Group"
        },
        {
          "text": "Guest User",
          "value": "AADUserGuest"
        },
        {
          "text": "Native User",
          "value": "AADUserNative"
        },
        {
          "text": "Other",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADCreateUser"
    },
    {
      "id": "aad_user_type_setadmin",
      "order": 3200,
      "controlType": "dropdown",
      "displayLabel": "Choose the type of AAD user that you want to set as an Admin",
      "required": true,
      "watermarkText": "AAD User Types",
      "infoBalloonText": "AAD User Types",
      "dropdownOptions": [
        {
          "text": "Service Principal",
          "value": "AADUserServicePrincipal"
        },
        {
          "text": "Outlook / Office 365 Group",
          "value": "AADUserOutlookOffice365Group"
        },
        {
          "text": "Guest User",
          "value": "AADUserGuest"
        },
        {
          "text": "Native User",
          "value": "AADUserNative"
        },
        {
          "text": "Other",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADSetupAdmin"
    },
    {
      "id": "aad_is_service_principal",
      "order": 4000,
      "controlType": "dropdown",
      "displayLabel": "Are you logged in as a Service Principal?",
      "required": true,
      "watermarkText": "Yes / No",
      "infoBalloonText": "Indicate if you are logged in as a service principal?",
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "Yes"
        },
        {
          "text": "No",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADCreateUser"
    },
    {
      "id": "aad_powershell_cli_usage",
      "order": 4200,
      "controlType": "dropdown",
      "displayLabel": "Have you tried using PowerShell or CLI in addition to the Portal interface?",
      "required": true,
      "watermarkText": "Yes / No",
      "infoBalloonText": "Indicate if you have tried using PowerShell or CLI in addition to the Portal interface?",
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "Yes"
        },
        {
          "text": "No",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADSetupAdmin"
    },
    {
      "id": "aad_setupadmin_issue_type",
      "order": 4100,
      "controlType": "dropdown",
      "displayLabel": "Choose the description that best describes the issue that you are facing while setting up the AAD Admin.",
      "required": true,
      "watermarkText": "Common AAD Admin setup issues",
      "infoBalloonText": "Common AAD Admin setup issues",
      "dropdownOptions": [
        {
          "text": "The AAD Object does not appear in the Azure Portal blade",
          "value": "Does_Not_Appear"
        },
        {
          "text": "The AAD Object appears in the portal blade but is greyed out",
          "value": "Appears_But_Is_Greyed_Out"
        },
        {
          "text": "When I try to Execution Query Timeout the PowerShell / CLI command it times out",
          "value": "CLI_Times_Out"
        },
        {
          "text": "My problem is not listed here",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == AADSetupAdmin"
    },
    {
      "id": "aad_other_setupadmin_login",
      "order": 5000,
      "controlType": "dropdown",
      "displayLabel": "Have you already set up an AAD Admin and successfully connected to the SQL Server?",
      "required": true,
      "watermarkText": "Yes / No",
      "infoBalloonText": "Indicate if you have already set up an AAD Admin and successfully connected to the SQL Server?",
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "Yes"
        },
        {
          "text": "No",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal",
      "visibility": "aad_issue_type == dont_know_answer"
    }
  ]
}
---
