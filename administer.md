---
copyright:
  years: 2023
lastupdated: "2023-03-08"

keywords: administer OpenPages, users and groups in OpenPages, administrator in OpenPages, GRC
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Administering {{site.data.keyword.openpages_short}}
{: #Administer_op}

Administering {{site.data.keyword.openpages_short}} includes managing users and groups, administering databases, managing environments, and other administrative actions.
{: shortdesc}

IBM maintains one set of documentation serving both cloud and on-premises {{site.data.keyword.openpages_short}} deployments. The {{site.data.keyword.openpages_short}} documentation describes certain features and functions which might not be available in {{site.data.keyword.openpages_full}}.

If you have any questions about the functionality available in the product version that you are using, contact {{site.data.keyword.openpages_short}} Support.

## Administration tasks unique to {{site.data.keyword.openpages_short}} as a Service
{: #Administer_service}

Most administration tasks are common between {{site.data.keyword.openpages_short}} as a Service and {{site.data.keyword.openpages_short}} on-premises. However, some tasks such as quota monitoring, environment management, and some aspects of database management, are unique to {{site.data.keyword.openpages_full}}.

- Adding GRC solutions
- Updating resouce allocation
- Setting allowed IP ranges to access
- Configuring IBM Cloud identity federation with your user directory
- Setting up ObjectManager

## Administration tasks
{: #Administer_common}

- Role-based security for users and groups:

     Access to objects and data in {{site.data.keyword.openpages_short}} is controlled through role-based security. A role defines access permissions, such as administrative rights, access to areas of the application, and so on. You configure roles and assign them to users and groups.

     You can also use security rules, if needed, to further refine access.

     For more information, see [Security](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_granting_access_control_using_role_templates.html).

- Setting up the application for users:

     Administrators set up {{site.data.keyword.openpages_short}} for users by creating views, workflows, calculations, dashboards, and more.

     For more information, see [Setting up the UI](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/t_adm_configuring_newui_overview.html).

- Profiles:

     Profiles provide end users with a localized view of information that is directly related to their responsibilities. Each user has at least one profile. You can assign users to multiple profiles.

     Use profiles to configure objects, fields, and views.

     You can use profiles to restrict the object types that individual users can view. You can also define the fields in each object that are visible to them. If an object type is absent from a profile, that object type is hidden from users of that profile.

     For more information, see [Profiles](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_managing_profiles.html).

- Migrate assets with ObjectManager:

     Assets such as views, calculations, and workflows can be migrated by an administrator from a source environment to a target environment by using ObjectManager. ObjectManager is a command line utility.

     With the ObjectManager tool, you can do the following tasks:

     - Import (load) data, such as objects and configuration data, into {{site.data.keyword.openpages_short}}.
     - Export (dump) filtered or unfiltered data from {{site.data.keyword.openpages_short}}. You can use this functionality, for example, to migrate data from one instance to another.
     - Batch-load multiple loader files in a single session.

     For more information, see the following topics:

     - [ObjectManager CLI](/docs/openpages?topic=openpages-openpages_CLI#ibmcloud_openpages_objectmanager)
     - [Working with loader files](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_working_with_loader_files.html)
     - [Settings in the ObjectManager properties file](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/r_adm_objectmanager_file_properties.html)
