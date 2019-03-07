<properties
	articleId="problemscopingques-appinsights-generic"
	pageTitle="Application Insights"
	description="Application Insights"
	authors="debugthings"
	ms.author="jamdavi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632994, 32546625, 32613001, 32402602, 32602201, 32402604, 32402605, 32602210, 32602213, 32632995, 32546622, 32602216, 32609670, 32602220, 32422335, 32402614, 32602206, 32632996, 32602207, 32602208, 32632997, 32609669, 32602211, 32602214, 32602218, 32402641, 32632981, 32632982, 32632983, 32632984, 32632985, 32632986, 32632987, 32632988, 32632989, 32632990, 32632991, 32632992, 32632993, 32402626, 32602209, 32602204, 32602205, 32602222, 32632998, 32633000, 32402629, 32402637, 32546624, 32602225, 32602224, 32402633, 32632999, 32602223, 32629553, 32402638"
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Application Insights
---
{
	"resourceRequired": true,
	"title": ".NET SDK",
	"fileAttachmentHint": "File Upload recommendations: ApplicationInsights.config; packages.config or PackageReferences; web.config or app.config; AppSettings.json; ApplicationInsights.xml; AI-Agent.xml. Please edit files to remove sensitive information",
	"formElements": [{
			"id": "environment_type",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "How is the monitored app deployed?",
			"dropdownOptions": [
				{
					"value": "Azure VM",
					"text": "Azure VM"
				},{
					"value": "On-Premises VM",
					"text": "On-Premises VM"
				},{
					"value": "Azure Web App or App Service",
					"text": "Azure Web App or App Service"
				},{
					"value": "Azure Cloud Service",
					"text": "Azure Cloud Service"
				},{
					"value": "Azure Functions",
					"text": "Azure Functions"
				},{
					"value": "Azure Service Fabric",
					"text": "Azure Service Fabric"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "environment_type_other",
			"order": 2,
            "visibility": "environment_type == Other",
			"controlType": "textbox",
			"displayLabel": "Please describe how the application is deployed:",
			"watermarkText": "Kubernetes, Cloud Provider XYZ",
			"required": true
		}, {
			"id": "os_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What is the operating system?",
			"dropdownOptions": [
				{
					"value": "Windows",
					"text": "Windows"
				},{
					"value": "Linux",
					"text": "Linux"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "os_type_other",
			"order": 4,
            "visibility": "os_type == Other",
			"controlType": "textbox",
			"displayLabel": "OS name and version:",
			"watermarkText": "MacOS 13.2",
			"required": true
		}, {
			"id": "os_type_linux",
			"order": 5,
            "visibility": "os_type == Linux",
			"controlType": "textbox",
			"displayLabel": "Linux distribution and version:",
			"watermarkText": "Ubuntu 16.4",
			"required": true
		}, {
			"id": "os_type_windows",
			"order": 6,
            "visibility": "os_type == Windows",
			"controlType": "textbox",
			"displayLabel": "Windows version:",
			"watermarkText": "Windows Server 2016",
			"required": true
		}, {
			"id": "language_used",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "What is the language of the technology that has the issue?",
			"dropdownOptions": [
				{
					"value": ".NET",
					"text": ".NET"
				},{
					"value": "Java",
					"text": "Java"
				},{
					"value": "Node.JS",
					"text": "Node.JS"
				},{
					"value": "JavaScript",
					"text": "JavaScript"
				}],
			"required": true
		},{
			"id": "javasdk_version",
			"order": 8,
            "visibility": "language_used == Java",
			"controlType": "dropdown",
			"displayLabel": "What version of Java are you using?",
			"dropdownOptions": [
				{
					"value": "Java 6",
					"text": "Java 6"
				},{
					"value": "Java 7",
					"text": "Java 7"
				},{
					"value": "Java 8",
					"text": "Java 8"
				},{
					"value": "Java 9",
					"text": "Java 9"
				},{
					"value": "Java 10",
					"text": "Java 10"
				},{
					"value": "Java 11",
					"text": "Java 11"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "webserver_type_java",
			"order": 9,
            "visibility": "language_used == Java",
			"controlType": "dropdown",
			"displayLabel": "What Java web server is being used?",
			"dropdownOptions": [
				{
					"value": "Apache Tomcat",
					"text": "Apache Tomcat"
				},{
					"value": "JBoss",
					"text": "JBoss"
				},{
					"value": "Jetty",
					"text": "Jetty"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "webserver_type_other",
			"order": 10,
            "visibility": "webserver_type_java == Other",
			"controlType": "textbox",
			"displayLabel": "What is the name of your web server?",
			"watermarkText": "WebLogic 10; WebSphere",
			"required": true
		}, {
			"id": "framework_type_java",
			"order": 11,
            "visibility": "language_used == Java",
			"controlType": "dropdown",
			"displayLabel": "What Java Web Framework are you using?",
			"dropdownOptions": [
				{
					"value": "J2EE",
					"text": "J2EE"
				},{
					"value": "Spring MVC",
					"text": "Spring MVC"
				},{
					"value": "Spring Boot",
					"text": "Spring Boot"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "framework_type_version_java",
			"order": 12,
            "visibility": "language_used == Java",
			"controlType": "textbox",
			"displayLabel": "What is the framework version being used",
			"watermarkText": "SpringBoot 2.1.0",
			"required": true
		}, {
			"id": "jvm_agent",
			"order": 13,
            "visibility": "language_used == Java",
			"controlType": "textbox",
			"displayLabel": "Is the JVM Agent Being used for dependency collection?",
			"watermarkText": "Yes or No",
			"required": true
		}, {
			"id": "app_type_net",
			"order": 14,
            "visibility": "language_used == .NET",
			"controlType": "dropdown",
			"displayLabel": "What is the application technology?",
			"dropdownOptions": [
				{
					"value": "ASP.NET Core",
					"text": "ASP.NET Core"
				},{
					"value": "ASP.NET Core Web API",
					"text": "ASP.NET Core Web API"
				},{
					"value": "ASP.NET Core MVC",
					"text": "ASP.NET Core MVC"
				},{
					"value": "ASP.NET Web API",
					"text": "ASP.NET Web API"
				},{
					"value": "ASP.NET MVC",
					"text": "ASP.NET MVC"
				},{
					"value": "WCF",
					"text": "WCF"
				},{
					"value": "Web Job",
					"text": "Web Job"
				},{
					"value": "Console",
					"text": "Console"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		},{
			"id": "app_type_other",
			"order": 15,
            "visibility": "app_type_net == Other",
			"controlType": "textbox",
			"displayLabel": "Please describe the application technology stack:",
			"watermarkText": "OWIN",
			"required": true
		}, {
			"id": "framework_type_net",
			"order": 16,
            "visibility": "language_used == .NET",
			"controlType": "dropdown",
			"displayLabel": "What is the target .NET Framework?",
			"dropdownOptions": [
				{
					"value": ".NET 4.5",
					"text": ".NET 4.5"
				},{
					"value": ".NET 4.6",
					"text": ".NET 4.6"
				},{
					"value": ".NET 4.7",
					"text": ".NET 4.7"
				},{
					"value": ".NET Core 2.0",
					"text": ".NET Core 2.0"
				},{
					"value": ".NET Core 2.1",
					"text": ".NET Core 2.1"
				},{
					"value": ".NET Core 2.2",
					"text": ".NET Core 2.2"
				},{
					"value": ".NET Core 1.6",
					"text": ".NET Core 1.6"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "framework_type_other_net",
			"order": 17,
            "visibility": "framework_type_net == Other",
			"controlType": "textbox",
			"displayLabel": "Please describe the target framework",
			"watermarkText": "Mono, .NET Core 3.0 Preview",
			"required": true
		}, {
			"id": "lightup_type",
			"order": 18,
			"controlType": "dropdown",
			"displayLabel": "What were the steps to instrument the app?",
			"dropdownOptions": [
				{
					"value": "Development Environment Plugin",
					"text": "Development Environment Plugin"
				},{
					"value": "Pacakge Manager",
					"text": "Pacakge Manager"
				},{
					"value": "Azure Integration (App Service, Function App, etc.)",
					"text": "Azure Integration (App Service, Function App, etc.)"
				},{
					"value": "Other",
					"text": "Other"
				}],
			"required": true
		}, {
			"id": "lightup_type_other",
			"order": 19,
            "visibility": "lightup_type == Other",
			"controlType": "textbox",
			"displayLabel": "Please describe the steps to instrument the app:",
			"watermarkText": "PowerShell Scripts, manually copied packages, Status Monitor",
			"required": true
		}, {
			"id": "sdk_Version_net",
			"order": 20,
			"controlType": "textbox",
            "displayLabel": "[Optional] What is the package version of AI SDK?",
			"watermarkText": "2.8.1, 2.6.1",
			"required": false
		}, {
			"id": "custom_config",
			"order": 21,
			"controlType": "multilinetextbox",
			"displayLabel": "Any custom configuration, custom telemetry collection, extensiblity on top of default SDK?",
            "watermarkText": "Telemetry Processor to filter out fast Dependency calls",
			"required": false
		}, {
			"id": "appservice_id",
			"order": 22,
            "visibility": "environment_type == Azure Web App or App Service",
			"controlType": "dropdown",
			"displayLabel": "Please select the app service where this application is deployed.",
			"watermarkText": "App Service XYZ",
            "dynamicDropdownOptions": {
				"uri":"/resources?api-version=2014-04-01-preview&%24filter=(subscriptionId%20eq%20'{subscriptionid}')%20and%20(resourceType%20eq%20'microsoft.web%2Fsites')",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
			"dropdownOptions": [{
					"value": "Unable to get the list of App Services",
					"text": "Unable to get the list of App Services"
				}],
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 23,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start occuring?",
			"required": true
		},{
			"id": "problem_description",
			"order": 24,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide the following details",
			"required": true,
			"watermarkText": "A detailed scenario of the error condition, troubleshooting done so far, log files if any, timestamp, screenshots, and any other relevant information.",
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Expected behavior, actual behavior"
				}, {
					"text": "Troubleshooting done so far"
				}, {
					"text": "Log files if any"
				}, {
					"text": "Timestamps"
				}, {
					"text": "Screenshots"
				}
			]
		}
	]
}
---
