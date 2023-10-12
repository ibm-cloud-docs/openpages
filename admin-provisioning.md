---
copyright:
  years: 2023
lastupdated: "2023-10-12"

keywords: provisioning OpenPages, IBM OpenPages as a Service, OpenPages environment
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Provisioning your {{site.data.keyword.openpages_short}} as a Service environment
{: #provisioning_environment}

Here's how to provision your OpenPages environment.{: shortdesc}

1. Log in to https://cloud.ibm.com/login by using your IBMid. 
2. On the Dashboard, click **Create resource**.
3. On the atalog page, in the search bar, type `openpages` and select **{{site.data.keyword.openpages_short}}**. <!--would a UI element also be a keyword ref such as IBM OpenPages?-->
4. Select the **Essentials** plan or the **Standard** plan 
5. Do the following steps:
    - Type a **Service Name** for your OpenPages instance. This will be the name of the first (dev) environment created for you. 
        - For the beta, your **AWS region** is automatically set to **US East (Virginia)** and cannot be changed.
        - You can change the base currency or use the default value.
        - You can choose to include sample data.
    - Click **Solutions** and choose at least one.
6. Read and agree to the terms, then click **Create**. Your OpenPages instance is being created.
7. To see the progress, go to the **Resource list**.
8. In the search box, type `openpages`. 

Your instance is listed twice because OpenPages is associated with two categories in the IBM Cloud catalog. {:note: .note}

You might need to refresh the page to update it. Your instance is ready when the **Status** column shows **Active**. {: tip} 

9. Click the name of your OpenPages instance. The overview page for the OpenPages instance is displayed. 
