<properties
	articleId="configuring-and-sending-data-from-application-insights-sdks"
	pageTitle="Configuring and sending data from Application Insights SDKs"
	description="Configuring and sending data from Application Insights SDKs"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729599, 32729603, 32729604, 32729605, 32729606, 32729609, 32729612"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Configuring and sending data from Application Insights SDKs
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring and sending data from Application Insights SDKs",
    "fileAttachmentHint": "File Upload recommendations: ApplicationInsights.config; packages.config or PackageReferences; web.config or app.config; AppSettings.json; ApplicationInsights.xml; AI-Agent.xml. Please edit files to remove sensitive information.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start occurring?",
            "required": true
        },
        {
            "id": "notification_type",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Where is the monitored application deployed?",
            "watermarkText": "Choose one or more",
            "dropdownOptions": [
                {
                    "value": "Azure VM",
                    "text": "Azure VM"
                },
                {
                    "value": "On-Premises VM",
                    "text": "On-Premises VM"
                },
                {
                    "value": "Azure Web App or App Service",
                    "text": "Azure Web App or App Service"
                },
                {
                    "value": "Azure Cloud Service",
                    "text": "Azure Cloud Service"
                },
                {
                    "value": "Azure Function",
                    "text": "Azure Function"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "notification_type_other",
            "order": 5,
            "visibility": "notification_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe how the monitored application is deployed:",
            "watermarkText": "Kubernetes, Cloud Provider XYZ",
            "required": false
        },
        {
            "id": "site_app",
            "order": 7,
            "visibility": "depend != null",
            "controlType": "textbox",
            "displayLabel": "What is the name of the site/app that is related to this issue?",
            "watermarkText": "What is the name of the site/app that is related to this issue?",
            "required": false
        },
        {
            "id": "sdk_used",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Which SDK is being utilized?",
            "dropdownOptions": [
                {
                    "value": ".NET/.Net Core",
                    "text": ".NET/.Net Core"
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
                    "value": "JavaScript",
                    "text": "JavaScript"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": true
        },
        {
            "id": "sdk_used_java",
            "order": 10,
            "visibility": "sdk_used == Java",
            "controlType": "dropdown",
            "displayLabel": "Which Application Server is being utilized?",
            "dropdownOptions": [
                {
                    "value": "Tomcat",
                    "text": "Tomcat"
                },
                {
                    "value": "Wildfly",
                    "text": "Wildfly"
                },
                {
                    "value": "Jetty",
                    "text": "Jetty"
                },
                {
                    "value": "Spring Boot",
                    "text": "Spring Boot"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_used_java_version",
            "order": 12,
            "visibility": "sdk_used == Java",
            "controlType": "dropdown",
            "displayLabel": "Which version of Java is being utilized?",
            "dropdownOptions": [
                {
                    "value": "Java 7",
                    "text": "Java 7"
                },
                {
                    "value": "Java 8",
                    "text": "Java 8"
                },
                {
                    "value": "Java 9",
                    "text": "Java 9"
                },
                {
                    "value": "Java 10",
                    "text": "Java 10"
                },
                {
                    "value": "Java 11",
                    "text": "Java 11"
                },
                {
                    "value": "Java 12",
                    "text": "Java 12"
                },
                {
                    "value": "Java 13",
                    "text": "Java 13"
                },
                {
                    "value": "Java 14",
                    "text": "Java 14"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_used_java_os",
            "order": 13,
            "visibility": "sdk_used == Java",
            "controlType": "dropdown",
            "displayLabel": "Which is the operating system running the application?",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "Mac OSX",
                    "text": "Max OSX"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_used_java_2x",
            "order": 14,
            "visibility": "sdk_used == Java",
            "controlType": "dropdown",
            "displayLabel": "•	If you are using a version a 2.X version, is the JVM Agent being used for dependency collection?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_used_other",
            "order": 15,
            "visibility": "sdk_used == Other",
            "controlType": "textbox",
            "displayLabel": "Which SDK is being utilized?",
            "watermarkText": "Which SDK is being utilized?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 16,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are seeing",
            "watermarkText": "Please include expected versus observed behavior, exact errors, etc",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide expected versus observed behavior"
                },
                {
                    "text": "Provide the exact errors"
                },
                {
                    "text": "Upload screenshots below as file attachments"
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 19,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---