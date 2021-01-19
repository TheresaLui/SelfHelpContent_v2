<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747611,32747614"
	productPesIds="17344"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-flexsvr-connectivity-dropped-errors"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - Established connection is dropped or terminated && Error while connecting to the server
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "ongoing",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you currently facing this issue?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "persistent_or_intermittent",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue persistent or intermittent?",
            "dropdownOptions": [
                {
                    "value": "persistent",
                    "text": "Persistent"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Intermittent"
                }
            ],
            "required": true
        },
        {
            "id": "intermittent",
            "order": 4,
            "visibility": "persistent_or_intermittent == dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "How often does this issue happen?",
            "dropdownOptions": [
                {
                    "value": "Everyday",
                    "text": "Everyday"
                },
                {
                    "value": "Several times a week",
                    "text": "Several times a week"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "resource_health",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Does your server show Unavailable in the Resource Health blade in portal?",
            "infoBalloonText": "Resource health menu item can be found above New support request.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "application",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Are you connecting to your database server from application?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "non_application",
            "order": 7,
            "visibility": "application == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "What is your client?",
            "watermarkText": "phpMyAdmin, MySQL Workbench, etc",
            "required": false
        },
        {
            "id": "container",
            "order": 8,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "Is your application running in any container service?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "Azure_application",
            "order": 9,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "Is your application running in Azure?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "Azure_application_subscription",
            "order": 10,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "Subscription ID of your Azure App Service:",
            "required": false
        },
        {
            "id": "Azure_application_type",
            "order": 11,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is the type of your Azure App Service?",
            "dropdownOptions": [
                {
                    "value": "Web Apps",
                    "text": "Web Apps"
                },
                {
                    "value": "Web App for Containers",
                    "text": "Web App for Containers"
                },
                {
                    "value": "Mobile Apps",
                    "text": "Mobile Apps"
                },
                {
                    "value": "API Apps",
                    "text": "API Apps"
                }
            ],
            "required": false
        },
        {
            "id": "Azure_application_name",
            "order": 12,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the name of your Azure App Service?",
            "required": false
        },
        {
            "id": "application_location",
            "order": 13,
            "visibility": "application == Yes && Azure_application == No",
            "controlType": "textbox",
            "displayLabel": "Where is your application running?",
            "required": false
        },
        {
            "id": "application_driver",
            "order": 14,
            "visibility": "application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the type and version of your client driver?",
            "watermarkText": "e.g. Connector/ODBC 8.0.16",
            "required": false
        },
        {
            "id": "application_retry",
            "order": 15,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "Does your application have retry mechanism?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "application_log",
            "order": 16,
            "visibility": "application == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Please share any client side logs:",
            "required": false
        },
        {
            "id": "connection_pooler",
            "order": 17,
            "controlType": "dropdown",
            "displayLabel": "Are you using a connection pooler?",
            "infoBalloonText": "It is highly recommended to use a connection pooler while connecting to the server.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "connection_pooler_type",
            "order": 18,
            "visibility": "connection_pooler == Yes",
            "controlType": "textbox",
            "displayLabel": "What connection pooler are you using?",
            "required": false
        },
        {
            "id": "connection_pooler_config",
            "order": 19,
            "visibility": "connection_pooler == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Could you provide connection pooling configuration?",
            "required": false
        },
        {
            "id": "query_running",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Does this issue happen while queries are running?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "impacted_query",
            "order": 21,
            "visibility": "query_running == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Can you Provide the query that is impacted more often?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 22,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any driver exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
