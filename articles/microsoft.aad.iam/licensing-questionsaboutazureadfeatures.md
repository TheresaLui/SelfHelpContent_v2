<properties
    pageTitle="Questions about Azure AD features"
    description="questionsaboutazureadfeatures"
    authors="chpate"
    ms.author="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615394"
    productPesIds="16578"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="licensing-questionsaboutazureadfeatures"
    />

# Problem assigning licenses to a group

---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Questions about Azure AD features",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "purchaseOrUpgradeLicense",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is your question regarding purchase/upgrade of license (including trial)?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "yes"
                },
                {
                    "text": "No",
                    "value": "no"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "purchaseOrUpgradeSelection",
            "visibility": "purchaseOrUpgradeLicense==yes",
            "order": 4,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please select License acquisition and upgrade support topic in previous screen.",
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "azureADLevel",
            "visibility": "purchaseOrUpgradeLicense==no",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is Azure AD level of your tenant. This information is below the Directory name on Overview blade.",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure AD free",
                    "value": "adfree"
                },
                {
                    "text": "Azure AD Premium P1",
                    "value": "p1"
                },
                {
                    "text": "Azure AD Premium P2",
                    "value": "p2"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "featureName",
            "visibility": "purchaseOrUpgradeLicense==no",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What Azure AD feature you want to use.",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "numberOfLines": 2
        }
    ],
    "$schema": "SelfHelpContent"
}
---