<properties
       pageTitle="Getting started and troubleshooting MFA"
       description="Getting started and troubleshooting MFA"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725796"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, usnat, ussec"
       schemaVersion="1"
       articleId="problemscopingques-partnercentermfatshoot"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Getting started and troubleshooting MFA (Multi-factor Authentication)",
    "fileAttachmentHint": "For interface isues include the screen shot or the error. If API problems provide request/response payload files.",
    "formElements": [
             {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional information about your issue",
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
            "displayLabel": "Were you challenged for MFA (Multi-factor Authentication)?",
            "watermarkText": "Were you challenged for MFA (Multi-factor Authentication)?",
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
            "id": "mfa_configured",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Where you able to succesfully configure MFA?",
            "watermarkText": "Where you able to succesfully configure MFA?",
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
            "id": "mfa_whatsnotworking",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "If challenged, what exactly is not working?",
            "watermarkText": "If challenged, wwhat exactly is not working?",
            "dropdownOptions": [
                {
                    "value": "Could not enroll into MFA",
                    "text": "Could not enroll into MFA"
                },
                {
                    "value": "A specific service stopped working",
                    "text": "A specific service stopped working"
                },
                {
                    "value": "Some other issue",
                    "text": "Some other issue"
                }
                ],
            "required": false
             },
	     {
            "id": "mfa_issuetype",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Tell us more about the kind of issue are you having.",
            "watermarkText": "Tell us more about the kind of issue are you having.",
            "dropdownOptions": [
                {
                    "value": "Problem logging into partner center",
                    "text": "Problem logging into partner center"
                },
                {
                    "value": "Cannot manage customer via delegated admin (AOBO)",
                    "text": "Cannot manage customer via delegated admin (AOBO)"
                },
                {
                    "value": "Using partner center APIs",
                    "text": "Using partner center APIs"
                },
                {
                    "value": "Using Microsoft online services APIs such as Microsoft Graph",
                    "text": "Using Microsoft online services APIs such as Microsoft Graph"
                },
                {
                    "value": "Cannot transact",
                    "text": "Cannot transact"
                },
                {
                    "value": "Some other issue",
                    "text": "Some other issue"
                }
                ],
            "required": false
             }
    ]
}
---
