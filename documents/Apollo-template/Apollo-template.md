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

<!--This template demonstrates best practices for Apollo articles for the Azure self-help platform. See tips [add internal link] in this template and see best practices [add link to separate document] for detailed guidance
Use the required title and headings in the order shown. Remove any optional headings you don’t need. 
In the body, use markdown for all elements, except for the following which use HTML tags: diagnostics/insights, charts, and videos..-->

# Template in progress! <!--swap this out when published: Internal-only title required for internal reference-->
<br> <!--Insert a blank line after every heading-->
## Title <!--Required. Level 2 heading that describes the article contents. Capitalize only the first word and product names (i.e., use sentence capitalization).-->
<br> <!--Insert a blank line after every heading-->
Clearly state the problem and include any relevant details not included in the title.<br>
For example: "Resolve issues for <problem_type> with these solutions." <br>
Alternatively, summarize the article and how it will help the customer.<br>
For example: "Learn more about setting up a new domain by watching this video."-->

## Sample body
<br> <!--Insert a blank line after every heading-->
The body contains the main content and contains the solution. It may include or more of the following components:
- Diagnostics (including insights/results)
- Metrics
- Solutions 
- Images
- Videos
- Azure KB and docs links
 

## Sample diagnostic
Below is an example of an insight. Use bullets and line breaks to present the textual information.
Briefly explain how this diagnostic provides helpful information to the customer about their issue.  

<Insight> 
*	<symptomId>NrtVmRestartAzurePortalInsight</symptomId><br>
*	<executionText>We are checking to see if your VM was restarted</executionText><br>
*	<timeoutText>Proceeding to the next operation</timeoutText><br>
*	<noResultText>No problems found. Your VM is running smoothly.</noResultText><br>
</Insight>

<Insight>
*	<symptomId_noloc>CannotRdpAzurePortalInsight1, CannotRdpAzurePortalInsight2, CannotRdpAzurePortalInsight3</symptomId_noloc><br>
*	<executionText>Assessing VM connectivity now<br></executionText><br>
*	<timeoutText>The diagnostic took longer than expected, so we stopped it<br></timeoutText><br>
*	<noResultText>Diagnostics are complete. No problems were found.</noResultText><br>
*	<additionalInputsReq>true</additionalInputsReq><br> 
</Insight><br>

## Sample guided troubleshooting 
<br> <!--Insert a blank line after every heading-->
<!--Include 1-2 sentences that point out specific aspects of the chart and explains how they are relevant to the problem. This summary is required to ensure accessibility for screen readers.

For example:
“Here is your CPU usage for the past 24 hours. Spikes indicate process-intensive operations which are affecting overall performance.”-->

Below is an example of a metric from Azure Monitor. Include bullets and line breaks to present the textual information.
<metric>
*	<name>Disk Write Operations/Sec</name> <!--Type of metric--><br>
*	<aggregationType>Sum</aggregationType> <!--Specify Sum, Avg, Count, or Percentile (default is value Sum)--><br>
*	<timeSpanDuration>1d</timeSpanDuration><!--Use these time measures: d for day, m for minute (default value is 1d)--><br>
*	<title>Virtual Machine Disk Write Operations/Sec</title><!--Include a title that clearly describes the information--><br>
</metric>

## Sample solution  
<br> <!--Insert a blank line after every heading-->
<!--Solutions must be instructions or videos specific to the problem statement, not just links to other articles-->

Below is an example of an ordered list. Use ordered lists for tasks that must be performed in a sequence.

<br> <!--Insert a blank line after every heading-->
### Sample ordered list  
<br> <!--Insert a blank line after every heading-->
1. This is a step with a link to an [external article](https://)
2. This is a step with no link, blade, or instructions. Note that because the next line is a continuation of the list, no <br> (br) break is needed.
3. As in the example above, this step contains multiple sentences. When a step has multiple complete sentences, the use of a period to end each sentence is acceptable.
4. This step does not have multiple sentences, so no period is required at the end
5. This is a step with a [link to a blade](data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam)
6. This is a step with a single line or snippet of code: `SELECT name, is_disabled FROM sys.sql_logins`
7. This is a step with multi-line code:

```
[cluster my-cluster]
    FormLayout = selectionpanel
    Category = My Templates
    CategoryOrder = 100
    MaxCount = 200
    Autoscale = $Autoscale
```
All lists require an empty line before the first item and after the last item.


### Sample bulleted list
<br> <!--Insert a blank line after every heading-->
Below is an example of a bulleted list. Only two levels of bullets are supported. (For step-by-step instructions, use an ordered list instead.)

* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB

All lists require an empty line before the first item and after the last item.


### Sample inline image
<br> <!--Insert a blank line after every heading-->
Below is an example of an inline image
![alt text](/images/image.png)
<!--Image requirements: Replace alt text with a concise description of what is being shown in the image (without punctuation). This ensures accessibility, required by Microsoft. Include only screenshots that contain legible text. Use colored boxes, not highlighting, for callouts.-->

### Sample videos
<br> <!--Insert a blank line after every heading-->
<!--Include a caption that describes how the video addresses this issue. Call out highlights of the video and include timecode to save the reader from having to scrub through it. To be accessible, video must include captions, a transcript, and audio description, and is delivered in an accessible media player.-->

**Video example 1 - Single video**

   Caption example: This video explains the difference between stopping a virtual machine in Windows and shutting it down with Azure IaaS. Benefits of each are highlighted at frame 1:30.<br>

<video>
	<src>https://www.youtube.com/watch?v=-Peb5IPGvVI</src>	
	<title>How to use Azure Bastion to securely connect to your VMs, 4:11</title>  
</video>

**Video example 2 - Multiple videos**<br>

   Caption example: The following videos can help you reduce costs associated with VMs.
   
<videoGroup>
	<video>
		<src>https://www.youtube.com/watch?v=-Peb5IPGvVI</src>	
		<title>How to use Azure Bastion to securely connect to your VMs, 4:11</title> 
	</video>
	<video>
		<src>https://www.youtube.com/watch?v=-Peb5IPGvVI</src>	
		<title>How to use Azure Bastion to securely connect to your VMs, 4:11</title> 
	</video>
</videoGroup>


## Recommended resources // Optional section. Level 2 heading required. 
<br> <!--Insert a blank line after every heading-->
<!--In this section, include relevant document links (not found in the preceding sections) from the following approved sources: MS docs, MSDN, and Stack Overflow.-->

This is an example of Azure KB portal and article links: 
<azureKB>
	<client>Portal</client>
</azureKB>
<CommonSolution>
	<articleId>d67fb475-a831-4f4b-a6ce-7fbacb0bf9df</articleId>
	<client>Portal</client>
</CommonSolution>



<!--Article close. Include this text "as is" in all topics.-->
> If you’ve followed the preceding steps and are still experiencing the issue, file a support ticket at Help + support - Microsoft Azure. 
 



<!--IN SUMMARY:
* Formatting is not identical to Microsoft Docs - tables do not work, neither do [!NOTE] tags
* Solutions should be instructions, recommendations, or videos, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, (i.e., they do not include /en-us/). This does not apply to articles for Mooncake.
* Don't link to internal review documentation. These URLs always start with "review.microsoft.docs", and users are unable to access them.
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the properties metadata at the beginning of this article.
-->
