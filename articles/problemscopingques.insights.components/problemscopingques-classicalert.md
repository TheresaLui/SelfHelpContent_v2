<properties
	pageTitle="Metrics Alert (Classic)"
	description="Metrics Alert (Classic)"
	authors="debugthings"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613002"
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-classicalert"
/>
# Metrics Alert (Classic)
---
{
	"resourceRequired": true,
	"title": "Metrics Alert (Classic)",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "classic_alert_id",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the affected Metrics Alert (Classic) resource name.",
			"watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resources?api-version=2017-06-01&%24filter=tagname%20eq%20'hidden-link%3A%2Fsubscriptions%2F{subscriptionid}%2FresourceGroups%2F{resourcegroup}%2Fproviders%2FMicrosoft.Insights%2Fcomponents%2F{resourcename}'%20and%20tagvalue%20eq%20'Resource'",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
			"dropdownOptions": [{
					"value": "Unable to get the list of Alerts",
					"text": "Unable to get the list of Alerts"
				}],
			"required": false
		}, {
			"id": "classic_alert_reason",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is the primary issue with this alert rule?",
			"dropdownOptions": [{
					"value": "I did not receive an e-mail notification even though the alert was triggered.",
					"text": "I did not receive an e-mail notification even though the alert was triggered."
				}, {
					"value": "I did not receive a web hook notification even though the alert was triggered.",
					"text": "I did not receive a web hook notification even though the alert was triggered."
				}, {
					"value": "My alert should have triggered with the given metric conditions.",
					"text": "My alert should have triggered with the given metric conditions."
				}, {
					"value": "The issue for my alert is not listed here.",
					"text": "The issue for my alert is not listed here."
				}],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Explain with as much detail what is occurring with the classic alert and what troubleshooting you've done so far."
				}
			]
		}
	]
}
---