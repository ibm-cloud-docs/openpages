---
copyright:
  years: 2023
lastupdated: "2023-10-18"

keywords: customer responsibilities, IBM responsibilities, terms and conditions

subcollection: openpages

content-type: reference

---
{{site.data.keyword.attribute-definition-list}}

# Understanding your responsibilities when using {{site.data.keyword.openpages_short}}
{: #Responsibility}

Learn about the management responsibilities and terms and conditions that you have when you use {{site.data.keyword.openpages_full}}. For a high-level view of the service types in {{site.data.keyword.cloud_notm}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities).
{: shortdesc}

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use {{site.data.keyword.openpages_full_notm}}. For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview?topic=overview-terms).


## Incident and operations management
{: #incident-and-ops}


| Task              | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|-------------------|-------------------------------------------------|-----------------------|
| Incident and operations management   | Maintain {{site.data.keyword.openpages_full_notm}} service instances and infrastructure workloads. | Maintain incident and operations management of your data. |
| Monitor incidents    | Provide notifications for planned maintenance, security bulletins, or unplanned outages. | Set preferences to [receive emails about platform notifications](/docs/account?topic=account-email-prefs).  \n Monitor the [IBM Cloud status page](https://{DomainName}/status?selected=announcement) for general announcements. |
| Maintain {{site.data.keyword.cloud_notm}} high availability SLA    | Provide Cloud Service across hosts.  \n Provide replication, fail-over features, and infrastructure maintenance and updates. | Plan for and create new instances of the service. For more information, see [Provisioning your IBM OpenPages as a Service environment](/docs-draft/openpages?topic=openpages-provisioning_environment).|
| Monitor logs    | [Logging for IBM OpenPages](/docs/openpages?topic=openpages-service-logs) publish relevant log data to their subscribing clients. {{site.data.keyword.openpages_full_notm}} provides clients with the ability to receive the logs once the client configures their instance. | [Logging in IBM OpenPages](/docs/openpages?topic=openpages-service-logs) |
{: caption="Table 1. Responsibilities for incident and operations" caption-side="top"}

## Change management
{: #change-management}

| Task                                                    | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|---------------------------------------------------------|-----------------------|--------|
| Update the {{site.data.keyword.openpages_full_notm}} service   | Provide major, minor, and patch version updates for {{site.data.keyword.openpages_full_notm}} interfaces.  \n Document changes in the release notes. | Keep your IBM OpenPages software up to date. \n For more information, see [Updating your instance of IBM OpenPages to the latest software version](/docs-draft/openpages?topic=openpages-updating-openpages).|
{: caption="Table 2. Responsibilities for change management" caption-side="top"}

## Identity and access management
{: #idnt_access_mgt}

Identity and access management includes tasks such as authentication, authorization, access control policies, and approving, granting, and revoking access.

| Task | IBM responsibilities |Your responsibilities |
|--------------------------|----------------|----------------|
| Access control of the service instance through IAM| Verify the user's permissions on the service instance before allowing access.| Maintain responsibility for any user access that you create for your instances.\n This includes security rules, roles, users,and groups in IBM Cloud IAM and OpenPages application security.|
{: caption="Table 3. Identity and access management" caption-side="bottom"}

## Security and regulation compliance
{: #security_comp}

Security and regulation compliance includes tasks such as security controls implementation and compliance certification.

| Task | IBM responsibilities |Your responsibilities |
|--------------------------|----------------|----------------|
| General| * Maintain controls commensurate to various industry compliance standards. \n * Monitor, isolate, and recover instances. \n * Monitor and report the health of instances in the various interfaces. \n * Secure cluster access through TLS (data plane in the IBM Services account). \n * Integrate {{site.data.keyword.openpages_short}} with IBM Cloud Identity and Access Management (IAM).| Set up and maintain security and regulation compliance for the {{site.data.keyword.openpages_short}} instances.|
{: caption="Table 4. Security and regulation compliance" caption-side="bottom"}

## Disaster recovery
{: #security_dr}

| Task | IBM responsibilities |Your responsibilities |
|--------------------------|----------------|----------------|
| General| * Restore or rebuild the service instances in alternatively available regions. \n * Restore existing {{site.data.keyword.openpages_short}} instances, where possible. | * Track instance state. \n * Configure external integrations, if they exist, with a newly assigned application URL.|
{: caption="Table 5. Disaster recovery" caption-side="bottom"}
