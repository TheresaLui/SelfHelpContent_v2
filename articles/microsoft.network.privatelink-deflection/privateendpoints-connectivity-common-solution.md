<properties
	pageTitle="My Azure Private Endpoint connectivity is not working"
	description="My Azure Private Endpoint connectivity is not working"
	infoBubbleText="Troubleshoot Azure Private Endpoint connectivity problems"
	service=""
	resource=""
	authors="rdhillon,malop"
	ms.author="rdhillon,malop"
	displayOrder=""
	articleId="722d2f21-85d2-42e8-99fb-d944c9d98003"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32681487"
	resourceTags=""
	productPesIds="16843"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_PrivateLink"
/>

# My Azure Private Endpoint connectivity is not working

Try the troubleshooting steps below if your Azure Private Endpoint connectivity is not working.

## **Recommended Steps**

1. Verify that connection state is **Approved** for Private Endpoint that you are trying to connect
2. Make sure the VM has connectivity to the VNet hosting the Private Endpoints
3. Review the VNet and DNS information for the Private Endpoint
4. Use Azure Monitor for Private Endpoints to check the data path status
5. Verify VM connectivity via Network Watcher VM Connection Troubleshoot
6. Check the configuration for secrets, tokens, passwords or application layer that might be impacting connectivity

## **Recommended Documents**

* [Troubleshoot Azure Private Endpoints connectivity problems](https://docs.microsoft.com/azure/private-link/troubleshoot-private-endpoint-connectivity)
* [Create a Private Endpoint using the Azure portal](https://docs.microsoft.com/azure/private-link/create-private-endpoint-portal)
