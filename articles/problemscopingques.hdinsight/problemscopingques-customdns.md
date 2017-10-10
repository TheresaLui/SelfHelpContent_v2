<properties
	pageTitle="Custom DNS Issues"
	description="Custom DNS Issues"
	authors="ansi12"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588505"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Custom DNS Issues
---
{
	"resourceRequired": true,
	"title": "Custom DNS Issues",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "custom_dns_tsg",
			"order": 1,
			"controlType": "infoblock",
			"displayLabel": Before submitting the case, please follow the steps in the <a href="https://hdinsight.github.io/ClusterCRUD/hdinsight-customdns.html">Custom DNS trouble shooting guide</a> to troubleshoot issues with custom DNS setup. Make sure that the Azure recursive resolver IP is in your DNS server list.",
			"required": false
		}, {
			"id": "hostname",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: "hostname -f". Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "nslookup",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: "nslookup <headnode_fqdn>". Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "dig",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: "dig @168.63.129.16 <headnode_fqdn>". Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide any other details relevant to the problem",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://hdinsight.github.io/ClusterCRUD/hdinsight-customdns.html'>Learn more</a> about about commonly faced issues with using Custom DNS on HDInsight"
		}
	]
}
---
