<properties
       pageTitle="MFA support request"
       description="MFA support request"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32674992,32674990"
       productPesIds="15960"
       cloudEnvironments="public"
       schemaVersion="1"
       articleId="problemscopingques-partnercentermfageneral"
       clientIds="partnercenter"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Questions about Secure App Model or other security requirements",
    "fileAttachmentHint": "Attach a file or screenshot that shows your question or issue.",
    "formElements": [
             {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional information about your question",
            "useAsAdditionalDetails": true,
            "required": true
             },
             {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did your issue begin",
            "required": true
             },
	     {
            "id": "mfa_configured",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you successfully confiugured MFA?",
            "watermarkText": "Have you successfully confiugured MFA?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
                ],
            "required": false
             }
    ]
}
---
