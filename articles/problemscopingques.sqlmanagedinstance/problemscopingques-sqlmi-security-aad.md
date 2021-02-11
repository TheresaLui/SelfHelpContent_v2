<properties
	articleId="problemscopingques-sqlmi-security-aad"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions for Configure or use Azure Active Directory (AAD) authentication"
	authors="keithelm"
	authoralias="keithelm"
	ms.author="keithelm,muruga,emlisa,swbhartims,vimahadi,subbuk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637236"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# Scoping questions for Configure or use Azure Active Directory (AAD) authentication
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time of the AAD Issue",
            "infoBalloonText": "Provide the start time of the most recent occurrence of AAD issue.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional context to help us solve your issue.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": ""
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
            "dynamicDropdownOptions": null
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 2000,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste detailed error message or stack trace. (Remove any personally identifiable information.)",
            "required": true,
            "visibility": "aad_issue_type == AADLogin || aad_issue_type == AADCreateUser || aad_issue_type == dont_know_answer"
        },
        {
            "id": "aad_user_type_login",
            "order": 2100,
            "controlType": "dropdown",
            "displayLabel": "Choose the type of AAD user that is trying to log in",
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
            "visibility": "aad_issue_type == AADLogin"
        },
        {
            "id": "aad_are_failures_conditional",
            "order": 2200,
            "controlType": "dropdown",
            "displayLabel": "Are the AAD failures conditional?",
            "required": true,
            "watermarkText": "Yes / No",
            "infoBalloonText": "Indicate if the errors are persistent or happening only when certain conditions are met.",
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
            "visibility": "aad_issue_type == AADLogin"
        },
        {
            "id": "aad_conditional_failures",
            "order": 2210,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes the condition when the failures occur.",
            "required": true,
            "watermarkText": "Conditional failure options",
            "infoBalloonText": "",
            "dropdownOptions": [
                {
                    "text": "Only from certain IPs",
                    "value": "ConditionalFailuresOnlyCertainIPs"
                },
                {
                    "text": "Only when using username and password",
                    "value": "ConditionalFailuresOnlyUserNamePassword"
                },
                {
                    "text": "When using Single Sign On (SSO)",
                    "value": "ConditionalFailuresSSO"
                },
                {
                    "text": "When using Multi Factor Authentication (MFA)",
                    "value": "ConditionalFailuresMFA"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADLogin && aad_are_failures_conditional == Yes"
        },
        {
            "id": "aad_login_aid",
            "order": 2500,
            "controlType": "textbox",
            "displayLabel": "Enter your Application Id (AppID)",
            "infoBalloonText": "Please enter your Application Id if you know it. Ex. '00000002-0000-0000-c000-000000000000'",
            "required": false,
            "visibility": "aad_issue_type == AADLogin",
            "content": null,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "aad_login_oid",
            "order": 2510,
            "controlType": "textbox",
            "displayLabel": "Enter your Object Id (OID)",
            "infoBalloonText": "Please enter your Object Id if you know it. Ex. '40b79501-b343-44ed-9ce7-da4c8cc7353f'",
            "required": false,
            "visibility": "aad_issue_type == AADLogin",
            "content": null,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "aad_login_sid",
            "order": 2520,
            "controlType": "textbox",
            "displayLabel": "Enter your Security Id (SID)",
            "infoBalloonText": "Please enter your Security Id if you know it.",
            "required": false,
            "visibility": "aad_issue_type == AADLogin",
            "content": null,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "add_login_tool",
            "order": 2600,
            "controlType": "dropdown",
            "displayLabel": "Which tool are you using to connect to the Managed Instance?",
            "required": false,
            "dropdownOptions": [
                {
                    "text": "SSMS",
                    "value": "ConnectingToolSSMS"
                },
                {
                    "text": "Query Editor",
                    "value": "ConnectingToolQueryEditor"
                },
                {
                    "text": "SSDT",
                    "value": "ConnectingToolSSDT"
                },
                {
                    "text": ".NET",
                    "value": "ConnectingToolDotNet"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADLogin"
        },
        {
            "id": "aad_login_tool_other",
            "order": 2610,
            "controlType": "textbox",
            "displayLabel": "Enter the tool name you're using to connect to the Managed Instance.",
            "infoBalloonText": "If you are using client tool(s) other than the ones listed above, please type in the tool name.",
            "required": true,
            "visibility": "add_login_tool == dont_know_answer",
            "content": null,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "aad_login_driver",
            "order": 2700,
            "controlType": "dropdown",
            "displayLabel": "What driver are you using to connect to the Managed Instance?",
            "required": false,
            "dropdownOptions": [
                {
                    "text": "JDBC",
                    "value": "ConnectingDriverJDBC"
                },
                {
                    "text": "ODBC",
                    "value": "ConnectingDriverODBC"
                },
                {
                    "text": "Python",
                    "value": "ConnectingDriverPython"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADLogin"
        },
        {
            "id": "aad_login_driver_other",
            "order": 2710,
            "controlType": "textbox",
            "displayLabel": "Enter the driver you're using to connect to the Managed Instance.",
            "infoBalloonText": "If you are using driver(s) other than the ones listed above, please type in the driver name and version.",
            "required": true,
            "visibility": "aad_login_driver == dont_know_answer",
            "content": null,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "aad_login_login_as_admin",
            "order": 2800,
            "controlType": "dropdown",
            "displayLabel": "Are you able to log in as an AAD Admin to the SQL Server?",
            "required": false,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADLogin"
        },
        {
            "id": "aad_login_check_non_master_database",
            "order": 2900,
            "controlType": "dropdown",
            "displayLabel": "By default the database is \"master\". Are you logging into the correct database?",
            "required": false,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                }
            ],
            "dynamicDropdownOptions": null,
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
            "visibility": "aad_issue_type == AADCreateUser"
        },
        {
            "id": "aad_user_type_currently_signed_in",
            "order": 3200,
            "controlType": "dropdown",
            "displayLabel": "Choose the type of AAD user that you are currently signed in as",
            "required": true,
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
            "visibility": "aad_issue_type == AADCreateUser"
        },
        {
            "id": "aad_are_failures_conditional_optional",
            "order": 3500,
            "controlType": "dropdown",
            "displayLabel": "Are the AAD failures conditional?",
            "required": false,
            "watermarkText": "Yes / No",
            "infoBalloonText": "Indicate if the errors are persistent or happening only when certain conditions are met.",
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
            "visibility": "aad_issue_type == AADCreateUser"
        },
        {
            "id": "aad_conditional_failures_optional",
            "order": 3510,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes the condition when the failures occur.",
            "required": false,
            "watermarkText": "Conditional failure options",
            "infoBalloonText": "",
            "dropdownOptions": [
                {
                    "text": "Only from certain IPs",
                    "value": "ConditionalFailuresOnlyCertainIPs"
                },
                {
                    "text": "Only when using username and password",
                    "value": "ConditionalFailuresOnlyUserNamePassword"
                },
                {
                    "text": "When using Single Sign On (SSO)",
                    "value": "ConditionalFailuresSSO"
                },
                {
                    "text": "When using Multi Factor Authentication (MFA)",
                    "value": "ConditionalFailuresMFA"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADCreateUser && aad_are_failures_conditional_optional == Yes"
        },
        {
            "id": "aad_admin_already_set_up",
            "order": 3600,
            "controlType": "dropdown",
            "displayLabel": "Have you already set up an AAD Admin for your SQL Server?",
            "required": false,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                }
            ],
            "dynamicDropdownOptions": null,
            "visibility": "aad_issue_type == AADCreateUser"
        },
        {
            "id": "aad_user_type_setadmin",
            "order": 4000,
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
            "visibility": "aad_issue_type == AADSetupAdmin"
        },
        {
            "id": "aad_powershell_cli_usage",
            "order": 4100,
            "controlType": "dropdown",
            "displayLabel": "Have you tried using PowerShell or CLI in addition to the Azure portal interface?",
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
            "visibility": "aad_issue_type == AADSetupAdmin"
        },
        {
            "id": "aad_setupadmin_issue_type",
            "order": 4200,
            "controlType": "dropdown",
            "displayLabel": "Choose the best description for the issue you're facing while setting up the AAD Admin.",
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
                    "text": "When I try to execute the query, the PowerShell / CLI command times out",
                    "value": "CLI_Times_Out"
                },
                {
                    "text": "My problem is not listed here",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
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
            "visibility": "aad_issue_type == dont_know_answer"
        }
    ]
}
---
