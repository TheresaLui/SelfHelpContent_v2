<properties
	pageTitle="Azure Information Protection - Protecting and Opening Content - Cannot open protected content (External)"
	description="Azure Information Protection - Protecting and Opening Content - Cannot open protected content (External)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32727937"
    productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_protectopencontent_cantopenexternal"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Unable to apply a protection label",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Export AIP logs Using Protect/Sensitivity button - Help and Feedback - Export Logs",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which file are you trying to open?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "office_files",
                            "text": "Office Files (Word, Excel, PowerPoint)"
                        },
                        {
                            "value": "email_files",
                            "text": "Email"
                        },
                        {
                            "value": "other_files",
                            "text": "Other Files"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                    "id": "office_type",
                    "order": 6,
                    "controlType": "dropdown",
                    "displayLabel": "Which Office version are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Office 20XX Standard (Not supported for Protection)",
                            "text": "Office 20XX Standard (Not supported for Protection)"
                        },
                        {
                            "value": "Office 20XX ProPlus (Microsoft Apps for Enterprise)",
                            "text": "Office 20XX ProPlus (Microsoft Apps for Enterprise)"
                        },
                        {
                            "value": "Office 365 Click-To-Run",
                            "text": "Office 365 Click-To-Run"
                        },	                    {
							"value": "dont_know_answer",
							"text": "None of the above"
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
