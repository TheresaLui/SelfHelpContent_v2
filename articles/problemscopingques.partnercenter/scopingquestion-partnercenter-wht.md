<properties
       pageTitle="Partner Center Tax Withholding"
       description="Partner Center Tax Withholding"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32692610"
       productPesIds="17003"
       cloudEnvironments="public, fairfax, usnat, ussec"
       schemaVersion="1"
       articleId="problemscopingques-partnercenterwht"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Tax Withholding",
       "fileAttachmentHint": "Only attach tax certificates if you were not able to create a withholding request through the new process. If you were unable to submit a withholding through the new process please tell us why.",
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
            "id": "pc_wht_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is this issue about?",
            "watermarkText": "Have you alrady created the request?",
            "dropdownOptions": [
                {
                    "value": "Existing request",
                    "text": "Existing request"
                },
                {
                    "value": "New request",
                    "text": "New request"
                }
            ],
            "required": false
        },
        {
            "id": "pc_wht_blocked",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "If you are unable to create a new request using the documented process, what was the reason?",
            "watermarkText": "Reason cannot create",
            "dropdownOptions": [
                {
                    "value": "Certificate file was too large",
                    "text": "My certificate file was too large"
                },
                {
                    "value": "Certificate non-English",
                    "text": "Cannot provide tax certificate in English"
                },
                {
                    "value": "Completed request not available",
                    "text": "Request is completed by I do not see the amounts in Last payment"
                },
                {
                    "value": "blocked other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "pc_taxwithholding_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide the tax withholding ID this is about.",
            "watermarkText": "Provide the tax withholding ID, it will look something like: 1048177",
            "required": true
        }
    ]
}
---
