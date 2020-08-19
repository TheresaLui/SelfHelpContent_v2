<properties
       pageTitle="Request for MFA exception"
       description="Request for MFA exception"
       authors="brentserbus"
       ms.author="a-crmire"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725807"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, usnat, ussec"
       schemaVersion="1"
       articleId="problemscopingques-partnercentermfaexception"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Request for MFA exception",
    "fileAttachmentHint": "Upload any supporting files that can help us understand the technical issue.",
    "formElements": [
             {
            "id": "mfa_exchange",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select 'yes' if this issue is related to the use of Exchange Online PowerShell to manage customer resources, and Exchange Online PowerShell does not support MFA.",
            "dropdownOptions": [
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "Yes",
                    "text": "Yes"
                },
		{
		    "value": "dont_know_answer",
		    "text": "Don't Know"
		}
                ],
            "required": true
             },
             {
            "id": "mfa_thirdparty",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select 'yes' if the issue is related to the use of 3rd party MFA solution, which cannot be configured to convey to Azure Active Directory that MFA verification has been completed.",
            "dropdownOptions": [
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "Yes",
                    "text": "Yes"
                },
		{
		    "value": "dont_know_answer",
		    "text": "Don't Know"
		}
                ],
            "required": true
             },
	     {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description of the technical issue for technical exception. Where applicable, please include detail steps on how to reproduce the issue and actual error message encountered.",
            "useAsAdditionalDetails": true,
            "required": true
             },
	    {
            "id": "problem_mfaimpact",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe impact if issue is not resolved.",
            "required": true
             },
             {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did your issue begin",
            "required": true
             },
             {
            "id": "mfa_suppress",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Microsoft does not recommend suppressing MFA verification for partner-related scenarios as it increases the security risk to both the partner and associated customers. Select 'yes' to indicate that you understand the risk. ",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
		{
		    "value": "dont_know_answer",
		    "text": "Don't Know"
		}
                ],
            "required": true
             }
    ]
}
---
