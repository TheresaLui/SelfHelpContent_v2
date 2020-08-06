<properties
    pageTitle="Receiving or Transmitting data through a specific Connector - SFTP"
    description="Receiving or Transmitting data through a specific Connector - SFTP"
    service="microsoft.logicapps"
    resource="logicapps"
    authors="v-miegge"
    ms.author="v-miegge"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32677631"
    resourceTags=""
    productPesIds="15791"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="66ef9c75-d32e-4bb9-ad9e-33f8ee8d4471"
	ownershipId="Compute_LogicApps"
/>

# Receiving or Transmitting data through a specific Connector - SFTP

SFTP is a network protocol that provides file access, file transfer, and file management over any reliable data stream.

## **Recommended Steps**

* The IP addresses that Azure Logic Apps uses for incoming and outgoing calls depend on the region where your logic app exists:

    * [Inbound IP Addresses – Logic Apps service only](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#inbound)
    * [Outbound IP address – Logic Apps service & managed connectors](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound)

* SFTP connector supports private key formats – use tools such as PuttyGen or PuTTY to generate private key. If you are using an SSH private key, make sure you copy the key from your SSH private key file and paste that key into the connection details.

**Note**: Don't manually enter or edit the key.

* If you are using ISE (Integration Service Environment), you may have [one or more blocked ports](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment#check-network-ports)
* The connector may return an "[HTTP 404 error](https://docs.microsoft.com/connectors/sftp/)", if a file is being deleted or renamed on server after it was transmitted

## **Recommended Documents**

* [Prerequisites](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp#prerequisites)<br>
* [Limits](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp#limits)<br>
* [SFTP Trigger Example](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp#examples)<br>
* [SFTP Action Example](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp#examples)<br>
* [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)<br>
* [Connect to Azure virtual networks from Azure Logic Apps by using an integration service environment (ISE)](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment)
