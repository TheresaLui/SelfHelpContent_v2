<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot becuse it is stuck on the Hyper-V procress."
    infoBubbleText="A boot error occurred because your VM failed to boot becuse it is stuck on the Hyper-V procress."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="BootError-HYPERV"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error

<!--issueDescription-->

We have investigated and determined that your virtual machine is in an inaccessible state because we could not find an operation system.

<!--/issueDescription-->


## **Recommended Steps**

1. Proceed with a redeploy, which will move the VM to another host
2. If that does not resolve the problem, recreate the VM so it is allocated in a different cluster all together
