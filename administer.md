---
copyright:
  years: 2023
lastupdated: "2023-03-08"

keywords: administer OpenPages, users and groups in OpenPages, administrator in OpenPagees, GRC
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Administering {{site.data.keyword.openpages_short}}
{: #Administer_op}

Administering {{site.data.keyword.openpages_short}} includes managing users and groups, administering databases, managing environments, and other administrative actions.
{: shortdesc}

<!---[Download a Welcome Kit from Planning Analytics Administration](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-download-welcome-kit-from-planning-analytics-administration)
When you receive initial notification that a {{site.data.keyword.PA_SaaS_short}} Welcome Kit is available, you must download the kit from IBM@Box. However, any subsequent Welcome Kits can be downloaded directly from {{site.data.keyword.PA_SaaS_short}} Administration.-->

<!---[Administer users and groups](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-administer-users-groups)
To administer users in {{site.data.keyword.PA_SaaS_short}}, you must be logged in to {{site.data.keyword.PA_SaaS_short}} as an **administrator**. If you have the administrator role and meet all of the requirements, you can invite people who are in the same organization (account) as you to become users in {{site.data.keyword.PA_SaaS_short}} on cloud or upload users to {{site.data.keyword.PA_SaaS_short}} Local.-->

IBM maintains one set of documentation serving both cloud and on-premises {{site.data.keyword.openpages_short}} deployments. The {{site.data.keyword.openpages_short}} documentation describes certain features and functions which might not be available in {{site.data.keyword.openpages_full}} as a Service.

If you have any questions about the functionality available in the product version that you are using, contact IBM OpenPages Support

## Administration tasks unique to {{site.data.keyword.openpages_short}} as a Service
{: #Administer_service}

Most administration tasks are common between {{site.data.keyword.openpages_short}} as a Service and {{site.data.keyword.openpages_short}} on-premises. However, some tasks such as quota monitoring, environment management, and some aspects of database management, are unique to {{site.data.keyword.openpages_short}} as a Service.

- Adding GRC solutions
- Updating resouce allocation
- Setting allowed IP ranges to access
- Configuring IBM Cloud identity federation with your user directory
- Setting up ObjectManager

## Administration tasks
{: #Administer_common}

- Role-based security for users and groups

    Access to objects and data in {{site.data.keyword.openpages_short}} is controlled through role-based security. A role defines access permissions, such as administrative rights, access to areas of the application, and so on. You configure roles and assign them to users and groups.

    You can also use security rules, if needed, to further refine access.

    For more information, see [Security](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_granting_access_control_using_role_templates.html)

- Setting up the application for users

    Administrators set up {{site.data.keyword.openpages_short}} for users by creating views, workflows, calculations, dashboards, and more.

    For more information, see [Setting up the UI](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/t_adm_configuring_newui_overview.html)

- Profiles

    Profiles provide end users with a localized view of information that is directly related to their responsibilities. Each user has at least one profile. You can assign users to multiple profiles.

    Use profiles to configure objects, fields, and views.

    You can use profiles to restrict the object types that individual users can view. You can also define the fields in each object that are visible to them. If an object type is absent from a profile, that object type is hidden from users of that profile.

    For more information, see [Profiles](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_managing_profiles.html).

- Migrate assets with ObjectManager

    Assets such as views, calculations, and workflows can be migrated by an administrator from a source environment to a target environment by using ObjectManager. ObjectManager is a command line utility.

    With the ObjectManager tool, you can do the following tasks:

    - Import (load) data, such as objects and configuration data, into {{site.data.keyword.openpages_short}}.
    - Export (dump) filtered or unfiltered data from {{site.data.keyword.openpages_short}}. You can use this functionality, for example, to migrate data from one instance to another.
    - Batch-load multiple loader files in a single session.

    For more information, see the following topics:

    - [Working with loader files](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_working_with_loader_files.html)
    - [Running ObjectManager commands](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/c_adm_running_objectmanager_commands.html)
    - [Settings in the ObjectManager properties file](https://www.ibm.com/docs/SSFUEU_latest/op_grc_admin/r_adm_objectmanager_file_properties.html)

<!---[Monitor and administer databases](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-monitor-administer-databases)
{{site.data.keyword.PA_SaaS_short}} Administration includes the ability to monitor and administer your databases from the Administration page. You must be an administrator to access and use the Administration page.-->

<!---[Administer IBM Secure Gateway (cloud only)](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-administer-secure-gateway-cloud-only)
IBM Secure Gateway creates a secure connection and establishes a tunnel between {{site.data.keyword.PA_SaaS_short}} TM1® on cloud and an on - premise data source, typically an RDBMS source.-->

<!---[Customize the interface for your company](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-customize-interface-your-company)
When you receive initial notification that a {{site.data.keyword.PA_SaaS_short}} Welcome Kit is available, you must download the kit from IBM@Box. However, any subsequent Welcome Kits can be downloaded directly from {{site.data.keyword.PA_SaaS_short}} Administration.-->

<!---[Manage integrations](https://www.ibm.com/docs/en/planning-analytics/2.0.0?topic=workspace-download-welcome-kit-from-planning-analytics-administration)
Use the **Integrations** tile to manage {{site.data.keyword.PA_SaaS_short}} integrations with other IBM products and services.-->
