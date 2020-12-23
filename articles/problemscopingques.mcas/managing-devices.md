<properties
	pageTitle="Cloud App Security - Access and session controls - Managing Devices"
	description="Cloud App Security - Access and session controls - Managing Devices"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32743390"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_MCAS_Managing Devices"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_CAAC"
/>
# Access and session controls - Managing Devices
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Access and session controls - Managing Devices",
				"fileAttachmentHint": "Please attach a screenshot of the alert/policy",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "MCAS_URL",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Please provide your MCAS tenant URL (e.g: https://(domain name).portal.cloudappsecurity.com/)",
                    "required": true
                },
				{
                    "id": "alert_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please provide the alert ID. You can find it from the URL of the alert itself",
                    "required": false
				},
				{
                    "id": "Without_Proxy",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "If relevant, once you exclude the proxy service, does this issue still occur? If yes, please create a ticket on the relevant service versus MCAS.",
                    "watermarkText": "Choose an option",
                    "dropdownOptions":
					[
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Not relevant"
                        }
                    ],
					"required": false
				},
				{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
