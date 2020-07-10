<properties
	pageTitle="Azure Information Client - Unable to open protected content"
	description="Azure Information Client - Unable to open protected content"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584381"
    productPesIds="14997"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    articleId="scoping_unable_to_open_protected_content"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Unable to open protected content",
				"subscriptionRequired": false,
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What program are you using to open the protected content?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "AIP Viewer",
                            "text": "AIP Viewer"
                        },
                        {
                            "value": "Office",
                            "text": "Office"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                    "id": "isexternal",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Is the person unable to open the content an external user?",
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
                    "id": "ismfaenabled",
                    "order": 6,
                    "visibility": "isexternal == Yes",
                    "controlType": "dropdown",
                    "displayLabel": "Do you have MFA or conditional access policy enabled?",
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
                    "id": "networkreq",
                    "order": 7,
                    "controlType": "dropdown",
                    "displayLabel": "Did you follow all networking requirements at https://docs.microsoft.com/azure/information-protection/requirements#firewalls-and-network-infrastructure ?",
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
