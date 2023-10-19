---
copyright:
  years: 2023
lastupdated: "2023-10-12"

keywords: customize OpenPages, IBM OpenPages as a Service, OpenPages environment
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Customizing the hostname in the {{site.data.keyword.openpages_short}} URL
{: #customizing_hostname}

By default, instances have a system-generated hostname in the URL. You can change the hostname to create a more user-friendly URL. {: shortdesc}

You can also transfer a custom hostname from one instance to another. 

## Changing the hostname of an instance 
{: #changing_hostname_instance}

1. Go to the **Resource list**.  
2. In the search box, type `openpages`.
3. Click the name of your OpenPages instance.
4. Click **Environment**. 
5. In the **Custom hostname** section, click the **Edit** icon. 
6. Type a name, and then click **Save**. Wait a few minutes for the change to take effect

The last character in the hostname must not be a minus sign or a period. {:note: .note}

You can now launch OpenPages by using the **Custom hostname** URL or the **Fixed URL**.

## Transferring a hostname to another instance
{: #transferring_hostname_instance}

If you have multiple instances, you can transfer a custom hostname from one instance to
another. 

This feature enables you to provision a new instance without the need to give users a different
URL.

1. Go to the **Resource list**. 
2. In the search box, type `openpages`.
3. Click the name of an OpenPages instance that doesn’t have a custom hostname.
4. Click **Environment**.

The **Transfer hostname** section lists the custom hostnames of your other OpenPages
instances. 

5. Click a custom hostname, and then click **Transfer**.
6. Click **Transfer** to confirm the change. 

When users go to the URL with the custom hostname, they are now using the instance that you
selected in step 3. 

## Providing users with the OpenPages URL
{: #provide_users_OP_url}

As an administrator, you can provide the {{site.data.keyword.openpages_short}} URL to your user community. To get that URL, do the following steps:

1. Go to the **Resource list**.
2. In the search box, type **openpages**. 
3. Click the name of your {{site.data.keyword.openpages_short}} instance. 
4. Click **Environment**. Under **Fixed URL**, click the **Copy** button. 

Or, if you customized the hostname, click the **Copy** button of the **Custom hostname** URL.

