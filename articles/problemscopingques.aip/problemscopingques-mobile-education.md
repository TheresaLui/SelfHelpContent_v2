<properties
	pageTitle="Azure Information Protection - AIP Mobile Education"
	description="Azure Information Protection - AIP Mobile Education"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584341"
    productPesIds="14997"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    articleId="scoping_mobile_app_education"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Azure Information Protection Mobile Education",
				"subscriptionRequired": false,
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "app_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which OS are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "iOS",
                            "text": "iOS"
                        },
                        {
                            "value": "Android",
                            "text": "Android"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                    "id": "latest_version",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Did you upgrade your app to the latest version in the store?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
                        }
                    ],
                    "required": false
                },{
                    "id": "aiporoffice",
                    "order": 6,
                    "controlType": "dropdown",
                    "displayLabel": "Is the issue related to AIP Viewer app or Office for Mobile Apps?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "AIP Viewer",
                            "text": "AIP Viewer"
                        },
                        {
                            "value": "Office for Mobile",
                            "text": "Office for Mobile"
                        }
                    ],
                    "required": false
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
