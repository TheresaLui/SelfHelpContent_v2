<properties
	pageTitle="Database Performance"
	description="Database Performance"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747641"
	productPesIds="17344"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-flexsvr-perf-query"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Performance - Query
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Query Performance",
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
            "id": "repro_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When was the most recent repro?",
            "required": true
        },
        {
            "id": "persistent",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Can you reproduce this performance issue consistently?",
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
            "id": "select_1",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the measured time when running 'SELECT 1' from your MySQL client?",
            "required": false
        },
        {
            "id": "client_location",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is your client located in the same region as your database server?",
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
            "id": "pooling",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Do you have connection pooling enabled?",
            "infoBalloonText": "It is highly recommended to enable connection pooling tools while testing the server performance with multiple connections.",
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
            "id": "accelerated_networking",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Is accelerated networking enabled on the client?",
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
            "id": "point_of_comparison",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "What is your point of comparison?",
            "dropdownOptions": [
                {
                    "value": "It is slower than it typically is",
                    "text": "It is slower than it typically is"
                },
                {
                    "value": "It is slower than another database server on Azure",
                    "text": "It is slower than another database server on Azure"
                },
                {
                    "value": "It is slower when connection is from VNET",
                    "text": "It is slower when connection is from VNET"
                },
                {
                    "value": "Non-Azure",
                    "text": "It is slower than server on Non-Azure cloud Environment"
                },
                {
                    "value": "It is slower than database server running on VM/Locally",
                    "text": "It is slower than database server running on VM/Locally"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "cloud_as_point_of_comparison",
            "order": 9,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "textbox",
            "displayLabel": "Please indicate to which cloud environment you are comparing:",
            "required": false
        },
        {
            "id": "cloud_as_point_of_comparison_config",
            "order": 10,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "multilinetextbox",
            "displayLabel": "What is your database configuration in the corresponding environment?",
            "watermarkText": "CPU, RAM, Storage type, etc",
            "required": false
        },
        {
            "id": "cloud_as_point_of_comparison_app",
            "order": 11,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "multilinetextbox",
            "displayLabel": "What is your application VM configuration in the corresponding environment?",
            "watermarkText": "CPU, RAM, Storage type, etc",
            "required": false
        },
        {
            "id": "other_point_of_comparison",
            "order": 12,
            "visibility": "point_of_comparison == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please specify your point of comparison:",
            "required": false
        },
        {
            "id": "measurement_tool",
            "order": 13,
            "controlType": "textbox",
            "displayLabel": "What tool are you using to measure your performance?",
            "watermarkText": "e.g. SysBench",
            "required": false
        },
        {
            "id": "measurement",
            "order": 14,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide your performance/latency numbers:",
            "required": false
        },
        {
            "id": "slow_queries",
            "order": 15,
            "controlType": "multilinetextbox",
            "displayLabel": "Please list all the slow running queries:",
            "watermarkText": "Enter All if all queries are slow.",
            "required": true
        },
        {
            "id": "query_plan",
            "order": 16,
            "controlType": "multilinetextbox",
            "displayLabel": "Please paste your query plan here for the slow running query:",
            "infoBalloonText": "Run: EXPLAIN [Your query]; to get the query plan for [Your query]",
            "required": false
        },
        {
            "id": "application",
            "order": 17,
            "controlType": "dropdown",
            "displayLabel": "Are you connecting to your database server from application?",
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
            "id": "application_language",
            "order": 18,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is your application programming language?",
            "dropdownOptions": [
                {
                    "value": "C++",
                    "text": "C++"
                },
                {
                    "value": "C#",
                    "text": "C#"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Node.js",
                    "text": "Node.js"
                },
                {
                    "value": "PHP",
                    "text": "PHP"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Ruby",
                    "text": "Ruby"
                },
                {
                    "value": "Others",
                    "text": "Others"
                }
            ],
            "required": false
        },
        {
            "id": "application_client",
            "order": 19,
            "visibility": "application == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is your application client type?",
            "dropdownOptions": [
                {
                    "value": "Web App",
                    "text": "Web App"
                },
                {
                    "value": "Mobile App",
                    "text": "Mobile App"
                },
                {
                    "value": "Others",
                    "text": "Others"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
