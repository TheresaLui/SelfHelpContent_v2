<properties
    pageTitle="Solution Vulnerability Assessment (BYOL)"
    description="Solution Vulnerability Assessment (BYOL)"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32749421"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0104"
    ownershipId="Azure_Security_Security_Center"
/>
# Solution Vulnerability Assessment (BYOL)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Solution Vulnerability Assessment (BYOL)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "issue_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the issue you are experiencing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Fail to provision VM extension",
                    "text": "Fail to provision VM extension"
                },
                {
                    "value": "Fail to get VA Recommendation to install",
                    "text": "Fail to get VA Recommendation to install"
                },
                {
                    "value": "Fail to get VA findings after install",
                    "text": "Fail to get VA findings after install"
                },
                {
                    "value": "dont_know_answer",
                    "text": "General questions"
                }
            ],
            "required": true
        },
        {
            "id": "power_status",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is auto-provisioning turned on?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "On",
                    "text": "On"
                },
                {
                    "value": "Off",
                    "text": "Off"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "os_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the operating system type?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Microsoft Windows 2016, Windows 10",
                    "text": "Microsoft Windows 2016, Windows 10"
                },
                {
                    "value": "Red Hat Enterprise Linux 5.4+, 6, 7.0-7.8, 8.0-8.1",
                    "text": "Red Hat Enterprise Linux 5.4+, 6, 7.0-7.8, 8.0-8.1"
                },
                {
                    "value": "Red Hat CentOS 5.4+, 6, 7.0-7.7, 8.0-8.1",
                    "text": "Red Hat CentOS 5.4+, 6, 7.0-7.7, 8.0-8.1"
                },
                {
                    "value": "Red Hat Fedora 22-31",
                    "text": "Red Hat Fedora 22-31"
                },
                {
                    "value": "SUSE Linux Enterprise Server (SLES) 11, 12, 15",
                    "text": "SUSE Linux Enterprise Server (SLES) 11, 12, 15"
                },
                {
                    "value": "SUSE OpenSUSE 12, 13, 15.0-15.2",
                    "text": "SUSE OpenSUSE 12, 13, 15.0-15.2"
                },
                {
                    "value": "SUSE Leap 42.1",
                    "text": "SUSE Leap 42.1"
                },
                {
                    "value": "Oracle Enterprise Linux 5.11, 6, 7.0-7.5",
                    "text": "Oracle Enterprise Linux 5.11, 6, 7.0-7.5"
                },
                {
                    "value": "Debian  7.x-10.x",
                    "text": "Debian  7.x-10.x"
                },
                {
                    "value": "Ubuntu 12.04 LTS, 14.04 LTS, 15.x, 16.04 LTS, 18.04 LTS, 19.10, 20.04 LTS",
                    "text": "Ubuntu 12.04 LTS, 14.04 LTS, 15.x, 16.04 LTS, 18.04 LTS, 19.10, 20.04 LTS"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
