<properties
	pageTitle="Default synchronization rules have been changed"
	description="Default synchronization rules have been changed"
	infoBubbleText="Found that some default synchronization rules have been modified"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="neliceat"
	displayOrder="1"
	articleId=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32404459"
	resourceTags=""
	productPesIds="14785"​
	cloudEnvironments="public"
/>

# Default synchronization rules have been changed
<!--issueDescription-->
Synchronization rules are a critical component in the Azure AD Connect (AADConnect) configuration, and when AADConnect is first installed it comes with several default synchronization rules.  
We noticed that one or more default synchronization rules in your Azure AD Connect installation had changes applied to them. It is not supported to make changes to the default synchronization rules.  
<!--/issueDescription-->

## **Recommended steps**

1. If you need to change the way a synchronization rule behaves, you should instead create a clone of the default synchronization rule and modify that cloned copy. This article provides details about how to modify synchronization rules in a supported manner: <br>
[Best practices changing default configuration - Changes to synchronization rules](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync-best-practices-changing-default-configuration#changes-to-synchronization-rules) <br>
2. Synchronization rules are implemented through a declarative provisioning  model, and you can read more about this model in this article: <br>
[Understanding declarative provisioning](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync-understanding-declarative-provisioning)<br>
3. To recover from this issue, you must clone the modified rule. By doing so, their changes will not be overwritten when the AADConnect deployment is upgraded to a new version. This document describes in detail how to do this: <br>
[Best practices changing default configuration - Changes an out-of-box rule](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync-best-practices-changing-default-configuration#change-an-out-of-box-rule) <br>


## **Recommended documents**

* [Learn more about the Default Synchronization Rules in Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync-understanding-default-configuration#synchronization-rule)<br>
