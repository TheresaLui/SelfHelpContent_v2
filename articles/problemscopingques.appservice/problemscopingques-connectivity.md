<properties
    pageTitle="App Service on Azure Stack Hub - Version and Connectivity"
    description="App Service on Azure Stack Hub - Version and Connectivity"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds=""
    productPesIds="17136"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-connectivity"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>
# App Service on Azure Stack Hub - Version and Connectivity
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack Environment Details",
    "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [
        {
            "id": "azure_stack_build_number",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Current build for Azure Stack Hub",
            "watermarkText": "Example: 2002 if your build number is 1.2002.0.35.",
            "dropdownOptions": [
                {
                    "value": "2005",
                    "text": "2005"
                },
                {
                    "value": "2002",
                    "text": "20002"
                },
                {
                    "value": "1910",
                    "text": "1910"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 2002 if your build number is 1.2002.0.35."
        },
        {
            "id": "app_service_version_number",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Current version of App Service",
            "watermarkText": "Example: 1.2002.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#determine-the-current-version'>determine the current build number</a>"
        },
        {
            "id": "connected_deployment",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Can Azure Stack Hub connect to Azure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                },{
                    "value": "No",
                    "text": "No"
                },{
                    "value": "dont_know_answer",
                    "text": "Unsure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 900,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---