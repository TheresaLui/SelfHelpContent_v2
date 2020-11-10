<properties
pageTitle="Top common problems for Application Insights"
description="Menu based workflow document for top AI problems"        
service="microsoft.insights"
resource="components"
authors="gansmore"
ms.author="jamdavi"
displayOrder=""
articleId="8eab3943-d5a7-4823-aeb0-faf5420d7184"
selfHelpType="diagnoseandsolve"
productPesIds="15693"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Top common problems for Application Insights?
---
{
"$schema":"SelfHelpContent",
	"commonProblems": [{
      			"id": "Where_is_my_data",
			"title": "Where is my data?",
			"description": "I am not able to see any data in the Azure Portal or the Analytics Portal",
			"category": "Data Collection",
			"searchTags": "missing data, no data, empty, blank",
			"supportTopicId": "32602225",
			"commonSolutionArticleId": "appinsights-missing-ingestion-data",
			"symptomId": "ApplicationInsightsMissingDataDiagnostic"
		}, {
			"id": "Why_is_my_data_not_showing_up_right_away",
      "title": "Why is my data not showing up right away?",
			"description": "I am sending data, but it is not showing up for a long period of time.",
			"category": "Data Collection",
			"searchTags": "latency, slow, collection, ingestion",
			"supportTopicId": "32546624",
			"commonSolutionArticleId": "insights_datalatency"
		},
		{
      "id": "Why_can_I_not_see_some_of_my_data",
      "title": "Why can I not see some of my data?",
			"description": "I am not able to see some data in the Azure Portal or the Analytics Portal; for example I see Performance data but not User Behavior data.",
			"category": "Data Collection",
			"searchTags": "partial data, no metric, usage",
			"supportTopicId": "32602224",
			"commonSolutionArticleId": "insights_usage_blade",
			"symptomId": "ApplicationInsightsMissingUsageDataDiagnostic"
		}, 
		{				    
			"id": "Why_did_I_not_receive_an_e-mail_notification",
      "title": "Why did I not receive an e-mail notification?",
			"description": "I can see that an alert was triggered but no e-mail notification was sent.",
			"category": "Alerts",
			"searchTags": "e-mail, notification, wrong people",			
			"supportTopicId": "32546625",
			"commonSolutionArticleId": "insights_missingemail"
		}, 
		{				    
			"id": "How_do_I_monitor_an_App_Service",
      "title": "How do I monitor an App Service?",
			"description": "I want to add Application Insights monitoring to my App Service.",
			"category": "Configuration",
			"searchTags": "app service, web app",
			"supportTopicId": "32602209",
			"commonSolutionArticleId": "insights_appservice"
		}, 
		{				    
			"id": "How_do_I_troubleshoot_my_Web_Test",
      "title": "How do I troubleshoot my Web Test?",
			"description": "I see an error on my webtest but don't know how to troubleshoot.",
			"category": "Web Tests",
			"searchTags": "availability test, web test",			
			"supportTopicId": "32422336",
			"commonSolutionArticleId": "insights_availabilitytests"
		}, 
		{				    
			"id": "I_need_help_configuring_the_.NET_SDK.",
      "title": "I need help configuring the .NET SDK.",
			"description": "I want to configure my .NET SDK to add or remove additional monitoring.",
			"category": "Configuration",
			"searchTags": ".net, iis, dotnetcore",			
			"supportTopicId": "32402631",
			"commonSolutionArticleId": "insights_dotnetsdk"
		}, 
		{				    
			"id": "I_need_help_configuring_the_Java_SDK.",
      "title": "I need help configuring the Java SDK.",
			"description": "I want to configure my Java SDK to add or remove additional monitoring.",
			"category": "Configuration",
			"searchTags": "java, tomcat, jboss, jvm",			
			"supportTopicId": "32402632",
			"commonSolutionArticleId": "insights_javasdk"
		}, 
		{				    
			"id": "I_need_help_configuring_the_OpenCensus_Python_SDK.",
      "title": "I need help configuring the OpenCensus Python SDK.",
			"description": "I want to configure my OpenCensus Python SDK to add or remove additional monitoring.",
			"category": "Configuration",
			"searchTags": "python, flask, django",			
			"supportTopicId": "32681426",
			"commonSolutionArticleId": "insights_python_configure"
		},
		{
      		"id": "Where_is_my_data_for_OpenCensus_Python_SDK",
			"title": "Where is my data for OpenCensus Python SDK?",
			"description": "I am not able to see any data in the Azure Portal or the Analytics Portal",
			"category": "Data Collection",
			"searchTags": "missing data, no data, empty, blank, python",
			"supportTopicId": "32681426",
			"commonSolutionArticleId": "insights_python_data"
		}
	],
	"troubleshootingTools": []
}
---
