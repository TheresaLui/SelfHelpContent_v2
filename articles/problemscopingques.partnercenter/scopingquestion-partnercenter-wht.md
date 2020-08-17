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
       "fileAttachmentHint": "Please attach any files that may help explain your issue, this could include image screen captures or tax certificate files.",
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
            "id": "pc_taxwithholding_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the tax withholding ID this is about.",
            "watermarkText": "Provide the tax withholding ID, it will look something like: 1048177",
            "required": true
              }
    ]
}
---
