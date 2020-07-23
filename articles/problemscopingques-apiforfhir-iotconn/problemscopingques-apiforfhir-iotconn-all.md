<properties
	pageTitle="Issues with IoT Connect on API for FHIR"
	description="Issues with IoT Connect on API for FHIR"
	service="Microsoft.HealthcareApis"
	resource="IoT Connector"
	authors="johnnygetHub"
	ms.author="johnnyc"
    displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742775,32742776,32742777,32742778,32742779,32742780"
	resourceTags=""
	productPesIds="16674"
	cloudEnvironments="public"
    schemaVersion="1"
	articleId="f29ea932-7dd8-4960-a619-4d9d4ec47bcf"
	ownershipId="API_FHIR_Health_Eng"
/>
# Recommended Steps
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Job details",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "job_id_selection",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the job ID which has the problem",
            "watermarkText": "The job ID which has the problem",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide additional information about your issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
