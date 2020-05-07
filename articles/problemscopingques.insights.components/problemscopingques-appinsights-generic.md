<properties
	articleId="problemscopingques-appinsights-generic"
	pageTitle="Application Insights"
	description="Application Insights"
	authors="debugthings"
	ms.author="jamdavi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32402602, 32602201, 32402604, 32402605, 32602213, 32402614, 32602206, 32632996, 32602207, 32602208, 32632997, 32609669, 32602211, 32602214, 32602218, 32452725, 32402641, 32632981, 32632988, 32632989, 32632990, 32632991, 32632993, 32402626, 32602209, 32602204, 32602205, 32602222, 32632998, 32546624, 32602225, 32602224, 32602223, 32629553"
	productPesIds="15693"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Application Insights
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": ".NET SDK",
    "fileAttachmentHint": "File Upload recommendations: ApplicationInsights.config; packages.config or PackageReferences; web.config or app.config; AppSettings.json; ApplicationInsights.xml; AI-Agent.xml. Please edit files to remove sensitive information",
    "formElements": [
        {
            "id": "category_classification",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the general category of the issue?",
            "dropdownOptions": [
                {
                    "value": "I do not see the data or values I expect.",
                    "text": "I do not see the data or values I expect."
                },
                {
                    "value": "I feel there is a bug or problem with a feature.",
                    "text": "I feel there is a bug or problem with a feature."
                },
                {
                    "value": "The feature is working as designed but I have additional questions.",
                    "text": "The feature is working as designed but I have additional questions."
                },
                {
                    "value": "There is an error message or notification that I cannot investigate further.",
                    "text": "There is an error message or notification that I cannot investigate further."
                },
                {
                    "value": "The documentation for this feature is missing, wrong, or out of date.",
                    "text": "The documentation for this feature is missing, wrong, or out of date."
                },
                {
                    "value": "I could not find an example, blog post, or document that helps.",
                    "text": "I could not find an example, blog post, or document that helps."
                },
                {
                    "value": "The problem is complex or not well defined and I need a human to help.",
                    "text": "The problem is complex or not well defined and I need a human to help."
                }
            ],
            "required": false
        },
        {
            "id": "environment_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How is the monitored application deployed?",
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
                    "value": "Azure Functions",
                    "text": "Azure Functions"
                },
                {
                    "value": "Azure Service Fabric",
                    "text": "Azure Service Fabric"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "environment_type_other",
            "order": 3,
            "visibility": "environment_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe how the application is deployed:",
            "watermarkText": "Kubernetes, Cloud Provider XYZ",
            "required": false
        },
        {
            "id": "os_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the operating system?",
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
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "os_type_other",
            "order": 5,
            "visibility": "os_type == Other",
            "controlType": "textbox",
            "displayLabel": "OS name and version:",
            "watermarkText": "MacOS 13.2",
            "required": false
        },
        {
            "id": "os_type_linux",
            "order": 6,
            "visibility": "os_type == Linux",
            "controlType": "textbox",
            "displayLabel": "Linux distribution and version:",
            "watermarkText": "Ubuntu 16.4",
            "required": false
        },
        {
            "id": "os_type_windows",
            "order": 7,
            "visibility": "os_type == Windows",
            "controlType": "textbox",
            "displayLabel": "Windows version:",
            "watermarkText": "Windows Server 2016",
            "required": false
        },
        {
            "id": "language_used",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "What is the language of the monitored application that has the issue?",
            "dropdownOptions": [
                {
                    "value": ".NET",
                    "text": ".NET"
                },
                {
                    "value": "Java ",
                    "text": "Java "
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
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "javasdk_version",
            "order": 9,
            "visibility": "language_used == Java && language_used != JavaScript",
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
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "webserver_type_java",
            "order": 10,
            "visibility": "language_used == Java && language_used != JavaScript",
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
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "webserver_type_other",
            "order": 11,
            "visibility": "webserver_type_java == Other",
            "controlType": "textbox",
            "displayLabel": "What is the name of your web server?",
            "watermarkText": "WebLogic 10; WebSphere",
            "required": false
        },
        {
            "id": "framework_type_java",
            "order": 12,
            "visibility": "language_used == Java && language_used != JavaScript",
            "controlType": "dropdown",
            "displayLabel": "What Java Web Framework is in use?",
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
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "framework_type_version_java",
            "order": 13,
            "visibility": "language_used == Java && language_used != JavaScript",
            "controlType": "textbox",
            "displayLabel": "What is the framework version being used",
            "watermarkText": "SpringBoot 2.1.0",
            "required": false
        },
        {
            "id": "jvm_agent",
            "order": 14,
            "visibility": "language_used == Java && language_used != JavaScript",
            "controlType": "textbox",
            "displayLabel": "Is the JVM Agent Being used for dependency collection?",
            "watermarkText": "Yes or No",
            "required": false
        },
        {
            "id": "app_type_net",
            "order": 15,
            "visibility": "language_used == .NET",
            "controlType": "dropdown",
            "displayLabel": "What is the application technology?",
            "dropdownOptions": [
                {
                    "value": "ASP.NET Core",
                    "text": "ASP.NET Core"
                },
                {
                    "value": "ASP.NET Core Web API",
                    "text": "ASP.NET Core Web API"
                },
                {
                    "value": "ASP.NET Core MVC",
                    "text": "ASP.NET Core MVC"
                },
                {
                    "value": "ASP.NET Web API",
                    "text": "ASP.NET Web API"
                },
                {
                    "value": "ASP.NET MVC",
                    "text": "ASP.NET MVC"
                },
                {
                    "value": "WCF",
                    "text": "WCF"
                },
                {
                    "value": "Web Job",
                    "text": "Web Job"
                },
                {
                    "value": "Console",
                    "text": "Console"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "app_type_other",
            "order": 16,
            "visibility": "app_type_net == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the application technology stack:",
            "watermarkText": "OWIN",
            "required": false
        },
        {
            "id": "framework_type_net",
            "order": 17,
            "visibility": "language_used == .NET",
            "controlType": "dropdown",
            "displayLabel": "What is the target .NET Framework?",
            "dropdownOptions": [
                {
                    "value": ".NET 4.5",
                    "text": ".NET 4.5"
                },
                {
                    "value": ".NET 4.6",
                    "text": ".NET 4.6"
                },
                {
                    "value": ".NET 4.7",
                    "text": ".NET 4.7"
                },
                {
                    "value": ".NET Core 2.0",
                    "text": ".NET Core 2.0"
                },
                {
                    "value": ".NET Core 2.1",
                    "text": ".NET Core 2.1"
                },
                {
                    "value": ".NET Core 2.2",
                    "text": ".NET Core 2.2"
                },
                {
                    "value": ".NET Core 1.6",
                    "text": ".NET Core 1.6"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "framework_type_other_net",
            "order": 18,
            "visibility": "framework_type_net == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the target framework",
            "watermarkText": "Mono, .NET Core 3.0 Preview",
            "required": false
        },
        {
            "id": "nodejs_version",
            "order": 19,
            "visibility": "language_used == Node.js",
            "controlType": "dropdown",
            "displayLabel": "What is the version of Node.js?",
            "dropdownOptions": [
                {
                    "value": "Node.js 10.x",
                    "text": "Node.js 10.x"
                },
                {
                    "value": "Node.js 9.x",
                    "text": "Node.js 9.x"
                },
                {
                    "value": "Node.js 8.x",
                    "text": "Node.js 8.x"
                },
                {
                    "value": "Node.js 7.x",
                    "text": "Node.js 7.x"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Older"
                }
            ],
            "required": false
        },
        {
            "id": "javascript_apptype",
            "order": 20,
            "visibility": "language_used == JavaScript",
            "controlType": "dropdown",
            "displayLabel": "What type of application is the JavaScript SDK monitoring?",
            "dropdownOptions": [
                {
                    "value": "Dynamic Application (Java, .NET)",
                    "text": "Dynamic Application (Java, .NET)"
                },
                {
                    "value": "Static HTML",
                    "text": "Static HTML"
                },
                {
                    "value": "Single Page Application (SPA)",
                    "text": "Single Page Application (SPA)"
                }
            ],
            "required": false
        },
        {
            "id": "lightup_type",
            "order": 21,
            "controlType": "dropdown",
            "displayLabel": "What were the steps to instrument the app?",
            "dropdownOptions": [
                {
                    "value": "Development Environment Plugin",
                    "text": "Development Environment Plugin"
                },
                {
                    "value": "Pacakge Manager",
                    "text": "Pacakge Manager"
                },
                {
                    "value": "Azure Integration (App Service, Function App, etc.)",
                    "text": "Azure Integration (App Service, Function App, etc.)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "lightup_type_other",
            "order": 22,
            "visibility": "lightup_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the steps to instrument the app:",
            "watermarkText": "PowerShell Scripts, manually copied packages, Status Monitor",
            "required": false
        },
        {
            "id": "sdk_Version",
            "order": 23,
            "controlType": "textbox",
            "displayLabel": "[Optional] What is the package version of AI SDK?",
            "watermarkText": "2.8.1, 2.6.1, 1.2.0, 1.0.8",
            "required": false
        },
        {
            "id": "custom_config",
            "order": 24,
            "controlType": "multilinetextbox",
            "displayLabel": "Any custom configuration, custom telemetry collection, extensiblity on top of default SDK?",
            "watermarkText": "Telemetry Processor to filter out fast Dependency calls",
            "required": false
        },
        {
            "id": "appservice_id",
            "order": 25,
            "visibility": "environment_type == Azure Web App or App Service",
            "controlType": "dropdown",
            "displayLabel": "Please select the app service where this application is deployed.",
            "watermarkText": "App Service XYZ",
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
            "order": 26,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start occuring?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 27,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the following details",
            "required": true,
            "watermarkText": "A detailed scenario of the error condition, troubleshooting done so far, log files if any, timestamp, screenshots, and any other relevant information.",
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Troubleshooting done so far"
                },
                {
                    "text": "Log files if any"
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
