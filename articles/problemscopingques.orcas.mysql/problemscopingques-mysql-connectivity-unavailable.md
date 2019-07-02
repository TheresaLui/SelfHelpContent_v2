<properties
    pageTitle="Database Connectivity"
    description="Database Connectivity"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640051"
    productPesIds="16221"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-mysql-connectivity-unavailable"
/>
# Database Connectivity - Database is currently unavailable
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
            "id": "down",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Why do you say database is down/unhealthy?",
            "dropdownOptions": [
                {
                    "value": "cannot_load",
                    "text": "Can’t load server information on portal"
                },
                {
                    "value": "unable_to_connect",
                    "text": "Unable to connect/Getting errors while logging in"
                },
                {
                    "value": "down_in_health",
                    "text": "Shows down in resource health menu"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Others"
                }
            ],
            "required": false
        },
        {
            "id": "dont_know_down",
            "order": 3,
            "visibility": "down == dont_know_answer",
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the reason why you think database is down/unhealthy:",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "server_recover",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did the server recover?",
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
            "id": "when_server_recovered",
            "order": 5,
            "visibility": "server_recover == Yes",
            "controlType": "datetimepicker",
            "displayLabel": "When did it recover?",
            "required": false
        },
        {
            "id": "steps_to_recover",
            "order": 6,
            "visibility": "server_recover == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "What steps did you take to recover the server?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "frequency",
            "order": 7,
            "visibility": "server_recover == Yes",
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
            "id": "application",
            "order": 8,
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
            "required": false
        },
        {
            "id": "non_application",
            "order": 9,
            "visibility": "application == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "What is your client?",
            "watermarkText": "phpMyAdmin, MySQL Workbench, etc",
            "required": false
        },
        {
            "id": "container",
            "order": 10,
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
            "order": 11,
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
            "order": 12,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "Subscription ID of your Azure App Service:",
            "required": false
        },
        {
            "id": "Azure_application_type",
            "order": 13,
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
            "order": 14,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the name of your Azure App Service?",
            "required": false
        },
        {
            "id": "application_location",
            "order": 15,
            "visibility": "application == Yes && Azure_application == No",
            "controlType": "textbox",
            "displayLabel": "Where is your application running?",
            "required": false
        },
        {
            "id": "application_driver",
            "order": 16,
            "visibility": "application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the type and version of your client driver?",
            "watermarkText": "e.g. Connector/ODBC 8.0.16",
            "required": false
        },
        {
            "id": "application_retry",
            "order": 17,
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
            "order": 18,
            "visibility": "application == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Please share any client side logs:",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "connection_pooler",
            "order": 19,
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
            "required": false
        },
        {
            "id": "connection_pooler_type",
            "order": 20,
            "visibility": "connection_pooler == Yes",
            "controlType": "textbox",
            "displayLabel": "What connection pooler are you using?",
            "required": false
        },
        {
            "id": "connection_pooler_config",
            "order": 21,
            "visibility": "connection_pooler == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Could you provide connection pooling configuration?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_description",
            "order": 22,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
            "watermarkText": "",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
