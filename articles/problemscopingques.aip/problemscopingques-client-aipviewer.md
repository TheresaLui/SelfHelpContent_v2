<properties
	pageTitle="Azure Information Client - Viewer Issues"
	description="Azure Information Client - Viewer Issues"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584328"
    productPesIds="14997"
    cloudEnvironments="Public"
    articleId="scoping_viewer_issues"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Viewer Issues",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Export AIP logs Using Protect/Sensitivity - Help and Feedback - Export Logs",
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
                "id": "version_number_classic",
                "order": 3,
                "visibility": "client_type == Azure Information Protection Classic Client",
                "controlType": "dropdown",
                "displayLabel": "What version are you using? if it's not listed, please upgrade to the latest version at http://aka.ms/getaip",
                "watermarkText": "Choose an option",
                "dropdownOptions": [
                    {
                        "value": "1.53.10.0",
                        "text": "1.53.10.0"
                    },
                    {
                        "value": "1.48.204.0",
                        "text": "1.48.204.0"
                    },
                    {
                        "value": "1.41.51.0",
                        "text": "1.41.51.0"
                    },
                    {
						"value": "dont_know_answer",
						"text": "I don't know"
                    }
                ],
                "required": true
                },{
                "id": "version_number_ul",
                "order": 4,
                "visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "dropdown",
                "displayLabel": "What version are you using? if it's not listed, please upgrade to the latest version at http://aka.ms/getaip",
                "watermarkText": "Choose an option",
                "dropdownOptions": [
                    {
                        "value": "2.2.19.0",
                        "text": "2.2.19.0"
                    },
                    {
                        "value": "2.2.14.0",
                        "text": "2.2.14.0"
                    },
                    {
                        "value": "2.0.779.0",
                        "text": "2.0.779.0"
                    },
                    {
                        "value": "2.0.778.0",
                        "text": "2.0.778.0"
                    },
                    {
						"value": "dont_know_answer",
						"text": "I don't know"
                    }
                ],
                "required": true
                },{
                    "id": "problem_description",
                    "order": 7,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": false,
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
