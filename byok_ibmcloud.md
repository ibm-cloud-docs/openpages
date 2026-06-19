# Customer-managed encryption key configuration guide

This document provides instructions for configuring customer-managed encryption keys using {{site.data.keyword.keymanagementservicelong_notm}} for {{site.data.keyword.openpages_short}} application provisioning.

---

## Prerequisites: Information required from {{site.data.keyword.openpages_short}}

Before starting the configuration, contact your {{site.data.keyword.openpages_short}} representative to obtain the following values:

| Item | Description | Placeholder |
|------|-------------|-------------|
| {{site.data.keyword.IBM_notm}} service ID | {{site.data.keyword.Bluemix_notm}} service identifier | `<IBM_SERVICE_ID>` |
| {{site.data.keyword.IBM_notm}} account ID | {{site.data.keyword.Bluemix_notm}} account ID | `<IBM_ACCOUNT_ID>` |

---

## Architecture overview

The custom encryption key implementation uses:
- {{site.data.keyword.keymanagementservicelong_notm}}: Customer-managed encryption key service
- Trusted profile: Secure identity federation between customer and {{site.data.keyword.IBM_notm}} accounts
- Service-to-service authorization: Controlled access for {{site.data.keyword.Bluemix_notm}} services ({{site.data.keyword.Db2_on_Cloud_short}}, {{site.data.keyword.cos_full_notm}})

---

## Section A: Customer-side configuration

### Step 1: Create {{site.data.keyword.keymanagementservicelong_notm}} service instance

Create an {{site.data.keyword.keymanagementservicelong_notm}} service instance via {{site.data.keyword.Bluemix_notm}} catalog. The encryption key can be in a different region than where your {{site.data.keyword.openpages_short}} application will be provisioned.

---

### Step 2: Create encryption key

Create a root key in your {{site.data.keyword.keymanagementservicelong_notm}} instance and capture the key CRN for provisioning.

**Key CRN Format:**
```
crn:v1:bluemix:public:kms:<REGION>:a/<YOUR_ACCOUNT_ID>:<KEY_PROTECT_INSTANCE_ID>:key:<KEY_ID>
```

---

### Step 3: Create trusted profile

Create a trusted profile in {{site.data.keyword.iamshort}} → Trusted profiles to establish secure access between your account and {{site.data.keyword.openpages_short}} services.

Configure the following:
- Establish trust with service ID: `<IBM_SERVICE_ID>` (provided by {{site.data.keyword.IBM_notm}})
- Assign access policy to {{site.data.keyword.keymanagementservicelong_notm}} service with Reader and ReaderPlus roles for your encryption key

Capture the profile ID for provisioning.

**Profile ID Format:**
```
Profile-<UUID>
```

---

### Step 4: Configure service-to-service authorizations

Configure authorizations in {{site.data.keyword.iamshort}} → Authorizations to grant {{site.data.keyword.Bluemix_notm}} services access to your {{site.data.keyword.keymanagementservicelong_notm}} instance.

#### 4.1 {{site.data.keyword.Db2_on_Cloud_short}} to {{site.data.keyword.keymanagementservicelong_notm}} authorization

Configure the following:
- Source service: {{site.data.keyword.Db2_on_Cloud_short}}
- Source account: `<IBM_ACCOUNT_ID>` (provided by {{site.data.keyword.IBM_notm}})
- Target service: {{site.data.keyword.keymanagementservicelong_notm}} (your instance)
- Roles: Reader, Authorization Delegator

#### 4.2 {{site.data.keyword.cos_full_notm}} to {{site.data.keyword.keymanagementservicelong_notm}} authorization

Configure the following:
- Source service: {{site.data.keyword.cos_full_notm}}
- Source account: `<IBM_ACCOUNT_ID>` (provided by {{site.data.keyword.IBM_notm}})
- Target service: {{site.data.keyword.keymanagementservicelong_notm}} (your instance)
- Roles: Reader

---

## Section B: Information required for {{site.data.keyword.openpages_short}} application provisioning

After completing the configuration, provide the following information when provisioning your {{site.data.keyword.openpages_short}} application:

### Required fields in provisioning catalog

| Field name | Description | Format |
|------------|-------------|--------|
| {{site.data.keyword.keymanagementservicelong_notm}} CRN | Specify your encryption key CRN to encrypt all data at rest using your own customer-managed key | `crn:v1:bluemix:public:kms:<REGION>:a/<YOUR_ACCOUNT_ID>:<INSTANCE_ID>:key:<KEY_ID>` |
| {{site.data.keyword.iamshort}} trusted profile ID | Trusted profile ID that grants access to your encryption key | `Profile-<UUID>` |

### Example values

**{{site.data.keyword.keymanagementservicelong_notm}} CRN:**
```
crn:v1:bluemix:public:kms:us-south:a/1234567890abcdef:a1b2c3d4-e5f6-7890-abcd-ef1234567890:key:9876543210fedcba
```

**{{site.data.keyword.iamshort}} trusted profile ID:**
```
Profile-1fd96a98-ffc2-4e11-92ab-fa1de563e19d
```

---

## Section C: Key management best practices

### Key lifecycle management

As the key owner, you are fully responsible for the lifecycle management of your encryption keys. This includes key rotation, monitoring, access control, and deletion policies. Any key lifecycle issues or risks are the customer's responsibility.
{: important}

### Key rotation

{{site.data.keyword.keymanagementservicelong_notm}} supports key rotation to enhance security:

- Manual rotation: Rotate keys on-demand based on your security requirements
- Rotation policy: Establish a key rotation schedule per your organization's security policies
- {{site.data.keyword.IBM_notm}} service compatibility: Key rotation does not impact {{site.data.keyword.openpages_short}} services - Encryption and decryption operations continue without interruption using the new key version

For detailed information on key rotation, see [{{site.data.keyword.keymanagementservicelong_notm}} key rotation](https://cloud.ibm.com/docs/key-protect?topic=key-protect-rotate-keys).

### Key deletion

Deleting an encryption key will make all encrypted data permanently inaccessible. This action is irreversible.
{: .warning}

- Never delete a key actively used by {{site.data.keyword.openpages_short}}
- {{site.data.keyword.Bluemix_notm}} enforces a 30-day waiting period before deletion
- Consider key disablement for temporary access revocation

For more information, see [{{site.data.keyword.keymanagementservicelong_notm}} key deletion](https://cloud.ibm.com/docs/key-protect?topic=key-protect-delete-keys)

## Additional resources

- [{{site.data.keyword.keymanagementservicelong_notm}}](https://cloud.ibm.com/docs/key-protect)
- [{{site.data.keyword.iamshort}} trusted profiles](https://cloud.ibm.com/docs/account?topic=account-create-trusted-profile)
- [{{site.data.keyword.iamshort}} service-to-service authorizations](https://cloud.ibm.com/docs/account?topic=account-serviceauth)

---
