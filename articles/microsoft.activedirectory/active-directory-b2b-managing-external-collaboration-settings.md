<properties
    pageTitle="Problem managing external collaboration settings"
    description="Problem managing external collaboration settings"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="marialai"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615396"
    resourceTags=""
    productPesIds="16580"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="c79c3519-fb7b-4635-9739-f3b9a23776ab"
	ownershipId="AzureIdentity_B2C"
/>

# Problem managing external collaboration settings

## **Recommended steps**

* To allow only certain users to invite guests, add those users to the Guest Inviter role. See [how to add users to Guest Inviter role](https://docs.microsoft.com/azure/active-directory/b2b/delegate-invitations#guest-inviter-role).
* Ensure that the Guest Inviter role is enabled to send invitations. To make this change, go to [Organizational relationships - Settings](https://portal.azure.com/#blade/Microsoft_AAD_IAM/CompanyRelationshipsMenuBlade/Settings).
* To allow all users to invite guests, ensure that the **Members can invite** setting is set to **Yes**. To make this change, go to [Organizational relationships - Settings](https://portal.azure.com/#blade/Microsoft_AAD_IAM/CompanyRelationshipsMenuBlade/Settings).

## **Recommended documents**

* [Delegate invitations for Azure Active Directory B2B collaboration](https://docs.microsoft.com/azure/active-directory/b2b/delegate-invitations)
