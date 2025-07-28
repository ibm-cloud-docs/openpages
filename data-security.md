---

copyright:
  years: 2025
lastupdated: "2025-07-28"

keywords: data encryption in openpages, data storage for openpages, personal data in openpages, data deletion for openpages, data in openpages, data security in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# Securing your data in {{site.data.keyword.openpages_short}}
{: #mng-data}

To ensure that you can securely manage your data when you use {{site.data.keyword.openpages_full}}, it is important to know exactly what data is stored and encrypted and how you can delete it.
{: shortdesc}

## How your data is stored and encrypted in {{site.data.keyword.openpages_short}}
{: #data-storage}

{{site.data.keyword.openpages_short}} service instance data is stored to a RDBMS on AWS / {{site.data.keyword.Bluemix_notm}} and S3 or {{site.data.keyword.cos_full_notm}} bucket The data on the storage is encrypted by using a 256-bit Advanced Encryption Standard (AES) cipher. The encryption key is owned by the {{site.data.keyword.openpages_short}} service.

In addition to the storage level encryption, {{site.data.keyword.openpages_short}} settings that are marked for encryption are further encrypted before they are stored to the relational database table. The encryption is done by using a 256-bit Advanced Encryption Standard (AES) cipher, and the encryption key is owned by the {{site.data.keyword.openpages_short}} service.

{{site.data.keyword.openpages_short}} also uses the following security mechanisms to protect your data in transit.

   - TLS 1.2+ for end to end communications
   - mTLS for internal communications
   - Web App Firewall and DDoS protection
   - Ingress and Egress network rules to isolate your dedicated instance

## Protecting your sensitive data in {{site.data.keyword.openpages_short}}
{: #data-encryption}

The {{site.data.keyword.openpages_short}} service stores personal data, such as a user's email address, first name, and last name, on RDBMS Service Instance. The data is replicated automatically from the {{site.data.keyword.Bluemix_notm}} account in the IAM service. After the data replication, the user can log in to the {{site.data.keyword.openpages_short}} service, and they can view the user selector object fields.

Credentials and API keys for external integration, such as Watson NLU and Regulatory change feeds, are further encrypted before they are stored to the relational database.

To protect access to your sensitive data, you can configure IP allowlisting of your service instance to limit the source IP address or IP address ranges to access the service. The IP allowlisting can be configured from the **Settings** page of OpenPages console UI.

Additional sensitive data can be stored with the encryped option of OpenPages settings.

## Deleting your data in {{site.data.keyword.openpages_short}}
{: #data-delete}

When you delete your instance of {{site.data.keyword.openpages_short}}, all the user data that is associated with it is also deleted. When the service instance is deleted, a 7-day reclamation period begins. During that time, you're able to restore the instance and all of its associated user data. However, if the instance and data are permanently deleted, it can no longer be restored. {{site.data.keyword.openpages_short}} does not store any data from permanently deleted instances.

If your instance was automatically deleted as part of the release of new pricing plans, you can use the reclamation process to restore it. After it is restored, you must upgrade your plan within 1 hour or it will be deleted again.
{: note}

The {{site.data.keyword.openpages_short}} data retention policy describes how long your data is stored after you delete the service. The data retention policy is included in the {{site.data.keyword.openpages_short}} service description, which you can find in the [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview?topic=overview-terms).

### Deleting an {{site.data.keyword.openpages_short}} instance
{: #service-delete}

If you no longer need an instance of {{site.data.keyword.openpages_short}}, you can delete the service instance and any data that is stored. Your instance enters a disabled state, and after 7 days its data is permanently deleted. You can also choose to delete your service instance by using the console.

1. Delete the service and place it in a reclamation period of 7 days.

    ```sh
    ibmcloud resource service-instance-delete "<instance_name>"
    ```
    {: pre}

    Replace `<instance_name>` with the name of the {{site.data.keyword.openpages_short}} instance that you want to delete.

2. Optional: To permanently delete your instance, get the reclamation ID.

    ```sh
    ibmcloud resource reclamations --resource-instance-id <instance_ID>
    ```
    {: pre}

    Replace `<instance_ID>` with your {{site.data.keyword.openpages_short}} instance ID.

    If you choose to permanently delete the instance by deleting its reclamation, you cannot restore your data.
    {: note}

3. Optional: Permanently delete the reclamation instance.

    ```sh
    ibmcloud resource reclamation-delete <reclamation_ID>
    ```
    {: pre}

    Replace `<reclamation_ID>` with the value that you retrieved in the previous step.

### Restoring a deleted service instance
{: #restore-instance}

If you haven't permanently deleted your instance, you can restore it during the 7-day reclamation period.

1. View which service instances are available for restoration.

    ```sh
    ibmcloud resource reclamations
    ```
    {: pre}

    From the list of available instances, copy the reclamation ID of the {{site.data.keyword.openpages_short}} instance that you want to restore.

2. Restore the reclamation.

    ```sh
    ibmcloud resource reclamation-restore <reclamation_ID>
    ```
    {: pre}

    Replace `<reclamation_ID>` with the value that you retrieved in the previous step.

[watsonx.governance]{: tag-blue} When you restore {{site.data.keyword.openpages_short}}, the integration with watsonx.governance is not restored. You need to re-enable the integration.
