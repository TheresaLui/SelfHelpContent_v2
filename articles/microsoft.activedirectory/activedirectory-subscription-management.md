Removing “seat subscriptions”
=============================

*Note: this is self-help content that will be shown in the context of a
“delete my AAD tenant”*

Microsoft Online Service subscriptions are related to products that
require user level license assignment, for example: Office 365
Enterprise E3, Enterprise Mobility + Security or Azure AD Premium.

To delete an Azure AD tenant, all subscriptions hosted in the tenant
need to be cancelled or moved to another tenant.

To view the list of all subscriptions present in your tenant go to the
[Office 365 Admin
Center-&gt;Billing-&gt;Subscriptions](https://portal.office.com/adminportal/home#/subscriptions).
You can see the type of each subscription (e.g. trial or paid) as well
as their state (active or expiring).

Your ability to manage subscriptions depends on how they were originally
purchased:

1.  Subscriptions purchased directly via Microsoft commerce systems
    (including trials) can be cancelled directly in Admin Center.
    \#\#\#Add blurb about how\#\#\#

2.  Subscriptions purchase via Enterprise Agreements cannot be canceled
    via Admin Center. Please contact your account manager to manage
    those subscriptions.

3.  Subscriptions created by a Cloud Solution Provider partner cannot be
    canceled via Admin Center. Please contact the partner using the
    information provided in the Admin Center for that subscription.

4.  If you would like to move a subscription to a different tenant, or
    have problems cancelling subscriptions, please open a
    support ticket. \#\#\#link to a very specific support path related
    to Office 365 commerce who handle these types of subscriptions\#\#\#

Note: when a subscription is cancelled it takes some time before it is
fully removed from the tenant. Typically that time is around \#\#\#day
value\#\#\#. Tenants cannot be deleted until all subscriptions are fully
removed. If you require the tenant to be removed sooner, please open a
support ticket to request quicker removal of all subscriptions
\#\#\#link to the specific support path\#\#\#

I can't assign licenses to a user or group &lt;- self-help blade
================================================================

To manage user licenses, you need to use an account with one of the
required [administrator
roles](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-assign-admin-roles):
Global Administrator or User Administrator. You can check the user’s
role in the **Directory role** tab on the user blade.

Here are some helpful tips for diagnosing problems with license
assignment:

1.  If you are using the Azure portal and license assignment is failing,
    click on the notification in the upper right hand corner. This will
    open a blade with more details about what went wrong, including all
    the common problem cases listed below.

2.  Before a license can be assigned to a user, the Usage Location
    property must be set for the user. Make sure the user has the
    property set by viewing the **Profile** tab on the user blade.

3.  Make sure there are enough available licenses for the product you
    are trying to assign. In the Azure portal, go to [Azure Active
    Directory-&gt;Licenses-&gt;All
    products](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)
    to see the number of available licenses.

4.  The user may already have another license with services that
    conflict with the new license you are trying to assign. For example,
    if the user has the *Exchange Online (Plan 1)* service enabled you
    won’t be able to assign a license with the *Exchange Online
    (Plan 2)*. One of the services will need to be disabled to allow the
    new license assignment.\
    \
    If you are using the Azure portal or PowerShell cmdlets the error
    message will list the specific services that are causing
    the conflict.

5.  If you are trying to remove a license and that is failing, it is
    possible the user has other licenses with services that depend on
    the services you are trying to remove.\
    \
    If you are using the Azure portal or PowerShell cmdlets the error
    message will list the specific services that have dependencies.

6.  If you are trying to assign a license to a group and groups are not
    listed in the assignment pane, please note that [group-based
    licensing](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-licensing-whatis-azure-portal)
    is currently in Public Preview and available only in tenants with
    licenses for Azure AD Basic or above.

