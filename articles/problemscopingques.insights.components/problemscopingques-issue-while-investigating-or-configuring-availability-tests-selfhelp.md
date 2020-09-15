<properties
	articleId="problemscopingques-issue-while-investigating-or-configuring-availability-tests-selfhelp"
	pageTitle="Issue while investigating or configuring Availability tests"
	description="Issue while investigating or configuring Availability tests"
	authors="gearama,zakima"
	ms.author="gearama"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729575, 32729576, 32729577, 32729582, 32729588"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Issue while investigating or configuring Availability tests
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue while investigating or configuring Availability tests",
	"fileAttachmentHint": "",
	"diagnosticCard": {
	"title": "Availability Test Troubleshooter",
	"description": "Our Availability Test Troubleshooter can help you troubleshoot and solve your problem.",
	"insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
	},
	"formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "classic_alert_id",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Please select the impacted Availability Tests resource.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.insights/components/{resourcename}/webtests?noLargeObjects=true&skipConfig=true&api-version=2015-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Unable to get the list of availability tests for this resource"
            }
          }
        }
	]
}
---