<properties
    pageTitle="Problem assigning licenses to a group"
    description="problemassigninglicensetoagroup"
    authors="chpate"
    ms.author="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615386"
    productPesIds="16575,16578"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="23c1cf4d-6fdd-475b-ba06-87595b53195b"
    />

# Problem assigning licenses to a group

---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Problem assigning licenses to a group",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "purchaseOrUpgradeLicense",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is your question regarding purchase/upgrade of license (including trial)?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "yes"
                },
                {
                    "text": "No",
                    "value": "no"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "purchaseOrUpgradeSelection",
            "visibility": "purchaseOrUpgradeLicense==yes",
            "order": 2,
            "controlType": "infoblock",
            "content": "Please select License acquisition and upgrade support topic in previous screen."
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---