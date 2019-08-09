<properties
	pageTitle="Issues with IoT Edge"
	description="Scoping questions for the most generic IoT Edge problems. Basically the same set of stuff as the issue template on https://github.com/Azure/iotedge/issues"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="04c1f45a-af94-4bba-b814-7106107ffae4"
/>
# Issues with IoT Edge
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": false,
	"resourceRequired": false,
	"title": "Issues with IoT Edge",
	"fileAttachmentHint": "Upload screenshots of errors if available",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": true
		},
		{
			"id": "edge_device_id",
			"order": 2,
			"controlType": "textbox",
			"infoBalloonText": "Run `iotedge version` on the device",
			"displayLabel": "IoT Edge device ID",
			"watermarkText": "Example: myEdgeDevice",
			"required": true
		},
		{
			"id": "iotedge_check",
			"order": 2,
			"controlType": "multilinetextbox",
			"infoBalloonText": "Your first step when troubleshooting IoT Edge should be to use the check command, which performs a collection of configuration and connectivity tests for common issues. The check command is available in <a href= 'https://github.com/Azure/azure-iotedge/releases/tag/1.0.7'>release 1.0.7</a> and later. To learn more, see <a href='https://docs.microsoft.com/azure/iot-edge/troubleshoot#run-the-iotedge-check-command'>Troubleshoot IoT Edge</a> ",
			"displayLabel": "Output of iotedge check",
			"watermarkText": "Paste here",
			"required": false
		},
		{
			"id": "os",
			"order": 3,
			"controlType": "dropdown",
			"infoBalloonText": "To learn more about the Azure IoT Device SDKs, see <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks'>Understand and use Azure IoT Hub SDKs</a> ",
			"displayLabel": "Device (host) operating system",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Raspbian-stretch",
					"text": "Raspbian-stretch"
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
					"value": "Other",
					"text": "Other"
				}
			],
			"required": false
		},
		{
			"id": "architecture",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Architecture",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
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
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Container operating system",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
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
			"id": "edge_version",
			"order": 5,
			"controlType": "textbox",
			"infoBalloonText": "Run `iotedge version` on the device",
			"displayLabel": "IoT Edge version",
			"watermarkText": "Example: 1.0.8",
			"required": false
		},
		{
			"id": "docker_version",
			"order": 6,
			"controlType": "textbox",
			"infoBalloonText": "Run <code>docker version</code> (<code>docker -H npipe:////./pipe/iotedge_moby_engine version</code> for Moby on Windows)",
			"displayLabel": "Docker version",
			"watermarkText": "Paste here",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Additional information",
			"infoBalloonText": "Follow <a href=\"https://docs.microsoft.com/en-us/azure/iot-edge/troubleshoot#standard-diagnostic-steps\">diagnostic steps</a> to help extract useful information.",
			"watermarkText": "Please provide any additional information that may be helpful in understanding the issue. ",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Steps to reproduce the issue"
				},
				{
					"text": "Expected behavior and current behavior"
				},
				{
					"text": "Share as many logs as possible (iotedged logs, edge-agent logs, edge-hub logs) "
				}
			]
		}
	]
}
---