<properties
	pageTitle="EmbeddedCSDKIssues"
	description="Embedded-C-SDK-Issues"
	ms.author="wduraes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32596697"
	productPesIds="16122"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="a3cd8d2d-eadb-4acd-a102-4ebb8b9b51c2"
	ownershipId="AzureIot_IotHub"
/>
# Issues with the Embedded C SDK
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Embedded C SDK Issues",
    "fileAttachmentHint": "",
    "formElements":
    [
		{
            "id": "problem_start_time", //This is a required value
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
		{
			"id": "sdk_version",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Version",
			"watermarkText": "What is the version of Embedded C SDK you're using? ",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints":
			[
				{
					"text": "SDK Version."
				},
				{
					"text": "Version of the Embedded C SDK you're using."
				}
			]
		},
		{
			"id": "external_components",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Version",
			"watermarkText": "Which external components does the solution use? ",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints":
			[
				{
					"text": "External components."
				},
				{
					"text": "Please list which libraries for MQTT, TLS and socket your aplication uses and any external Hardware components like HSM chips."
				}
			]
		},
		{
			"id": "reconnection_retry_issues",
			"order": 4,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Are you experiencing reconnection / retry issues?",
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
					"text": "Don't Know"
				}
			],
			"required": false
		},
		{
			"id": "internet_connectivity",
			"order": 5,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Is the device able to connect to Internet?",
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
					"text": "Don't Know"
				}
			],
			"required": false
		},
		{
			"id": "firewall_connectivity",
			"order": 6,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Is the device using any proxy or firewall?",
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
					"text": "Don't Know"
				}
			],
			"required": false
		},
		{
			"id": "Certificate_issues",
			"order": 7,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Are root certificates set on TLS layer for server validation?",
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
					"value": "No certificates",
					"text": "Don't use certificates"
				},
				{
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": false
		},
		{
			"id": "SAS_issues",
			"order": 8,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Is the SAS token still valid (not expired)?",
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
					"value": "No SAS",
					"text": "Don't use SAS Tokens"
				},
				{
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": false
		},
		{
			"id": "problem_description",
			"order": 10,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints":
			[
				{
					"text": "Issue description."
				},
				{
					"text": "Please provide any aditional detail to the problem."
				}
			]
		}
	]
}
---