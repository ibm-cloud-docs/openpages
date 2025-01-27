---

copyright:
  years: 2025
lastupdated: "2025-01-27"

keywords: assigning access in openpages, IAM access for openpages, service roles in openpages, access policies in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}


# Managing IAM access for {{site.data.keyword.openpages_short}}
{: #iam-openpages}

Access to {{site.data.keyword.openpages_short}} service instances for users in your account is controlled by {{site.data.keyword.cloud}} Identity and Access Management (IAM). Further access controls are managed within {{site.data.keyword.openpages_short}}.
{: shortdesc}

Every user that accesses the {{site.data.keyword.openpages_short}} service in your account must be assigned an access policy with an IAM role. Review the following roles, actions, and more to help determine the best way to assign access to {{site.data.keyword.openpages_short}}.

The access policy that you assign users in your account determines what actions a user can perform within the context of the service or specific instance that you select. The allowable actions are customized and defined by {{site.data.keyword.openpages_short}} as operations that are allowed to be performed on the service. Each action is mapped to an IAM platform or service role that you can assign to a user.

If a specific role and its actions don't fit the use case that you're looking to address, you can [create a custom role](/docs/account?topic=account-custom-roles&interface=ui#custom-access-roles) and pick the actions to include.
{: tip}

IAM access policies enable access to be granted at different levels. Some of the options include the following:

* Access across all instances of the service in your account
* Access to an individual service instance in your account 

Review the following tables that outline what types of tasks each role allows for when you're working with the {{site.data.keyword.openpages_short}} service. Platform management roles enable users to perform tasks on service resources at the platform level, for example, assign user access to the service, create or delete instances, and bind instances to applications. Service access roles enable users access to {{site.data.keyword.openpages_short}} and the ability to call the {{site.data.keyword.openpages_short}}'s API.

| Platform role |  Description of actions |
|---------------|-------------------------|
| Viewer                 |  As a Viewer, you can log in to the {{site.data.keyword.openpages_short}} application. You can view {{site.data.keyword.openpages_short}} service instances, but you can't modify them. |
| Operator               |  As an operator, you can complete platform actions that are required to configure and operate {{site.data.keyword.openpages_short}} service instances. You can log in to {{site.data.keyword.openpages_short}}.            |
| Editor                 |  As an Editor, you can create, modify, and delete {{site.data.keyword.openpages_short}} service instances, but you can't assign access policies to other users. You can log in to the {{site.data.keyword.openpages_short}} application.            |
| Administrator          |  As an administrator, you can complete all platform actions for {{site.data.keyword.openpages_short}}, including the ability to assign access policies to other users. As an application administrator, you have complete access to all objects, folders, application permissions and security groups and users in {{site.data.keyword.openpages_short}}. You can log in to the {{site.data.keyword.openpages_short}} application as an Administrator.            |
{: row-headers}
{: class="simple-tab-table"}
{: caption="IAM platform roles" caption-side="bottom"}
{: #iamrolesplatform}
{: tab-title="Platform roles"}
{: tab-group="IAM"}

| Service role   |  Description of actions |
|----------------|------------------------|
| OpenPages User | As a User, you can log in to the {{site.data.keyword.openpages_short}} application. You can also make calls to the {{site.data.keyword.openpages_short}} REST API. Further access is defined in {{site.data.keyword.openpages_short}}.   |
{: row-headers}
{: class="simple-tab-table"}
{: caption="IAM service access roles" caption-side="bottom"}
{: #iamrolesservice}
{: tab-title="Service roles"}
{: tab-group="IAM"}

## Connecting to an external identity provider for authentication
{: #iam-openpages-appid}

You can connect your external identity provider to an {{site.data.keyword.cloud}} App ID instance, and then configure that App ID to connect directly to {{site.data.keyword.cloud}} Identity and Access Management (IAM) to federate authentication users of an enterprise to an {{site.data.keyword.cloud}} account.

To configure App ID, do the following steps:
1. Configure the integration by doing the steps in the following topic: [Configuring App ID with your identity provider](https://www.ibm.com/docs/en/watsonx/saas?topic=overview-configuring-app-id-your-identity-provider).

    The topic discusses watsonx, but the steps are the same for {{site.data.keyword.openpages_short}}.
    {: tip}

3. Get the URL for your identify provider.

   From the Identity provider pages, click the Actions icon for the identify provider and click **Select View IdP URL**. Copy the IdP URL link. This is the URL to give to your users.

2. Test the identity provider URL. Verify that your {{site.data.keyword.cloud}} dashboard is displayed.
3. Give the identity provider URL to your users. When users log in, they are added to {{site.data.keyword.cloud}} IAM.
4. Assign users access to {{site.data.keyword.openpages_short}}.

    For example, see [Assigning access to {{site.data.keyword.openpages_short}} in the console](/docs/openpages?topic=openpages-iam-openpages&interface=ui#assign-access-console)

When users log in successfully by using the identity provider URL, they are taken to their {{site.data.keyword.cloud}} dashboard. From here, they can access {{site.data.keyword.openpages_short}}, for example by using the **Resource List**.

## Assigning access to {{site.data.keyword.openpages_short}} in the console
{: #assign-access-console}
{: ui}

Before you assign access, consider federating identities with your {{site.data.keyword.cloud_notm}} account. This authentication option simplifies the process of adding users to your account, without requiring an IBMid with a separate password.

For more information, see [Which is the right federation option for you?](/docs/account?topic=account-federation-option-for-you&interface=ui).

There are two common ways to assign access in the console:

* Access policies per user. You can manage access policies per user from the **Manage** > **Access (IAM)** > **Users** page in the console. For information about the steps to assign IAM access, see [Managing access to resources in the console](/docs/account?topic=account-assign-access-resources&interface=ui#access-resources-console).
* Access groups. Access groups are used to streamline access management by assigning access to a group once, then you can add or remove users as needed from the group to control their access. You manage access groups and their access from the **Manage** > **Access (IAM)** > **Access groups** page in the console. For more information, see [Assigning access to a group in the console](/docs/account?topic=account-groups&interface=ui#access_ag).

Users and groups are synchronized to {{site.data.keyword.openpages_short}}. Users are synchronized after they accept your invitation to join your account. Groups are synchronized when they are assigned access. For more information, see [User and group synchronization from {{site.data.keyword.Bluemix_notm}} to {{site.data.keyword.openpages_short}}](/docs/openpages?topic=openpages-iam-openpages-synchronization&interface=api).

## Assigning access to {{site.data.keyword.openpages_short}} in the CLI
{: #assign-access-cli}
{: cli}

For step-by-step instructions for assigning, removing, and reviewing access, see [Assigning access to resources by using the CLI](/docs/account?topic=account-assign-access-resources&interface=cli#access-resources-cli). The following example shows a command for assigning the `GRCUser` role for `openpages`:

Use `openpages` for the service name. Also, use quotations around role names that are more than one word like the example here.
{: tip}

```bash
ibmcloud iam user-policy-create USER@EXAMPLE.COM --service-name openpages --roles "openpages.service.login"
```
{: pre}

## Assigning access to {{site.data.keyword.openpages_short}} by using the API
{: #assign-access-api}
{: api}

For step-by-step instructions for assigning, removing, and reviewing access, see [Assigning access to resources by using the API](/docs/account?topic=account-assign-access-resources&interface=api) or the [Create a policy API docs](/apidocs/iam-policy-management#create-policy). Role cloud resource names (CRN) in the following table are used to assign access with the API.


| Role name | Role CRN |
|---------------|-----------------|
| Viewer                 | `crn:v1:bluemix:public:openpages::::serviceRole:Viewer`        |
| Operator               | `crn:v1:bluemix:public:openpages::::serviceRole:Operator`      |
| Editor                 | `crn:v1:bluemix:public:openpages::::serviceRole:Editor`        |
| Administrator          | `crn:v1:bluemix:public:openpages::::serviceRole:Administrator` |
| OpenPages User         | `crn:v1:bluemix:public:openpages::::serviceRole:GRCUser`       |
{: caption="Role ID values for API use" caption-side="bottom"}

The following example is for assigning the `openpages.service.login` role for `openpages`:

Use `openpages` for the service name, and refer to the Role ID values table to ensure that you're using the correct value for the CRN.
{: tip}

```curl
curl -X POST 'https://iam.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' -H 'Content-Type: application/json' -d '{
  "type": "access",
  "description": "Service login role for OpenPages",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }'
  ],
  "roles":[
    {
      "role_id": "crn:v1:bluemix:public:openpages::::serviceRole:openpages.service.login"
    }
  ],
  "resources":[
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "$ACCOUNT_ID"
        },
        {
          "name": "serviceName",
          "value": "openpages"
        }
      ]
    }
  ]
}
```
{: curl}
{: codeblock}

```java
SubjectAttribute subjectAttribute = new SubjectAttribute.Builder()
      .name("iam_id")
      .value("IBMid-123453user")
      .build();

PolicySubject policySubjects = new PolicySubject.Builder()
      .addAttributes(subjectAttribute)
      .build();

PolicyRole policyRoles = new PolicyRole.Builder()
      .roleId("crn:v1:bluemix:public:openpages::::serviceRole:openpages.service.login")
      .build();

ResourceAttribute accountIdResourceAttribute = new ResourceAttribute.Builder()
      .name("accountId")
      .value("ACCOUNT_ID")
      .operator("stringEquals")
      .build();

ResourceAttribute serviceNameResourceAttribute = new ResourceAttribute.Builder()
      .name("serviceName")
      .value("openpages")
      .operator("stringEquals")
      .build();

PolicyResource policyResources = new PolicyResource.Builder()
      .addAttributes(accountIdResourceAttribute)
      .addAttributes(serviceNameResourceAttribute)
      .build();

CreatePolicyOptions options = new CreatePolicyOptions.Builder()
      .type("access")
      .subjects(Arrays.asList(policySubjects))
      .roles(Arrays.asList(policyRoles))
      .resources(Arrays.asList(policyResources))
      .build();

Response<Policy> response = service.createPolicy(options).execute();
Policy policy = response.getResult();

System.out.println(policy);
```
{: java}
{: codeblock}

```javascript
const policySubjects = [
  {
    attributes: [
      {
        name: 'iam_id',
        value: 'IBMid-123453user',
      },
    ],
  },
];
const policyRoles = [
  {
    role_id: 'crn:v1:bluemix:public:openpages::::serviceRole:openpages.service.login',
  },
];
const accountIdResourceAttribute = {
  name: 'accountId',
  value: 'ACCOUNT_ID',
  operator: 'stringEquals',
};
const serviceNameResourceAttribute = {
  name: 'serviceName',
  value: 'openpages',
  operator: 'stringEquals',
};
const policyResources = [
  {
    attributes: [accountIdResourceAttribute, serviceNameResourceAttribute]
  },
];
const params = {
  type: 'access',
  subjects: policySubjects,
  roles: policyRoles,
  resources: policyResources,
};

iamPolicyManagementService.createPolicy(params)
  .then(res => {
    examplePolicyId = res.result.id;
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: javascript}
{: codeblock}

```python
policy_subjects = PolicySubject(
  attributes=[SubjectAttribute(name='iam_id', value='IBMid-123453user')])
policy_roles = PolicyRole(
  role_id='crn:v1:bluemix:public:openpages::::serviceRole:openpages.service.login')
account_id_resource_attribute = ResourceAttribute(
  name='accountId', value='ACCOUNT_ID')
service_name_resource_attribute = ResourceAttribute(
  name='serviceName', value='openpages')
policy_resources = PolicyResource(
  attributes=[account_id_resource_attribute,
        service_name_resource_attribute])

policy = iam_policy_management_service.create_policy(
  type='access',
  subjects=[policy_subjects],
  roles=[policy_roles],
  resources=[policy_resources]
).get_result()

print(json.dumps(policy, indent=2))
```
{: python}
{: codeblock}

```go
subjectAttribute := &iampolicymanagementv1.SubjectAttribute{
  Name:  core.StringPtr("iam_id"),
  Value: core.StringPtr("IBMid-123453user"),
}
policySubjects := &iampolicymanagementv1.PolicySubject{
  Attributes: []iampolicymanagementv1.SubjectAttribute{*subjectAttribute},
}
policyRoles := &iampolicymanagementv1.PolicyRole{
  RoleID: core.StringPtr("crn:v1:bluemix:public:openpages::::serviceRole:openpages.service.login"),
}
accountIDResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("accountId"),
  Value:    core.StringPtr("ACCOUNT_ID"),
  Operator: core.StringPtr("stringEquals"),
}
serviceNameResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("serviceName"),
  Value:    core.StringPtr("openpages"),
  Operator: core.StringPtr("stringEquals"),
}
policyResources := &iampolicymanagementv1.PolicyResource{
  Attributes: []iampolicymanagementv1.ResourceAttribute{
    *accountIDResourceAttribute, *serviceNameResourceAttribute}
}

options := iamPolicyManagementService.NewCreatePolicyOptions(
  "access",
  []iampolicymanagementv1.PolicySubject{*policySubjects},
  []iampolicymanagementv1.PolicyRole{*policyRoles},
  []iampolicymanagementv1.PolicyResource{*policyResources},
)

policy, response, err := iamPolicyManagementService.CreatePolicy(options)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(policy, "", "  ")
fmt.Println(string(b))
```
{: go}
{: codeblock}
