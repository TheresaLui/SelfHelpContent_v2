<properties
	pageTitle="Security and Compliance Requests"
	description="Security and Compliance Requests"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32741673"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="othersecurityandcompliancerequests"
	ownershipId="ASMS_SubscriptionManagement"
/>


# Other Security and Compliance Requests
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Other Security and Compliance Requests",
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
            "id": "Subscription_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "",
	    "required": true
        },
	{
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
	    "watermarkText": "Please provide brief description of the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Learn more on Azure Compliance <a href='https://azure.microsoft.com/overview/trusted-cloud/compliance/'>here</a>"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
