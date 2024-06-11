---

copyright:
  years: 2024
lastupdated: "2024-05-27"

keywords: question about warning, solutions in use

subcollection: openpages

content-type: troubleshoot

---



{{site.data.keyword.attribute-definition-list}}






# How do I fix a warning about solutions that are in use?
{: #troubleshoot-solutions}
{: troubleshoot}







On the **Manage** page for your instance, you see a warning about solutions that are not selected but are in use.
{: shortdesc}






On the **Manage** page for your instance, you see a warning that you are using objects that not included in the solutions that you selected. The warning states that the solutions will be added to your instance and in how many days the change will take effect. The warning includes a list of object types and the solutions that include them. The warning is displayed for two weeks.
{: tsSymptoms}

When you provisioned {{site.data.keyword.openpages_short}}, you installed the sample data. The sample data includes objects from all solutions. The warning indicates that your instance is using objects that are outside of the solutions that you are currently subscribed to.
{: tsCauses}

You can resolve the issue by taking one of the following actions:
{: tsResolve}

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
