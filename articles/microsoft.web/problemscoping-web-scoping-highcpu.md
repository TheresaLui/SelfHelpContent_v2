<properties
	pageTitle="Scoping questions for high CPU usage"
	description="High CPU usage"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32583701"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="d65501bd-4146-474a-b467-2c84e613b369"
/>

# High CPU usage



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
                    "text": "Which indicators are you looking at for CPU usage?"
                },
                {
                    "text": "How much CPU consumption are you seeing?"
                },
                {
                    "text": "What framework(s) is your app using (e.g. ASP.NET, Node, Java, Python etc.)?"
                },
                {
                    "text": "Is the issue still occurring? If not, how was the issue resolved?"
                },
                {
                    "text": "Has the site volume increased?"
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