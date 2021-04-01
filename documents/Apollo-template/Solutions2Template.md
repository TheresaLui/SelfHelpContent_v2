<!--For information about each property, see the Metadata page-->
<properties
	pageTitle="Apollo common solutions"
	description="Apollo common solutions"
	ms.author="bernardm"
	displayOrder=""
	articleId="0008d965-e21e-4e73-80ef-0ccc0765fb0c"
	selfHelpType="Apollo"
        supportTopicIds="7d8fb79f-7fbc-7125-b4dc-3060a75a755d"
        productPesIds="16342,16065,15797,16454,16470"
	cloudEnvironments="public"
	ownershipId="b6015c21-c91a-4248-8d13-426894cd5140"
/>
<!--**Directions:** Copy the raw form of this page to create a Solution 2.0 (Apollo) article. <br>
Be sure to review the **Validation Rules & Checklist** at the end of this template to prevent soft validation errors and comply with [Authoring Guidelines](https://azsupportdocs.azurewebsites.net/elixir/articles/AuthoringGuidelines.html).-->

<!-- H1 title is required and is used only internally -->
# Title
 
<!--Required H2 title. This is presented to the customer-->
## Issue Title
 
<!--Clearly state the specific issue and how the article addresses it. Use sentence capitalization for all headings (capitalize only the first word).
Example: "Resolve issues related to configuring NetApps by reviewing these best practices."
Alternatively, for how-to or conceptual articles, summarize the article and how the article will help the customer.
For example: "Learn how to adjust resource limits for NetApp files by watching the following video."-->
 
Description of the issue
 
<!--Next is the Body. Body contains the main content.  At minimum, the body of the article must contain substantive content that clearly addresses the topic or issue.
- For a solution-based article, define the issue and provide one or more solutions.
- For a how-to or general information article, provide instructions (e.g., steps, video, links, etc.)
 
Solutions can comprise of the following components:
- Procedures / Plain markdown content that contains recommended steps, and document links
- Diagnostics
- Azure Monitor Metric charts
- Images
- Videos
- AzureKB
-->
 
### Procedures title. <!-- Use Procedures when the solution is a task-based procedure. -->
 
For a sequence of tasks, use ordered (numbered) lists.
Example:
1. This is a step
2. This step contains multiple sentences. When a step has multiple complete sentences, use a period to end each sentence.
3. This is a step with a [link](http://)
4. This is a step with inline code: `SELECT name, is_disabled FROM sys.sql_logins`
5. This is a step with multi-line code:
 
```
[cluster my-cluster]
    FormLayout = selectionpanel
    Category = My Templates
    CategoryOrder = 100
    MaxCount = 200
    Autoscale = $Autoscale
```
 
For non-sequential tasks, use unordered (bullet) lists.
Example:
* Item1
* Item2
* Item3
    * Sub-ItemA
    * Sub-ItemB
 
<!-- This is the format to include "Images". No heading required. Use the following format, replacing "alt text" with a description of what is being shown, without punctuation, to ensure accessibility for all users.
![alt text](https://wallpapercave.com/wp/mJRWj5T.jpg)
-->
 
### Diagnostics Title <!-- Title is required. Example: VM Connectivity diagnostics -->
 
<!--Insight Diagnostics available in the Azure Diagnostic Service can be presented to customers during case submission and on the Diagnose and Solve problems page in the Azure portal. -->
 
<insight>
    <symptomId></symptomId> <!-- Add the symptomIds of the diagnostics you want to execute in this block. Learn more: <link> -->
    <executionText></executionText> <!-- Be specific on what checks the diagnostics will be performing on the resource E.g: We are checking to see if your VM was restarted-->
    <timeoutText></timeoutText> <!-- Timeout text E.g: This check was taking too long, so we stopped the operation -->
    <noResultText></noResultText> <!-- Text when no issues are found by the diagnostic. E.g: No problems found. Your VM is running smoothly -->
    <additionalInputsReq>false</additionalInputsReq> <!-- This property should be set to true, if you wish to collect additional information from the customer for your diagnostics to run. Learn more about Scoping questios for Diagnostics : https://support-docs.azurewebsites.net/docs/articles/onboarding/diagnostics/enableDsq.html#create-or-update-scoping-questions-file  -->
    <maxInsightCount>2</maxInsightCount> <!-- By default the portal will return a maximum of 3 critical insights. If you need to adjust this number then mention the number in this property -->
</insight>
 
### Chart title <!--Level 3 heading required. -->
 
Description <!-- Explain what information to look for and how the reader will use that information. This text is required to ensure accessibility for all users. -->
 
<metric>
    <name></name> <!-- Metric namespace emitted by Azure Monitor. E.g.: Percentage CPU for a virtual machine -->
    <aggregationType></aggregationType> <!--Defines how you want to aggregate data on the chart . Values: Sum, Avg, Count, Min, Max. Default: Sum -->
    <timeSpanDuration></timeSpanDuration> <!-- Metrics is a time series data. This property shows the period when the data will be plotted and relative to the current time (UTC). Default: 1d -->
    <title></title> <!-- Title of the chart displayed right above the chart Example: Virtual Machine Disk Write Operations/Sec -->
</metric>
 
### Videos <!--Level 3 heading required. -->
 
Video Description <!-- Include a caption that describes how the video addresses this issue. Call out highlights of the video.
To be accessible, video must include captions, a transcript, and audio description, and is delivered in an accessible media player.-->
 
<!-- Single video example: -->
 
Description of the video
 
   <video>
    <src></src> <!-- Video source. E.g: https://www.youtube.com/watch?v=-Peb5IPGvVI -->
    <title></title>  <!-- Title of the video. E.g: How to use Azure Bastion to securely connect to your VMs -->
   </video>
 
Outline steps covered in the video
 
<!-- Multiple video example:-->
 
    Description of the videos
 
    <videoGroup>
        <video>
            <src></src> <!-- Video source. E.g: https://www.youtube.com/watch?v=-Peb5IPGvVI -->
            <title></title>  <!-- Title of the video. E.g: How to use Azure Bastion to securely connect to your VMs -->
        </video>
        <video>
            <src></src> <!-- Video source. E.g: https://www.youtube.com/watch?v=-Peb5IPGvVI -->
            <title></title>  <!-- Title of the video. E.g: How to use Azure Bastion to securely connect to your VMs -->
        </video>
    </videoGroup>
 
### Resources Title <!-- Additional resources title needed -->
 
<!-- Include links that aren't already listed in the solution. Approved sources include: MS docs, MSDN, and Stack Overflow. -->
 
<!-- You can also use Markdown syntax: [Description of document](URL) -->
 
Here are some relevant results from the web:
<azureKB>
  <client>portal</client>
</azureKB> 


