---
copyright:
  years: 2025
lastupdated: "2025-05-07"

keywords: provisioning OpenPages, IBM OpenPages as a Service, OpenPages environment
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Provisioning your {{site.data.keyword.openpages_short}} as a Service environment
{: #provisioning_environment}

Do the following steps to provision your {{site.data.keyword.openpages_short}} environment:
{: shortdesc}

To do this task, you must have the Editor or Administrator platform role on the {{site.data.keyword.openpages_short}} service or you must be the account owner.

To provision an {{site.data.keyword.openpages_short}} instance, do the following steps:
1. Log in to [{{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/) by using your IBMid.
2. On the **Dashboard**, click **Create resource**.
3. On the **Catalog** page, in the search bar, type `openpages` and select **IBM OpenPages**.
4. Click **Location** and select the location to provision. Select **Global** for deployment to AWS regions. See the following table for supported IBM Cloud regions:

| Supported {{site.data.keyword.Bluemix_notm}} regions  |
|---|
|  Sydney ( au-syd )  |

{: caption="Supported {{site.data.keyword.Bluemix_notm}} regions for {{site.data.keyword.openpages_short}}" caption-side="bottom"}

5. Select the **Essentials** plan or the **Standard** plan.
6. Do the following steps:
    - Type a **Service Name** for your {{site.data.keyword.openpages_short}} instance. This will be the name of the first (dev) environment created for you.
      - You can change the base currency or use the default value.
      - You can choose to include sample data.
    - Click **Solutions** and choose at least one.
7. Read and agree to the terms, then click **Create**. Your {{site.data.keyword.openpages_short}} instance is being created.
8. To see the progress, go to the **Resource list**.
9. In the search box, type **openpages**.

   Your instance is listed twice because {{site.data.keyword.openpages_short}} is associated with two categories in the {{site.data.keyword.Bluemix_notm}} catalog.

   You might need to refresh the page to update it. Your instance is ready when the **Status** column shows **Active**. {: tip}
10. Click the name of your {{site.data.keyword.openpages_short}} instance. The overview page for the {{site.data.keyword.openpages_short}} instance is displayed.
