<properties
	pageTitle="Scoping questions for Web app restarted"
	description="Web app restarted"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32570954"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="84fdb6ef-131e-457d-9c12-4b83f9f95802"
/>

# Web app restarted





---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "What framework is your app using (e.g. ASP.NET, Node, Java, Python etc.)?"
                },
                {
                    "text": "Is the issue still occurring? If not, how was the issue resolved?"
                },
                {
                    "text": "Have you seen any application errors during the restart timeframe? If so, what was the error?"
                },
                {
                    "text": "What is the frequency of the restarts?"
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