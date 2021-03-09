<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640051"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-mysql-connectivity-unavailable"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - Database is currently unavailable
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for MySQL Connectivity Troubleshooter",
        "description": "Our Azure Database for MySQL Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Follow the steps in the Recommended Solution section to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank.)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "down",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Why is the database down or in an unhealthy state?",
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
            "required": true
        },
        {
            "id": "dont_know_down",
            "order": 4,
            "visibility": "down == dont_know_answer",
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the reason why the database is down/unhealthy",
            "required": false
        },
        {
            "id": "server_recover",
            "order": 5,
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
            "order": 6,
            "visibility": "server_recover == Yes",
            "controlType": "datetimepicker",
            "displayLabel": "When did it recover?",
            "required": false
        },
        {
            "id": "steps_to_recover",
            "order": 7,
            "visibility": "server_recover == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "What steps did you take to recover the server?",
            "required": false
        },
        {
            "id": "frequency",
            "order": 8,
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
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Are you connecting to your database server from the application?",
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
            "order": 10,
            "visibility": "application == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "What is your client?",
            "watermarkText": "phpMyAdmin, MySQL Workbench, etc",
            "required": false
        },
        {
            "id": "container",
            "order": 11,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "Is your application running in a container service?",
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
            "order": 12,
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
            "order": 13,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "Subscription ID of your Azure App Service",
            "required": false
        },
        {
            "id": "Azure_application_type",
            "order": 14,
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
            "order": 15,
            "visibility": "application == Yes && Azure_application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the name of your Azure App Service?",
            "required": false
        },
        {
            "id": "application_location",
            "order": 16,
            "visibility": "application == Yes && Azure_application == No",
            "controlType": "textbox",
            "displayLabel": "Where is your application running?",
            "required": false
        },
        {
            "id": "application_driver",
            "order": 17,
            "visibility": "application == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the type and version of your client driver?",
            "watermarkText": "e.g. Connector/ODBC 8.0.16",
            "required": false
        },
        {
            "id": "application_retry",
            "order": 18,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "Does your application have a retry mechanism?",
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
            "order": 19,
            "visibility": "application == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Share any client-side logs",
            "required": false
        },
        {
            "id": "connection_pooler",
            "order": 20,
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
            "order": 21,
            "visibility": "connection_pooler == Yes",
            "controlType": "textbox",
            "displayLabel": "Which connection pooler are you using?",
            "required": false
        },
        {
            "id": "connection_pooler_config",
            "order": 22,
            "visibility": "connection_pooler == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Can you provide the connection pooling configuration?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 23,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any driver exceptions or errors you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
