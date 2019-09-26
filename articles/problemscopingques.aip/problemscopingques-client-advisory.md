<properties
	pageTitle="Azure Information Client - Advisory"
	description="Azure Information Client - Advisory"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32592926"
    productPesIds="14997"
    cloudEnvironments="Public"
    articleId="scoping_client_advisory"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Advisory",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Export AIP logs using Settings button in AIP Viewer - Export Logs",
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
                "displayLabel": "What version are you using? You can get the latest version at http://aka.ms/getaip",
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
