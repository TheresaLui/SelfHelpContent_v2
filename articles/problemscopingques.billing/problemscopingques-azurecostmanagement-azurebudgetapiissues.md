<properties
	pageTitle="Azure Cost Management"
	description="Azure Cost Managements"
	articleId="azurebudgetapiissues-problemscopingquestion"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615281,32615284"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Billing and Payment Issues
---
{
	"resourceRequired": false,
	"title": "Azure Cost Management",
	"fileAttachmentHint": "",
	"formElements": [
      {
      "id": "problem_start_time",
      "visibility": null,
      "order": 4,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
  },
  {
			"id": "problem_description",
			"order": 1,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Subscription ID"
				}, {
					"text": "Email ID accessing the subscription"
				}, {
					"text": "Screenshot of the error"
				}, {
					"text": "Browser network trace – <a href='https://blogs.msdn.microsoft.com/benjaminperkins/2016/10/18/capture-a-trace-for-troubleshooting-azure-portal-issues/'>how to</a>"
				}
			]
		}
	]
}
---
