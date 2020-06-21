<properties
	articleId="problemscopingques-sdk-net"
	pageTitle=".NET SDK"
	description=".NET SDK"
	authors="debugthings, Dmitry-Matveev"
	ms.author="jamdavi, dmitmatv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32402631"
	productPesIds="15693"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# .Net SDK
---
{
    "resourceRequired": true,
    "title": ".NET SDK",
    "fileAttachmentHint": "File Upload recommendations: ApplicationInsights.config; packages.config or PackageReferences; web.config or app.config; AppSettings.json. Please edit files to remove sensitive information",
    "formElements": [
        {
            "id": "environment_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How is the monitored app deployed?",
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
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                }
            ],
            "required": true
        },
        {
            "id": "environment_type_other",
            "order": 2,
            "visibility": "environment_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe how the application is deployed:",
            "watermarkText": "Kubernetes, Cloud Provider XYZ",
            "required": false
        },
        {
            "id": "os_type",
            "order": 3,
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "os_type_other",
            "order": 4,
            "visibility": "os_type == Other",
            "controlType": "textbox",
            "displayLabel": "OS name and version:",
            "watermarkText": "MacOS 13.2",
            "required": false
        },
        {
            "id": "os_type_linux",
            "order": 5,
            "visibility": "os_type == Linux",
            "controlType": "textbox",
            "displayLabel": "Linux distribution and version:",
            "watermarkText": "Ubuntu 16.4",
            "required": false
        },
        {
            "id": "os_type_windows",
            "order": 6,
            "visibility": "os_type == Windows",
            "controlType": "textbox",
            "displayLabel": "Windows version:",
            "watermarkText": "Windows Server 2016",
            "required": false
        },
        {
            "id": "app_type",
            "order": 7,
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
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                }
            ],
            "required": true
        },
        {
            "id": "app_type_other",
            "order": 8,
            "visibility": "app_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the application technology stack:",
            "watermarkText": "OWIN",
            "required": false
        },
        {
            "id": "framework_type",
            "order": 9,
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "framework_type_other",
            "order": 10,
            "visibility": "framework_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the target framework",
            "watermarkText": "Mono, .NET Core 3.0 Preview",
            "required": false
        },
        {
            "id": "lightup_type",
            "order": 11,
            "controlType": "dropdown",
            "displayLabel": "What were the steps to instrument the app?",
            "dropdownOptions": [
                {
                    "value": "Visual Studio Plugin",
                    "text": "Visual Studio Plugin"
                },
                {
                    "value": "Visual Studio Nuget Package Manager",
                    "text": "Visual Studio Nuget Package Manager"
                },
                {
                    "value": "App Service Extension (Manual)",
                    "text": "App Service Extension (Manual)"
                },
                {
                    "value": "App Service Extension (Automated)",
                    "text": "App Service Extension (Automated)"
                },
                {
                    "value": "Status Monitor",
                    "text": "Status Monitor"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                }
            ],
            "required": true
        },
        {
            "id": "lightup_type_other",
            "order": 12,
            "visibility": "lightup_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe the steps to instrument the app:",
            "watermarkText": "PowerShell Scripts",
            "required": false
        },
        {
            "id": "lightup_type_ext_version",
            "order": 13,
            "visibility": "lightup_type == App Service Extension (Manual)",
            "controlType": "textbox",
            "displayLabel": "What is the AI App Services extension version?",
            "watermarkText": "1.3",
            "required": false
        },
        {
            "id": "lightup_type_sm_version",
            "order": 14,
            "visibility": "lightup_type == Status Monitor",
            "controlType": "textbox",
            "displayLabel": "What is the Status Monitor version?",
            "watermarkText": "2.4",
            "required": false
        },
        {
            "id": "sdk_Version",
            "order": 15,
            "controlType": "textbox",
            "displayLabel": "[Optional] What is the Nuget package version of AI SDK?",
            "watermarkText": "2.8.1, 2.6.1",
            "required": false
        },
        {
            "id": "custom_config",
            "order": 16,
            "controlType": "multilinetextbox",
            "displayLabel": "Any custom configuration, custom telemetry collection, extensiblity on top of default SDK?",
            "watermarkText": "Telemetry Processor to filter out fast Dependency calls",
            "required": false
        },
        {
            "id": "appservice_id",
            "order": 17,
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
            "order": 18,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start occuring?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 19,
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
