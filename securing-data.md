---

copyright:
  years: 2023
lastupdated: "2023-03-08"

keywords: data encryption in openpages, data storage for openpages, personal data in openpages, data deletion for openpages, data in openpages, data security in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# Securing your data in {{site.data.keyword.openpages_short}}
{: #mng-data}

To ensure that you can securely manage your data when you use {{site.data.keyword.openpages_short}}, it is important to know exactly what data is stored and encrypted and how you can delete any stored data. Depending on your security requirements, you can encrypt data with customer-managed keys by integrating with {{site.data.keyword.cloud_notm}} key management services such as {{site.data.keyword.keymanagementserviceshort}}, which supports the bring your own key (BYOK) method, or {{site.data.keyword.hscrypto}}, which supports the keep your own key (KYOK) method.
{: shortdesc}

## How your data is stored and encrypted in {{site.data.keyword.openpages_short}}
{: #data-storage}

{{site.data.keyword.openpages_full}} uses an Oracle RDS on AWS database system to store data. Oracle encrypts data, both while in storage and in transit.

The database used to store data during the beta testing phase for the {{site.data.keyword.openpages_full_notm}} service will be deleted from the database after the testing phase is complete. No testing data will be retained.

_Document how your offering stores and encrypts user data as it relates to user activities. What data is encrypted and what is not? How is data encrypted?_

_If you are using separate keys to encrypt each customer, provide that information here._

_Do not include any details that would give malicious persons an advantage to compromising your offering environment._

## Protecting your sensitive data in {{site.data.keyword.openpages_short}}
{: #data-encryption}

_Document if your services supports Key Protect and/or Hyper Protect Crypto Services for customer-managed keys (whether it's using BYOK or KYOK or both methods). Explain what data is encrypted with customer-managed keys and what data is not. The following is example text from a Watson service that uses Key Protect for BYOK:_

You can add a higher level of encryption protection and control to your data at rest (when it is stored) and data in motion (when it is transported) by enabling integration with {{site.data.keyword.keymanagementservicefull}}.

The data that you store in {{site.data.keyword.cloud_notm}} is encrypted at rest by using a randomly generated key. If you need to control the encryption keys, you can integrate {{site.data.keyword.keymanagementserviceshort}}. This process is commonly referred to as Bring your own keys (BYOK). With {{site.data.keyword.keymanagementserviceshort}} you can create, import, and manage encryption keys. You can assign access policies to the keys, assign users or service IDs to the keys, or give the key access only to a specific service. The first 20 keys are free.

_The template has more about BYOK and KYOK

## Deleting your data in {{site.data.keyword.openpages_short}}
{: #data-delete}

_Document how users can delete their data within the service._

_If applicable, add H3s in this section to tailor the information to particular types of data. For example, you might have a "Deleting keys" section and a "Deleting a database" section._

### Deleting {{site.data.keyword.openpages_short}}
{: #service-delete}

_Include information about whether deleting the service fully erases all data. If deleting the service doesn't remove all personal data, include information about how users can completely delete their data._

_Information about how long services keep data after instances are deleted is covered in the service description. Include the following reference for users to find their data retention period._

The {{site.data.keyword.openpages_short}} data retention policy describes how long your data is stored after you delete the service. The data retention policy is included in the {{site.data.keyword.openpages_short}} service description, which you can find in the [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview?topic=overview-terms).

### Restoring deleted data for {{site.data.keyword.openpages_short}}
{: #data-restore}

_If users can restore deleted data within your service, include this optional section and the task that users can complete to do so._

_Important: Don't include information about restoring your resource via the reclamation controller because it's available only on a limited basis._
