<properties
	pageTitle="Scoping questions for Web App Down or Reporting Errors"
	description="Availability, Performance, and Application Issues/Web app down or reporting errors"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542218"
	productPesIds="14748"
	cloudEnvironments="public, MoonCake"
   schemaVersion="1"
   articleId="0f5a571f-63b9-46c9-baf3-5a35c15b65b3"
/>

# Web App Down or Reporting Errors
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
                    "text": "What framework is your app using (i.e. ASP.NET, Node, Java, Python etc.)?"
                },
                {
                    "text": "Is the issue still occurring? If not, how was the issue resolved (i.e. App or Service Restarted, Scaling etc.)?"
                },
                {
                    "text": "Is there a specific error you are seeing? Please include the text of the error."
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