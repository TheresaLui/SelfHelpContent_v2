<properties
                pageTitle="MDM Authority Not Set"
                description="MDM Authority Not Set"
                infoBubbleText="You need to set your tenant's MDM Authority before using Intune. Please review the steps on the right for how to resolve this."
                service="microsoft.intune"
                resource="intune"
                authors="rciliax"
                displayOrder=""
                articleId="intune_set_mdm_authority"
                selfHelpType="diagnostics"
                supportTopicIds="32599580,32599582,32599583,32599591,32599653,32599665"
                resourceTags=""
                productPesIds="15584"
                cloudEnvironments="public"
/>
 
# We ran diagnostics on your Microsoft Intune subscription and found an issue
 
## Recommended steps
 
<!--issueDescription-->
The mobile device management (MDM) authority of this tenant is not set. Without setting the MDM authority you won't be able to use Intune's MDM features. 
<!--/issueDescription-->

The MDM authority setting determines how you manage your devices. As an IT admin, you must set an MDM authority before enrolling and managing devices through Intune MDM. 
To review the different MDM authority options, please refer to the article [Set the mobile device management authority](https://docs.microsoft.com/intune/mdm-authority-set). After determining the appropriate MDM authority, follow the steps below to set your Intune MDM authority configuration.
 
**Step 1.** Navigate to the [Choose MDM authority](https://portal.azure.com/#blade/Microsoft_Intune_Enrollment/EnrollmentMenu/overview) blade in the Azure Portal.
 
**Step 2.** Choose the appropriate authority based on your adminstrative needs. For more information on the options listed, reivew how to [Set the mobile device management authority](https://docs.microsoft.com/intune/mdm-authority-set).
