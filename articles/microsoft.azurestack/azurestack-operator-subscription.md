<properties
    pageTitle="Azure Stack subscriptions"
    description="Issues related to Azure Stack subscriptions"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629263"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="azurestack-operator-subscription"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Azure Stack subscriptions

[Offers](https://docs.microsoft.com/azure-stack/operator/azure-stack-overview) are groups of one or more plans that providers present to users, which those users can buy or subscribe to. This article describes how to create an offer that includes the [plan that you created](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-plan). This offer gives subscribers the ability to set up virtual machines (VMs).

## **Recommended Steps**

After you [create an offer](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-offer), users need a subscription to that offer before they can use it. There are two ways that users can get subscribed to an offer:

* As a cloud operator, you can create a subscription for a user from within the administrator portal. Subscriptions you create can be for both public and private offers. For more information, see: [Create a subscription as a cloud operator](https://docs.microsoft.com/azure-stack/operator/azure-stack-subscribe-plan-provision-vm#create-a-subscription-as-a-cloud-operator)
* As a tenant user, you can subscribe to a public offer when you use the user portal. For more information see: [Create a subscription as a user](https://docs.microsoft.com/azure-stack/operator/azure-stack-subscribe-plan-provision-vm#create-a-subscription-as-a-user)

## **Recommended Documents**

* [Plan, offer, quota, and subscription overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview)
* [Offers](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview#offers)
* [Subscription](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview#subscriptions)
* [Manage API version profiles](https://docs.microsoft.com/azure-stack/user/azure-stack-version-profiles)
