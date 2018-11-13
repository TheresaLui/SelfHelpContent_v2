<properties
	pageTitle="Scoping questions for Web app slow"
	description="Web app slow"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32457411"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="a9219edd-364b-4dc7-9b67-099847303e2a"
/>

# Web app slow



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
                    "text": "Can you quantify normal and slow performance metrics?"
                },
                {
                    "text": "Is the issue intermittent or consistent? If intermittent, what is the observed pattern when it occurs?"
                },
                {
                    "text": "Which URL(s) are experiencing the slowdown?"
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