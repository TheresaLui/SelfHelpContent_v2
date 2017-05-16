<properties
	pageTitle="Virtual Network selection and configuration issues"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="generic"
	supportTopicIds="32570966"
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Virtual Network selection and configuration issue

## **Recommended steps**
1.	If planning on using an existent virtual network, ensure it is deployed in the same [Azure Region](https://azure.microsoft.com/regions/#services/) as your Azure AD Domain Services managed domain. 
2.  If planning on using an existent virtual network, ensure it is a classic Azure [regional virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-networks-migrate-to-regional-vnet). Note: Azure AD Domain Services cannot be enabled in virtual networks created using Azure Resource Manager.
3.  If planning on using an existent virtual network, ensure 
4.  Ensure the virtual network does not have custom DNS servers configured. 
5.  Ensure that you don't have an existent domain with the same domain name, available on the virtual network.
6.  If you need to connect the Azure AD Domain Services classic vitual network with a resource manager-based vritual network, see [network connectivity](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-networking#network-connectivity).

## **Recommended documents**
* [Migrating legacy virtual networks to regional virtual networks](https://docs.microsoft.com/azure/virtual-network/virtual-networks-migrate-to-regional-vnet)
* [Azure AD Domain Services troubleshooting guide](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting) 
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
