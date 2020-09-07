<properties
	pageTitle="Problems with provisioning in MIM Sync"
	description="Problems with provisioning in MIM Sync"
	infoBubbleText="Problems with provisioning in MIM Sync"
	service="microsoft.activedirectory"
	resource="activedirectory"
	ms.author="markwahl-msft"
	displayOrder=""
	articleId="active-directory-mim-problem-with-sync"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742349"
	resourceTags=""
	productPesIds="16666"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with provisioning in MIM Sync

Microsoft Identity Manager (MIM) Synchronization Service is a component of Microsoft Identity Manager. It is a centralized on-premises service that stores and integrates information for organizations that have multiple on-premises directories and databases. You may be able to resolve your problem with MIM Sync if the issue was addressed in a recent update to MIM or is one of the other issues mentioned below.

## **Recommended Steps**

1. Ensure that you are using a recent update of MIM Sync and check the [MIM Sync release notes](https://docs.microsoft.com/microsoft-identity-manager/reference/version-history) to determine if the issue has been resolved in an update
2. If the problem is with the Generic LDAP, Generic SQL, Lotus Domino or Web Services connector, ensure that you are using a recent update of the [generic connectors](https://docs.microsoft.com/microsoft-identity-manager/reference/microsoft-identity-manager-2016-connector-version-history)
3. If a MIM Sync run stops with an error, consult the table of [run error codes](https://docs.microsoft.com/microsoft-identity-manager/reference/maerrorcodes) to determine the potential causes
4. If the run stops with ```extension-dll-exception```, then click on those words to open the Connector Space Object properties window, and click on ```Stack Trace...``` to see more information on the underlying cause, as described in [Extension-DLL-Exception](https://social.technet.microsoft.com/wiki/contents/articles/7515.fim-troubleshooting-extension-dll-exception.aspx)
5. If the Password Change Notification Service (PCNS) component reports error 6025 in the event log during password synchronization, check the guide for troubleshooting [PCNS reporting error 6025](https://social.technet.microsoft.com/wiki/contents/articles/4159.pcns-troubleshooting-event-id-6025.aspx)
6. If full synchronization with the FIM Service Management Agent is slow, check the auto grow setting for TempDB, as described in [Troubleshooting slow or hanging full synchronization](https://social.technet.microsoft.com/wiki/contents/articles/14713.troubleshooting-fim-performance-slow-or-hanging-full-synchronization.aspx)
7. If you are encountering an error of ```stopped-server``` with ```failed-creation-via-web-services``` using the FIM Service Management Agent, see [Support-Info: failed-creation-via-web-services](https://docs.microsoft.com/archive/blogs/iamsupport/support-info-fimma-failed-creation-via-web-services) for an overview of causes

## **Recommended Documents**

* [MIM version history](https://docs.microsoft.com/microsoft-identity-manager/reference/version-history)
* [Connector run error codes](https://docs.microsoft.com/microsoft-identity-manager/reference/maerrorcodes)
* [PCNS reporting error 6025](https://social.technet.microsoft.com/wiki/contents/articles/4159.pcns-troubleshooting-event-id-6025.aspx)
* [Troubleshooting slow or hanging full synchronization](https://social.technet.microsoft.com/wiki/contents/articles/14713.troubleshooting-fim-performance-slow-or-hanging-full-synchronization.aspx)
* [Support-Info: failed-creation-via-web-services](https://docs.microsoft.com/archive/blogs/iamsupport/support-info-fimma-failed-creation-via-web-services)
