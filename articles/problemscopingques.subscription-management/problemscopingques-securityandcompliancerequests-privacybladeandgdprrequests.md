<properties
	pageTitle="Privacy Blade and GDPR Requests"
	description="Privacy Blade and GDPR Requests"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32607561"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="privacybladeandGDPRRequests-problemscopingquestions"
	ownershipId="ASMS_SubscriptionManagement"
/>


# Privacy Blade and GDPR Requests
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Privacy Blade and GDPR Requests",
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
                    "text": "Learn more on Privacy and GDPR <a href='https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure'>here</a>"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
