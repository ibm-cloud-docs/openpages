---

copyright:
  years: 2024
lastupdated: "2024-05-27"

keywords: question about warning, solutions in use

subcollection: openpages

content-type: troubleshoot

---

<!-- keywords values above are place holders. Actual values should be pulled from the Troubleshooting questions or error message to which the issue relates. Only use a messageID if the troubleshooting topic is about an issue encountered from an error message that has an ID.  -->

{{site.data.keyword.attribute-definition-list}}

<!-- You must add the troubleshoot content type in your attribute definitions AND on a new line under each troubleshooting topic H1 ID. This will ensure that the troubleshooting entry is pulled into other locations, like chatbots. Use the support attribute definition for reuse in the support center. For more information, see  https://test.cloud.ibm.com/docs/writing?topic=writing-support-center#support-center-troubleshoot-->

<!-- Remember that this is the individual topic template for each troubleshooting entry that belongs in a troubleshooting topic group in the Help left nav group. For more information, see the guidance page: https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics-->


# How do I fix a warning about solutions that are in use?
{: #troubleshoot-solutions}
{: troubleshoot}

<!-- {: support} -->

<!-- Only add the supprt attribute to entries that you want to display in the support center. -->

<!--The title of your H1 should be a problem statement in question format of the issue that the user is experiencing. Think about the user's language they might use to describe or search for the answer to the issue they are experiencing. Use keywords for other variations of ways to ask the question at the top of the file. -->

On the **Manage** page for your instance, you see a warning about solutions that are not selected but are in use.
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

On the **Manage** page for your instance, you see a warning that you are using objects that not included in the solutions that you selected. The warning states that the solutions will be added to your instance in ten days. The warning includes a list of object types and the solutions that include them.
{: tsSymptoms}

When you provisioned {{site.data.keyword.openpages_short}}, you installed the sample data. The sample data includes objects from all solutions. The warning indicates that your instance is using objects that are outside of the solutions that you are currently licensed to use.
{: tsCauses}

- Add the additional solutions to your instance, or
- Delete the objects that are not in the solutions that you selected when you provisioned {{site.data.keyword.openpages_short}}.

To add solutions:
1. Make a list of the solutions that are listed in the warning message.
2. On the **Manage** page, click **Manage solutions**.
3. Enable the solutions, and click **Update**.
4. Wait 30 minutes, and then return to the **Manage** page to verify that the warning no longer appears.

To delete objects:
1. Make a list of the object types that are listed in the warning message.
2. For each object type, go to its grid view and delete all object instances.
3. Wait 30 minutes, and then return to the **Manage** page to verify that the warning no longer appears.
{: tsResolve}
