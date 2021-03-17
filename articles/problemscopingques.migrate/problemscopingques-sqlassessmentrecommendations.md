<properties
         pageTitle="Scoping questions for SQL Assessment Recommendations"
         description="Scoping questions SQL Assessment Recommendations"
         authors="bhpat"
         ms.author="bhpat"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32786257"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="c2a32eea-03dc-d311-0b42-dc3c36845fe2"
	ownershipId="Compute_AzureMigrate"
/>

# SQL Assessment Recommendations

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
                    "value": "Azure SQL",
                    "text": "Azure SQL"
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
            "displayLabel": "Provide the name of the assessment in which you are facing the issue.",
            "watermarkText": "E.g. MyContosoAssessment",
            "required": false
        },
	{
            "id": "SQL_name",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the names of the impacted SQL instances:",
            "watermarkText": "E.g. MyContosoSQL",
            "required": false
	 },
         {
            "id": "Problem Type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Your Problem is related to:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Understanding the target Azure SQL configuration recommendation",
                    "text": "Understanding the target Azure SQL configuration recommendation"
                },
				{
                    "value": "Understanding the reported migration issues",
                    "text": "Understanding the reported migration issues"
                },
                {
                    "value": "Understanding the cost estimate calculation",
                    "text": "Understanding the cost estimate calculation"
                },
				{
                    "value": "None of the above",
                    "text": "None of the above"
                }
            ],
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
