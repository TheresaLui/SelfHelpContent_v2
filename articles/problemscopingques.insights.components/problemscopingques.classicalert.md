<properties
	pageTitle="Metrics Alert (Classic)"
	description="Metrics Alert (Classic)"
	authors="debugthings"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613002"
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Metrics Alert (Classic)
---
{
	"resourceRequired": true,
	"title": "Affected Metrics Alert (Classic)",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "classic_alert_id",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the affected Metrics Alert (Classic) resource name.",
			"watermarkText": "Choose an option",
			"dropdownOptions": null,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resources?api-version=2017-06-01&%24filter=tagname%20eq%20'hidden-link%3A%2Fsubscriptions%2F{subscriptionid}%2FresourceGroups%2F{resourcegroup}%2Fproviders%2FMicrosoft.Insights%2Fcomponents%2F{resourcename}'%20and%20tagvalue%20eq%20'Resource'",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+/.+$"
            }
			"required": false
		}, {
			"id": "classic_alert_reason",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What is the primary issue with this alert rule?",
			"dropdownOptions": [{
					"value": "MISSINGEMAIL",
					"text": "I did not receive an e-mail notification even though the alert was triggered."
				}, {
					"value": "MISSINGWEBHOOK",
					"text": "I did not receive a web hook notification even though the alert was triggered."
				}, {
					"value": "NOTRTRIGGERED",
					"text": "My alert should have triggered with the given metric conditions."
				},
			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
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
					"text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."
				}
			]
		}
	]
}
---