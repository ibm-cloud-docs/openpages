---

copyright:
  years: 2024
lastupdated: "2024-01-03"

keywords: question about Unexpected error, FastMap times out

subcollection: openpages

content-type: troubleshoot

---



{{site.data.keyword.attribute-definition-list}}






# How do I fix a FastMap time out error?
{: #troubleshoot-fastmap}
{: troubleshoot}







You try to import a large FastMap file, but you get `Unexpected error`.
{: shortdesc}






When you select a large FastMap file to import (.xlsx file) and click **Validate**, you get the message: `Unexpected error` after three minutes.
{: tsSymptoms}

The FastMap file is large and the file validation process is taking longer than the time out for FastMap.
{: tsCauses}

- Make the changes in smaller increments by creating multiple, smaller FastMap files, or
- Load the changes by using ObjectManager instead of FastMap. For more information, see [ObjectManager CLI](/docs/openpages?topic=openpages-openpages_CLI#ibmcloud_openpages_objectmanager).
{: tsResolve}
