<properties
	pageTitle="Problems with provisioning in MIM Service or MIM Portal"
	description="Problems with provisioning in MIM Service or MIM Portal"
	infoBubbleText="Problems with provisioning in MIM Service or MIM Portal"
	service="microsoft.activedirectory"
	resource="activedirectory"
	ms.author="markwahl-msft"
	displayOrder=""
	articleId="active-directory-mim-problem-with-service-or-portal"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742348"
	resourceTags=""
	productPesIds="16666"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with provisioning in MIM Service or MIM Portal

Microsoft Identity Manager (MIM) Service and Portal are components of Microsoft Identity Manager. You may be able to resolve your problem with MIM Service or MIM Portal if the issue was addressed in a recent update to MIM, or is one of the other issues mentioned below.

## **Recommended Steps**

1. Ensure that you are using a recent update of MIM and check the [release notes](https://docs.microsoft.com/microsoft-identity-manager/reference/version-history) to determine if the issue has been resolved in an update
2. If you are encountering an error during installation and have configured Exchange Online, then there may be a local security policy problem, as described in the [Support-Tip EXO Configuration Failure during installation](https://docs.microsoft.com/archive/blogs/iamsupport/support-tip-installation-exo-configuration-failure-during-installation)
3. If you are encountering an error of `stopped-server` with `failed-creation-via-web-services` using the FIM Service Management Agent, see [Support-Info: failed-creation-via-web-services](https://docs.microsoft.com/archive/blogs/iamsupport/support-info-fimma-failed-creation-via-web-services) for an overview of causes


## **Recommended Documents**

* [MIM version history](https://docs.microsoft.com/microsoft-identity-manager/reference/version-history)
* [Support-Tip EXO Configuration Failure during installation](https://docs.microsoft.com/archive/blogs/iamsupport/support-tip-installation-exo-configuration-failure-during-installation)
* [Support-Info: failed-creation-via-web-services](https://docs.microsoft.com/archive/blogs/iamsupport/support-info-fimma-failed-creation-via-web-services)
