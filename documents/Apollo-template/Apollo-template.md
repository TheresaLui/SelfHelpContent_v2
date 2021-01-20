<!--DIRECTIONS: Copy the raw form of this article to create Apollo common solutions articles for the Azure self-help platform. Include the required properties, title, and body sections in the order shown. Use markdown, except where HTML is specified. Be sure to review the <Rules> at the end of this template to prevent validation errors.-->

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


# Apollo template title 
<br> 
<!--Head1 required for internal reference only--> 

Directions: Copy the raw form of this article to create Apollo common solutions articles for the Azure self-help platform.

## Title - Required
<!--Clearly state the specific issue and how the article addresses it. Use sentence capitalization for all headings. 
Example: "Resolve issues related to configuring NetApps by reviewing these best practices." <br>
Alternatively, summarize general articles by stating how the article will help the customer.<br>
For example: "Learn how to adjust resource limits for NetApp files by watching the following video."-->

## Body - Required
<!--The body contains the main content. In a solution-based article, the body includes the solution and any other information that can help the customer resolve the stated issue. The body can include the following elements: 
- Diagnostics  
- Metrics 
- Images 
- Videos 
- Azure KB and document links-->
 

## Sample diagnostic
<!--Explain how this information can help the customer. Include bullets and line breaks in insights to improve readability.
Example:
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
-->

## Sample guided troubleshooting
<!--Include 1-2 sentences that point out specific aspects of the chart, how they are relevant to the issue, and next steps to resolve the issue. This text is required to ensure accessibility for all users. 
Example:
“Here is your CPU usage for the past 24 hours. Spikes indicate process-intensive operations which are affecting overall performance.”
<metric>
*	<name>Disk Write Operations/Sec</name> Type of metric
*	<aggregationType>Sum</aggregationType> Specify Sum, Avg, Count, or Percentile (default is value Sum)
*	<timeSpanDuration>1d</timeSpanDuration> Use these time measures: d for day, m for minute (default value is 1d)
*	<title>Virtual Machine Disk Write Operations/Sec</title> Include a title that clearly describes the information
</metric>
-->

## Sample solutions
<!--Solutions must be instructions or videos specific to the problem statement, not just links to other articles.
Use ordered (numbered) lists for a sequence of tasks. Example:
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
Use uordered (bullet) lists for non-sequential tasks. Example:
* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB
-->

### Sample inline image
<!--Use the following format for images. Replace alt text with a description of what is being shown, without punctuation, to ensure accessibility. 
![alt text](/images/image.png)
-->

### Sample videos
<!--Include a caption that describes how the video addresses this issue. Call out highlights of the video and include timecode to save the reader from having to scrub through it. To be accessible, video must include captions, a transcript, and audio description, and is delivered in an accessible media player.-->

<!--
Single video example:
Caption
<video>
	<src>https://www.youtube.com/watch?v=-Peb5IPGvVI</src>	
	<title>How to use Azure Bastion to securely connect to your VMs, 4:11</title>  
</video>
Multiple video example:
Caption
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
-->

## Sample of recommended resources
<br> <!--Insert a blank line after every heading-->
<!--Include relevant document links that are NOT in the body/solution. Approved sources include: MS docs, MSDN, and Stack Overflow.
<azureKB>
	<client>Portal</client>
</azureKB>
<CommonSolution>
	<articleId>d67fb475-a831-4f4b-a6ce-7fbacb0bf9df</articleId>
	<client>Portal</client>
</CommonSolution>
-->

<!--Include the following text at the end of all topics.-->
**Contact us**
> If you’ve followed the preceding steps and are still experiencing the issue, file a support ticket at Help + support - Microsoft Azure. 
 

<!--RULES:
* Use active, imperative verbs and present tense (not passive verbs; not past or future tense) 
* Use contractions (“don’t” instead of “do not”; “you’ll” instead of “you will”) 
* Use sentence capitalization for all headings (capitalize only the first word) 
* Check product, feature, and service names for accuracy, including capitalization 
* Spell out product, feature, and service names on first mention, followed by acronym in parentheses (“Azure Active Directory (AAD”), and after that, use the acronym (“AAD”) 
* Use “select,” not “click” 
* Don’t use “please” 
* Bold all UI elements. Don’t overuse bold in text. 
* Use code formatting for code (inline and block), values, parameters, properties, operations, methods, functions, language keywords, and directory and file names 
* Enclose error messages in text in quotation marks 
* Insert a blank line after every heading
* All lists require an empty line before the first item and after the last item.
* Tables using Markdown will work.
* Don't link to internal review documentation. These URLs always start with "review.microsoft.docs", and users are unable to access them.
* Do not use aka.ms links
-->
