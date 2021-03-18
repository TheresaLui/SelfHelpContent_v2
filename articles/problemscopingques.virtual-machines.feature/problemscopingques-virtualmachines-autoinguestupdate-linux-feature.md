<properties
                pageTitle="automatic vm guest patching"
                description="automatic vm guest patching linux"
                authors="bhpat"
                ms.author="bhpat"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32743880"
                productPesIds="15571"
                cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
                schemaVersion="1"
                articleId="problemscopingques.virtual-machines.autoinguestupdate.linux.feature.md"
                ownershipId="Compute_VirtualMachines_Content"
/>
# automatic vm guest patching for linux
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "automatic vm guest patching",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "if_missing_update",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Does your virtual machine have missing Critical or Security Update(s) and your system was running every day during off-peak hours local time?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                },
                {
                    "text": "I don't know",
                    "value": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "missing_update_id",
            "visibility": "if_missing_update == Yes",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the package ID that did not install.",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "if_need_enable_disable_update",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you need assistance enabling or disabling automatic in-guest updates for a virtual machine?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                }
            ],
            "required": false
        },
        {
            "id": "vm_names",
            "visibility": "if_need_enable_disable_update == Yes",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the Azure VM name(s).",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "if_need_confirm_compliance",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you need assistance confirming update compliance?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
