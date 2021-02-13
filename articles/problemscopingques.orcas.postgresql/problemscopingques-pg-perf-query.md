<properties
	pageTitle="Database Performance"
	description="Database Performance"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640025, 32781011, 32781012"
	productPesIds="17067,17068,17069"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-pg-perf-query"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Database Performance - Query
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Query Performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Perf Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Perf Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
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
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "repro_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When was the most recent repro?",
            "required": true
        },
        {
            "id": "persistent",
            "order": 4,
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
            "id": "statement_stats",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you enabled server parameters like log_statement_stats or pg_stat_statements?",
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
            "id": "compare_performance",
            "order": 6,
            "visibility": "statement_stats == Yes",
            "controlType": "dropdown",
            "displayLabel": "Was the performance better before enabling these server parameters?",
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
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the measured time when running 'SELECT 1' from your Postgres client?",
            "required": false
        },
        {
            "id": "client_location",
            "order": 8,
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
            "order": 9,
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
            "order": 10,
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
            "order": 11,
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
            "order": 12,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "textbox",
            "displayLabel": "Please indicate to which cloud environment you are comparing:",
            "required": false
        },
        {
            "id": "cloud_as_point_of_comparison_config",
            "order": 13,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "multilinetextbox",
            "displayLabel": "What is your database configuration in the corresponding environment?",
            "watermarkText": "CPU, RAM, Storage type, etc",
            "required": false
        },
        {
            "id": "cloud_as_point_of_comparison_app",
            "order": 14,
            "visibility": "point_of_comparison == Non-Azure",
            "controlType": "multilinetextbox",
            "displayLabel": "What is your application VM configuration in the corresponding environment?",
            "watermarkText": "CPU, RAM, Storage type, etc",
            "required": false
        },
        {
            "id": "other_point_of_comparison",
            "order": 15,
            "visibility": "point_of_comparison == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please specify your point of comparison:",
            "required": false
        },
        {
            "id": "measurement_tool",
            "order": 16,
            "controlType": "textbox",
            "displayLabel": "What tool are you using to measure your performance?",
            "watermarkText": "e.g. pgbench",
            "required": false
        },
        {
            "id": "measurement",
            "order": 17,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide your performance/latency numbers:",
            "required": false
        },
        {
            "id": "slow_queries",
            "order": 18,
            "controlType": "multilinetextbox",
            "displayLabel": "Please list all the slow running queries:",
            "watermarkText": "Enter All if all queries are slow.",
            "required": true
        },
        {
            "id": "query_plan",
            "order": 19,
            "controlType": "multilinetextbox",
            "displayLabel": "Please paste your query plan here for the slow running query:",
            "infoBalloonText": "Run: EXPLAIN [Your query]; to get the query plan for [Your query]",
            "required": false
        },
        {
            "id": "application",
            "order": 20,
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
            "order": 21,
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
            "order": 22,
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
            "order": 23,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---