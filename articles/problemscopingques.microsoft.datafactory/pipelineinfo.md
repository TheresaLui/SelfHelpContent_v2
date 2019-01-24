<properties
	pageTitle="Azure Data Factory Pipeline Info"
	description="Scoping questions to gather Azure Data Factory pipeline information"
	authors="lisaliu"
    ms.author="lisaliu"
	selfHelpType="problemScopingQuestions" 
    supportTopicIds="32629483, 32629550, 32629529, 32629491, 32629490, 32629507, 32629504, 32629505, 32629488, 32629489, 32629431, 32629470, 32629463, 32629461, 32629468, 32629466, 32629469, 32629465, 32629462, 32629464, 32629467, 32629536, 32629538, 32629537, 32629539, 32629541, 32629540, 32629455, 32629457, 32629456, 32629460, 32629458, 32629459"
	productPesIds="15613"
	cloudEnvironments="public"
	schemaVersion="1"
    articleId="BE3D6801-3F87-41BC-ACF9-B9DA8A86C55C"
/>
# Azure Data Factory Pipeline Info
---
{
    "resourceRequired": true,
    "title": "Azure Data Factory Pipeline Info",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank.",
			"required": false
		},
        {
            "id": "pipeline_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Name of the affected pipeline(s) (seperate with commas)",
            "required": true
        },
        {
            "id": "pipeline_json_code",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "JSON code of the affected pipeline",
            "required": true
        },
        {
            "id": "sample_pipeline_run_ids",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Sample problem pipeline RunIDs (separate with commas)",
            "required": true
        },
        {
            "id": "sample_activity_run_ids",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Sample problem activity RunIDs (separate with commas)",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue. ",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the issue, including the exact error message if available"
                }
            ]
        }
    ]
}
---
