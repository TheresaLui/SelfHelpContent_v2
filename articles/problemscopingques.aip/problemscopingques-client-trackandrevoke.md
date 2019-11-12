<properties
	pageTitle="Azure Information Client - Track and Revoke"
	description="Azure Information Client - Track and Revoke"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584380"
    productPesIds="14997"
    cloudEnvironments="Public"
    articleId="scoping_client_track_revoke"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Client Track and Revoke",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Export AIP logs Using Protect/Sensitivity button - Help and Feedback - Export Logs",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which AIP client are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure Information Protection Classic Client",
                            "text": "Azure Information Protection Classic Client"
                        },
                        {
                            "value": "Azure Information Protection Unified Labeling Client",
                            "text": "Azure Information Protection Unified Labeling Client"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                "id": "version_number",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "What version are you using? You can get the latest version at https://www.microsoft.com/download/details.aspx?id=53018",
                "required": true
                },{
                    "id": "sccmigrate",
                    "order": 5,
                    "visibility": "client_type == Azure Information Protection Classic Client",
                    "controlType": "dropdown",
                    "displayLabel": "Did you activate Unified Labeling in your tenant?",
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
                    "order": 7,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
