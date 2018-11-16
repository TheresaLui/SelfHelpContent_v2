<properties
	pageTitle="Application Gateway URL"
	description="Application Gateway URL"
	authors="radwiv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32436964, 32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
	productPesIds="15922"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Application Gateway URL
---
{
	"resourceRequired": true,
	"title": "Application Gateway URL",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "app_gw_url",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Please provide the URL you are using to access the Application Gateway.",
			"watermarkText": "Provide full URL such as http://www.contoso.com:8081/home.aspx",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "additional_details",
			"order": 3,
			"controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
			"displayLabel": "Details of the issue.",
			"watermarkText": "Provide additional information about your issue including error messages.",
			"required": false
		}, {
			"id": "learn_more_text",
			"order": 4,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
		}
	]
}
---
