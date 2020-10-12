<properties
    pageTitle="Group-based licensing"
    description="Group-based licensing"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="SumitParikh"
    ms.author="sumitp"
    displayOrder="1770"
    supportTopicIds="32615386"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="531923ab-135b-47e4-a02f-2ef2a0f05a24"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Group-based licensing

**Prerequisites**

1. To manage licenses on groups, you must use an account with one of the required [administrator roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles): Global Administrator, License Administrator or User Account Administrator. You can check the user’s role in the **Roles and administrators** tab on the Overview blade.
2. If you are using the Azure portal and license assignment is failing, make sure to click the notification in the upper-right corner. This opens a blade with details about what went wrong. In most cases, the information in the notification pop-up window should be sufficient to understand the underlying problem and implement a solution.
3. Assigning licenses to groups has limitations. Learn more about the limitations and known issues [here](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#limitations-and-known-issues).
4. Learn more about licensing requirements to assign licenses to groups [here](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal#licensing-requirements). You can check if you meet licensing requirements by going to [Licenses/All products](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products) in the Azure portal.

## **Recommended Steps**

1. If you cannot assign a license to a group, check if the group is a security group. Office 365 groups and distribution groups are currently not supported.
2. When a license is assigned or modified for a group it may take a while for the changes to be reflected on the users. To [confirm the status of license processing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal#step-2-verify-that-the-initial-assignment-has-completed) go to the **Licenses** tab of the group. If processing changes takes hours, please try reprocessing by clicking the Reprocess button. If you see your changes take more than 24 hours to process, please open a support ticket to allow us to investigate.
3. In certain situations, licenses cannot be assigned or removed from users. When investigating a problem with a user, make sure to go to the user's **Licenses** tab to view the complete information about their state; in most cases that is enough to understand the problem and solve it. Get more information on the state and details to resolve the issue [here](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal).
4. If some users did not receive licenses from the group and [you did not identify any errors in the portal](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal), then, check if the [proxy address configuration is correct](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal#license-assignment-fails-silently-for-a-user-due-to-duplicate-proxy-addresses-in-exchange-online) in Exchange Online.
5. To prevent users in your organization getting enabled for new Microsoft services added to existing products, follow the steps [here](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#managing-new-services-added-to-products) to disable newly added services.
6. If you want to understand why a license was added/removed from a user or a group (for example, who else in your organization may have made changes) review the [audit logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit). Setting the filter to license activities will show all modifications including the "actor" that performed them.
7. PowerShell support for group-based licensing is currently limited, but some functionality is exposed via PowerShell v1.0 cmdlets and MS Graph. [See here for examples](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-ps-examples).
