<properties
	pageTitle="Scoping questions for high memory usage"
	description="High memory usage"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581616"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="d3e7d7e1-ccbd-4b55-8191-4539de3408c8"
/>

# High memory usage



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
                    "text": "Which indicators are you looking at for memory usage?"
                },
                {
                    "text": "How much memory consumption are you seeing?"
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