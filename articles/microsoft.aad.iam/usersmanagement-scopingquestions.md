<properties
    pageTitle="User Management scoping questions"
    description="Problem scoping for User Management problems"
    authors="jeffsta"
    ms.author="Jeffsta-MSFT"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615378,32045780,32615470,32615469,32586793,32615430"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="94b91e4f-caac-4673-9481-3034272e0fa7"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# User Management questions
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "User management problems",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the task you need to accomplish",
            "watermarkText": "If the task pertains to managing an existing user, include the user name ('alice@contoso.com') or object ID of that user.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "whatProblem",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Where does the problem occur?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure portal (portal.azure.com)",
                    "value": "azurePortal"
                },
                {
                    "text": "Another web page",
                    "value": "otherPage"
                },
                {
                    "text": "PowerShell",
                    "value": "powerShell"
                },
                {
                    "text": "Other, don't know, or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
		{
            "id": "problem_detail_AzurePortal",
            "visibility": "whatProblem==azurePortal",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Describe the problem that prevents you from completing the task. Include the URL of the page where the problem occurs, and any error messages you observed.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_detail_otherPage",
            "visibility": "whatProblem==otherPage",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Describe the problem that prevents you from completing the task. Include the URL of the page where the problem occurs, and any error messages you observed.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_detail_powerShell",
            "visibility": "whatProblem==powerShell",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Describe the problem that prevents you from completing the task. Include the text of your PowerShell request and the response, if available.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_detail_otherTool",
            "visibility": "whatProblem==don't_know_answer",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Describe the problem that prevents you from completing the task, including any error messages you observed.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did you first notice the problem?",
            "required": true
        },
        {
            "id": "problem_steps_taken",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have taken any steps to troubleshoot this problem, please provide details here",
            "watermarkText": "If you have taken any steps to troubleshoot this problem, please provide details here",
            "required": false
        },
        {
            "id": "audit_logs",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Audit logs",
            "watermarkText": "If there are any audit logs for activity related to the problem, enter the correlation ID(s) of the audit log(s) here. E.g., '94b91e4f-caac-4673-9481-3034272e0fa6'",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
