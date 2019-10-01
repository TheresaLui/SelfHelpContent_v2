<properties
       pageTitle="Submit technical enforcement exception"
       description="Submit technical enforcement exception"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32684683"
       productPesIds="15960"
       cloudEnvironments="public"
       schemaVersion="1"
       articleId="problemscopingques-partnercentermfaexception"
       clientIds="partnercenter"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Submit technical enforcement exception",
    "fileAttachmentHint": "For interface isues include the screen shot or the error. If API problems provide request/response payload files.",
    "formElements": [
             {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Description of the technical issues for your exception request.",
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
            "id": "mfa_challenged",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I use Exchange Online PowerShell to manage my customer tenants, and Exchange Online PowerShell does not support MFA.",
            "watermarkText": "I use Exchange Online PowerShell to manage my customer tenants, and Exchange Online PowerShell does not support MFA",
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
             },
	    {
            "id": "problem_mfarepro",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "If problems with MFA please provide steps to reproduce the issue, including detailed error codes if applicable.",
            "useAsAdditionalDetails": true,
            "required": true
             },
	    {
            "id": "problem_mfaimpact",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the overall impact if exception is not approved.",
            "useAsAdditionalDetails": true,
            "required": true
             },
    ]
}
---