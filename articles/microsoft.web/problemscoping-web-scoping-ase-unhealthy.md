<properties
	pageTitle="Scoping questions for ASE is unavailable or unhealthy"
	description="ASE is unavailable or unhealthy"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581609"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="5f2982f2-c334-4fbd-ac90-27edb5dd22b1"
	ownershipId="Compute_AppService"
/>

# ASE is unavailable or unhealthy
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "What is the name of the ASE?"
                },
                {
                    "text": "Is there a banner at the top of the ASE overview blade in the Azure portal that indicates a problem?"
                },
                {
                    "text": "Describe the exact error and location where you see the symptoms."
                },
                {
                    "text": "Are you aware of any recent changes to the ASE or the environment (including Azure Networking)? If so, please describe."
                },
                {
                    "text": "Are any of the Web Apps that are hosted in your ASE working?"
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---