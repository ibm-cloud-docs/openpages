---

copyright:
  years: 2024
lastupdated: "2024-01-03"

keywords: openpages, tutorial, managing openpages instance

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}



# Getting started with {{site.data.keyword.openpages_short}}
{: #gettingstartedtutorial}

In this getting started tutorial, we'll take you through what you need to do to set up your {{site.data.keyword.openpages_short}} service.
{: shortdesc}

## Before you begin
{: #prereqs}

You need an [{{site.data.keyword.Bluemix}} account](https://cloud.ibm.com/registration/) and an instance of the {{site.data.keyword.openpages_short}} service. For more information, see [Provisioning your IBM OpenPages as a Service environment](/docs/openpages?topic=openpages-provisioning_environment&interface=api).

## Open the UI
{: #step1}

Open the UI to begin managing your {{site.data.keyword.openpages_short}} instance.

1. Log in to [{{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/) by using your IBMid.
2. Go to the **Resource list**.
3. Locate your {{site.data.keyword.openpages_short}} instance in the **AI / Machine Learning** or **Analytics** category.
4. Click the **Name** of the instance.

   The UI where you manage your {{site.data.keyword.openpages_short}} instance is displayed.

Here you can open your instance of {{site.data.keyword.openpages_short}} by clicking **Launch OpenPages**. For your users, you'll want to set up a URL to allow them to get to {{site.data.keyword.openpages_short}} more easily.

## Set up a URL
{: #step2}

Set up a URL that you and your users can use to access your {{site.data.keyword.openpages_short}} instance. You can use the default fixed URL or you can customize the URL.

To get the fixed URL, do the following steps:

1. Click **Environment**.
2. Under **Fixed URL**, click the **Copy** icon.
3. Paste the URL in your browser to ensure that the new URL opens your {{site.data.keyword.openpages_short}} instance.

To customize the URL, do the following steps:

1. Click **Environment**.
2. In the **Custom hostname** section, click the **Edit** icon.
3. Type a name, and then click **Save**. Wait a few minutes for the change to take effect.

   The last character in the hostname must not be a minus sign or a period. {:note: .note}

After you've added users to your {{site.data.keyword.openpages_short}} instance, you can provide the {{site.data.keyword.openpages_short}} URL to your user community.

## Next steps
{: #next-steps}

Now you'll want to begin applying security and granting access to users and groups.

1. Learn how to enhance security for your {{site.data.keyword.openpages_short}} instance and your data. 

   For example, to ensure that you have enhanced control and security over your data when you use {{site.data.keyword.openpages_short}}, you can specify the IP addresses that are allowed to connect to your {{site.data.keyword.openpages_short}} service instance. 
   
   For more information, see [Managing IP addresses for IBM OpenPages](/docs/openpages?topic=openpages-service-endpoints&interface=ui) and [Securing your data in IBM OpenPages](/docs/openpages?topic=openpages-mng-data&interface=ui).
2. Learn how to manage access to your {{site.data.keyword.openpages_short}} instance, including how to add users and groups, how to assign them access in {{site.data.keyword.openpages_short}}, and how {{site.data.keyword.Bluemix_notm}} synchronizes users and groups with {{site.data.keyword.openpages_short}}. 

   For more information, see [Managing IAM access for IBM OpenPages](/docs/openpages?topic=openpages-iam-openpages&interface=ui) and [User and group synchronization from IBM Cloud to IBM OpenPages](/docs/openpages?topic=openpages-iam-openpages-synchronization&interface=ui).
