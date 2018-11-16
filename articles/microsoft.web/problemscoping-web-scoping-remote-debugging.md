<properties
	pageTitle="Scoping questions for Remote debugging"
	description="Remote debugging"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581620"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="5f322fa9-2039-452c-a39b-028cde102221"
/>

# Remote debugging

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
                    "text": "Have you updated Visual Studio to the latest updates?"
                },
                {
                    "text": "Have you updated the Azure SDK to the latest updates?"
                },
                {
                    "text": "What is the version and release of Visual Studio you are using (Help About shows this)?"
                },
                {
                    "text": "Are you using Cloud Explorer to start debugging or manually attaching the debugger?"
                },
                {
                    "text": "What is the exact error message?"
                },
                {
                    "text": "Are you behind a firewall?"
                },
                {
                    "text": "What language is your Web App written in?"
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
    ]
}
---