<properties
	pageTitle="Scoping questions for Port25 email flow"
	description="Scoping questions for Port25 email flow"
	authors="prdasneo"
	ms.author="prdasneo"
  selfHelpType="problemScopingQuestions"
	supportTopicIds="32640601"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
  schemaVersion="1"
   articleId="port25emailflow-problemscopingquestion"
	ownershipId="ASMS_SubscriptionManagement"
/>
#  Port 25 email flow
---
{
    "resourceRequired": false,
    "SubscriptionRequired": false,
    "title": "Port 25 email flow",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
	},
	{
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description of your request",
             "useAsAdditionalDetails": true,
            "required": true,
            "hints": [
                {
                    "text": "Note: Make sure that you add details about why your deployment has to send mail directly to mail providers instead of using an authenticated relay"
                }
		]
		}
		],
    "$schema": "SelfHelpContent"
}
---
