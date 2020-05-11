<properties
         pageTitle="Scoping questions for recovery plans"
         description="Scoping questions for recovery plans"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32574721"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="q2ade905-df87-4222-9534-98223c9c0527"
	ownershipId="Compute_SiteRecovery"
/>

# Recovery plans
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Recovery plans",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "plan_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the recovery plan",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the failed operation",
            "watermarkText": "Enter in the error ID or job ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job ID of failed re-protect job",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am trying to re-protect, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I am unable to create a recovery plan",
                    "text": "I am unable to create a recovery plan"
                },
                {
                    "value": "I am unable to add a group to my recovery plan",
                    "text": "I am unable to add a group to my recovery plan"
                },
                {
                    "value": "I am unable to add a script to my recovery plan",
                    "text": "I am unable to add a script to my recovery plan"
                },
                {
                    "value": "I am unable to add a manual action to my recovery plan",
                    "text": "I am unable to add a manual action to my recovery plan"
                },
                {
                    "value": "I am unable to perform a test failover using my recovery plan",
                    "text": "I am unable to perform a test failover using my recovery plan"
                },
                {
                    "value": "I am unable to perform a failover using my recovery plan",
                    "text": "I am unable to perform a failover using my recovery plan"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "tried_steps",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "I have gone through steps provided in the following articles",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "About recovery plans",
                    "text": "About recovery plans"
                },
                {
                    "value": "Create/customize recovery plans",
                    "text": "Create or customize recovery plans"
                },
                {
                    "value": "Add Azure Automation runbooks to recovery plans",
                    "text": "Add Azure Automation runbooks to recovery plans"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
       {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Enter in local time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
