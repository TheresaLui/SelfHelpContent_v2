<properties
	pageTitle="Azure Information Client - Performance Issues"
	description="Azure Information Client - Performance Issues"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584367"
    productPesIds="14997"
    cloudEnvironments="Public"
    articleId="scoping_perofrmance_issues"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Performance Issues",
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
				"visibility": "client_type == Azure Information Protection Classic Client",
                "controlType": "textbox",
                "displayLabel": "What version are you using? View the Info Balloon on the right for more details",
				"infoBalloonText": "Verify that you use a supported version <a href='https://docs.microsoft.com/azure/information-protection/rms-client/client-version-release-history#servicing-information-and-timelines'>Here</a>",
                "required": true
                },{
                "id": "version_number_ul",
                "order": 4,
				"visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "textbox",
                "displayLabel": "What version are you using? View the Info Balloon on the right for more details",
				"infoBalloonText": "Verify that you use a supported version <a href='https://docs.microsoft.com/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history'>Here</a>",
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
                    "id": "publishlabels",
                    "order": 6,
                    "visibility": "client_type == Azure Information Protection Unified Labeling Client",
                    "controlType": "dropdown",
                    "displayLabel": "Did you publish labels in the SCC portal?",
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
