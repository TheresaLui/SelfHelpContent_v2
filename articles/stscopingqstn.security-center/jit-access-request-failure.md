<properties
    pageTitle="JIT Access request failure"
    description="How to resolve a JIT Access request failure"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680772"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="b43f0825-9006-480d-86a8-a5520821b4f1"
	ownershipId="Azure_Security_Security_Center"
/>

# JIT Access request failure

To request access for Just in Time (JIT), you need these permissions:

* Owner
* Contributor
* Security Admin
* Custom role:
  * For the least permissive access, a custom role can be defined to allow only JIT Access request, while denying any other involvement in the subscription.
  * Custom roles definitions are described [here](https://docs.microsoft.com/azure/security-center/security-center-just-in-time#permissions-needed-to-configure-and-use-jit)

If you comply with all of the above, and still receive an error in the Activity Log, please continue creating the support request (providing the Activity Log JSON) and describe whether the request was initiated from the Security Center portal or from the virtual machine (VM) connect button.

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
