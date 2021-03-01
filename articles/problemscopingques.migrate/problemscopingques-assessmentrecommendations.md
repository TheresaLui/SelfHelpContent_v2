<properties
         pageTitle="Scoping questions for Assessment Recommendations"
         description="Scoping questions for Assessment Recommendations"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675736"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="5a50e5a6-4466-46c7-83bf-70918fcee374"
	 ownershipId="Compute_AzureMigrate"
/>

# Assessment Recommendations

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Discovery issues",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "Assessment Type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Provide the assessment type",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Azure VM",
                    "text": "Azure VM"
                },
                {
                    "value": "Azure VMware Solution(AVS)",
                    "text": "Azure VMware Solution(AVS)"
                }
            ],
            "required": false
	},
        {
            "id": "assessment_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the assessment in which you are facing an issue.",
            "watermarkText": "E.g. MyContosoAssessment",
            "required": false
        },
        {
            "id": "VM_name",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the VM name (if applicable)",
            "watermarkText": "E.g. MyContosoVM01",
            "required": false
        },
        {
            "id": "disk_name",
            "order": 4,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the disk name (if applicable)",
            "watermarkText": "E.g. MyContosodisk01",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
