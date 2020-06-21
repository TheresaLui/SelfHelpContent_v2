<properties
pageTitle="Scoping questions for Web App Down or Reporting Errors"
description="Availability, Performance, and Application Issues/Web app down or reporting errors"
service="microsoft.web"
authors="shrahman, khaled-zayed"
ms.author="shrahman, khzayed"
selfHelpType="problemScopingQuestions"
supportTopicIds="32542218"
productPesIds="14748"
cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
schemaVersion="1"
articleId="0f5a571f-63b9-46c9-baf3-5a35c15b65b3"
ownershipId="Compute_AppService"
/>

# Web App Down or Reporting Errors
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true
        },
        {
			"id": "3",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What framework is your app using (i.e. ASP.NET, Node, Java, Python etc.)?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Is the issue still occurring? If not, how was the issue resolved (i.e. App or Service Restarted, Scaling etc.)?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Is there a specific error you are seeing? Please include the text of the error.",
			"watermarkText": "...",
			"required": false
		},
		{
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
