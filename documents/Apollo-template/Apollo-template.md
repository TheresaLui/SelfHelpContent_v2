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

# Internal-only title  // Required. Level 1 heading for internal reference only. 
<br>//Insert a black line after every heading.

## Title //Required. Level 2 heading that briefly describes the issue (5-7 words, optimally). 
<br>//Insert a black line after every heading.
For example: “Windows Virtual //Desktop: Connectivity issues”. Use sentence capitalization---first word and product names or features only.

//Introduction: Required. No heading. Clearly describe the issue and any relevant details not included in the title. Alternatively, summarize the article and how it will help the customer.
This topic can help you resolve issues <on X problem> by providing useful solutions and documentation. Review the solutions and documentation first. If the issues continue, then file a support ticket.

## Sample diagnostics
<br>//Insert a black line after every heading.

// About this section: Graphs and diagnostics from Azure portal metrics will be visually contained in a card.
If we’re using terms like diagnostic/insight and metric, let’s make it clear in the introductory text to the user how to use each.


<Insight> 
	<symptomId>NrtVmRestartAzurePortalInsight</symptomId>
	<executionText>We are checking to see if your VM was restarted</executionText>
	<timeoutText>Proceeding to the next operation</timeoutText>  
	<noResultText>No problems found. Your VM is running smoothly. </noResultText> 
</Insight>

//Include an example of intro sentence and bulleted results.


<Insight>
	<symptomId_noloc>CannotRdpAzurePortalInsight1, CannotRdpAzurePortalInsight2, CannotRdpAzurePortalInsight3</symptomId_noloc> //TBD
	<executionText>Assessing VM connectivity now </executionText>
	<timeoutText> The diagnostic was taking longer than expected, so we stopped it</timeoutText> 
	<noResultText>Diagnostics are complete. No problems found. </noResultText>
	<additionalInputsReq>true</additionalInputsReq> //TBD
</Insight>

<metric>
	<name>Disk Write Operations/Sec</name> //Type of metric
	<aggregationType>Sum</aggregationType> // It can be Sum/Avg/Count/Percentile (default value Sum)
	<timeSpanDuration>1d</timeSpanDuration> //d- day, m-minute (default value 1d)
	<title>Virtual Machine Disk Write Operations/Sec</title>
</metric>

<Insight>
	<symptomId>CannotRdpLRDAzurePortalInsight</symptomId>
	<executionText>Next, let’s run a more detailed diagnostic of your VM’s connectivity </executionText	<timeoutText>The diagnostic exceeded the allotted time of n:nn and timed out. </timeoutText> 
	<noResultText>Zero problems found! </noResultText> 
	<client>ASC</client>
</Insight>


## Sample guided troubleshooting 
<br>//Insert a black line after every heading.
//Include 1-2 sentences that point out specific aspects of the chart and explains how they are relevant to the problem. This summary is required to ensure accessibility for screen readers. 

For example:
“Here is your CPU usage for the past 24 hours. Spikes indicate process-intensive operations which are affecting overall performance.”

<metric>
	<name>* Percentage CPU</name>
	<aggregationType>* Sum </aggregationType>
	<timeSpanType>* relative</ timeSpanType > 
	<timeSpanDuration>* 1d</timeSpanDuration>
	<title>Virtual Machine CPU usage</title>
</metric>


## Sample solution // Required heading.  
<br>//Insert a black line after every heading.

<br>//Insert a black line before every heading
### Sample instructions //Optional.  
<br>//Insert a black line after every heading.

Below is an example of an ordered list. Use these for tasks that must be performed in a sequence.

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

### Sample bulleted list
Below is an example of a bulleted list; two levels of bullets are supported. For a sequence of tasks, use an ordered list.

* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB

All lists require an empty line before the first item and after the last item.


### Sample inline image 
![alt text](/images/image.png)
// Image requirements:
//Replace alt text with a concise description of what is being shown in the image to provide accessibility. Remove punctuation. Include only screenshots that have legible text. Use colored boxes, not highlighting, for callouts.

### Sample videos
// Include a caption that describes how the video addresses this issue. Call out highlights of the video and include timecode to save the reader from having to scrub through it. To be accessible, video must include captions, a transcript, and audio description, and is delivered in an accessible media player. 


This is a description of a video that includes highlights and the timecodes where they occur. 
       <video>
	<src>http://www.URL_OF_THE_VIDEO</src>	
	<title>Video title and duration in minutes and sections, m:ss</title>  
</video>

This is a description of a group of videos, including highlights from each and the timecodes where they occur.  
   <videoGroup>
	<video>
		<src>URL OF FIRST VIDEO</src>	
		<title> Video title and duration in minutes and sections, m:ss </title>  
	</video>
	<video>
		<src>URL OF SECOND VIDEO</src>	
		<title> Video title and duration in minutes and sections, m:ss </title> 
	</video>
</videoGroup>


## Recommended resources // Optional section. Level 2 heading required. 
<br>//

//In this section, include relevant document links (not found in the preceding sections) from the following approved sources: MS docs, MSDN, and Stack Overflow. 

//For example, format an Azure KB article, as follows. 
<azureKB>
	<client>Portal</client>
</azureKB>
<CommonSolution>
	<articleId>d67fb475-a831-4f4b-a6ce-7fbacb0bf9df</articleId>
	<client>Portal</client>
</CommonSolution>

