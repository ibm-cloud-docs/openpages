---

copyright:
  years: 2019, 2020
lastupdated: "2023-11-22"

keywords: question about Unexpected error, FastMap times out

subcollection: openpages

content-type: troubleshoot

---

<!-- keywords values above are place holders. Actual values should be pulled from the Troubleshooting questions or error message to which the issue relates. Only use a messageID if the troubleshooting topic is about an issue encountered from an error message that has an ID.  -->

{{site.data.keyword.attribute-definition-list}}

<!-- You must add the troubleshoot content type in your attribute definitions AND on a new line under each troubleshooting topic H1 ID. This will ensure that the troubleshooting entry is pulled into other locations, like chatbots. Use the support attribute definition for reuse in the support center. For more information, see  https://test.cloud.ibm.com/docs/writing?topic=writing-support-center#support-center-troubleshoot-->

<!-- Remember that this is the individual topic template for each troubleshooting entry that belongs in a troubleshooting topic group in the Help left nav group. For more information, see the guidance page: https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics-->


## How do I fix a FastMap time out error?
{: #troubleshoot-fastmap}
{: troubleshoot}
{: support} <!-- Only add this attribute to entries that you want to display in the support center. -->

<!--The title of your H1 should be a problem statement in question format of the issue that the user is experiencing. Think about the user's language they might use to describe or search for the answer to the issue they are experiencing. Use keywords for other variations of ways to ask the question at the top of the file. -->

You try to import a large FastMap file, but you get `Unexpected error`.
{: shortdesc}

<!-- The short description should give a quick summary about the issue the user is experiencing. -->
<!-- Example short description for an error troubleshooting topic: You try to create more than one instance in your Lite account, but you received error `message-id.0001E`.-->

<!-- Tips:
* Organize one troubleshooting issue per topic in a  topic group called "Troubleshooting" in the Help left nav section
* Name your topic group "Troubleshooting". If you have more than one topic group to organize a large set of troubleshooting topics, use "Troubleshoting _xxx_" to provide descriptive topic group titles.
* Use a title that uses a problem statement in the form of a question for each H1 in your topic group
* Use an H1 ID of `troubleshoot-xx` where the `xx` is a descriptive word to match the issue the customer is experiencing for URL readability.
* Set the `troubleshoot` content type attribute definition at the top of your file.
* Set the `troubleshoot` content type attribute on a new line following each H1 ID.
* Use the three attributes for the symptom, cause, and resolution.-->

When you import a large FastMap file (.xlsx file), the import process times out after three minutes and you get the message: `Unexpected error`.
{: tsSymptoms}

The FastMap file is large and the import is taking longer than the time out for FastMap.
{: tsCauses}

To resolve the issue, use the following options:
- Wait. The import process will complete in time. Refresh the UI to see the status of the import.
- Make the changes in smaller increments by creating multiple, smaller FastMap files.
- Load the changes by using ObjectManager instead of FastMap.
{: tsResolve}
