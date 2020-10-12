<properties
  pageTitle="Troubleshoot Virtual Machine firewall"
  description="Troubleshoot Virtual Machine firewall"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740108"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="fc1792bf-b2fc-4998-9e4a-90024c6c3f07"
  ownershipId="AzureData_AzureSQLVM"
/>
# Troubleshoot Virtual Machine firewall
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Troubleshoot Virtual Machine firewall",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "connect_source",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "From where are you trying to connect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "On premise",
                    "text": "On premise"
                },
                {
                    "value": "Another machine in Azure",
                    "text": "Another machine in Azure"
                },
                {
                    "value": "Another cloud provider",
                    "text": "Another cloud provider"
                },
                {
                    "value": "Azure Marketplace",
                    "text": "Azure Marketplace"
                }
            ],
            "required": false
        },
        {
            "id": "connect_sourcesubnetip",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your source subnet or IP that you are trying to connect from?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "connect_firewall",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What firewall are you trying to troubleshoot?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows Defender",
                    "text": "Windows Defender"
                },
                {
                    "value": "Third-party firewall",
                    "text": "Third-party firewall"
                }
            ],
            "required": false
        },
        {
            "id": "connect_ifinternet",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you have connectivity issues from/to this VM?",
            "watermarkText": "Choose an option",
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
            "id": "connect_internetissue",
            "order": 6,
            "visibility": "connect_ifinternet == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is the problem you are having?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Cannot connect to the RDP port",
                    "text": "Cannot connect to the RDP port"
                },
                {
                    "value": "Cannot connect to the Powershell port",
                    "text": "Cannot connect to the Powershell port"
                },
                {
                    "value": "Cannot connect to my SQL instance",
                    "text": "Cannot connect to my SQL instance"
                },
                {
                    "value": "Cannot connect to another port",
                    "text": "Cannot connect to another port"
                },
                {
                    "value": "My VM doesn't have access to Internet",
                    "text": "My VM doesn't have access to Internet"
                }
            ],
            "required": false
        },
        {
            "id": "isadmin",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Is this the built-in administrator account?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "name_useraccount",
            "order": 8,
            "visibility": "isadmin == No || isadmin == I do not know",
            "controlType": "textbox",
            "displayLabel": "What is the name of the user account trying to login?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
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
