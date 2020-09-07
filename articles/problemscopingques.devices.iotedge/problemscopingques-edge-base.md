<properties
  pageTitle="Issues with IoT Edge"
  description="Scoping questions for the most generic IoT Edge problems. Basically the same set of stuff as the issue template on https://github.com/Azure/iotedge/issues"
  authors="jlian"
  ms.author="jlian"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32680950,32680966,32680969,32680976,32680986,32680963,32680983,32680985,32680987,32680945,32680946,32680949,32680952,32680953,32680962,32680967,32680973,32680942,32680958,32680959,32680960,32680977,32680943,32680961,32680978,32680979,32680980,32680981,32680982,32680970,32680971,32680972,32680936,32680937,32680940,32689202,32680941,32680944,32680947,32680948,32680954,32680964,32680968,32680984"
  productPesIds="16509"
  cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
  schemaVersion="1"
  articleId="04c1f45a-af94-4bba-b814-7106107ffae4"
  ownershipId="AzureIot_IotEdge"
/>
# Issues with IoT Edge
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
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "infoBalloonText": "To get iotedged logs, edge-agent logs, and edge-hub logs, see <a href='https://docs.microsoft.com/azure/iot-edge/troubleshoot#standard-diagnostic-steps'>IoT Edge diagnostic steps</a>",
      "watermarkText": "Please provide the description of the issue and expected behavior vs. what you're observing.",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "edge_device_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Affected IoT Edge device ID",
      "watermarkText": "Example: myEdgeDevice",
      "required": false
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
          "text": "Other (please specify) or not available"
        }
      ],
      "required": true
    },
    {
      "id": "edge_version_specify",
      "visibility": "edge_version == dont_know_answer",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Enter IoT Edge version",
      "watermarkText": "Example: 1.0.6",
      "required": false
    },
    {
      "id": "include_sb",
      "visibility": "edge_version == 109+",
      "order": 14,
      "controlType": "multilinetextbox",
      "displayLabel": "iotedge support-bundle",
      "watermarkText": "You can help reduce the issue resolution time by attaching the file output from 'iotedge support-bundle'.\n\nOn Linux, use command:\nsudo iotedge support-bundle --since 24h\n\nOn Windows, use:\niotedge support-bundle --since 24h",
      "infoBalloonText": "To learn more, see the <a href='https://docs.microsoft.com/azure/iot-edge/troubleshoot#gather-debug-information-with-iotedge-support-bundle-command'>docs page</a>"
    },
    {
      "id": "sb_included",
      "visibility": "edge_version == 109+",
      "order": 15,
      "controlType": "dropdown",
       "displayLabel": "'iotedge support-bundle' output attached?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "y",
          "text": "Yes"
        },
        {
          "value": "dont_know_answer",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "update_to_109",
      "visibility": "edge_version == 107 || edge_version == dont_know_answer || edge_version == 108",
      "order": 13,
      "controlType": "multilinetextbox",
      "displayLabel": "Latest version advisory",
      "watermarkText": "1.0.9 release is now available with many improvements!\n\nIf you haven't already, you should strongly consider updating the IoT Edge runtime containers and IoT Edge daemon to this version.",
      "infoBalloonText": "To learn more, see the <a href='https://techcommunity.microsoft.com/t5/internet-of-things/iot-edge-1-0-9/ba-p/1237100'>release blog post</a>"
    },
    {
      "id": "iotedge_check_108",
      "visibility": "edge_version == 108",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Output of 'sudo iotedge check --output json'",
      "infoBalloonText": "Remove `sudo` on Windows: `iotedge check --output json`",
      "watermarkText": "Example: \n{\"additional_info\":{\"docker_version\":\"3.0.5\",\"iotedged_version\":\"1.0.8\",\"now\":\"2019-08-15T19:21:07.163516400Z\",\"os\":{\"id\":\"windows\"blah,\"version_id\":\"10.0.17763 \",\"bitness\":64}}\n...",
      "required": false
    },
    {
      "id": "iotedge_check",
      "visibility": "edge_version == 107",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Output of 'sudo iotedge check'",
      "infoBalloonText": "Remove `sudo` on Windows: `iotedge check`",
      "watermarkText": "Example: \n√ config.yaml is well-formed - OK\n√ config.yaml has well-formed connection string - OK\n√ container engine is installed and functional - OK\n...",
      "required": false
    },
    {
      "id": "os",
      "visibility": "edge_version == 107 || edge_version == dont_know_answer",
      "order": 7,
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
          "value": "dont_know_answer",
          "text": "dont_know_answer"
        }
      ],
      "required": false
    },
    {
      "id": "architecture",
      "visibility": "edge_version == 107 || edge_version == dont_know_answer",
      "order": 8,
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
        }
      ],
      "required": false
    },
    {
      "id": "container_os",
      "visibility": "edge_version == 107 || edge_version == dont_know_answer",
      "order": 9,
      "controlType": "dropdown",
      "displayLabel": "Container operating system",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Linux containers",
          "text": "Linux containers"
        },
        {
          "value": "Windows containers",
          "text": "Windows containers"
        }
      ],
      "required": false
    },
    {
      "id": "docker_version",
      "visibility": "edge_version == 107 || edge_version == dont_know_answer",
      "order": 10,
      "controlType": "textbox",
      "infoBalloonText": "Run `docker version` (`docker -H npipe:////./pipe/iotedge_moby_engine version` for Moby on Windows)",
      "displayLabel": "Docker version",
      "watermarkText": "Paste output of `docker version` here",
      "required": false
    }
  ]
}
---