<properties
	pageTitle="My Azure Private Link connectivity is not working"
	description="My Azure Private Link connectivity is not working"
	infoBubbleText="Troubleshoot Azure Private Link connectivity problems"
	service=""
	resource=""
	authors="rdhillon,sumi"
	ms.author="rdhillon,sumi"
	displayOrder=""
	articleId="722d2f21-85d2-42e8-99fb-d944c9d98005"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32681488"
	resourceTags=""
	productPesIds="16843"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_PrivateLink"
/>

# My Azure Private Link connectivity is not working

Try the troubleshooting steps below if your Azure Private Link service connectivity is not working.

## **Recommended Steps**

1. Verify that Private Endpoints that you are trying to connect to are in **Approved** state. If they are in **Pending** state, approve them for connectivity.
2. Verify that the **Aliases / Resource ID** for Private Endpoints are correct
3. Review the Azure Load Balancer information for correctness and check whether it is working as expected
4. Use Azure Monitor for Private Link Service to check the data path status

## **Recommended Documents**

* [Troubleshoot Azure Private Link Service connectivity problems](https://docs.microsoft.com/azure/private-link/troubleshoot-private-link-connectivity)
* [Create a Private Link service using the Azure portal](https://docs.microsoft.com/azure/private-link/create-private-link-service-portal)
