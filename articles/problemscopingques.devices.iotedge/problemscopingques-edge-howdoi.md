<properties
  pageTitle="Issues with IoT Edge"
  description="Scoping questions for  IoT Edge 'How Do I' questions."
  authors="veyalla"
  ms.author="veyalla"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32680951, 32680955, 32680956, 32680957, 32680965, 32680974, 32680975, 32680988, 32680938, 32680939"
  productPesIds="16509"
  cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
  schemaVersion="1"
  articleId="466c630e-d70e-4b98-b7a9-d4f388a7b9db"
  ownershipId="AzureIot_IotEdge"
/>
# IoT Edge "how do i"
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issue with IoT Edge",
  "fileAttachmentHint": "On releases 1.0.9 and later, please attach the output of 'sudo iotedge support-bundle --since 24h'",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Please provide the description of the issue and expected behavior vs. what you're observing.",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "edge_version",
      "order": 3,
      "controlType": "dropdown",
      "infoBalloonText": "Run `iotedge version` on the device",
      "displayLabel": "IoT Edge version",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "109+",
          "text": "1.0.9 or higher"
        },
        {
          "value": "108",
          "text": "1.0.8"
        },
        {
          "value": "107",
          "text": "1.0.7"
        },
        {
          "value": "dont_know_answer",
          "text": "dont_know_answer"
        }
      ],
      "required": true
    },
    {
      "id": "os",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Device (host) operating system",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Raspbian Stretch",
          "text": "Raspbian Stretch"
        },
        {
          "value": "Ubuntu Server 16.04",
          "text": "Ubuntu Server 16.04"
        },
        {
          "value": "Ubuntu Server 18.04",
          "text": "Ubuntu Server 18.04"
        },
        {
          "value": "Windows 10 IoT Enterprise",
          "text": "Windows 10 IoT Enterprise"
        },
        {
          "value": "Windows Server 2019",
          "text": "Windows Server 2019"
        },
        {
          "value": "Windows Server IoT 2019",
          "text": "Windows Server IoT 2019"
        },
        {
          "value": "Windows 10 IoT Core",
          "text": "Windows 10 IoT Core"
        },
        {
          "value": "CentOS 7.5",
          "text": "CentOS 7.5"
        },
        {
          "value": "Debian 8 or 9",
          "text": "Debian 8 or 9"
        },
        {
          "value": "Debian 10",
          "text": "Debian 10"
        },
        {
          "value": "RHEL 7.5",
          "text": "RHEL 7.5"
        },
        {
          "value": "Ubuntu 16.04",
          "text": "Ubuntu 16.04"
        },
        {
          "value": "Ubuntu 18.04",
          "text": "Ubuntu 18.04"
        },
        {
          "value": "Kubernetes",
          "text": "Kubernetes"
        },
        {
          "value": "Wind River 8",
          "text": "Wind River 8"
        },
        {
          "value": "Yocto",
          "text": "Yocto"
        },
        {
          "value": "Raspbian Buster",
          "text": "Raspbian Buster"
        },
        {
          "value": "Other",
          "text": "Other"
        },
        {
          "value": "dont_know_answer",
          "text": "dont_know_answer"
        }
      ],
      "required": true
    },
    {
      "id": "architecture",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Architecture",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "AMD64",
          "text": "AMD64 (x86-64)"
        },
        {
          "value": "ARM32",
          "text": "ARM32"
        },
        {
          "value": "ARM64",
          "text": "ARM64"
        },
        {
          "value": "dont_know_answer",
          "text": "dont_know_answer"
        }
      ],
      "required": true
    }
  ]
}
---