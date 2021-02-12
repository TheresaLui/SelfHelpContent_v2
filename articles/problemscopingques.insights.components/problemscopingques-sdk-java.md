<properties
	articleId="problemscopingques-sdk-java"
	pageTitle="Java SDK"
	description="Java SDK"
	authors="debugthings, dhaval24"
	ms.author="jamdavi, dhdoshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32402632"
	productPesIds="15693"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Java SDK)
---
{
    "resourceRequired": true,
    "title": "Java SDK",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "javasdk_version",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What version of Java are you using?",
            "dropdownOptions": [
                {
                    "value": "Java 6",
                    "text": "Java 6"
                },
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "insights_version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What version of Application Insights SDK is being used?",
            "watermarkText": "2.3.0 or SpringBoot Starter 1.1.1",
            "required": true
        },
        {
            "id": "webserver_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What Java web server is being used?",
            "dropdownOptions": [
                {
                    "value": "Apache Tomcat",
                    "text": "Apache Tomcat"
                },
                {
                    "value": "JBoss",
                    "text": "JBoss"
                },
                {
                    "value": "Jetty",
                    "text": "Jetty"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "webserver_type_other",
            "order": 4,
            "visibility": "webserver_type == Other",
            "controlType": "textbox",
            "displayLabel": "What is the name of your web server?",
            "watermarkText": "WebLogic 10; WebSphere",
            "required": true
        },
        {
            "id": "framework_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What Java Web Framework are you using?",
            "dropdownOptions": [
                {
                    "value": "J2EE",
                    "text": "J2EE"
                },
                {
                    "value": "Spring MVC",
                    "text": "Spring MVC"
                },
                {
                    "value": "Spring Boot",
                    "text": "Spring Boot"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "framework_type_version",
            "order": 6,
            "controlType": "textBox",
            "displayLabel": "What is the framework version being used",
            "watermarkText": "SpringBoot 2.1.0",
            "required": true
        },
        {
            "id": "jvm_agent",
            "order": 7,
            "controlType": "textBox",
            "displayLabel": "Is the JVM Agent Being used for dependency collection?",
            "watermarkText": "Yes or No",
            "required": true
        },
        {
            "id": "build_system",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "What type of build system is being used?",
            "dropdownOptions": [
                {
                    "value": "Maven",
                    "text": "Maven"
                },
                {
                    "value": "Gradle",
                    "text": "Gradle"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "OS",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "What is the operating system running the application?",
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
                    "text": "Mac OSX"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "application_location",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Where is this application deployed?",
            "dropdownOptions": [
                {
                    "value": "Azure App Service",
                    "text": "Azure App Service"
                },
                {
                    "value": "Azure Kubernetes Service",
                    "text": "Azure Kubernetes Service"
                },
                {
                    "value": "On premises application",
                    "text": "On premises application"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "appservice_id",
            "order": 11,
            "controlType": "dropdown",
            "displayLabel": "Please select the app service where this application is deployed.",
            "watermarkText": "Choose an alert",
            "dynamicDropdownOptions": {
                "uri": "/resources?api-version=2014-04-01-preview&%24filter=(subscriptionId%20eq%20'{subscriptionid}')%20and%20(resourceType%20eq%20'microsoft.web%2Fsites')",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of App Services",
                    "text": "Unable to get the list of App Services"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 12,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 13,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": true,
            "watermarkText": "Please provide: a detailed scenario of the error condition, troubleshooting done so far, log files, timestamp, screenshots and any other relevant information.",
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Troubleshooting done so far"
                },
                {
                    "text": "Log Files"
                },
                {
                    "text": "Timestamps"
                },
                {
                    "text": "Screenshots"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---

