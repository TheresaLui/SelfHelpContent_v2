<properties
	pageTitle="Problems with provisioning in MIM Sync connectors"
	description="Problems with provisioning in MIM Sync connectors"
	infoBubbleText="Problems with provisioning in MIM Sync connectors"
	service="microsoft.activedirectory"
	resource="activedirectory"
	ms.author="markwahl-msft"
	displayOrder=""
	articleId="active-directory-mim-problem-with-connectors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742347"
	resourceTags=""
	productPesIds="16666"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with provisioning in MIM Sync connectors

In Microsoft Identity Manager (MIM), a connector moves data from a connected data source to MIM Sync. When data in MIM Sync is modified, the connector can also export the data to the connected data source to keep it synchronized with MIM.  You may be able to resolve your problem with the connector if the issue was fixed in an update to the connector.

## **Recommended Steps**

1. If the problem is with the Generic LDAP, Generic SQL, Lotus Domino or Web Services connectors, ensure that you are using a recent update of the [generic connectors](https://docs.microsoft.com/microsoft-identity-manager/reference/microsoft-identity-manager-2016-connector-version-history)
2. If the problem is with the AD Connector, AD LDS Connector, FIM Service Connector, or another connector not listed above, ensure that you are using a recent supported update of [MIM Sync](https://docs.microsoft.com/microsoft-identity-manager/reference/version-history)
3. If a MIM Sync run stops with an error, consult the table of [run error codes](https://docs.microsoft.com/microsoft-identity-manager/reference/maerrorcodes)
4. If the run stops with `extension-dll-exception`, then click on those words to open the Connector Space Object properties window, and click on `Stack Trace...` to see more information on the underlying cause, as described in [Extension-DLL-Exception](https://social.technet.microsoft.com/wiki/contents/articles/7515.fim-troubleshooting-extension-dll-exception.aspx)
5. If you wish to have additional information on what led to a connector returning an error causing a run to stop, you can [Enable ETW tracing for the connector](https://social.technet.microsoft.com/wiki/contents/articles/21086.fim-2010-r2-troubleshooting-how-to-enable-etw-tracing-for-connectors.aspx) and collect the connector's events in a file or the event log

## **Recommended Documents**

* [Connector release history for generic connectors that have been released separately from MIM](https://docs.microsoft.com/microsoft-identity-manager/reference/microsoft-identity-manager-2016-connector-version-history)
* [List of supported connectors and data sources](https://docs.microsoft.com/microsoft-identity-manager/supported-management-agents)
* [Connector run error codes](https://docs.microsoft.com/microsoft-identity-manager/reference/maerrorcodes)
* [Troubleshooting Extension-DLL-Exception](https://social.technet.microsoft.com/wiki/contents/articles/7515.fim-troubleshooting-extension-dll-exception.aspx)
* [Enable ETW tracing for connectors](https://social.technet.microsoft.com/wiki/contents/articles/21086.fim-2010-r2-troubleshooting-how-to-enable-etw-tracing-for-connectors.aspx)
