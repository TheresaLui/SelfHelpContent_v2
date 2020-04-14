<properties
	pageTitle="RMS Connector - Exchange"
	description="RMS Connector - Exchange"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584345"
    productPesIds="14997"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    articleId="scoping_rms_exchange"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "RMS Connector - Exchange",
				"subscriptionRequired": false,
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which Exchange Verison are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Exchange 2010",
                            "text": "Exchange 2010"
                        },
                        {
                            "value": "Exchange 2013 and up",
                            "text": "Exchange 2013 and up"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
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
