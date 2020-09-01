<properties
	pageTitle="Check Tenant Enrollment Success"
	description="Check Tenant Enrollment Success"
	infoBubbleText="MDM Authority is setup correctly"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	ms.author="bretb"
	displayOrder=""
	articleId="intune_default_tenant_success_maven"
	diagnosticScenario="IntuneCheckTenantEnrollment"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft Intune subscription

<div>
No issues found, however, please review the following troubleshooting tips for more information. 
<br/>
You can change your MDM authority without opening a support case. See the following documents for instructions:
  <ol>
    <li><a href="https://docs.microsoft.com/sccm/mdm/deploy-use/migrate-change-mdm-authority" target="_blank">Change MDM authority from the Configuration Manager to Intune standalone</a></li>
    <li><a href="https://docs.microsoft.com/sccm/mdm/deploy-use/change-mdm-authority" target="_blank">Change MDM authority from Intune standalone to Configuration Manager</a></li>
  </ol>
<br/>
MDM Authority Co-Existence
  <ol>    
    <li>You can have both MDM authorities active concurrently if you already have Office 365 MDM enabled but you want to try Intune MDM.</li>
    <li>Admins who already have O365 MDM active can simply mark Intune MDM as active from the Azure portal.</li>
    <li>If you have Intune MDM but want to make use of Office 365 MDM: please open a ticket below and a support agent will help enable this for you.</li>
  </ol>
</div>