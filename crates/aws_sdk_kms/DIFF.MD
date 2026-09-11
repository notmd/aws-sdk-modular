# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/kms`
- model: `aws-models/kms.json`
- package: `aws-sdk-kms`
- library: `aws_sdk_kms`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_cancel_key_deletion`: `CancelKeyDeletion`
- `op_connect_custom_key_store`: `ConnectCustomKeyStore`
- `op_create_alias`: `CreateAlias`
- `op_create_custom_key_store`: `CreateCustomKeyStore`
- `op_create_grant`: `CreateGrant`
- `op_create_key`: `CreateKey`
- `op_decrypt`: `Decrypt`
- `op_delete_alias`: `DeleteAlias`
- `op_delete_custom_key_store`: `DeleteCustomKeyStore`
- `op_delete_imported_key_material`: `DeleteImportedKeyMaterial`
- `op_derive_shared_secret`: `DeriveSharedSecret`
- `op_describe_custom_key_stores`: `DescribeCustomKeyStores`
- `op_describe_key`: `DescribeKey`
- `op_disable_key`: `DisableKey`
- `op_disable_key_rotation`: `DisableKeyRotation`
- `op_disconnect_custom_key_store`: `DisconnectCustomKeyStore`
- `op_enable_key`: `EnableKey`
- `op_enable_key_rotation`: `EnableKeyRotation`
- `op_encrypt`: `Encrypt`
- `op_generate_data_key`: `GenerateDataKey`
- `op_generate_data_key_pair`: `GenerateDataKeyPair`
- `op_generate_data_key_pair_without_plaintext`: `GenerateDataKeyPairWithoutPlaintext`
- `op_generate_data_key_without_plaintext`: `GenerateDataKeyWithoutPlaintext`
- `op_generate_mac`: `GenerateMac`
- `op_generate_random`: `GenerateRandom`
- `op_get_key_last_usage`: `GetKeyLastUsage`
- `op_get_key_policy`: `GetKeyPolicy`
- `op_get_key_rotation_status`: `GetKeyRotationStatus`
- `op_get_parameters_for_import`: `GetParametersForImport`
- `op_get_public_key`: `GetPublicKey`
- `op_import_key_material`: `ImportKeyMaterial`
- `op_list_aliases`: `ListAliases`
- `op_list_grants`: `ListGrants`
- `op_list_key_policies`: `ListKeyPolicies`
- `op_list_key_rotations`: `ListKeyRotations`
- `op_list_keys`: `ListKeys`
- `op_list_resource_tags`: `ListResourceTags`
- `op_list_retirable_grants`: `ListRetirableGrants`
- `op_put_key_policy`: `PutKeyPolicy`
- `op_re_encrypt`: `ReEncrypt`
- `op_replicate_key`: `ReplicateKey`
- `op_retire_grant`: `RetireGrant`
- `op_revoke_grant`: `RevokeGrant`
- `op_rotate_key_on_demand`: `RotateKeyOnDemand`
- `op_schedule_key_deletion`: `ScheduleKeyDeletion`
- `op_sign`: `Sign`
- `op_tag_resource`: `TagResource`
- `op_untag_resource`: `UntagResource`
- `op_update_alias`: `UpdateAlias`
- `op_update_custom_key_store`: `UpdateCustomKeyStore`
- `op_update_key_description`: `UpdateKeyDescription`
- `op_update_primary_region`: `UpdatePrimaryRegion`
- `op_verify`: `Verify`
- `op_verify_mac`: `VerifyMac`

## Changed files

- `Cargo.toml`
- `src/client.rs`
- `src/error_meta.rs`
- `src/lens.rs`
- `src/operation.rs`
- `src/protocol_serde.rs`
- `src/serde_util.rs`
- `src/types.rs`
- `src/types/builders.rs`
- `src/types/error.rs`
- `src/types/error/builders.rs`

## File diffs

### `Cargo.toml`

```diff
diff --git a/Cargo.toml b/Cargo.toml
--- a/Cargo.toml
+++ b/Cargo.toml
@@ -19,50 +19,39 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 version = "1.9.2"

 [dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 version = "1.3.0"

 [dependencies.aws-smithy-http]
-path = "../aws-smithy-http"
 version = "0.64.0"

 [dependencies.aws-smithy-json]
-path = "../aws-smithy-json"
 version = "0.63.0"

 [dependencies.aws-smithy-observability]
-path = "../aws-smithy-observability"
 version = "0.3.0"

 [dependencies.aws-smithy-runtime]
-path = "../aws-smithy-runtime"
 features = ["client"]
 version = "1.14.0"

 [dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["client", "http-1x"]
 version = "1.16.0"

 [dependencies.aws-smithy-schema]
-path = "../aws-smithy-schema"
 version = "0.2.0"

 [dependencies.aws-smithy-types]
-path = "../aws-smithy-types"
 features = ["http-body-1-x"]
 version = "1.6.3"

 [dependencies.aws-types]
-path = "../aws-types"
 version = "1.6.0"

 [dependencies.bytes]
@@ -84,45 +73,36 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["test-util"]
 version = "1.9.2"

 [dev-dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-smithy-http-client]
-path = "../aws-smithy-http-client"
 features = ["test-util", "wire-mock"]
 version = "1.4.0"

 [dev-dependencies.aws-smithy-protocol-test]
-path = "../aws-smithy-protocol-test"
 version = "0.64.0"

 [dev-dependencies.aws-smithy-runtime]
-path = "../aws-smithy-runtime"
 features = ["test-util"]
 version = "1.14.0"

 [dev-dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["test-util"]
 version = "1.16.0"

 [dev-dependencies.aws-smithy-types]
-path = "../aws-smithy-types"
 features = ["http-body-1-x", "test-util"]
 version = "1.6.3"

@@ -153,3 +133,57 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_cancel_key_deletion = []
+op_connect_custom_key_store = []
+op_create_alias = []
+op_create_custom_key_store = []
+op_create_grant = []
+op_create_key = []
+op_decrypt = []
+op_delete_alias = []
+op_delete_custom_key_store = []
+op_delete_imported_key_material = []
+op_derive_shared_secret = []
+op_describe_custom_key_stores = []
+op_describe_key = []
+op_disable_key = []
+op_disable_key_rotation = []
+op_disconnect_custom_key_store = []
+op_enable_key = []
+op_enable_key_rotation = []
+op_encrypt = []
+op_generate_data_key = []
+op_generate_data_key_pair = []
+op_generate_data_key_pair_without_plaintext = []
+op_generate_data_key_without_plaintext = []
+op_generate_mac = []
+op_generate_random = []
+op_get_key_last_usage = []
+op_get_key_policy = []
+op_get_key_rotation_status = []
+op_get_parameters_for_import = []
+op_get_public_key = []
+op_import_key_material = []
+op_list_aliases = []
+op_list_grants = []
+op_list_key_policies = []
+op_list_key_rotations = []
+op_list_keys = []
+op_list_resource_tags = []
+op_list_retirable_grants = []
+op_put_key_policy = []
+op_re_encrypt = []
+op_replicate_key = []
+op_retire_grant = []
+op_revoke_grant = []
+op_rotate_key_on_demand = []
+op_schedule_key_deletion = []
+op_sign = []
+op_tag_resource = []
+op_untag_resource = []
+op_update_alias = []
+op_update_custom_key_store = []
+op_update_key_description = []
+op_update_primary_region = []
+op_verify = []
+op_verify_mac = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,16 +136,22 @@
     }
 }

+#[cfg(feature = "op_cancel_key_deletion")]
 mod cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 mod connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 mod create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 mod create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 mod create_grant;

+#[cfg(feature = "op_create_key")]
 mod create_key;

 /// Operation customization and supporting types.
@@ -175,98 +181,146 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_decrypt")]
 mod decrypt;

+#[cfg(feature = "op_delete_alias")]
 mod delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 mod delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 mod delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 mod derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 mod describe_key;

+#[cfg(feature = "op_disable_key")]
 mod disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 mod disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 mod disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 mod enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 mod enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 mod encrypt;

+#[cfg(feature = "op_generate_data_key")]
 mod generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 mod generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 mod generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 mod generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 mod generate_mac;

+#[cfg(feature = "op_generate_random")]
 mod generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 mod get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 mod get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 mod get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 mod get_public_key;

+#[cfg(feature = "op_import_key_material")]
 mod import_key_material;

+#[cfg(feature = "op_list_aliases")]
 mod list_aliases;

+#[cfg(feature = "op_list_grants")]
 mod list_grants;

+#[cfg(feature = "op_list_key_policies")]
 mod list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 mod list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 mod list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 mod list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 mod list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 mod put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 mod re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 mod replicate_key;

+#[cfg(feature = "op_retire_grant")]
 mod retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 mod revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 mod rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 mod schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 mod sign;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_alias")]
 mod update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 mod update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 mod update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 mod update_primary_region;

+#[cfg(feature = "op_verify")]
 mod verify;

+#[cfg(feature = "op_verify_mac")]
 mod verify_mac;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,11 +3,19 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
     /// <p>The request was rejected because it attempted to create a resource that already exists.</p>
     AlreadyExistsException(crate::types::error::AlreadyExistsException),
+    #[cfg(feature = "op_create_custom_key_store")]
     /// <p>The request was rejected because the specified CloudHSM cluster is already associated with an CloudHSM key store in the account, or it shares a backup history with an CloudHSM key store in the account. Each CloudHSM key store in the account must be associated with a different CloudHSM cluster.</p>
     /// <p>CloudHSM clusters that share a backup history have the same cluster certificate. To view the cluster certificate of an CloudHSM cluster, use the <a href="https://docs.aws.amazon.com/cloudhsm/latest/APIReference/API_DescribeClusters.html">DescribeClusters</a> operation.</p>
     CloudHsmClusterInUseException(crate::types::error::CloudHsmClusterInUseException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because the associated CloudHSM cluster did not meet the configuration requirements for an CloudHSM key store.</p>
     /// <ul>
     /// <li>
@@ -20,18 +28,35 @@
     /// </ul>
     /// <p>For information about the requirements for an CloudHSM cluster that is associated with an CloudHSM key store, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/create-keystore.html#before-keystore">Assemble the Prerequisites</a> in the <i>Key Management Service Developer Guide</i>. For information about creating a private subnet for an CloudHSM cluster, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/create-subnets.html">Create a Private Subnet</a> in the <i>CloudHSM User Guide</i>. For information about cluster security groups, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/configure-sg.html">Configure a Default Security Group</a> in the <i> <i>CloudHSM User Guide</i> </i>.</p>
     CloudHsmClusterInvalidConfigurationException(crate::types::error::CloudHsmClusterInvalidConfigurationException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_custom_key_store",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because the CloudHSM cluster associated with the CloudHSM key store is not active. Initialize and activate the cluster and try the command again. For detailed instructions, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/getting-started.html">Getting Started</a> in the <i>CloudHSM User Guide</i>.</p>
     CloudHsmClusterNotActiveException(crate::types::error::CloudHsmClusterNotActiveException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because KMS cannot find the CloudHSM cluster with the specified cluster ID. Retry the request with a different cluster ID.</p>
     CloudHsmClusterNotFoundException(crate::types::error::CloudHsmClusterNotFoundException),
+    #[cfg(feature = "op_update_custom_key_store")]
     /// <p>The request was rejected because the specified CloudHSM cluster has a different cluster certificate than the original cluster. You cannot use the operation to specify an unrelated cluster for an CloudHSM key store.</p>
     /// <p>Specify an CloudHSM cluster that shares a backup history with the original cluster. This includes clusters that were created from a backup of the current cluster, and clusters that were created from the same backup that produced the current cluster.</p>
     /// <p>CloudHSM clusters that share a backup history have the same cluster certificate. To view the cluster certificate of an CloudHSM cluster, use the <a href="https://docs.aws.amazon.com/cloudhsm/latest/APIReference/API_DescribeClusters.html">DescribeClusters</a> operation.</p>
     CloudHsmClusterNotRelatedException(crate::types::error::CloudHsmClusterNotRelatedException),
+    #[cfg(feature = "op_rotate_key_on_demand")]
     /// <p>The request was rejected because an automatic rotation of this key is currently in progress or scheduled to begin within the next 20 minutes.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_delete_custom_key_store")]
     /// <p>The request was rejected because the custom key store contains KMS keys. After verifying that you do not need to use the KMS keys, use the <code>ScheduleKeyDeletion</code> operation to delete the KMS keys. After they are deleted, you can delete the custom key store.</p>
     CustomKeyStoreHasCmKsException(crate::types::error::CustomKeyStoreHasCmKsException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_delete_custom_key_store",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_generate_random",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because of the <code>ConnectionState</code> of the custom key store. To get the <code>ConnectionState</code> of a custom key store, use the <code>DescribeCustomKeyStores</code> operation.</p>
     /// <p>This exception is thrown under the following conditions:</p>
     /// <ul>
@@ -47,38 +72,205 @@
     /// <p>You requested the <code>GenerateRandom</code> operation in an CloudHSM key store that is not connected. This operation is valid only when the CloudHSM key store <code>ConnectionState</code> is <code>CONNECTED</code>.</p></li>
     /// </ul>
     CustomKeyStoreInvalidStateException(crate::types::error::CustomKeyStoreInvalidStateException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the specified custom key store name is already assigned to another custom key store in the account. Try again with a custom key store name that is unique in the account.</p>
     CustomKeyStoreNameInUseException(crate::types::error::CustomKeyStoreNameInUseException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_delete_custom_key_store",
+        feature = "op_describe_custom_key_stores",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_generate_random",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because KMS cannot find a custom key store with the specified key store name or ID.</p>
     CustomKeyStoreNotFoundException(crate::types::error::CustomKeyStoreNotFoundException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_random",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_keys",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_verify"
+    ))]
     /// <p>The system timed out while trying to fulfill the request. You can retry the request.</p>
     DependencyTimeoutException(crate::types::error::DependencyTimeoutException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_sign",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified KMS key is not enabled.</p>
     DisabledException(crate::types::error::DisabledException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the DryRun parameter was specified.</p>
     DryRunOperationException(crate::types::error::DryRunOperationException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the specified import token is expired. Use <code>GetParametersForImport</code> to get a new import token and public key, use the new public key to encrypt the key material, and then try the request again.</p>
     ExpiredImportTokenException(crate::types::error::ExpiredImportTokenException),
+    #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
     /// <p>The request was rejected because the specified KMS key cannot decrypt the data. The <code>KeyId</code> in a <code>Decrypt</code> request and the <code>SourceKeyId</code> in a <code>ReEncrypt</code> request must identify the same KMS key that was used to encrypt the ciphertext.</p>
     IncorrectKeyException(crate::types::error::IncorrectKeyException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the key material in the request is, expired, invalid, or does not meet expectations. For example, it is not the same key material that was previously imported or KMS expected new key material but the key material being imported is already associated with the KMS key.</p>
     IncorrectKeyMaterialException(crate::types::error::IncorrectKeyMaterialException),
+    #[cfg(feature = "op_create_custom_key_store")]
     /// <p>The request was rejected because the trust anchor certificate in the request to create an CloudHSM key store is not the trust anchor certificate for the specified CloudHSM cluster.</p>
     /// <p>When you <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/initialize-cluster.html#sign-csr">initialize the CloudHSM cluster</a>, you create the trust anchor certificate and save it in the <code>customerCA.crt</code> file.</p>
     IncorrectTrustAnchorException(crate::types::error::IncorrectTrustAnchorException),
+    #[cfg(feature = "op_create_alias")]
     /// <p>The request was rejected because the specified alias name is not valid.</p>
     InvalidAliasNameException(crate::types::error::InvalidAliasNameException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_delete_imported_key_material",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region"
+    ))]
     /// <p>The request was rejected because a specified ARN, or an ARN in a key policy, is not valid.</p>
     InvalidArnException(crate::types::error::InvalidArnException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_import_key_material",
+        feature = "op_re_encrypt"
+    ))]
     /// <p>From the <code>Decrypt</code> or <code>ReEncrypt</code> operation, the request was rejected because the specified ciphertext, or additional authenticated data incorporated into the ciphertext, such as the encryption context, is corrupted, missing, or otherwise invalid.</p>
     /// <p>From the <code>ImportKeyMaterial</code> operation, the request was rejected because KMS could not decrypt the encrypted (wrapped) key material.</p>
     InvalidCiphertextException(crate::types::error::InvalidCiphertextException),
+    #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
     /// <p>The request was rejected because the specified <code>GrantId</code> is not valid.</p>
     InvalidGrantIdException(crate::types::error::InvalidGrantIdException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified grant token is not valid.</p>
     InvalidGrantTokenException(crate::types::error::InvalidGrantTokenException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the provided import token is invalid or is associated with a different KMS key.</p>
     InvalidImportTokenException(crate::types::error::InvalidImportTokenException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected for one of the following reasons:</p>
     /// <ul>
     /// <li>
@@ -89,14 +281,123 @@
     /// <p>For encrypting, decrypting, re-encrypting, and generating data keys, the <code>KeyUsage</code> must be <code>ENCRYPT_DECRYPT</code>. For signing and verifying messages, the <code>KeyUsage</code> must be <code>SIGN_VERIFY</code>. For generating and verifying message authentication codes (MACs), the <code>KeyUsage</code> must be <code>GENERATE_VERIFY_MAC</code>. For deriving key agreement secrets, the <code>KeyUsage</code> must be <code>KEY_AGREEMENT</code>. To find the <code>KeyUsage</code> of a KMS key, use the <code>DescribeKey</code> operation.</p>
     /// <p>To find the encryption or signing algorithms supported for a particular KMS key, use the <code>DescribeKey</code> operation.</p>
     InvalidKeyUsageException(crate::types::error::InvalidKeyUsageException),
+    #[cfg(any(
+        feature = "op_describe_custom_key_stores",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_rotations",
+        feature = "op_list_keys",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants"
+    ))]
     /// <p>The request was rejected because the marker that specifies where pagination should next begin is not valid.</p>
     InvalidMarkerException(crate::types::error::InvalidMarkerException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_alias",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_custom_key_store",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_custom_key_stores",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_generate_random",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_keys",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_custom_key_store",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because an internal exception occurred. The request can be retried.</p>
     KmsInternalException(crate::types::error::KmsInternalException),
+    #[cfg(feature = "op_verify_mac")]
     /// <p>The request was rejected because the HMAC verification failed. HMAC verification fails when the HMAC computed by using the specified message, HMAC KMS key, and MAC algorithm does not match the HMAC specified in the request.</p>
     KmsInvalidMacException(crate::types::error::KmsInvalidMacException),
+    #[cfg(feature = "op_verify")]
     /// <p>The request was rejected because the signature verification failed. Signature verification fails when it cannot confirm that signature was produced by signing the specified message with the specified KMS key and signing algorithm.</p>
     KmsInvalidSignatureException(crate::types::error::KmsInvalidSignatureException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the state of the specified resource is not valid for this request.</p>
     /// <p>This exceptions means one of the following:</p>
     /// <ul>
@@ -107,48 +408,163 @@
     /// <p>For cryptographic operations on KMS keys in custom key stores, this exception represents a general failure with many possible causes. To identify the cause, see the error message that accompanies the exception.</p></li>
     /// </ul>
     KmsInvalidStateException(crate::types::error::KmsInvalidStateException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified KMS key was not available. You can retry the request.</p>
     KeyUnavailableException(crate::types::error::KeyUnavailableException),
+    #[cfg(any(
+        feature = "op_create_alias",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_enable_key",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_tag_resource",
+        feature = "op_update_alias"
+    ))]
     /// <p>The request was rejected because a length constraint or quota was exceeded. For more information, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/limits.html">Quotas</a> in the <i>Key Management Service Developer Guide</i>.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key"
+    ))]
     /// <p>The request was rejected because the specified policy is not syntactically or semantically correct.</p>
     MalformedPolicyDocumentException(crate::types::error::MalformedPolicyDocumentException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified entity or resource could not be found.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_replicate_key",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>The request was rejected because one or more tags are not valid.</p>
     TagException(crate::types::error::TagException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_delete_imported_key_material",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key_rotation",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_random",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_key_rotations",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_update_primary_region"
+    ))]
     /// <p>The request was rejected because a specified parameter is not supported or a specified resource is not valid for this operation.</p>
     UnsupportedOperationException(crate::types::error::UnsupportedOperationException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the (<code>XksKeyId</code>) is already associated with another KMS key in this external key store. Each KMS key in an external key store must be associated with a different external key.</p>
     XksKeyAlreadyInUseException(crate::types::error::XksKeyAlreadyInUseException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the external key specified by the <code>XksKeyId</code> parameter did not meet the configuration requirements for an external key store.</p>
     /// <p>The external key must be an AES-256 symmetric key that is enabled and performs encryption and decryption.</p>
     XksKeyInvalidConfigurationException(crate::types::error::XksKeyInvalidConfigurationException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the external key store proxy could not find the external key. This exception is thrown when the value of the <code>XksKeyId</code> parameter doesn't identify a key in the external key manager associated with the external key proxy.</p>
     /// <p>Verify that the <code>XksKeyId</code> represents an existing key in the external key manager. Use the key identifier that the external key store proxy uses to identify the key. For details, see the documentation provided with your external key store proxy or key manager.</p>
     XksKeyNotFoundException(crate::types::error::XksKeyNotFoundException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the proxy credentials failed to authenticate to the specified external key store proxy. The specified external key store proxy rejected a status request from KMS due to invalid credentials. This can indicate an error in the credentials or in the identification of the external key store proxy.</p>
     XksProxyIncorrectAuthenticationCredentialException(
         crate::types::error::XksProxyIncorrectAuthenticationCredentialException,
     ),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the external key store proxy is not configured correctly. To identify the cause, see the error message that accompanies the exception.</p>
     XksProxyInvalidConfigurationException(crate::types::error::XksProxyInvalidConfigurationException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p></p>
     /// <p>KMS cannot interpret the response it received from the external key store proxy. The problem might be a poorly constructed response, but it could also be a transient network issue. If you see this error repeatedly, report it to the proxy vendor.</p>
     XksProxyInvalidResponseException(crate::types::error::XksProxyInvalidResponseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the <code>XksProxyUriEndpoint</code> is already associated with another external key store in this Amazon Web Services Region. To identify the cause, see the error message that accompanies the exception.</p>
     XksProxyUriEndpointInUseException(crate::types::error::XksProxyUriEndpointInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the concatenation of the <code>XksProxyUriEndpoint</code> and <code>XksProxyUriPath</code> is already associated with another external key store in this Amazon Web Services Region. Each external key store in a Region must use a unique external key store proxy API address.</p>
     XksProxyUriInUseException(crate::types::error::XksProxyUriInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>KMS was unable to reach the specified <code>XksProxyUriPath</code>. The path must be reachable before you create the external key store or update its settings.</p>
     /// <p>This exception is also thrown when the external key store proxy response to a <code>GetHealthStatus</code> request indicates that all external key manager instances are unavailable.</p>
     XksProxyUriUnreachableException(crate::types::error::XksProxyUriUnreachableException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the specified Amazon VPC endpoint service is already associated with another external key store in this Amazon Web Services Region. Each external key store in a Region must use a different Amazon VPC endpoint service.</p>
     XksProxyVpcEndpointServiceInUseException(crate::types::error::XksProxyVpcEndpointServiceInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the Amazon VPC endpoint service configuration does not fulfill the requirements for an external key store. To identify the cause, see the error message that accompanies the exception and <a href="https://docs.aws.amazon.com/kms/latest/developerguide/vpc-connectivity.html#xks-vpc-requirements">review the requirements</a> for Amazon VPC endpoint service connectivity for an external key store.</p>
     XksProxyVpcEndpointServiceInvalidConfigurationException(
         crate::types::error::XksProxyVpcEndpointServiceInvalidConfigurationException,
     ),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because KMS could not find the specified VPC endpoint service. Use <code>DescribeCustomKeyStores</code> to verify the VPC endpoint service name for the external key store. Also, confirm that the <code>Allow principals</code> list for the VPC endpoint service includes the KMS service principal for the Region, such as <code>cks.kms.us-east-1.amazonaws.com</code>.</p>
     XksProxyVpcEndpointServiceNotFoundException(crate::types::error::XksProxyVpcEndpointServiceNotFoundException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -165,53 +581,469 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Error::AlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::CloudHsmClusterInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterNotActiveException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CloudHsmClusterNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_custom_key_store")]
             Error::CloudHsmClusterNotRelatedException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Error::CustomKeyStoreHasCmKsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CustomKeyStoreNameInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Error::DependencyTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DryRunOperationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::ExpiredImportTokenException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Error::IncorrectKeyException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::IncorrectKeyMaterialException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::IncorrectTrustAnchorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_alias")]
             Error::InvalidAliasNameException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Error::InvalidArnException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Error::InvalidCiphertextException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Error::InvalidGrantIdException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidGrantTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::InvalidImportTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidKeyUsageException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Error::InvalidMarkerException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInternalException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify_mac")]
             Error::KmsInvalidMacException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify")]
             Error::KmsInvalidSignatureException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KeyUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Error::UnsupportedOperationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyAlreadyInUseException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidResponseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriEndpointInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriUnreachableException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -236,58 +1068,475 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Self::AlreadyExistsException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::CloudHsmClusterInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterNotActiveException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CloudHsmClusterNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Self::CloudHsmClusterNotRelatedException(inner) => inner.meta(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Self::CustomKeyStoreHasCmKsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CustomKeyStoreNameInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Self::DependencyTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DryRunOperationException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::ExpiredImportTokenException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Self::IncorrectKeyException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::IncorrectKeyMaterialException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::IncorrectTrustAnchorException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_alias")]
             Self::InvalidAliasNameException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Self::InvalidArnException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Self::InvalidCiphertextException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Self::InvalidGrantIdException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidGrantTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::InvalidImportTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidKeyUsageException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Self::InvalidMarkerException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInternalException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify_mac")]
             Self::KmsInvalidMacException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify")]
             Self::KmsInvalidSignatureException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KeyUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Self::MalformedPolicyDocumentException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Self::UnsupportedOperationException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyAlreadyInUseException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidResponseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriEndpointInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriUnreachableException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_cancel_key_deletion")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -313,6 +1562,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_key_deletion")]
 impl From<crate::operation::cancel_key_deletion::CancelKeyDeletionError> for Error {
     fn from(err: crate::operation::cancel_key_deletion::CancelKeyDeletionError) -> Self {
         match err {
@@ -335,6 +1585,7 @@
         }
     }
 }
+#[cfg(feature = "op_connect_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -360,6 +1611,7 @@
         }
     }
 }
+#[cfg(feature = "op_connect_custom_key_store")]
 impl From<crate::operation::connect_custom_key_store::ConnectCustomKeyStoreError> for Error {
     fn from(err: crate::operation::connect_custom_key_store::ConnectCustomKeyStoreError) -> Self {
         match err {
@@ -380,6 +1632,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_alias::CreateAliasError, R>>
     for Error
 where
@@ -397,6 +1650,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_alias")]
 impl From<crate::operation::create_alias::CreateAliasError> for Error {
     fn from(err: crate::operation::create_alias::CreateAliasError) -> Self {
         match err {
@@ -425,6 +1679,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -450,6 +1705,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_key_store")]
 impl From<crate::operation::create_custom_key_store::CreateCustomKeyStoreError> for Error {
     fn from(err: crate::operation::create_custom_key_store::CreateCustomKeyStoreError) -> Self {
         match err {
@@ -506,6 +1762,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_grant::CreateGrantError, R>>
     for Error
 where
@@ -523,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_grant")]
 impl From<crate::operation::create_grant::CreateGrantError> for Error {
     fn from(err: crate::operation::create_grant::CreateGrantError) -> Self {
         match err {
@@ -557,6 +1815,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_key::CreateKeyError, R>>
     for Error
 where
@@ -574,6 +1833,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_key")]
 impl From<crate::operation::create_key::CreateKeyError> for Error {
     fn from(err: crate::operation::create_key::CreateKeyError) -> Self {
         match err {
@@ -618,6 +1878,7 @@
         }
     }
 }
+#[cfg(feature = "op_decrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::decrypt::DecryptError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -634,6 +1895,7 @@
         }
     }
 }
+#[cfg(feature = "op_decrypt")]
 impl From<crate::operation::decrypt::DecryptError> for Error {
     fn from(err: crate::operation::decrypt::DecryptError) -> Self {
         match err {
@@ -668,6 +1930,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_alias::DeleteAliasError, R>>
     for Error
 where
@@ -685,6 +1948,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_alias")]
 impl From<crate::operation::delete_alias::DeleteAliasError> for Error {
     fn from(err: crate::operation::delete_alias::DeleteAliasError) -> Self {
         match err {
@@ -704,6 +1968,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -729,6 +1994,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_key_store")]
 impl From<crate::operation::delete_custom_key_store::DeleteCustomKeyStoreError> for Error {
     fn from(err: crate::operation::delete_custom_key_store::DeleteCustomKeyStoreError) -> Self {
         match err {
@@ -746,6 +2012,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_imported_key_material")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -771,6 +2038,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_imported_key_material")]
 impl From<crate::operation::delete_imported_key_material::DeleteImportedKeyMaterialError> for Error {
     fn from(err: crate::operation::delete_imported_key_material::DeleteImportedKeyMaterialError) -> Self {
         match err {
@@ -796,6 +2064,7 @@
         }
     }
 }
+#[cfg(feature = "op_derive_shared_secret")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -821,6 +2090,7 @@
         }
     }
 }
+#[cfg(feature = "op_derive_shared_secret")]
 impl From<crate::operation::derive_shared_secret::DeriveSharedSecretError> for Error {
     fn from(err: crate::operation::derive_shared_secret::DeriveSharedSecretError) -> Self {
         match err {
@@ -857,6 +2127,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_custom_key_stores")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -882,6 +2153,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_custom_key_stores")]
 impl From<crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresError> for Error {
     fn from(err: crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresError) -> Self {
         match err {
@@ -898,6 +2170,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_key::DescribeKeyError, R>>
     for Error
 where
@@ -915,6 +2188,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_key")]
 impl From<crate::operation::describe_key::DescribeKeyError> for Error {
     fn from(err: crate::operation::describe_key::DescribeKeyError) -> Self {
         match err {
@@ -934,6 +2208,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::disable_key::DisableKeyError, R>>
     for Error
 where
@@ -951,6 +2226,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key")]
 impl From<crate::operation::disable_key::DisableKeyError> for Error {
     fn from(err: crate::operation::disable_key::DisableKeyError) -> Self {
         match err {
@@ -971,6 +2247,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key_rotation")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -996,6 +2273,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key_rotation")]
 impl From<crate::operation::disable_key_rotation::DisableKeyRotationError> for Error {
     fn from(err: crate::operation::disable_key_rotation::DisableKeyRotationError) -> Self {
         match err {
@@ -1026,6 +2304,7 @@
         }
     }
 }
+#[cfg(feature = "op_disconnect_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1051,6 +2330,7 @@
         }
     }
 }
+#[cfg(feature = "op_disconnect_custom_key_store")]
 impl From<crate::operation::disconnect_custom_key_store::DisconnectCustomKeyStoreError> for Error {
     fn from(err: crate::operation::disconnect_custom_key_store::DisconnectCustomKeyStoreError) -> Self {
         match err {
@@ -1067,6 +2347,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::enable_key::EnableKeyError, R>>
     for Error
 where
@@ -1084,6 +2365,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key")]
 impl From<crate::operation::enable_key::EnableKeyError> for Error {
     fn from(err: crate::operation::enable_key::EnableKeyError) -> Self {
         match err {
@@ -1107,6 +2389,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key_rotation")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1132,6 +2415,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key_rotation")]
 impl From<crate::operation::enable_key_rotation::EnableKeyRotationError> for Error {
     fn from(err: crate::operation::enable_key_rotation::EnableKeyRotationError) -> Self {
         match err {
@@ -1160,6 +2444,7 @@
         }
     }
 }
+#[cfg(feature = "op_encrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::encrypt::EncryptError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1176,6 +2461,7 @@
         }
     }
 }
+#[cfg(feature = "op_encrypt")]
 impl From<crate::operation::encrypt::EncryptError> for Error {
     fn from(err: crate::operation::encrypt::EncryptError) -> Self {
         match err {
@@ -1204,6 +2490,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1229,6 +2516,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key")]
 impl From<crate::operation::generate_data_key::GenerateDataKeyError> for Error {
     fn from(err: crate::operation::generate_data_key::GenerateDataKeyError) -> Self {
         match err {
@@ -1263,6 +2551,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1288,6 +2577,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair")]
 impl From<crate::operation::generate_data_key_pair::GenerateDataKeyPairError> for Error {
     fn from(err: crate::operation::generate_data_key_pair::GenerateDataKeyPairError) -> Self {
         match err {
@@ -1327,6 +2617,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1352,6 +2643,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 impl From<crate::operation::generate_data_key_pair_without_plaintext::GenerateDataKeyPairWithoutPlaintextError>
     for Error
 {
@@ -1395,6 +2687,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1420,6 +2713,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 impl From<crate::operation::generate_data_key_without_plaintext::GenerateDataKeyWithoutPlaintextError> for Error {
     fn from(err: crate::operation::generate_data_key_without_plaintext::GenerateDataKeyWithoutPlaintextError) -> Self {
         match err {
@@ -1454,6 +2748,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_mac")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::generate_mac::GenerateMacError, R>>
     for Error
 where
@@ -1471,6 +2766,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_mac")]
 impl From<crate::operation::generate_mac::GenerateMacError> for Error {
     fn from(err: crate::operation::generate_mac::GenerateMacError) -> Self {
         match err {
@@ -1502,6 +2798,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_random")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::generate_random::GenerateRandomError, R>>
     for Error
@@ -1523,6 +2820,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_random")]
 impl From<crate::operation::generate_random::GenerateRandomError> for Error {
     fn from(err: crate::operation::generate_random::GenerateRandomError) -> Self {
         match err {
@@ -1545,6 +2843,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_last_usage")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1570,6 +2869,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_last_usage")]
 impl From<crate::operation::get_key_last_usage::GetKeyLastUsageError> for Error {
     fn from(err: crate::operation::get_key_last_usage::GetKeyLastUsageError) -> Self {
         match err {
@@ -1589,6 +2889,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_policy")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_key_policy::GetKeyPolicyError, R>>
     for Error
 where
@@ -1606,6 +2907,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_policy")]
 impl From<crate::operation::get_key_policy::GetKeyPolicyError> for Error {
     fn from(err: crate::operation::get_key_policy::GetKeyPolicyError) -> Self {
         match err {
@@ -1628,6 +2930,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_rotation_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1653,6 +2956,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_rotation_status")]
 impl From<crate::operation::get_key_rotation_status::GetKeyRotationStatusError> for Error {
     fn from(err: crate::operation::get_key_rotation_status::GetKeyRotationStatusError) -> Self {
         match err {
@@ -1680,6 +2984,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_parameters_for_import")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1705,6 +3010,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_parameters_for_import")]
 impl From<crate::operation::get_parameters_for_import::GetParametersForImportError> for Error {
     fn from(err: crate::operation::get_parameters_for_import::GetParametersForImportError) -> Self {
         match err {
@@ -1732,6 +3038,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_public_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_public_key::GetPublicKeyError, R>>
     for Error
 where
@@ -1749,6 +3056,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_public_key")]
 impl From<crate::operation::get_public_key::GetPublicKeyError> for Error {
     fn from(err: crate::operation::get_public_key::GetPublicKeyError) -> Self {
         match err {
@@ -1786,6 +3094,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_key_material")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1811,6 +3120,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_key_material")]
 impl From<crate::operation::import_key_material::ImportKeyMaterialError> for Error {
     fn from(err: crate::operation::import_key_material::ImportKeyMaterialError) -> Self {
         match err {
@@ -1848,6 +3158,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aliases")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_aliases::ListAliasesError, R>>
     for Error
 where
@@ -1865,6 +3176,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aliases")]
 impl From<crate::operation::list_aliases::ListAliasesError> for Error {
     fn from(err: crate::operation::list_aliases::ListAliasesError) -> Self {
         match err {
@@ -1887,6 +3199,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_grants")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_grants::ListGrantsError, R>>
     for Error
 where
@@ -1904,6 +3217,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_grants")]
 impl From<crate::operation::list_grants::ListGrantsError> for Error {
     fn from(err: crate::operation::list_grants::ListGrantsError) -> Self {
         match err {
@@ -1930,6 +3244,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1955,6 +3270,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_policies")]
 impl From<crate::operation::list_key_policies::ListKeyPoliciesError> for Error {
     fn from(err: crate::operation::list_key_policies::ListKeyPoliciesError) -> Self {
         match err {
@@ -1977,6 +3293,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_rotations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2002,6 +3319,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_rotations")]
 impl From<crate::operation::list_key_rotations::ListKeyRotationsError> for Error {
     fn from(err: crate::operation::list_key_rotations::ListKeyRotationsError) -> Self {
         match err {
@@ -2027,6 +3345,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_keys")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_keys::ListKeysError, R>>
     for Error
 where
@@ -2044,6 +3363,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_keys")]
 impl From<crate::operation::list_keys::ListKeysError> for Error {
     fn from(err: crate::operation::list_keys::ListKeysError) -> Self {
         match err {
@@ -2060,6 +3380,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tags")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2085,6 +3406,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tags")]
 impl From<crate::operation::list_resource_tags::ListResourceTagsError> for Error {
     fn from(err: crate::operation::list_resource_tags::ListResourceTagsError) -> Self {
         match err {
@@ -2104,6 +3426,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_retirable_grants")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2129,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_retirable_grants")]
 impl From<crate::operation::list_retirable_grants::ListRetirableGrantsError> for Error {
     fn from(err: crate::operation::list_retirable_grants::ListRetirableGrantsError) -> Self {
         match err {
@@ -2153,6 +3477,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_key_policy")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_key_policy::PutKeyPolicyError, R>>
     for Error
 where
@@ -2170,6 +3495,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_key_policy")]
 impl From<crate::operation::put_key_policy::PutKeyPolicyError> for Error {
     fn from(err: crate::operation::put_key_policy::PutKeyPolicyError) -> Self {
         match err {
@@ -2201,6 +3527,7 @@
         }
     }
 }
+#[cfg(feature = "op_re_encrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::re_encrypt::ReEncryptError, R>>
     for Error
 where
@@ -2218,6 +3545,7 @@
         }
     }
 }
+#[cfg(feature = "op_re_encrypt")]
 impl From<crate::operation::re_encrypt::ReEncryptError> for Error {
     fn from(err: crate::operation::re_encrypt::ReEncryptError) -> Self {
         match err {
@@ -2254,6 +3582,7 @@
         }
     }
 }
+#[cfg(feature = "op_replicate_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::replicate_key::ReplicateKeyError, R>>
     for Error
 where
@@ -2271,6 +3600,7 @@
         }
     }
 }
+#[cfg(feature = "op_replicate_key")]
 impl From<crate::operation::replicate_key::ReplicateKeyError> for Error {
     fn from(err: crate::operation::replicate_key::ReplicateKeyError) -> Self {
         match err {
@@ -2306,6 +3636,7 @@
         }
     }
 }
+#[cfg(feature = "op_retire_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::retire_grant::RetireGrantError, R>>
     for Error
 where
@@ -2323,6 +3654,7 @@
         }
     }
 }
+#[cfg(feature = "op_retire_grant")]
 impl From<crate::operation::retire_grant::RetireGrantError> for Error {
     fn from(err: crate::operation::retire_grant::RetireGrantError) -> Self {
         match err {
@@ -2354,6 +3686,7 @@
         }
     }
 }
+#[cfg(feature = "op_revoke_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::revoke_grant::RevokeGrantError, R>>
     for Error
 where
@@ -2371,6 +3704,7 @@
         }
     }
 }
+#[cfg(feature = "op_revoke_grant")]
 impl From<crate::operation::revoke_grant::RevokeGrantError> for Error {
     fn from(err: crate::operation::revoke_grant::RevokeGrantError) -> Self {
         match err {
@@ -2399,6 +3733,7 @@
         }
     }
 }
+#[cfg(feature = "op_rotate_key_on_demand")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2424,6 +3759,7 @@
         }
     }
 }
+#[cfg(feature = "op_rotate_key_on_demand")]
 impl From<crate::operation::rotate_key_on_demand::RotateKeyOnDemandError> for Error {
     fn from(err: crate::operation::rotate_key_on_demand::RotateKeyOnDemandError) -> Self {
         match err {
@@ -2458,6 +3794,7 @@
         }
     }
 }
+#[cfg(feature = "op_schedule_key_deletion")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2483,6 +3820,7 @@
         }
     }
 }
+#[cfg(feature = "op_schedule_key_deletion")]
 impl From<crate::operation::schedule_key_deletion::ScheduleKeyDeletionError> for Error {
     fn from(err: crate::operation::schedule_key_deletion::ScheduleKeyDeletionError) -> Self {
         match err {
@@ -2507,6 +3845,7 @@
         }
     }
 }
+#[cfg(feature = "op_sign")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::sign::SignError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2521,6 +3860,7 @@
         }
     }
 }
+#[cfg(feature = "op_sign")]
 impl From<crate::operation::sign::SignError> for Error {
     fn from(err: crate::operation::sign::SignError) -> Self {
         match err {
@@ -2547,6 +3887,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -2564,6 +3905,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -2587,6 +3929,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2608,6 +3951,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2628,6 +3972,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_alias::UpdateAliasError, R>>
     for Error
 where
@@ -2645,6 +3990,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_alias")]
 impl From<crate::operation::update_alias::UpdateAliasError> for Error {
     fn from(err: crate::operation::update_alias::UpdateAliasError) -> Self {
         match err {
@@ -2667,6 +4013,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2692,6 +4039,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_key_store")]
 impl From<crate::operation::update_custom_key_store::UpdateCustomKeyStoreError> for Error {
     fn from(err: crate::operation::update_custom_key_store::UpdateCustomKeyStoreError) -> Self {
         match err {
@@ -2748,6 +4096,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_key_description")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2773,6 +4122,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_key_description")]
 impl From<crate::operation::update_key_description::UpdateKeyDescriptionError> for Error {
     fn from(err: crate::operation::update_key_description::UpdateKeyDescriptionError) -> Self {
         match err {
@@ -2797,6 +4147,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_primary_region")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2822,6 +4173,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_primary_region")]
 impl From<crate::operation::update_primary_region::UpdatePrimaryRegionError> for Error {
     fn from(err: crate::operation::update_primary_region::UpdatePrimaryRegionError) -> Self {
         match err {
@@ -2849,6 +4201,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::verify::VerifyError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2863,6 +4216,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify")]
 impl From<crate::operation::verify::VerifyError> for Error {
     fn from(err: crate::operation::verify::VerifyError) -> Self {
         match err {
@@ -2894,6 +4248,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_mac")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::verify_mac::VerifyMacError, R>>
     for Error
 where
@@ -2911,6 +4266,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_mac")]
 impl From<crate::operation::verify_mac::VerifyMacError> for Error {
     fn from(err: crate::operation::verify_mac::VerifyMacError) -> Self {
         match err {
@@ -2944,53 +4300,469 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Error::AlreadyExistsException(inner) => inner.source(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::CloudHsmClusterInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterNotActiveException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CloudHsmClusterNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Error::CloudHsmClusterNotRelatedException(inner) => inner.source(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Error::CustomKeyStoreHasCmKsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreInvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CustomKeyStoreNameInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Error::DependencyTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DryRunOperationException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::ExpiredImportTokenException(inner) => inner.source(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Error::IncorrectKeyException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::IncorrectKeyMaterialException(inner) => inner.source(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::IncorrectTrustAnchorException(inner) => inner.source(),
+            #[cfg(feature = "op_create_alias")]
             Error::InvalidAliasNameException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Error::InvalidArnException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Error::InvalidCiphertextException(inner) => inner.source(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Error::InvalidGrantIdException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidGrantTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::InvalidImportTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidKeyUsageException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Error::InvalidMarkerException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInternalException(inner) => inner.source(),
+            #[cfg(feature = "op_verify_mac")]
             Error::KmsInvalidMacException(inner) => inner.source(),
+            #[cfg(feature = "op_verify")]
             Error::KmsInvalidSignatureException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInvalidStateException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KeyUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Error::UnsupportedOperationException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyAlreadyInUseException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidResponseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriEndpointInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriUnreachableException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2999,53 +4771,469 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Self::AlreadyExistsException(e) => e.request_id(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::CloudHsmClusterInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterNotActiveException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CloudHsmClusterNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Self::CloudHsmClusterNotRelatedException(e) => e.request_id(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Self::CustomKeyStoreHasCmKsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreInvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CustomKeyStoreNameInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Self::DependencyTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DryRunOperationException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::ExpiredImportTokenException(e) => e.request_id(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Self::IncorrectKeyException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::IncorrectKeyMaterialException(e) => e.request_id(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::IncorrectTrustAnchorException(e) => e.request_id(),
+            #[cfg(feature = "op_create_alias")]
             Self::InvalidAliasNameException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Self::InvalidArnException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Self::InvalidCiphertextException(e) => e.request_id(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Self::InvalidGrantIdException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidGrantTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::InvalidImportTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidKeyUsageException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Self::InvalidMarkerException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInternalException(e) => e.request_id(),
+            #[cfg(feature = "op_verify_mac")]
             Self::KmsInvalidMacException(e) => e.request_id(),
+            #[cfg(feature = "op_verify")]
             Self::KmsInvalidSignatureException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInvalidStateException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KeyUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Self::MalformedPolicyDocumentException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Self::UnsupportedOperationException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyAlreadyInUseException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyIncorrectAuthenticationCredentialException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidResponseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriEndpointInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriUnreachableException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceNotFoundException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
```

### `src/lens.rs`

```diff
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) fn reflens_describe_custom_key_stores_output_output_next_marker(
     input: &crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aliases")]
 pub(crate) fn reflens_list_aliases_output_output_next_marker(
     input: &crate::operation::list_aliases::ListAliasesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_grants")]
 pub(crate) fn reflens_list_grants_output_output_next_marker(
     input: &crate::operation::list_grants::ListGrantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) fn reflens_list_key_policies_output_output_next_marker(
     input: &crate::operation::list_key_policies::ListKeyPoliciesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) fn reflens_list_key_rotations_output_output_next_marker(
     input: &crate::operation::list_key_rotations::ListKeyRotationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_keys")]
 pub(crate) fn reflens_list_keys_output_output_next_marker(
     input: &crate::operation::list_keys::ListKeysOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) fn reflens_list_resource_tags_output_output_next_marker(
     input: &crate::operation::list_resource_tags::ListResourceTagsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) fn reflens_list_retirable_grants_output_output_next_marker(
     input: &crate::operation::list_retirable_grants::ListRetirableGrantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) fn lens_describe_custom_key_stores_output_output_custom_key_stores(
     input: crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::CustomKeyStoresListEntry>> {
@@ -86,6 +95,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aliases")]
 pub(crate) fn lens_list_aliases_output_output_aliases(
     input: crate::operation::list_aliases::ListAliasesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AliasListEntry>> {
@@ -93,6 +103,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_grants")]
 pub(crate) fn lens_list_grants_output_output_grants(
     input: crate::operation::list_grants::ListGrantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::GrantListEntry>> {
@@ -100,6 +111,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) fn lens_list_key_policies_output_output_policy_names(
     input: crate::operation::list_key_policies::ListKeyPoliciesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -107,6 +119,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) fn lens_list_key_rotations_output_output_rotations(
     input: crate::operation::list_key_rotations::ListKeyRotationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::RotationsListEntry>> {
@@ -114,6 +127,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_keys")]
 pub(crate) fn lens_list_keys_output_output_keys(
     input: crate::operation::list_keys::ListKeysOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::KeyListEntry>> {
@@ -121,6 +135,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) fn lens_list_resource_tags_output_output_tags(
     input: crate::operation::list_resource_tags::ListResourceTagsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Tag>> {
@@ -128,6 +143,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) fn lens_list_retirable_grants_output_output_grants(
     input: crate::operation::list_retirable_grants::ListRetirableGrantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::GrantListEntry>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,164 +1,218 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_cancel_key_deletion")]
 /// Types for the `CancelKeyDeletion` operation.
 pub mod cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 /// Types for the `ConnectCustomKeyStore` operation.
 pub mod connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 /// Types for the `CreateAlias` operation.
 pub mod create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 /// Types for the `CreateCustomKeyStore` operation.
 pub mod create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 /// Types for the `CreateGrant` operation.
 pub mod create_grant;

+#[cfg(feature = "op_create_key")]
 /// Types for the `CreateKey` operation.
 pub mod create_key;

+#[cfg(feature = "op_decrypt")]
 /// Types for the `Decrypt` operation.
 pub mod decrypt;

+#[cfg(feature = "op_delete_alias")]
 /// Types for the `DeleteAlias` operation.
 pub mod delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 /// Types for the `DeleteCustomKeyStore` operation.
 pub mod delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 /// Types for the `DeleteImportedKeyMaterial` operation.
 pub mod delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 /// Types for the `DeriveSharedSecret` operation.
 pub mod derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 /// Types for the `DescribeCustomKeyStores` operation.
 pub mod describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 /// Types for the `DescribeKey` operation.
 pub mod describe_key;

+#[cfg(feature = "op_disable_key")]
 /// Types for the `DisableKey` operation.
 pub mod disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 /// Types for the `DisableKeyRotation` operation.
 pub mod disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 /// Types for the `DisconnectCustomKeyStore` operation.
 pub mod disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 /// Types for the `EnableKey` operation.
 pub mod enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 /// Types for the `EnableKeyRotation` operation.
 pub mod enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 /// Types for the `Encrypt` operation.
 pub mod encrypt;

+#[cfg(feature = "op_generate_data_key")]
 /// Types for the `GenerateDataKey` operation.
 pub mod generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 /// Types for the `GenerateDataKeyPair` operation.
 pub mod generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 /// Types for the `GenerateDataKeyPairWithoutPlaintext` operation.
 pub mod generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 /// Types for the `GenerateDataKeyWithoutPlaintext` operation.
 pub mod generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 /// Types for the `GenerateMac` operation.
 pub mod generate_mac;

+#[cfg(feature = "op_generate_random")]
 /// Types for the `GenerateRandom` operation.
 pub mod generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 /// Types for the `GetKeyLastUsage` operation.
 pub mod get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 /// Types for the `GetKeyPolicy` operation.
 pub mod get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 /// Types for the `GetKeyRotationStatus` operation.
 pub mod get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 /// Types for the `GetParametersForImport` operation.
 pub mod get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 /// Types for the `GetPublicKey` operation.
 pub mod get_public_key;

+#[cfg(feature = "op_import_key_material")]
 /// Types for the `ImportKeyMaterial` operation.
 pub mod import_key_material;

+#[cfg(feature = "op_list_aliases")]
 /// Types for the `ListAliases` operation.
 pub mod list_aliases;

+#[cfg(feature = "op_list_grants")]
 /// Types for the `ListGrants` operation.
 pub mod list_grants;

+#[cfg(feature = "op_list_key_policies")]
 /// Types for the `ListKeyPolicies` operation.
 pub mod list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 /// Types for the `ListKeyRotations` operation.
 pub mod list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 /// Types for the `ListKeys` operation.
 pub mod list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 /// Types for the `ListResourceTags` operation.
 pub mod list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 /// Types for the `ListRetirableGrants` operation.
 pub mod list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 /// Types for the `PutKeyPolicy` operation.
 pub mod put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 /// Types for the `ReEncrypt` operation.
 pub mod re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 /// Types for the `ReplicateKey` operation.
 pub mod replicate_key;

+#[cfg(feature = "op_retire_grant")]
 /// Types for the `RetireGrant` operation.
 pub mod retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 /// Types for the `RevokeGrant` operation.
 pub mod revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 /// Types for the `RotateKeyOnDemand` operation.
 pub mod rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 /// Types for the `ScheduleKeyDeletion` operation.
 pub mod schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 /// Types for the `Sign` operation.
 pub mod sign;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_alias")]
 /// Types for the `UpdateAlias` operation.
 pub mod update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 /// Types for the `UpdateCustomKeyStore` operation.
 pub mod update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 /// Types for the `UpdateKeyDescription` operation.
 pub mod update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 /// Types for the `UpdatePrimaryRegion` operation.
 pub mod update_primary_region;

+#[cfg(feature = "op_verify")]
 /// Types for the `Verify` operation.
 pub mod verify;

+#[cfg(feature = "op_verify_mac")]
 /// Types for the `VerifyMac` operation.
 pub mod verify_mac;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +73,62 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,114 +140,224 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_cancel_key_deletion")]
 pub(crate) mod shape_cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 pub(crate) mod shape_connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 pub(crate) mod shape_create_grant;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_create_key;

+#[cfg(feature = "op_decrypt")]
 pub(crate) mod shape_decrypt;

+#[cfg(feature = "op_delete_alias")]
 pub(crate) mod shape_delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 pub(crate) mod shape_delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 pub(crate) mod shape_derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 pub(crate) mod shape_describe_key;

+#[cfg(feature = "op_disable_key")]
 pub(crate) mod shape_disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 pub(crate) mod shape_disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 pub(crate) mod shape_disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 pub(crate) mod shape_enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 pub(crate) mod shape_enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 pub(crate) mod shape_encrypt;

+#[cfg(feature = "op_generate_data_key")]
 pub(crate) mod shape_generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 pub(crate) mod shape_generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 pub(crate) mod shape_generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 pub(crate) mod shape_generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 pub(crate) mod shape_generate_mac;

+#[cfg(feature = "op_generate_random")]
 pub(crate) mod shape_generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 pub(crate) mod shape_get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 pub(crate) mod shape_get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub(crate) mod shape_get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 pub(crate) mod shape_get_public_key;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_import_key_material;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_list_aliases;

+#[cfg(feature = "op_list_grants")]
 pub(crate) mod shape_list_grants;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) mod shape_list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) mod shape_list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 pub(crate) mod shape_put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 pub(crate) mod shape_re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 pub(crate) mod shape_replicate_key;

+#[cfg(feature = "op_retire_grant")]
 pub(crate) mod shape_retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 pub(crate) mod shape_revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 pub(crate) mod shape_schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 pub(crate) mod shape_sign;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_alias")]
 pub(crate) mod shape_update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 pub(crate) mod shape_update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 pub(crate) mod shape_update_primary_region;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_verify;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_verify_mac;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -144,264 +366,797 @@
     }
 }

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub(crate) mod shape_already_exists_exception;

+#[cfg(feature = "op_cancel_key_deletion")]
 pub(crate) mod shape_cancel_key_deletion_input;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_cloud_hsm_cluster_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_cloud_hsm_cluster_invalid_configuration_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_cloud_hsm_cluster_not_active_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_cloud_hsm_cluster_not_found_exception;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_cloud_hsm_cluster_not_related_exception;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_connect_custom_key_store")]
 pub(crate) mod shape_connect_custom_key_store_input;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_create_alias_input;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_create_custom_key_store_input;

+#[cfg(feature = "op_create_grant")]
 pub(crate) mod shape_create_grant_input;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_create_key_input;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_custom_key_store_has_cmks_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_custom_key_store_invalid_state_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_custom_key_store_name_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_custom_key_store_not_found_exception;

+#[cfg(feature = "op_decrypt")]
 pub(crate) mod shape_decrypt_input;

+#[cfg(feature = "op_delete_alias")]
 pub(crate) mod shape_delete_alias_input;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_delete_custom_key_store_input;

+#[cfg(feature = "op_delete_imported_key_material")]
 pub(crate) mod shape_delete_imported_key_material_input;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub(crate) mod shape_dependency_timeout_exception;

+#[cfg(feature = "op_derive_shared_secret")]
 pub(crate) mod shape_derive_shared_secret_input;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_describe_custom_key_stores_input;

+#[cfg(feature = "op_describe_key")]
 pub(crate) mod shape_describe_key_input;

+#[cfg(feature = "op_disable_key")]
 pub(crate) mod shape_disable_key_input;

+#[cfg(feature = "op_disable_key_rotation")]
 pub(crate) mod shape_disable_key_rotation_input;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_disabled_exception;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 pub(crate) mod shape_disconnect_custom_key_store_input;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_dry_run_operation_exception;

+#[cfg(feature = "op_enable_key")]
 pub(crate) mod shape_enable_key_input;

+#[cfg(feature = "op_enable_key_rotation")]
 pub(crate) mod shape_enable_key_rotation_input;

+#[cfg(feature = "op_encrypt")]
 pub(crate) mod shape_encrypt_input;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_expired_import_token_exception;

+#[cfg(feature = "op_generate_data_key")]
 pub(crate) mod shape_generate_data_key_input;

+#[cfg(feature = "op_generate_data_key_pair")]
 pub(crate) mod shape_generate_data_key_pair_input;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 pub(crate) mod shape_generate_data_key_pair_without_plaintext_input;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 pub(crate) mod shape_generate_data_key_without_plaintext_input;

+#[cfg(feature = "op_generate_mac")]
 pub(crate) mod shape_generate_mac_input;

+#[cfg(feature = "op_generate_random")]
 pub(crate) mod shape_generate_random_input;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_get_key_last_usage_input;

+#[cfg(feature = "op_get_key_policy")]
 pub(crate) mod shape_get_key_policy_input;

+#[cfg(feature = "op_get_key_rotation_status")]
 pub(crate) mod shape_get_key_rotation_status_input;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub(crate) mod shape_get_parameters_for_import_input;

+#[cfg(feature = "op_get_public_key")]
 pub(crate) mod shape_get_public_key_input;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_import_key_material_input;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub(crate) mod shape_incorrect_key_exception;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_incorrect_key_material_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_incorrect_trust_anchor_exception;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_invalid_alias_name_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub(crate) mod shape_invalid_arn_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub(crate) mod shape_invalid_ciphertext_exception;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub(crate) mod shape_invalid_grant_id_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_invalid_grant_token_exception;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_invalid_import_token_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_invalid_key_usage_exception;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_invalid_marker_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_key_unavailable_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_kms_internal_exception;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_kms_invalid_mac_exception;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_kms_invalid_signature_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_kms_invalid_state_exception;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_list_aliases_input;

+#[cfg(feature = "op_list_grants")]
 pub(crate) mod shape_list_grants_input;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_list_key_policies_input;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_list_key_rotations_input;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_list_keys_input;

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) mod shape_list_resource_tags_input;

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) mod shape_list_retirable_grants_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_malformed_policy_document_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_put_key_policy")]
 pub(crate) mod shape_put_key_policy_input;

+#[cfg(feature = "op_re_encrypt")]
 pub(crate) mod shape_re_encrypt_input;

+#[cfg(feature = "op_replicate_key")]
 pub(crate) mod shape_replicate_key_input;

+#[cfg(feature = "op_retire_grant")]
 pub(crate) mod shape_retire_grant_input;

+#[cfg(feature = "op_revoke_grant")]
 pub(crate) mod shape_revoke_grant_input;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_rotate_key_on_demand_input;

+#[cfg(feature = "op_schedule_key_deletion")]
 pub(crate) mod shape_schedule_key_deletion_input;

+#[cfg(feature = "op_sign")]
 pub(crate) mod shape_sign_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub(crate) mod shape_unsupported_operation_exception;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_alias")]
 pub(crate) mod shape_update_alias_input;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_update_custom_key_store_input;

+#[cfg(feature = "op_update_key_description")]
 pub(crate) mod shape_update_key_description_input;

+#[cfg(feature = "op_update_primary_region")]
 pub(crate) mod shape_update_primary_region_input;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_verify_input;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_verify_mac_input;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_already_in_use_exception;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_invalid_configuration_exception;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_not_found_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_incorrect_authentication_credential_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_invalid_response_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_endpoint_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_unreachable_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_not_found_exception;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_alias_list;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_custom_key_stores_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_encryption_algorithm_spec_list;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_grant_constraints;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_key_agreement_algorithm_spec_list;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_key_last_usage_data;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_key_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_key_metadata;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_policy_name_list;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub(crate) mod shape_recipient_info;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_rotations_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_signing_algorithm_spec_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(feature = "op_list_resource_tags", feature = "op_replicate_key"))]
 pub(crate) mod shape_tag_list;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_authentication_credential_type;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_alias_list_entry;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_custom_key_stores_list_entry;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_list_entry;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_key_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_mac_algorithm_spec_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_configuration;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_rotations_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_xks_key_configuration_type;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_operation_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_key;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_key_list;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_xks_proxy_configuration_type;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_encryption_context_type;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) fn key_metadata_correct_errors(
     mut builder: crate::types::builders::KeyMetadataBuilder,
 ) -> crate::types::builders::KeyMetadataBuilder {
@@ -8,6 +9,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,182 +1,452 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_describe_custom_key_stores"))]
 pub use crate::types::_custom_key_store_type::CustomKeyStoreType;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::_xks_proxy_authentication_credential_type::XksProxyAuthenticationCredentialType;

+#[cfg(any(
+    feature = "op_create_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::_xks_proxy_connectivity_type::XksProxyConnectivityType;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_constraints::GrantConstraints;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_usage_type::KeyUsageType;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_customer_master_key_spec::CustomerMasterKeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_spec::KeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_origin_type::OriginType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_metadata::KeyMetadata;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_describe_key",
+    feature = "op_encrypt",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_encryption_algorithm_spec::EncryptionAlgorithmSpec;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_recipient_info::RecipientInfo;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_agreement_algorithm_spec::KeyAgreementAlgorithmSpec;

+#[cfg(any(feature = "op_generate_data_key", feature = "op_generate_data_key_without_plaintext"))]
 pub use crate::types::_data_key_spec::DataKeySpec;

+#[cfg(any(
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext"
+))]
 pub use crate::types::_data_key_pair_spec::DataKeyPairSpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_generate_mac",
+    feature = "op_replicate_key",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::_mac_algorithm_spec::MacAlgorithmSpec;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_data::KeyLastUsageData;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub use crate::types::_algorithm_spec::AlgorithmSpec;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub use crate::types::_wrapping_key_spec::WrappingKeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_expiration_model_type::ExpirationModelType;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::_import_type::ImportType;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_include_key_material::IncludeKeyMaterial;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_replicate_key",
+    feature = "op_schedule_key_deletion"
+))]
 pub use crate::types::_key_state::KeyState;

+#[cfg(any(feature = "op_sign", feature = "op_verify"))]
 pub use crate::types::_message_type::MessageType;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key",
+    feature = "op_sign",
+    feature = "op_verify"
+))]
 pub use crate::types::_signing_algorithm_spec::SigningAlgorithmSpec;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_operation::GrantOperation;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_manager_type::KeyManagerType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_configuration::MultiRegionConfiguration;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_xks_key_configuration_type::XksKeyConfigurationType;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_key_encryption_mechanism::KeyEncryptionMechanism;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::_dry_run_modifier_type::DryRunModifierType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_custom_key_stores_list_entry::CustomKeyStoresListEntry;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_tracking_operation::KeyLastUsageTrackingOperation;

+#[cfg(feature = "op_list_aliases")]
 pub use crate::types::_alias_list_entry::AliasListEntry;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub use crate::types::_grant_list_entry::GrantListEntry;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotations_list_entry::RotationsListEntry;

+#[cfg(feature = "op_list_keys")]
 pub use crate::types::_key_list_entry::KeyListEntry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key_type::MultiRegionKeyType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key::MultiRegionKey;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_connection_state_type::ConnectionStateType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_connection_error_code_type::ConnectionErrorCodeType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_xks_proxy_configuration_type::XksProxyConfigurationType;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_import_state::ImportState;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_key_material_state::KeyMaterialState;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotation_type::RotationType;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod _algorithm_spec;

+#[cfg(feature = "op_list_aliases")]
 mod _alias_list_entry;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _connection_error_code_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _connection_state_type;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_describe_custom_key_stores"))]
 mod _custom_key_store_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _custom_key_stores_list_entry;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _customer_master_key_spec;

+#[cfg(any(
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext"
+))]
 mod _data_key_pair_spec;

+#[cfg(any(feature = "op_generate_data_key", feature = "op_generate_data_key_without_plaintext"))]
 mod _data_key_spec;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 mod _dry_run_modifier_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_describe_key",
+    feature = "op_encrypt",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key"
+))]
 mod _encryption_algorithm_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_replicate_key"
+))]
 mod _expiration_model_type;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 mod _grant_constraints;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 mod _grant_list_entry;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 mod _grant_operation;

+#[cfg(feature = "op_list_key_rotations")]
 mod _import_state;

+#[cfg(feature = "op_import_key_material")]
 mod _import_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _include_key_material;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_agreement_algorithm_spec;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 mod _key_encryption_mechanism;

+#[cfg(feature = "op_get_key_last_usage")]
 mod _key_last_usage_data;

+#[cfg(feature = "op_get_key_last_usage")]
 mod _key_last_usage_tracking_operation;

+#[cfg(feature = "op_list_keys")]
 mod _key_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _key_manager_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _key_material_state;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _key_metadata;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_replicate_key",
+    feature = "op_schedule_key_deletion"
+))]
 mod _key_state;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_usage_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_generate_mac",
+    feature = "op_replicate_key",
+    feature = "op_verify_mac"
+))]
 mod _mac_algorithm_spec;

+#[cfg(any(feature = "op_sign", feature = "op_verify"))]
 mod _message_type;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_configuration;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_key;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_key_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_replicate_key"
+))]
 mod _origin_type;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 mod _recipient_info;

+#[cfg(feature = "op_list_key_rotations")]
 mod _rotation_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _rotations_list_entry;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key",
+    feature = "op_sign",
+    feature = "op_verify"
+))]
 mod _signing_algorithm_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod _wrapping_key_spec;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _xks_key_configuration_type;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_authentication_credential_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _xks_proxy_configuration_type;

+#[cfg(any(
+    feature = "op_create_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_update_custom_key_store"
+))]
 mod _xks_proxy_connectivity_type;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,30 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::_xks_proxy_authentication_credential_type::XksProxyAuthenticationCredentialTypeBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_constraints::GrantConstraintsBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_metadata::KeyMetadataBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_recipient_info::RecipientInfoBuilder;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_data::KeyLastUsageDataBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_configuration::MultiRegionConfigurationBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_xks_key_configuration_type::XksKeyConfigurationTypeBuilder;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_custom_key_stores_list_entry::CustomKeyStoresListEntryBuilder;

+#[cfg(feature = "op_list_aliases")]
 pub use crate::types::_alias_list_entry::AliasListEntryBuilder;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub use crate::types::_grant_list_entry::GrantListEntryBuilder;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotations_list_entry::RotationsListEntryBuilder;

+#[cfg(feature = "op_list_keys")]
 pub use crate::types::_key_list_entry::KeyListEntryBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key::MultiRegionKeyBuilder;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_xks_proxy_configuration_type::XksProxyConfigurationTypeBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,194 +1,1026 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub use crate::types::error::_dependency_timeout_exception::DependencyTimeoutException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_invalid_arn_exception::InvalidArnException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_internal_exception::KmsInternalException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_invalid_configuration_exception::CloudHsmClusterInvalidConfigurationException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_not_active_exception::CloudHsmClusterNotActiveException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_invalid_state_exception::CustomKeyStoreInvalidStateException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_not_found_exception::CustomKeyStoreNotFoundException;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsException;

+#[cfg(feature = "op_create_alias")]
 pub use crate::types::error::_invalid_alias_name_exception::InvalidAliasNameException;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_in_use_exception::CloudHsmClusterInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_cloud_hsm_cluster_not_found_exception::CloudHsmClusterNotFoundException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_custom_key_store_name_in_use_exception::CustomKeyStoreNameInUseException;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_incorrect_trust_anchor_exception::IncorrectTrustAnchorException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_incorrect_authentication_credential_exception::XksProxyIncorrectAuthenticationCredentialException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_configuration_exception::XksProxyInvalidConfigurationException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_response_exception::XksProxyInvalidResponseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_endpoint_in_use_exception::XksProxyUriEndpointInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_in_use_exception::XksProxyUriInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_unreachable_exception::XksProxyUriUnreachableException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_in_use_exception::XksProxyVpcEndpointServiceInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_invalid_configuration_exception::XksProxyVpcEndpointServiceInvalidConfigurationException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_not_found_exception::XksProxyVpcEndpointServiceNotFoundException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_disabled_exception::DisabledException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_dry_run_operation_exception::DryRunOperationException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_grant_token_exception::InvalidGrantTokenException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_exception::TagException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_unsupported_operation_exception::UnsupportedOperationException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_already_in_use_exception::XksKeyAlreadyInUseException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_invalid_configuration_exception::XksKeyInvalidConfigurationException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_not_found_exception::XksKeyNotFoundException;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::error::_incorrect_key_exception::IncorrectKeyException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub use crate::types::error::_invalid_ciphertext_exception::InvalidCiphertextException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_key_usage_exception::InvalidKeyUsageException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_key_unavailable_exception::KeyUnavailableException;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub use crate::types::error::_custom_key_store_has_cmks_exception::CustomKeyStoreHasCmKsException;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::error::_invalid_marker_exception::InvalidMarkerException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_expired_import_token_exception::ExpiredImportTokenException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_incorrect_key_material_exception::IncorrectKeyMaterialException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_invalid_import_token_exception::InvalidImportTokenException;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub use crate::types::error::_invalid_grant_id_exception::InvalidGrantIdException;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(feature = "op_update_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_not_related_exception::CloudHsmClusterNotRelatedException;

+#[cfg(feature = "op_verify")]
 pub use crate::types::error::_kms_invalid_signature_exception::KmsInvalidSignatureException;

+#[cfg(feature = "op_verify_mac")]
 pub use crate::types::error::_kms_invalid_mac_exception::KmsInvalidMacException;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 mod _already_exists_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 mod _cloud_hsm_cluster_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 mod _cloud_hsm_cluster_invalid_configuration_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 mod _cloud_hsm_cluster_not_active_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _cloud_hsm_cluster_not_found_exception;

+#[cfg(feature = "op_update_custom_key_store")]
 mod _cloud_hsm_cluster_not_related_exception;

+#[cfg(feature = "op_rotate_key_on_demand")]
 mod _conflict_exception;

+#[cfg(feature = "op_delete_custom_key_store")]
 mod _custom_key_store_has_cmks_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 mod _custom_key_store_invalid_state_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _custom_key_store_name_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 mod _custom_key_store_not_found_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 mod _dependency_timeout_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _disabled_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _dry_run_operation_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _expired_import_token_exception;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 mod _incorrect_key_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _incorrect_key_material_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 mod _incorrect_trust_anchor_exception;

+#[cfg(feature = "op_create_alias")]
 mod _invalid_alias_name_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 mod _invalid_arn_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 mod _invalid_ciphertext_exception;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 mod _invalid_grant_id_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _invalid_grant_token_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _invalid_import_token_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _invalid_key_usage_exception;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 mod _invalid_marker_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _key_unavailable_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _kms_internal_exception;

+#[cfg(feature = "op_verify_mac")]
 mod _kms_invalid_mac_exception;

+#[cfg(feature = "op_verify")]
 mod _kms_invalid_signature_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _kms_invalid_state_exception;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 mod _malformed_policy_document_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _not_found_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 mod _unsupported_operation_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_already_in_use_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_invalid_configuration_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_not_found_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_incorrect_authentication_credential_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_invalid_response_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_endpoint_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_unreachable_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_not_found_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,96 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub use crate::types::error::_dependency_timeout_exception::DependencyTimeoutExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_invalid_arn_exception::InvalidArnExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_internal_exception::KmsInternalExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_invalid_configuration_exception::CloudHsmClusterInvalidConfigurationExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_not_active_exception::CloudHsmClusterNotActiveExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_invalid_state_exception::CustomKeyStoreInvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_not_found_exception::CustomKeyStoreNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_create_alias")]
 pub use crate::types::error::_invalid_alias_name_exception::InvalidAliasNameExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_in_use_exception::CloudHsmClusterInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_cloud_hsm_cluster_not_found_exception::CloudHsmClusterNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_custom_key_store_name_in_use_exception::CustomKeyStoreNameInUseExceptionBuilder;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_incorrect_trust_anchor_exception::IncorrectTrustAnchorExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_incorrect_authentication_credential_exception::XksProxyIncorrectAuthenticationCredentialExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_configuration_exception::XksProxyInvalidConfigurationExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_response_exception::XksProxyInvalidResponseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_endpoint_in_use_exception::XksProxyUriEndpointInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_in_use_exception::XksProxyUriInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_unreachable_exception::XksProxyUriUnreachableExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_in_use_exception::XksProxyVpcEndpointServiceInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_invalid_configuration_exception::XksProxyVpcEndpointServiceInvalidConfigurationExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_not_found_exception::XksProxyVpcEndpointServiceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_disabled_exception::DisabledExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_dry_run_operation_exception::DryRunOperationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_grant_token_exception::InvalidGrantTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_exception::TagExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_unsupported_operation_exception::UnsupportedOperationExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_already_in_use_exception::XksKeyAlreadyInUseExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_invalid_configuration_exception::XksKeyInvalidConfigurationExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_not_found_exception::XksKeyNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::error::_incorrect_key_exception::IncorrectKeyExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub use crate::types::error::_invalid_ciphertext_exception::InvalidCiphertextExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_key_usage_exception::InvalidKeyUsageExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_key_unavailable_exception::KeyUnavailableExceptionBuilder;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub use crate::types::error::_custom_key_store_has_cmks_exception::CustomKeyStoreHasCmKsExceptionBuilder;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::error::_invalid_marker_exception::InvalidMarkerExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_expired_import_token_exception::ExpiredImportTokenExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_incorrect_key_material_exception::IncorrectKeyMaterialExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_invalid_import_token_exception::InvalidImportTokenExceptionBuilder;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub use crate::types::error::_invalid_grant_id_exception::InvalidGrantIdExceptionBuilder;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(feature = "op_update_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_not_related_exception::CloudHsmClusterNotRelatedExceptionBuilder;

+#[cfg(feature = "op_verify")]
 pub use crate::types::error::_kms_invalid_signature_exception::KmsInvalidSignatureExceptionBuilder;

+#[cfg(feature = "op_verify_mac")]
 pub use crate::types::error::_kms_invalid_mac_exception::KmsInvalidMacExceptionBuilder;
```

## Unified diff

```diff
diff --git a/Cargo.toml b/Cargo.toml
--- a/Cargo.toml
+++ b/Cargo.toml
@@ -19,50 +19,39 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 version = "1.9.2"

 [dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 version = "1.3.0"

 [dependencies.aws-smithy-http]
-path = "../aws-smithy-http"
 version = "0.64.0"

 [dependencies.aws-smithy-json]
-path = "../aws-smithy-json"
 version = "0.63.0"

 [dependencies.aws-smithy-observability]
-path = "../aws-smithy-observability"
 version = "0.3.0"

 [dependencies.aws-smithy-runtime]
-path = "../aws-smithy-runtime"
 features = ["client"]
 version = "1.14.0"

 [dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["client", "http-1x"]
 version = "1.16.0"

 [dependencies.aws-smithy-schema]
-path = "../aws-smithy-schema"
 version = "0.2.0"

 [dependencies.aws-smithy-types]
-path = "../aws-smithy-types"
 features = ["http-body-1-x"]
 version = "1.6.3"

 [dependencies.aws-types]
-path = "../aws-types"
 version = "1.6.0"

 [dependencies.bytes]
@@ -84,45 +73,36 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["test-util"]
 version = "1.9.2"

 [dev-dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-smithy-http-client]
-path = "../aws-smithy-http-client"
 features = ["test-util", "wire-mock"]
 version = "1.4.0"

 [dev-dependencies.aws-smithy-protocol-test]
-path = "../aws-smithy-protocol-test"
 version = "0.64.0"

 [dev-dependencies.aws-smithy-runtime]
-path = "../aws-smithy-runtime"
 features = ["test-util"]
 version = "1.14.0"

 [dev-dependencies.aws-smithy-runtime-api]
-path = "../aws-smithy-runtime-api"
 features = ["test-util"]
 version = "1.16.0"

 [dev-dependencies.aws-smithy-types]
-path = "../aws-smithy-types"
 features = ["http-body-1-x", "test-util"]
 version = "1.6.3"

@@ -153,3 +133,57 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_cancel_key_deletion = []
+op_connect_custom_key_store = []
+op_create_alias = []
+op_create_custom_key_store = []
+op_create_grant = []
+op_create_key = []
+op_decrypt = []
+op_delete_alias = []
+op_delete_custom_key_store = []
+op_delete_imported_key_material = []
+op_derive_shared_secret = []
+op_describe_custom_key_stores = []
+op_describe_key = []
+op_disable_key = []
+op_disable_key_rotation = []
+op_disconnect_custom_key_store = []
+op_enable_key = []
+op_enable_key_rotation = []
+op_encrypt = []
+op_generate_data_key = []
+op_generate_data_key_pair = []
+op_generate_data_key_pair_without_plaintext = []
+op_generate_data_key_without_plaintext = []
+op_generate_mac = []
+op_generate_random = []
+op_get_key_last_usage = []
+op_get_key_policy = []
+op_get_key_rotation_status = []
+op_get_parameters_for_import = []
+op_get_public_key = []
+op_import_key_material = []
+op_list_aliases = []
+op_list_grants = []
+op_list_key_policies = []
+op_list_key_rotations = []
+op_list_keys = []
+op_list_resource_tags = []
+op_list_retirable_grants = []
+op_put_key_policy = []
+op_re_encrypt = []
+op_replicate_key = []
+op_retire_grant = []
+op_revoke_grant = []
+op_rotate_key_on_demand = []
+op_schedule_key_deletion = []
+op_sign = []
+op_tag_resource = []
+op_untag_resource = []
+op_update_alias = []
+op_update_custom_key_store = []
+op_update_key_description = []
+op_update_primary_region = []
+op_verify = []
+op_verify_mac = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,16 +136,22 @@
     }
 }

+#[cfg(feature = "op_cancel_key_deletion")]
 mod cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 mod connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 mod create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 mod create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 mod create_grant;

+#[cfg(feature = "op_create_key")]
 mod create_key;

 /// Operation customization and supporting types.
@@ -175,98 +181,146 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_decrypt")]
 mod decrypt;

+#[cfg(feature = "op_delete_alias")]
 mod delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 mod delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 mod delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 mod derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 mod describe_key;

+#[cfg(feature = "op_disable_key")]
 mod disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 mod disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 mod disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 mod enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 mod enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 mod encrypt;

+#[cfg(feature = "op_generate_data_key")]
 mod generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 mod generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 mod generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 mod generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 mod generate_mac;

+#[cfg(feature = "op_generate_random")]
 mod generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 mod get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 mod get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 mod get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 mod get_public_key;

+#[cfg(feature = "op_import_key_material")]
 mod import_key_material;

+#[cfg(feature = "op_list_aliases")]
 mod list_aliases;

+#[cfg(feature = "op_list_grants")]
 mod list_grants;

+#[cfg(feature = "op_list_key_policies")]
 mod list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 mod list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 mod list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 mod list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 mod list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 mod put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 mod re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 mod replicate_key;

+#[cfg(feature = "op_retire_grant")]
 mod retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 mod revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 mod rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 mod schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 mod sign;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_alias")]
 mod update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 mod update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 mod update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 mod update_primary_region;

+#[cfg(feature = "op_verify")]
 mod verify;

+#[cfg(feature = "op_verify_mac")]
 mod verify_mac;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,11 +3,19 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
     /// <p>The request was rejected because it attempted to create a resource that already exists.</p>
     AlreadyExistsException(crate::types::error::AlreadyExistsException),
+    #[cfg(feature = "op_create_custom_key_store")]
     /// <p>The request was rejected because the specified CloudHSM cluster is already associated with an CloudHSM key store in the account, or it shares a backup history with an CloudHSM key store in the account. Each CloudHSM key store in the account must be associated with a different CloudHSM cluster.</p>
     /// <p>CloudHSM clusters that share a backup history have the same cluster certificate. To view the cluster certificate of an CloudHSM cluster, use the <a href="https://docs.aws.amazon.com/cloudhsm/latest/APIReference/API_DescribeClusters.html">DescribeClusters</a> operation.</p>
     CloudHsmClusterInUseException(crate::types::error::CloudHsmClusterInUseException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because the associated CloudHSM cluster did not meet the configuration requirements for an CloudHSM key store.</p>
     /// <ul>
     /// <li>
@@ -20,18 +28,35 @@
     /// </ul>
     /// <p>For information about the requirements for an CloudHSM cluster that is associated with an CloudHSM key store, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/create-keystore.html#before-keystore">Assemble the Prerequisites</a> in the <i>Key Management Service Developer Guide</i>. For information about creating a private subnet for an CloudHSM cluster, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/create-subnets.html">Create a Private Subnet</a> in the <i>CloudHSM User Guide</i>. For information about cluster security groups, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/configure-sg.html">Configure a Default Security Group</a> in the <i> <i>CloudHSM User Guide</i> </i>.</p>
     CloudHsmClusterInvalidConfigurationException(crate::types::error::CloudHsmClusterInvalidConfigurationException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_custom_key_store",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because the CloudHSM cluster associated with the CloudHSM key store is not active. Initialize and activate the cluster and try the command again. For detailed instructions, see <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/getting-started.html">Getting Started</a> in the <i>CloudHSM User Guide</i>.</p>
     CloudHsmClusterNotActiveException(crate::types::error::CloudHsmClusterNotActiveException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because KMS cannot find the CloudHSM cluster with the specified cluster ID. Retry the request with a different cluster ID.</p>
     CloudHsmClusterNotFoundException(crate::types::error::CloudHsmClusterNotFoundException),
+    #[cfg(feature = "op_update_custom_key_store")]
     /// <p>The request was rejected because the specified CloudHSM cluster has a different cluster certificate than the original cluster. You cannot use the operation to specify an unrelated cluster for an CloudHSM key store.</p>
     /// <p>Specify an CloudHSM cluster that shares a backup history with the original cluster. This includes clusters that were created from a backup of the current cluster, and clusters that were created from the same backup that produced the current cluster.</p>
     /// <p>CloudHSM clusters that share a backup history have the same cluster certificate. To view the cluster certificate of an CloudHSM cluster, use the <a href="https://docs.aws.amazon.com/cloudhsm/latest/APIReference/API_DescribeClusters.html">DescribeClusters</a> operation.</p>
     CloudHsmClusterNotRelatedException(crate::types::error::CloudHsmClusterNotRelatedException),
+    #[cfg(feature = "op_rotate_key_on_demand")]
     /// <p>The request was rejected because an automatic rotation of this key is currently in progress or scheduled to begin within the next 20 minutes.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_delete_custom_key_store")]
     /// <p>The request was rejected because the custom key store contains KMS keys. After verifying that you do not need to use the KMS keys, use the <code>ScheduleKeyDeletion</code> operation to delete the KMS keys. After they are deleted, you can delete the custom key store.</p>
     CustomKeyStoreHasCmKsException(crate::types::error::CustomKeyStoreHasCmKsException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_delete_custom_key_store",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_generate_random",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because of the <code>ConnectionState</code> of the custom key store. To get the <code>ConnectionState</code> of a custom key store, use the <code>DescribeCustomKeyStores</code> operation.</p>
     /// <p>This exception is thrown under the following conditions:</p>
     /// <ul>
@@ -47,38 +72,205 @@
     /// <p>You requested the <code>GenerateRandom</code> operation in an CloudHSM key store that is not connected. This operation is valid only when the CloudHSM key store <code>ConnectionState</code> is <code>CONNECTED</code>.</p></li>
     /// </ul>
     CustomKeyStoreInvalidStateException(crate::types::error::CustomKeyStoreInvalidStateException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the specified custom key store name is already assigned to another custom key store in the account. Try again with a custom key store name that is unique in the account.</p>
     CustomKeyStoreNameInUseException(crate::types::error::CustomKeyStoreNameInUseException),
+    #[cfg(any(
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_key",
+        feature = "op_delete_custom_key_store",
+        feature = "op_describe_custom_key_stores",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_generate_random",
+        feature = "op_update_custom_key_store"
+    ))]
     /// <p>The request was rejected because KMS cannot find a custom key store with the specified key store name or ID.</p>
     CustomKeyStoreNotFoundException(crate::types::error::CustomKeyStoreNotFoundException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_random",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_keys",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_verify"
+    ))]
     /// <p>The system timed out while trying to fulfill the request. You can retry the request.</p>
     DependencyTimeoutException(crate::types::error::DependencyTimeoutException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_sign",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified KMS key is not enabled.</p>
     DisabledException(crate::types::error::DisabledException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the DryRun parameter was specified.</p>
     DryRunOperationException(crate::types::error::DryRunOperationException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the specified import token is expired. Use <code>GetParametersForImport</code> to get a new import token and public key, use the new public key to encrypt the key material, and then try the request again.</p>
     ExpiredImportTokenException(crate::types::error::ExpiredImportTokenException),
+    #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
     /// <p>The request was rejected because the specified KMS key cannot decrypt the data. The <code>KeyId</code> in a <code>Decrypt</code> request and the <code>SourceKeyId</code> in a <code>ReEncrypt</code> request must identify the same KMS key that was used to encrypt the ciphertext.</p>
     IncorrectKeyException(crate::types::error::IncorrectKeyException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the key material in the request is, expired, invalid, or does not meet expectations. For example, it is not the same key material that was previously imported or KMS expected new key material but the key material being imported is already associated with the KMS key.</p>
     IncorrectKeyMaterialException(crate::types::error::IncorrectKeyMaterialException),
+    #[cfg(feature = "op_create_custom_key_store")]
     /// <p>The request was rejected because the trust anchor certificate in the request to create an CloudHSM key store is not the trust anchor certificate for the specified CloudHSM cluster.</p>
     /// <p>When you <a href="https://docs.aws.amazon.com/cloudhsm/latest/userguide/initialize-cluster.html#sign-csr">initialize the CloudHSM cluster</a>, you create the trust anchor certificate and save it in the <code>customerCA.crt</code> file.</p>
     IncorrectTrustAnchorException(crate::types::error::IncorrectTrustAnchorException),
+    #[cfg(feature = "op_create_alias")]
     /// <p>The request was rejected because the specified alias name is not valid.</p>
     InvalidAliasNameException(crate::types::error::InvalidAliasNameException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_delete_imported_key_material",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region"
+    ))]
     /// <p>The request was rejected because a specified ARN, or an ARN in a key policy, is not valid.</p>
     InvalidArnException(crate::types::error::InvalidArnException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_import_key_material",
+        feature = "op_re_encrypt"
+    ))]
     /// <p>From the <code>Decrypt</code> or <code>ReEncrypt</code> operation, the request was rejected because the specified ciphertext, or additional authenticated data incorporated into the ciphertext, such as the encryption context, is corrupted, missing, or otherwise invalid.</p>
     /// <p>From the <code>ImportKeyMaterial</code> operation, the request was rejected because KMS could not decrypt the encrypted (wrapped) key material.</p>
     InvalidCiphertextException(crate::types::error::InvalidCiphertextException),
+    #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
     /// <p>The request was rejected because the specified <code>GrantId</code> is not valid.</p>
     InvalidGrantIdException(crate::types::error::InvalidGrantIdException),
+    #[cfg(any(
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_retire_grant",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified grant token is not valid.</p>
     InvalidGrantTokenException(crate::types::error::InvalidGrantTokenException),
+    #[cfg(feature = "op_import_key_material")]
     /// <p>The request was rejected because the provided import token is invalid or is associated with a different KMS key.</p>
     InvalidImportTokenException(crate::types::error::InvalidImportTokenException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected for one of the following reasons:</p>
     /// <ul>
     /// <li>
@@ -89,14 +281,123 @@
     /// <p>For encrypting, decrypting, re-encrypting, and generating data keys, the <code>KeyUsage</code> must be <code>ENCRYPT_DECRYPT</code>. For signing and verifying messages, the <code>KeyUsage</code> must be <code>SIGN_VERIFY</code>. For generating and verifying message authentication codes (MACs), the <code>KeyUsage</code> must be <code>GENERATE_VERIFY_MAC</code>. For deriving key agreement secrets, the <code>KeyUsage</code> must be <code>KEY_AGREEMENT</code>. To find the <code>KeyUsage</code> of a KMS key, use the <code>DescribeKey</code> operation.</p>
     /// <p>To find the encryption or signing algorithms supported for a particular KMS key, use the <code>DescribeKey</code> operation.</p>
     InvalidKeyUsageException(crate::types::error::InvalidKeyUsageException),
+    #[cfg(any(
+        feature = "op_describe_custom_key_stores",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_rotations",
+        feature = "op_list_keys",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants"
+    ))]
     /// <p>The request was rejected because the marker that specifies where pagination should next begin is not valid.</p>
     InvalidMarkerException(crate::types::error::InvalidMarkerException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_connect_custom_key_store",
+        feature = "op_create_alias",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_custom_key_store",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_custom_key_stores",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_disconnect_custom_key_store",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_generate_random",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_keys",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_custom_key_store",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because an internal exception occurred. The request can be retried.</p>
     KmsInternalException(crate::types::error::KmsInternalException),
+    #[cfg(feature = "op_verify_mac")]
     /// <p>The request was rejected because the HMAC verification failed. HMAC verification fails when the HMAC computed by using the specified message, HMAC KMS key, and MAC algorithm does not match the HMAC specified in the request.</p>
     KmsInvalidMacException(crate::types::error::KmsInvalidMacException),
+    #[cfg(feature = "op_verify")]
     /// <p>The request was rejected because the signature verification failed. Signature verification fails when it cannot confirm that signature was produced by signing the specified message with the specified KMS key and signing algorithm.</p>
     KmsInvalidSignatureException(crate::types::error::KmsInvalidSignatureException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the state of the specified resource is not valid for this request.</p>
     /// <p>This exceptions means one of the following:</p>
     /// <ul>
@@ -107,48 +408,163 @@
     /// <p>For cryptographic operations on KMS keys in custom key stores, this exception represents a general failure with many possible causes. To identify the cause, see the error message that accompanies the exception.</p></li>
     /// </ul>
     KmsInvalidStateException(crate::types::error::KmsInvalidStateException),
+    #[cfg(any(
+        feature = "op_decrypt",
+        feature = "op_derive_shared_secret",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_public_key",
+        feature = "op_re_encrypt",
+        feature = "op_sign",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified KMS key was not available. You can retry the request.</p>
     KeyUnavailableException(crate::types::error::KeyUnavailableException),
+    #[cfg(any(
+        feature = "op_create_alias",
+        feature = "op_create_custom_key_store",
+        feature = "op_create_grant",
+        feature = "op_create_key",
+        feature = "op_enable_key",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_tag_resource",
+        feature = "op_update_alias"
+    ))]
     /// <p>The request was rejected because a length constraint or quota was exceeded. For more information, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/limits.html">Quotas</a> in the <i>Key Management Service Developer Guide</i>.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key"
+    ))]
     /// <p>The request was rejected because the specified policy is not syntactically or semantically correct.</p>
     MalformedPolicyDocumentException(crate::types::error::MalformedPolicyDocumentException),
+    #[cfg(any(
+        feature = "op_cancel_key_deletion",
+        feature = "op_create_alias",
+        feature = "op_create_grant",
+        feature = "op_decrypt",
+        feature = "op_delete_alias",
+        feature = "op_delete_imported_key_material",
+        feature = "op_derive_shared_secret",
+        feature = "op_describe_key",
+        feature = "op_disable_key",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key",
+        feature = "op_enable_key_rotation",
+        feature = "op_encrypt",
+        feature = "op_generate_data_key",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_data_key_without_plaintext",
+        feature = "op_generate_mac",
+        feature = "op_get_key_last_usage",
+        feature = "op_get_key_policy",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_aliases",
+        feature = "op_list_grants",
+        feature = "op_list_key_policies",
+        feature = "op_list_key_rotations",
+        feature = "op_list_resource_tags",
+        feature = "op_list_retirable_grants",
+        feature = "op_put_key_policy",
+        feature = "op_re_encrypt",
+        feature = "op_replicate_key",
+        feature = "op_retire_grant",
+        feature = "op_revoke_grant",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_schedule_key_deletion",
+        feature = "op_sign",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_alias",
+        feature = "op_update_key_description",
+        feature = "op_update_primary_region",
+        feature = "op_verify",
+        feature = "op_verify_mac"
+    ))]
     /// <p>The request was rejected because the specified entity or resource could not be found.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_replicate_key",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>The request was rejected because one or more tags are not valid.</p>
     TagException(crate::types::error::TagException),
+    #[cfg(any(
+        feature = "op_create_key",
+        feature = "op_delete_imported_key_material",
+        feature = "op_disable_key_rotation",
+        feature = "op_enable_key_rotation",
+        feature = "op_generate_data_key_pair",
+        feature = "op_generate_data_key_pair_without_plaintext",
+        feature = "op_generate_random",
+        feature = "op_get_key_rotation_status",
+        feature = "op_get_parameters_for_import",
+        feature = "op_get_public_key",
+        feature = "op_import_key_material",
+        feature = "op_list_key_rotations",
+        feature = "op_put_key_policy",
+        feature = "op_replicate_key",
+        feature = "op_rotate_key_on_demand",
+        feature = "op_update_primary_region"
+    ))]
     /// <p>The request was rejected because a specified parameter is not supported or a specified resource is not valid for this operation.</p>
     UnsupportedOperationException(crate::types::error::UnsupportedOperationException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the (<code>XksKeyId</code>) is already associated with another KMS key in this external key store. Each KMS key in an external key store must be associated with a different external key.</p>
     XksKeyAlreadyInUseException(crate::types::error::XksKeyAlreadyInUseException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the external key specified by the <code>XksKeyId</code> parameter did not meet the configuration requirements for an external key store.</p>
     /// <p>The external key must be an AES-256 symmetric key that is enabled and performs encryption and decryption.</p>
     XksKeyInvalidConfigurationException(crate::types::error::XksKeyInvalidConfigurationException),
+    #[cfg(feature = "op_create_key")]
     /// <p>The request was rejected because the external key store proxy could not find the external key. This exception is thrown when the value of the <code>XksKeyId</code> parameter doesn't identify a key in the external key manager associated with the external key proxy.</p>
     /// <p>Verify that the <code>XksKeyId</code> represents an existing key in the external key manager. Use the key identifier that the external key store proxy uses to identify the key. For details, see the documentation provided with your external key store proxy or key manager.</p>
     XksKeyNotFoundException(crate::types::error::XksKeyNotFoundException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the proxy credentials failed to authenticate to the specified external key store proxy. The specified external key store proxy rejected a status request from KMS due to invalid credentials. This can indicate an error in the credentials or in the identification of the external key store proxy.</p>
     XksProxyIncorrectAuthenticationCredentialException(
         crate::types::error::XksProxyIncorrectAuthenticationCredentialException,
     ),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the external key store proxy is not configured correctly. To identify the cause, see the error message that accompanies the exception.</p>
     XksProxyInvalidConfigurationException(crate::types::error::XksProxyInvalidConfigurationException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p></p>
     /// <p>KMS cannot interpret the response it received from the external key store proxy. The problem might be a poorly constructed response, but it could also be a transient network issue. If you see this error repeatedly, report it to the proxy vendor.</p>
     XksProxyInvalidResponseException(crate::types::error::XksProxyInvalidResponseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the <code>XksProxyUriEndpoint</code> is already associated with another external key store in this Amazon Web Services Region. To identify the cause, see the error message that accompanies the exception.</p>
     XksProxyUriEndpointInUseException(crate::types::error::XksProxyUriEndpointInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the concatenation of the <code>XksProxyUriEndpoint</code> and <code>XksProxyUriPath</code> is already associated with another external key store in this Amazon Web Services Region. Each external key store in a Region must use a unique external key store proxy API address.</p>
     XksProxyUriInUseException(crate::types::error::XksProxyUriInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>KMS was unable to reach the specified <code>XksProxyUriPath</code>. The path must be reachable before you create the external key store or update its settings.</p>
     /// <p>This exception is also thrown when the external key store proxy response to a <code>GetHealthStatus</code> request indicates that all external key manager instances are unavailable.</p>
     XksProxyUriUnreachableException(crate::types::error::XksProxyUriUnreachableException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the specified Amazon VPC endpoint service is already associated with another external key store in this Amazon Web Services Region. Each external key store in a Region must use a different Amazon VPC endpoint service.</p>
     XksProxyVpcEndpointServiceInUseException(crate::types::error::XksProxyVpcEndpointServiceInUseException),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because the Amazon VPC endpoint service configuration does not fulfill the requirements for an external key store. To identify the cause, see the error message that accompanies the exception and <a href="https://docs.aws.amazon.com/kms/latest/developerguide/vpc-connectivity.html#xks-vpc-requirements">review the requirements</a> for Amazon VPC endpoint service connectivity for an external key store.</p>
     XksProxyVpcEndpointServiceInvalidConfigurationException(
         crate::types::error::XksProxyVpcEndpointServiceInvalidConfigurationException,
     ),
+    #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
     /// <p>The request was rejected because KMS could not find the specified VPC endpoint service. Use <code>DescribeCustomKeyStores</code> to verify the VPC endpoint service name for the external key store. Also, confirm that the <code>Allow principals</code> list for the VPC endpoint service includes the KMS service principal for the Region, such as <code>cks.kms.us-east-1.amazonaws.com</code>.</p>
     XksProxyVpcEndpointServiceNotFoundException(crate::types::error::XksProxyVpcEndpointServiceNotFoundException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -165,53 +581,469 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Error::AlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::CloudHsmClusterInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterNotActiveException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CloudHsmClusterNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_custom_key_store")]
             Error::CloudHsmClusterNotRelatedException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Error::CustomKeyStoreHasCmKsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CustomKeyStoreNameInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Error::DependencyTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DryRunOperationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::ExpiredImportTokenException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Error::IncorrectKeyException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::IncorrectKeyMaterialException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::IncorrectTrustAnchorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_alias")]
             Error::InvalidAliasNameException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Error::InvalidArnException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Error::InvalidCiphertextException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Error::InvalidGrantIdException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidGrantTokenException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_key_material")]
             Error::InvalidImportTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidKeyUsageException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Error::InvalidMarkerException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInternalException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify_mac")]
             Error::KmsInvalidMacException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify")]
             Error::KmsInvalidSignatureException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KeyUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Error::UnsupportedOperationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyAlreadyInUseException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidResponseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriEndpointInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriUnreachableException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInUseException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -236,58 +1068,475 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Self::AlreadyExistsException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::CloudHsmClusterInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterNotActiveException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CloudHsmClusterNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Self::CloudHsmClusterNotRelatedException(inner) => inner.meta(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Self::CustomKeyStoreHasCmKsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CustomKeyStoreNameInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Self::DependencyTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DryRunOperationException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::ExpiredImportTokenException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Self::IncorrectKeyException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::IncorrectKeyMaterialException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::IncorrectTrustAnchorException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_alias")]
             Self::InvalidAliasNameException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Self::InvalidArnException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Self::InvalidCiphertextException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Self::InvalidGrantIdException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidGrantTokenException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_key_material")]
             Self::InvalidImportTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidKeyUsageException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Self::InvalidMarkerException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInternalException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify_mac")]
             Self::KmsInvalidMacException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify")]
             Self::KmsInvalidSignatureException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KeyUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Self::MalformedPolicyDocumentException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Self::UnsupportedOperationException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyAlreadyInUseException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidResponseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriEndpointInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriUnreachableException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInUseException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_cancel_key_deletion")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -313,6 +1562,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_key_deletion")]
 impl From<crate::operation::cancel_key_deletion::CancelKeyDeletionError> for Error {
     fn from(err: crate::operation::cancel_key_deletion::CancelKeyDeletionError) -> Self {
         match err {
@@ -335,6 +1585,7 @@
         }
     }
 }
+#[cfg(feature = "op_connect_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -360,6 +1611,7 @@
         }
     }
 }
+#[cfg(feature = "op_connect_custom_key_store")]
 impl From<crate::operation::connect_custom_key_store::ConnectCustomKeyStoreError> for Error {
     fn from(err: crate::operation::connect_custom_key_store::ConnectCustomKeyStoreError) -> Self {
         match err {
@@ -380,6 +1632,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_alias::CreateAliasError, R>>
     for Error
 where
@@ -397,6 +1650,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_alias")]
 impl From<crate::operation::create_alias::CreateAliasError> for Error {
     fn from(err: crate::operation::create_alias::CreateAliasError) -> Self {
         match err {
@@ -425,6 +1679,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -450,6 +1705,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_key_store")]
 impl From<crate::operation::create_custom_key_store::CreateCustomKeyStoreError> for Error {
     fn from(err: crate::operation::create_custom_key_store::CreateCustomKeyStoreError) -> Self {
         match err {
@@ -506,6 +1762,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_grant::CreateGrantError, R>>
     for Error
 where
@@ -523,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_grant")]
 impl From<crate::operation::create_grant::CreateGrantError> for Error {
     fn from(err: crate::operation::create_grant::CreateGrantError) -> Self {
         match err {
@@ -557,6 +1815,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_key::CreateKeyError, R>>
     for Error
 where
@@ -574,6 +1833,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_key")]
 impl From<crate::operation::create_key::CreateKeyError> for Error {
     fn from(err: crate::operation::create_key::CreateKeyError) -> Self {
         match err {
@@ -618,6 +1878,7 @@
         }
     }
 }
+#[cfg(feature = "op_decrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::decrypt::DecryptError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -634,6 +1895,7 @@
         }
     }
 }
+#[cfg(feature = "op_decrypt")]
 impl From<crate::operation::decrypt::DecryptError> for Error {
     fn from(err: crate::operation::decrypt::DecryptError) -> Self {
         match err {
@@ -668,6 +1930,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_alias::DeleteAliasError, R>>
     for Error
 where
@@ -685,6 +1948,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_alias")]
 impl From<crate::operation::delete_alias::DeleteAliasError> for Error {
     fn from(err: crate::operation::delete_alias::DeleteAliasError) -> Self {
         match err {
@@ -704,6 +1968,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -729,6 +1994,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_key_store")]
 impl From<crate::operation::delete_custom_key_store::DeleteCustomKeyStoreError> for Error {
     fn from(err: crate::operation::delete_custom_key_store::DeleteCustomKeyStoreError) -> Self {
         match err {
@@ -746,6 +2012,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_imported_key_material")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -771,6 +2038,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_imported_key_material")]
 impl From<crate::operation::delete_imported_key_material::DeleteImportedKeyMaterialError> for Error {
     fn from(err: crate::operation::delete_imported_key_material::DeleteImportedKeyMaterialError) -> Self {
         match err {
@@ -796,6 +2064,7 @@
         }
     }
 }
+#[cfg(feature = "op_derive_shared_secret")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -821,6 +2090,7 @@
         }
     }
 }
+#[cfg(feature = "op_derive_shared_secret")]
 impl From<crate::operation::derive_shared_secret::DeriveSharedSecretError> for Error {
     fn from(err: crate::operation::derive_shared_secret::DeriveSharedSecretError) -> Self {
         match err {
@@ -857,6 +2127,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_custom_key_stores")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -882,6 +2153,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_custom_key_stores")]
 impl From<crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresError> for Error {
     fn from(err: crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresError) -> Self {
         match err {
@@ -898,6 +2170,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_key::DescribeKeyError, R>>
     for Error
 where
@@ -915,6 +2188,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_key")]
 impl From<crate::operation::describe_key::DescribeKeyError> for Error {
     fn from(err: crate::operation::describe_key::DescribeKeyError) -> Self {
         match err {
@@ -934,6 +2208,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::disable_key::DisableKeyError, R>>
     for Error
 where
@@ -951,6 +2226,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key")]
 impl From<crate::operation::disable_key::DisableKeyError> for Error {
     fn from(err: crate::operation::disable_key::DisableKeyError) -> Self {
         match err {
@@ -971,6 +2247,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key_rotation")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -996,6 +2273,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_key_rotation")]
 impl From<crate::operation::disable_key_rotation::DisableKeyRotationError> for Error {
     fn from(err: crate::operation::disable_key_rotation::DisableKeyRotationError) -> Self {
         match err {
@@ -1026,6 +2304,7 @@
         }
     }
 }
+#[cfg(feature = "op_disconnect_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1051,6 +2330,7 @@
         }
     }
 }
+#[cfg(feature = "op_disconnect_custom_key_store")]
 impl From<crate::operation::disconnect_custom_key_store::DisconnectCustomKeyStoreError> for Error {
     fn from(err: crate::operation::disconnect_custom_key_store::DisconnectCustomKeyStoreError) -> Self {
         match err {
@@ -1067,6 +2347,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::enable_key::EnableKeyError, R>>
     for Error
 where
@@ -1084,6 +2365,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key")]
 impl From<crate::operation::enable_key::EnableKeyError> for Error {
     fn from(err: crate::operation::enable_key::EnableKeyError) -> Self {
         match err {
@@ -1107,6 +2389,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key_rotation")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1132,6 +2415,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_key_rotation")]
 impl From<crate::operation::enable_key_rotation::EnableKeyRotationError> for Error {
     fn from(err: crate::operation::enable_key_rotation::EnableKeyRotationError) -> Self {
         match err {
@@ -1160,6 +2444,7 @@
         }
     }
 }
+#[cfg(feature = "op_encrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::encrypt::EncryptError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1176,6 +2461,7 @@
         }
     }
 }
+#[cfg(feature = "op_encrypt")]
 impl From<crate::operation::encrypt::EncryptError> for Error {
     fn from(err: crate::operation::encrypt::EncryptError) -> Self {
         match err {
@@ -1204,6 +2490,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1229,6 +2516,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key")]
 impl From<crate::operation::generate_data_key::GenerateDataKeyError> for Error {
     fn from(err: crate::operation::generate_data_key::GenerateDataKeyError) -> Self {
         match err {
@@ -1263,6 +2551,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1288,6 +2577,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair")]
 impl From<crate::operation::generate_data_key_pair::GenerateDataKeyPairError> for Error {
     fn from(err: crate::operation::generate_data_key_pair::GenerateDataKeyPairError) -> Self {
         match err {
@@ -1327,6 +2617,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1352,6 +2643,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 impl From<crate::operation::generate_data_key_pair_without_plaintext::GenerateDataKeyPairWithoutPlaintextError>
     for Error
 {
@@ -1395,6 +2687,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1420,6 +2713,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 impl From<crate::operation::generate_data_key_without_plaintext::GenerateDataKeyWithoutPlaintextError> for Error {
     fn from(err: crate::operation::generate_data_key_without_plaintext::GenerateDataKeyWithoutPlaintextError) -> Self {
         match err {
@@ -1454,6 +2748,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_mac")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::generate_mac::GenerateMacError, R>>
     for Error
 where
@@ -1471,6 +2766,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_mac")]
 impl From<crate::operation::generate_mac::GenerateMacError> for Error {
     fn from(err: crate::operation::generate_mac::GenerateMacError) -> Self {
         match err {
@@ -1502,6 +2798,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_random")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::generate_random::GenerateRandomError, R>>
     for Error
@@ -1523,6 +2820,7 @@
         }
     }
 }
+#[cfg(feature = "op_generate_random")]
 impl From<crate::operation::generate_random::GenerateRandomError> for Error {
     fn from(err: crate::operation::generate_random::GenerateRandomError) -> Self {
         match err {
@@ -1545,6 +2843,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_last_usage")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1570,6 +2869,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_last_usage")]
 impl From<crate::operation::get_key_last_usage::GetKeyLastUsageError> for Error {
     fn from(err: crate::operation::get_key_last_usage::GetKeyLastUsageError) -> Self {
         match err {
@@ -1589,6 +2889,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_policy")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_key_policy::GetKeyPolicyError, R>>
     for Error
 where
@@ -1606,6 +2907,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_policy")]
 impl From<crate::operation::get_key_policy::GetKeyPolicyError> for Error {
     fn from(err: crate::operation::get_key_policy::GetKeyPolicyError) -> Self {
         match err {
@@ -1628,6 +2930,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_rotation_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1653,6 +2956,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_key_rotation_status")]
 impl From<crate::operation::get_key_rotation_status::GetKeyRotationStatusError> for Error {
     fn from(err: crate::operation::get_key_rotation_status::GetKeyRotationStatusError) -> Self {
         match err {
@@ -1680,6 +2984,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_parameters_for_import")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1705,6 +3010,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_parameters_for_import")]
 impl From<crate::operation::get_parameters_for_import::GetParametersForImportError> for Error {
     fn from(err: crate::operation::get_parameters_for_import::GetParametersForImportError) -> Self {
         match err {
@@ -1732,6 +3038,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_public_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_public_key::GetPublicKeyError, R>>
     for Error
 where
@@ -1749,6 +3056,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_public_key")]
 impl From<crate::operation::get_public_key::GetPublicKeyError> for Error {
     fn from(err: crate::operation::get_public_key::GetPublicKeyError) -> Self {
         match err {
@@ -1786,6 +3094,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_key_material")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1811,6 +3120,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_key_material")]
 impl From<crate::operation::import_key_material::ImportKeyMaterialError> for Error {
     fn from(err: crate::operation::import_key_material::ImportKeyMaterialError) -> Self {
         match err {
@@ -1848,6 +3158,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aliases")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_aliases::ListAliasesError, R>>
     for Error
 where
@@ -1865,6 +3176,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aliases")]
 impl From<crate::operation::list_aliases::ListAliasesError> for Error {
     fn from(err: crate::operation::list_aliases::ListAliasesError) -> Self {
         match err {
@@ -1887,6 +3199,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_grants")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_grants::ListGrantsError, R>>
     for Error
 where
@@ -1904,6 +3217,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_grants")]
 impl From<crate::operation::list_grants::ListGrantsError> for Error {
     fn from(err: crate::operation::list_grants::ListGrantsError) -> Self {
         match err {
@@ -1930,6 +3244,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1955,6 +3270,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_policies")]
 impl From<crate::operation::list_key_policies::ListKeyPoliciesError> for Error {
     fn from(err: crate::operation::list_key_policies::ListKeyPoliciesError) -> Self {
         match err {
@@ -1977,6 +3293,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_rotations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2002,6 +3319,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_key_rotations")]
 impl From<crate::operation::list_key_rotations::ListKeyRotationsError> for Error {
     fn from(err: crate::operation::list_key_rotations::ListKeyRotationsError) -> Self {
         match err {
@@ -2027,6 +3345,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_keys")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_keys::ListKeysError, R>>
     for Error
 where
@@ -2044,6 +3363,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_keys")]
 impl From<crate::operation::list_keys::ListKeysError> for Error {
     fn from(err: crate::operation::list_keys::ListKeysError) -> Self {
         match err {
@@ -2060,6 +3380,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tags")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2085,6 +3406,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tags")]
 impl From<crate::operation::list_resource_tags::ListResourceTagsError> for Error {
     fn from(err: crate::operation::list_resource_tags::ListResourceTagsError) -> Self {
         match err {
@@ -2104,6 +3426,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_retirable_grants")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2129,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_retirable_grants")]
 impl From<crate::operation::list_retirable_grants::ListRetirableGrantsError> for Error {
     fn from(err: crate::operation::list_retirable_grants::ListRetirableGrantsError) -> Self {
         match err {
@@ -2153,6 +3477,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_key_policy")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_key_policy::PutKeyPolicyError, R>>
     for Error
 where
@@ -2170,6 +3495,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_key_policy")]
 impl From<crate::operation::put_key_policy::PutKeyPolicyError> for Error {
     fn from(err: crate::operation::put_key_policy::PutKeyPolicyError) -> Self {
         match err {
@@ -2201,6 +3527,7 @@
         }
     }
 }
+#[cfg(feature = "op_re_encrypt")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::re_encrypt::ReEncryptError, R>>
     for Error
 where
@@ -2218,6 +3545,7 @@
         }
     }
 }
+#[cfg(feature = "op_re_encrypt")]
 impl From<crate::operation::re_encrypt::ReEncryptError> for Error {
     fn from(err: crate::operation::re_encrypt::ReEncryptError) -> Self {
         match err {
@@ -2254,6 +3582,7 @@
         }
     }
 }
+#[cfg(feature = "op_replicate_key")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::replicate_key::ReplicateKeyError, R>>
     for Error
 where
@@ -2271,6 +3600,7 @@
         }
     }
 }
+#[cfg(feature = "op_replicate_key")]
 impl From<crate::operation::replicate_key::ReplicateKeyError> for Error {
     fn from(err: crate::operation::replicate_key::ReplicateKeyError) -> Self {
         match err {
@@ -2306,6 +3636,7 @@
         }
     }
 }
+#[cfg(feature = "op_retire_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::retire_grant::RetireGrantError, R>>
     for Error
 where
@@ -2323,6 +3654,7 @@
         }
     }
 }
+#[cfg(feature = "op_retire_grant")]
 impl From<crate::operation::retire_grant::RetireGrantError> for Error {
     fn from(err: crate::operation::retire_grant::RetireGrantError) -> Self {
         match err {
@@ -2354,6 +3686,7 @@
         }
     }
 }
+#[cfg(feature = "op_revoke_grant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::revoke_grant::RevokeGrantError, R>>
     for Error
 where
@@ -2371,6 +3704,7 @@
         }
     }
 }
+#[cfg(feature = "op_revoke_grant")]
 impl From<crate::operation::revoke_grant::RevokeGrantError> for Error {
     fn from(err: crate::operation::revoke_grant::RevokeGrantError) -> Self {
         match err {
@@ -2399,6 +3733,7 @@
         }
     }
 }
+#[cfg(feature = "op_rotate_key_on_demand")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2424,6 +3759,7 @@
         }
     }
 }
+#[cfg(feature = "op_rotate_key_on_demand")]
 impl From<crate::operation::rotate_key_on_demand::RotateKeyOnDemandError> for Error {
     fn from(err: crate::operation::rotate_key_on_demand::RotateKeyOnDemandError) -> Self {
         match err {
@@ -2458,6 +3794,7 @@
         }
     }
 }
+#[cfg(feature = "op_schedule_key_deletion")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2483,6 +3820,7 @@
         }
     }
 }
+#[cfg(feature = "op_schedule_key_deletion")]
 impl From<crate::operation::schedule_key_deletion::ScheduleKeyDeletionError> for Error {
     fn from(err: crate::operation::schedule_key_deletion::ScheduleKeyDeletionError) -> Self {
         match err {
@@ -2507,6 +3845,7 @@
         }
     }
 }
+#[cfg(feature = "op_sign")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::sign::SignError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2521,6 +3860,7 @@
         }
     }
 }
+#[cfg(feature = "op_sign")]
 impl From<crate::operation::sign::SignError> for Error {
     fn from(err: crate::operation::sign::SignError) -> Self {
         match err {
@@ -2547,6 +3887,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -2564,6 +3905,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -2587,6 +3929,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2608,6 +3951,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2628,6 +3972,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_alias")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_alias::UpdateAliasError, R>>
     for Error
 where
@@ -2645,6 +3990,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_alias")]
 impl From<crate::operation::update_alias::UpdateAliasError> for Error {
     fn from(err: crate::operation::update_alias::UpdateAliasError) -> Self {
         match err {
@@ -2667,6 +4013,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_key_store")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2692,6 +4039,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_key_store")]
 impl From<crate::operation::update_custom_key_store::UpdateCustomKeyStoreError> for Error {
     fn from(err: crate::operation::update_custom_key_store::UpdateCustomKeyStoreError) -> Self {
         match err {
@@ -2748,6 +4096,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_key_description")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2773,6 +4122,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_key_description")]
 impl From<crate::operation::update_key_description::UpdateKeyDescriptionError> for Error {
     fn from(err: crate::operation::update_key_description::UpdateKeyDescriptionError) -> Self {
         match err {
@@ -2797,6 +4147,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_primary_region")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2822,6 +4173,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_primary_region")]
 impl From<crate::operation::update_primary_region::UpdatePrimaryRegionError> for Error {
     fn from(err: crate::operation::update_primary_region::UpdatePrimaryRegionError) -> Self {
         match err {
@@ -2849,6 +4201,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::verify::VerifyError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2863,6 +4216,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify")]
 impl From<crate::operation::verify::VerifyError> for Error {
     fn from(err: crate::operation::verify::VerifyError) -> Self {
         match err {
@@ -2894,6 +4248,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_mac")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::verify_mac::VerifyMacError, R>>
     for Error
 where
@@ -2911,6 +4266,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_mac")]
 impl From<crate::operation::verify_mac::VerifyMacError> for Error {
     fn from(err: crate::operation::verify_mac::VerifyMacError) -> Self {
         match err {
@@ -2944,53 +4300,469 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Error::AlreadyExistsException(inner) => inner.source(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::CloudHsmClusterInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CloudHsmClusterNotActiveException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CloudHsmClusterNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Error::CloudHsmClusterNotRelatedException(inner) => inner.source(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Error::CustomKeyStoreHasCmKsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreInvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::CustomKeyStoreNameInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Error::CustomKeyStoreNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Error::DependencyTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::DryRunOperationException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::ExpiredImportTokenException(inner) => inner.source(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Error::IncorrectKeyException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::IncorrectKeyMaterialException(inner) => inner.source(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Error::IncorrectTrustAnchorException(inner) => inner.source(),
+            #[cfg(feature = "op_create_alias")]
             Error::InvalidAliasNameException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Error::InvalidArnException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Error::InvalidCiphertextException(inner) => inner.source(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Error::InvalidGrantIdException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidGrantTokenException(inner) => inner.source(),
+            #[cfg(feature = "op_import_key_material")]
             Error::InvalidImportTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::InvalidKeyUsageException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Error::InvalidMarkerException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInternalException(inner) => inner.source(),
+            #[cfg(feature = "op_verify_mac")]
             Error::KmsInvalidMacException(inner) => inner.source(),
+            #[cfg(feature = "op_verify")]
             Error::KmsInvalidSignatureException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KmsInvalidStateException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::KeyUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Error::MalformedPolicyDocumentException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Error::UnsupportedOperationException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyAlreadyInUseException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(feature = "op_create_key")]
             Error::XksKeyNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyIncorrectAuthenticationCredentialException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyInvalidResponseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriEndpointInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyUriUnreachableException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInUseException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceInvalidConfigurationException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Error::XksProxyVpcEndpointServiceNotFoundException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2999,53 +4771,469 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
             Self::AlreadyExistsException(e) => e.request_id(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::CloudHsmClusterInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_custom_key_store",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CloudHsmClusterNotActiveException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CloudHsmClusterNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_update_custom_key_store")]
             Self::CloudHsmClusterNotRelatedException(e) => e.request_id(),
+            #[cfg(feature = "op_rotate_key_on_demand")]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_delete_custom_key_store")]
             Self::CustomKeyStoreHasCmKsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreInvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::CustomKeyStoreNameInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_key",
+                feature = "op_delete_custom_key_store",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_generate_random",
+                feature = "op_update_custom_key_store"
+            ))]
             Self::CustomKeyStoreNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_keys",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_verify"
+            ))]
             Self::DependencyTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_sign",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::DryRunOperationException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::ExpiredImportTokenException(e) => e.request_id(),
+            #[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
             Self::IncorrectKeyException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::IncorrectKeyMaterialException(e) => e.request_id(),
+            #[cfg(feature = "op_create_custom_key_store")]
             Self::IncorrectTrustAnchorException(e) => e.request_id(),
+            #[cfg(feature = "op_create_alias")]
             Self::InvalidAliasNameException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region"
+            ))]
             Self::InvalidArnException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_import_key_material",
+                feature = "op_re_encrypt"
+            ))]
             Self::InvalidCiphertextException(e) => e.request_id(),
+            #[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
             Self::InvalidGrantIdException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_retire_grant",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidGrantTokenException(e) => e.request_id(),
+            #[cfg(feature = "op_import_key_material")]
             Self::InvalidImportTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::InvalidKeyUsageException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_describe_custom_key_stores",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants"
+            ))]
             Self::InvalidMarkerException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_connect_custom_key_store",
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_custom_key_store",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_custom_key_stores",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_disconnect_custom_key_store",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_generate_random",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_keys",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_custom_key_store",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInternalException(e) => e.request_id(),
+            #[cfg(feature = "op_verify_mac")]
             Self::KmsInvalidMacException(e) => e.request_id(),
+            #[cfg(feature = "op_verify")]
             Self::KmsInvalidSignatureException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KmsInvalidStateException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_decrypt",
+                feature = "op_derive_shared_secret",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_public_key",
+                feature = "op_re_encrypt",
+                feature = "op_sign",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::KeyUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_alias",
+                feature = "op_create_custom_key_store",
+                feature = "op_create_grant",
+                feature = "op_create_key",
+                feature = "op_enable_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_tag_resource",
+                feature = "op_update_alias"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key"
+            ))]
             Self::MalformedPolicyDocumentException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_key_deletion",
+                feature = "op_create_alias",
+                feature = "op_create_grant",
+                feature = "op_decrypt",
+                feature = "op_delete_alias",
+                feature = "op_delete_imported_key_material",
+                feature = "op_derive_shared_secret",
+                feature = "op_describe_key",
+                feature = "op_disable_key",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key",
+                feature = "op_enable_key_rotation",
+                feature = "op_encrypt",
+                feature = "op_generate_data_key",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_data_key_without_plaintext",
+                feature = "op_generate_mac",
+                feature = "op_get_key_last_usage",
+                feature = "op_get_key_policy",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_aliases",
+                feature = "op_list_grants",
+                feature = "op_list_key_policies",
+                feature = "op_list_key_rotations",
+                feature = "op_list_resource_tags",
+                feature = "op_list_retirable_grants",
+                feature = "op_put_key_policy",
+                feature = "op_re_encrypt",
+                feature = "op_replicate_key",
+                feature = "op_retire_grant",
+                feature = "op_revoke_grant",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_schedule_key_deletion",
+                feature = "op_sign",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_alias",
+                feature = "op_update_key_description",
+                feature = "op_update_primary_region",
+                feature = "op_verify",
+                feature = "op_verify_mac"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_replicate_key",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_key",
+                feature = "op_delete_imported_key_material",
+                feature = "op_disable_key_rotation",
+                feature = "op_enable_key_rotation",
+                feature = "op_generate_data_key_pair",
+                feature = "op_generate_data_key_pair_without_plaintext",
+                feature = "op_generate_random",
+                feature = "op_get_key_rotation_status",
+                feature = "op_get_parameters_for_import",
+                feature = "op_get_public_key",
+                feature = "op_import_key_material",
+                feature = "op_list_key_rotations",
+                feature = "op_put_key_policy",
+                feature = "op_replicate_key",
+                feature = "op_rotate_key_on_demand",
+                feature = "op_update_primary_region"
+            ))]
             Self::UnsupportedOperationException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyAlreadyInUseException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(feature = "op_create_key")]
             Self::XksKeyNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyIncorrectAuthenticationCredentialException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyInvalidResponseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriEndpointInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyUriUnreachableException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInUseException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceInvalidConfigurationException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
             Self::XksProxyVpcEndpointServiceNotFoundException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) fn reflens_describe_custom_key_stores_output_output_next_marker(
     input: &crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aliases")]
 pub(crate) fn reflens_list_aliases_output_output_next_marker(
     input: &crate::operation::list_aliases::ListAliasesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_grants")]
 pub(crate) fn reflens_list_grants_output_output_next_marker(
     input: &crate::operation::list_grants::ListGrantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) fn reflens_list_key_policies_output_output_next_marker(
     input: &crate::operation::list_key_policies::ListKeyPoliciesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) fn reflens_list_key_rotations_output_output_next_marker(
     input: &crate::operation::list_key_rotations::ListKeyRotationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_keys")]
 pub(crate) fn reflens_list_keys_output_output_next_marker(
     input: &crate::operation::list_keys::ListKeysOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) fn reflens_list_resource_tags_output_output_next_marker(
     input: &crate::operation::list_resource_tags::ListResourceTagsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) fn reflens_list_retirable_grants_output_output_next_marker(
     input: &crate::operation::list_retirable_grants::ListRetirableGrantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) fn lens_describe_custom_key_stores_output_output_custom_key_stores(
     input: crate::operation::describe_custom_key_stores::DescribeCustomKeyStoresOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::CustomKeyStoresListEntry>> {
@@ -86,6 +95,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aliases")]
 pub(crate) fn lens_list_aliases_output_output_aliases(
     input: crate::operation::list_aliases::ListAliasesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AliasListEntry>> {
@@ -93,6 +103,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_grants")]
 pub(crate) fn lens_list_grants_output_output_grants(
     input: crate::operation::list_grants::ListGrantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::GrantListEntry>> {
@@ -100,6 +111,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) fn lens_list_key_policies_output_output_policy_names(
     input: crate::operation::list_key_policies::ListKeyPoliciesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -107,6 +119,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) fn lens_list_key_rotations_output_output_rotations(
     input: crate::operation::list_key_rotations::ListKeyRotationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::RotationsListEntry>> {
@@ -114,6 +127,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_keys")]
 pub(crate) fn lens_list_keys_output_output_keys(
     input: crate::operation::list_keys::ListKeysOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::KeyListEntry>> {
@@ -121,6 +135,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) fn lens_list_resource_tags_output_output_tags(
     input: crate::operation::list_resource_tags::ListResourceTagsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Tag>> {
@@ -128,6 +143,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) fn lens_list_retirable_grants_output_output_grants(
     input: crate::operation::list_retirable_grants::ListRetirableGrantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::GrantListEntry>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,164 +1,218 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_cancel_key_deletion")]
 /// Types for the `CancelKeyDeletion` operation.
 pub mod cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 /// Types for the `ConnectCustomKeyStore` operation.
 pub mod connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 /// Types for the `CreateAlias` operation.
 pub mod create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 /// Types for the `CreateCustomKeyStore` operation.
 pub mod create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 /// Types for the `CreateGrant` operation.
 pub mod create_grant;

+#[cfg(feature = "op_create_key")]
 /// Types for the `CreateKey` operation.
 pub mod create_key;

+#[cfg(feature = "op_decrypt")]
 /// Types for the `Decrypt` operation.
 pub mod decrypt;

+#[cfg(feature = "op_delete_alias")]
 /// Types for the `DeleteAlias` operation.
 pub mod delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 /// Types for the `DeleteCustomKeyStore` operation.
 pub mod delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 /// Types for the `DeleteImportedKeyMaterial` operation.
 pub mod delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 /// Types for the `DeriveSharedSecret` operation.
 pub mod derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 /// Types for the `DescribeCustomKeyStores` operation.
 pub mod describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 /// Types for the `DescribeKey` operation.
 pub mod describe_key;

+#[cfg(feature = "op_disable_key")]
 /// Types for the `DisableKey` operation.
 pub mod disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 /// Types for the `DisableKeyRotation` operation.
 pub mod disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 /// Types for the `DisconnectCustomKeyStore` operation.
 pub mod disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 /// Types for the `EnableKey` operation.
 pub mod enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 /// Types for the `EnableKeyRotation` operation.
 pub mod enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 /// Types for the `Encrypt` operation.
 pub mod encrypt;

+#[cfg(feature = "op_generate_data_key")]
 /// Types for the `GenerateDataKey` operation.
 pub mod generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 /// Types for the `GenerateDataKeyPair` operation.
 pub mod generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 /// Types for the `GenerateDataKeyPairWithoutPlaintext` operation.
 pub mod generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 /// Types for the `GenerateDataKeyWithoutPlaintext` operation.
 pub mod generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 /// Types for the `GenerateMac` operation.
 pub mod generate_mac;

+#[cfg(feature = "op_generate_random")]
 /// Types for the `GenerateRandom` operation.
 pub mod generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 /// Types for the `GetKeyLastUsage` operation.
 pub mod get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 /// Types for the `GetKeyPolicy` operation.
 pub mod get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 /// Types for the `GetKeyRotationStatus` operation.
 pub mod get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 /// Types for the `GetParametersForImport` operation.
 pub mod get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 /// Types for the `GetPublicKey` operation.
 pub mod get_public_key;

+#[cfg(feature = "op_import_key_material")]
 /// Types for the `ImportKeyMaterial` operation.
 pub mod import_key_material;

+#[cfg(feature = "op_list_aliases")]
 /// Types for the `ListAliases` operation.
 pub mod list_aliases;

+#[cfg(feature = "op_list_grants")]
 /// Types for the `ListGrants` operation.
 pub mod list_grants;

+#[cfg(feature = "op_list_key_policies")]
 /// Types for the `ListKeyPolicies` operation.
 pub mod list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 /// Types for the `ListKeyRotations` operation.
 pub mod list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 /// Types for the `ListKeys` operation.
 pub mod list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 /// Types for the `ListResourceTags` operation.
 pub mod list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 /// Types for the `ListRetirableGrants` operation.
 pub mod list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 /// Types for the `PutKeyPolicy` operation.
 pub mod put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 /// Types for the `ReEncrypt` operation.
 pub mod re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 /// Types for the `ReplicateKey` operation.
 pub mod replicate_key;

+#[cfg(feature = "op_retire_grant")]
 /// Types for the `RetireGrant` operation.
 pub mod retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 /// Types for the `RevokeGrant` operation.
 pub mod revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 /// Types for the `RotateKeyOnDemand` operation.
 pub mod rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 /// Types for the `ScheduleKeyDeletion` operation.
 pub mod schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 /// Types for the `Sign` operation.
 pub mod sign;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_alias")]
 /// Types for the `UpdateAlias` operation.
 pub mod update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 /// Types for the `UpdateCustomKeyStore` operation.
 pub mod update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 /// Types for the `UpdateKeyDescription` operation.
 pub mod update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 /// Types for the `UpdatePrimaryRegion` operation.
 pub mod update_primary_region;

+#[cfg(feature = "op_verify")]
 /// Types for the `Verify` operation.
 pub mod verify;

+#[cfg(feature = "op_verify_mac")]
 /// Types for the `VerifyMac` operation.
 pub mod verify_mac;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +73,62 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,114 +140,224 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_cancel_key_deletion")]
 pub(crate) mod shape_cancel_key_deletion;

+#[cfg(feature = "op_connect_custom_key_store")]
 pub(crate) mod shape_connect_custom_key_store;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_create_alias;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_create_custom_key_store;

+#[cfg(feature = "op_create_grant")]
 pub(crate) mod shape_create_grant;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_create_key;

+#[cfg(feature = "op_decrypt")]
 pub(crate) mod shape_decrypt;

+#[cfg(feature = "op_delete_alias")]
 pub(crate) mod shape_delete_alias;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_delete_custom_key_store;

+#[cfg(feature = "op_delete_imported_key_material")]
 pub(crate) mod shape_delete_imported_key_material;

+#[cfg(feature = "op_derive_shared_secret")]
 pub(crate) mod shape_derive_shared_secret;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_describe_custom_key_stores;

+#[cfg(feature = "op_describe_key")]
 pub(crate) mod shape_describe_key;

+#[cfg(feature = "op_disable_key")]
 pub(crate) mod shape_disable_key;

+#[cfg(feature = "op_disable_key_rotation")]
 pub(crate) mod shape_disable_key_rotation;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 pub(crate) mod shape_disconnect_custom_key_store;

+#[cfg(feature = "op_enable_key")]
 pub(crate) mod shape_enable_key;

+#[cfg(feature = "op_enable_key_rotation")]
 pub(crate) mod shape_enable_key_rotation;

+#[cfg(feature = "op_encrypt")]
 pub(crate) mod shape_encrypt;

+#[cfg(feature = "op_generate_data_key")]
 pub(crate) mod shape_generate_data_key;

+#[cfg(feature = "op_generate_data_key_pair")]
 pub(crate) mod shape_generate_data_key_pair;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 pub(crate) mod shape_generate_data_key_pair_without_plaintext;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 pub(crate) mod shape_generate_data_key_without_plaintext;

+#[cfg(feature = "op_generate_mac")]
 pub(crate) mod shape_generate_mac;

+#[cfg(feature = "op_generate_random")]
 pub(crate) mod shape_generate_random;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_get_key_last_usage;

+#[cfg(feature = "op_get_key_policy")]
 pub(crate) mod shape_get_key_policy;

+#[cfg(feature = "op_get_key_rotation_status")]
 pub(crate) mod shape_get_key_rotation_status;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub(crate) mod shape_get_parameters_for_import;

+#[cfg(feature = "op_get_public_key")]
 pub(crate) mod shape_get_public_key;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_import_key_material;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_list_aliases;

+#[cfg(feature = "op_list_grants")]
 pub(crate) mod shape_list_grants;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_list_key_policies;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_list_key_rotations;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_list_keys;

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) mod shape_list_resource_tags;

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) mod shape_list_retirable_grants;

+#[cfg(feature = "op_put_key_policy")]
 pub(crate) mod shape_put_key_policy;

+#[cfg(feature = "op_re_encrypt")]
 pub(crate) mod shape_re_encrypt;

+#[cfg(feature = "op_replicate_key")]
 pub(crate) mod shape_replicate_key;

+#[cfg(feature = "op_retire_grant")]
 pub(crate) mod shape_retire_grant;

+#[cfg(feature = "op_revoke_grant")]
 pub(crate) mod shape_revoke_grant;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_rotate_key_on_demand;

+#[cfg(feature = "op_schedule_key_deletion")]
 pub(crate) mod shape_schedule_key_deletion;

+#[cfg(feature = "op_sign")]
 pub(crate) mod shape_sign;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_alias")]
 pub(crate) mod shape_update_alias;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_update_custom_key_store;

+#[cfg(feature = "op_update_key_description")]
 pub(crate) mod shape_update_key_description;

+#[cfg(feature = "op_update_primary_region")]
 pub(crate) mod shape_update_primary_region;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_verify;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_verify_mac;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -144,264 +366,797 @@
     }
 }

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub(crate) mod shape_already_exists_exception;

+#[cfg(feature = "op_cancel_key_deletion")]
 pub(crate) mod shape_cancel_key_deletion_input;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_cloud_hsm_cluster_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_cloud_hsm_cluster_invalid_configuration_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_cloud_hsm_cluster_not_active_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_cloud_hsm_cluster_not_found_exception;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_cloud_hsm_cluster_not_related_exception;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_connect_custom_key_store")]
 pub(crate) mod shape_connect_custom_key_store_input;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_create_alias_input;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_create_custom_key_store_input;

+#[cfg(feature = "op_create_grant")]
 pub(crate) mod shape_create_grant_input;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_create_key_input;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_custom_key_store_has_cmks_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_custom_key_store_invalid_state_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_custom_key_store_name_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub(crate) mod shape_custom_key_store_not_found_exception;

+#[cfg(feature = "op_decrypt")]
 pub(crate) mod shape_decrypt_input;

+#[cfg(feature = "op_delete_alias")]
 pub(crate) mod shape_delete_alias_input;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub(crate) mod shape_delete_custom_key_store_input;

+#[cfg(feature = "op_delete_imported_key_material")]
 pub(crate) mod shape_delete_imported_key_material_input;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub(crate) mod shape_dependency_timeout_exception;

+#[cfg(feature = "op_derive_shared_secret")]
 pub(crate) mod shape_derive_shared_secret_input;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_describe_custom_key_stores_input;

+#[cfg(feature = "op_describe_key")]
 pub(crate) mod shape_describe_key_input;

+#[cfg(feature = "op_disable_key")]
 pub(crate) mod shape_disable_key_input;

+#[cfg(feature = "op_disable_key_rotation")]
 pub(crate) mod shape_disable_key_rotation_input;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_disabled_exception;

+#[cfg(feature = "op_disconnect_custom_key_store")]
 pub(crate) mod shape_disconnect_custom_key_store_input;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_dry_run_operation_exception;

+#[cfg(feature = "op_enable_key")]
 pub(crate) mod shape_enable_key_input;

+#[cfg(feature = "op_enable_key_rotation")]
 pub(crate) mod shape_enable_key_rotation_input;

+#[cfg(feature = "op_encrypt")]
 pub(crate) mod shape_encrypt_input;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_expired_import_token_exception;

+#[cfg(feature = "op_generate_data_key")]
 pub(crate) mod shape_generate_data_key_input;

+#[cfg(feature = "op_generate_data_key_pair")]
 pub(crate) mod shape_generate_data_key_pair_input;

+#[cfg(feature = "op_generate_data_key_pair_without_plaintext")]
 pub(crate) mod shape_generate_data_key_pair_without_plaintext_input;

+#[cfg(feature = "op_generate_data_key_without_plaintext")]
 pub(crate) mod shape_generate_data_key_without_plaintext_input;

+#[cfg(feature = "op_generate_mac")]
 pub(crate) mod shape_generate_mac_input;

+#[cfg(feature = "op_generate_random")]
 pub(crate) mod shape_generate_random_input;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_get_key_last_usage_input;

+#[cfg(feature = "op_get_key_policy")]
 pub(crate) mod shape_get_key_policy_input;

+#[cfg(feature = "op_get_key_rotation_status")]
 pub(crate) mod shape_get_key_rotation_status_input;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub(crate) mod shape_get_parameters_for_import_input;

+#[cfg(feature = "op_get_public_key")]
 pub(crate) mod shape_get_public_key_input;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_import_key_material_input;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub(crate) mod shape_incorrect_key_exception;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_incorrect_key_material_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 pub(crate) mod shape_incorrect_trust_anchor_exception;

+#[cfg(feature = "op_create_alias")]
 pub(crate) mod shape_invalid_alias_name_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub(crate) mod shape_invalid_arn_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub(crate) mod shape_invalid_ciphertext_exception;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub(crate) mod shape_invalid_grant_id_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_invalid_grant_token_exception;

+#[cfg(feature = "op_import_key_material")]
 pub(crate) mod shape_invalid_import_token_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_invalid_key_usage_exception;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_invalid_marker_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_key_unavailable_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_kms_internal_exception;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_kms_invalid_mac_exception;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_kms_invalid_signature_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_kms_invalid_state_exception;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_list_aliases_input;

+#[cfg(feature = "op_list_grants")]
 pub(crate) mod shape_list_grants_input;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_list_key_policies_input;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_list_key_rotations_input;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_list_keys_input;

+#[cfg(feature = "op_list_resource_tags")]
 pub(crate) mod shape_list_resource_tags_input;

+#[cfg(feature = "op_list_retirable_grants")]
 pub(crate) mod shape_list_retirable_grants_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_malformed_policy_document_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_put_key_policy")]
 pub(crate) mod shape_put_key_policy_input;

+#[cfg(feature = "op_re_encrypt")]
 pub(crate) mod shape_re_encrypt_input;

+#[cfg(feature = "op_replicate_key")]
 pub(crate) mod shape_replicate_key_input;

+#[cfg(feature = "op_retire_grant")]
 pub(crate) mod shape_retire_grant_input;

+#[cfg(feature = "op_revoke_grant")]
 pub(crate) mod shape_revoke_grant_input;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub(crate) mod shape_rotate_key_on_demand_input;

+#[cfg(feature = "op_schedule_key_deletion")]
 pub(crate) mod shape_schedule_key_deletion_input;

+#[cfg(feature = "op_sign")]
 pub(crate) mod shape_sign_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub(crate) mod shape_unsupported_operation_exception;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_alias")]
 pub(crate) mod shape_update_alias_input;

+#[cfg(feature = "op_update_custom_key_store")]
 pub(crate) mod shape_update_custom_key_store_input;

+#[cfg(feature = "op_update_key_description")]
 pub(crate) mod shape_update_key_description_input;

+#[cfg(feature = "op_update_primary_region")]
 pub(crate) mod shape_update_primary_region_input;

+#[cfg(feature = "op_verify")]
 pub(crate) mod shape_verify_input;

+#[cfg(feature = "op_verify_mac")]
 pub(crate) mod shape_verify_mac_input;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_already_in_use_exception;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_invalid_configuration_exception;

+#[cfg(feature = "op_create_key")]
 pub(crate) mod shape_xks_key_not_found_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_incorrect_authentication_credential_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_invalid_response_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_endpoint_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_uri_unreachable_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_vpc_endpoint_service_not_found_exception;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_alias_list;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_custom_key_stores_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_encryption_algorithm_spec_list;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_grant_constraints;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_key_agreement_algorithm_spec_list;

+#[cfg(feature = "op_get_key_last_usage")]
 pub(crate) mod shape_key_last_usage_data;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_key_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_key_metadata;

+#[cfg(feature = "op_list_key_policies")]
 pub(crate) mod shape_policy_name_list;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub(crate) mod shape_recipient_info;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_rotations_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub(crate) mod shape_signing_algorithm_spec_list;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(feature = "op_list_resource_tags", feature = "op_replicate_key"))]
 pub(crate) mod shape_tag_list;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub(crate) mod shape_xks_proxy_authentication_credential_type;

+#[cfg(feature = "op_list_aliases")]
 pub(crate) mod shape_alias_list_entry;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_custom_key_stores_list_entry;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_list_entry;

+#[cfg(feature = "op_list_keys")]
 pub(crate) mod shape_key_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_mac_algorithm_spec_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_configuration;

+#[cfg(feature = "op_list_key_rotations")]
 pub(crate) mod shape_rotations_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_xks_key_configuration_type;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub(crate) mod shape_grant_operation_list;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_key;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) mod shape_multi_region_key_list;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub(crate) mod shape_xks_proxy_configuration_type;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub(crate) mod shape_encryption_context_type;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub(crate) fn key_metadata_correct_errors(
     mut builder: crate::types::builders::KeyMetadataBuilder,
 ) -> crate::types::builders::KeyMetadataBuilder {
@@ -8,6 +9,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,182 +1,452 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_describe_custom_key_stores"))]
 pub use crate::types::_custom_key_store_type::CustomKeyStoreType;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::_xks_proxy_authentication_credential_type::XksProxyAuthenticationCredentialType;

+#[cfg(any(
+    feature = "op_create_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::_xks_proxy_connectivity_type::XksProxyConnectivityType;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_constraints::GrantConstraints;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_usage_type::KeyUsageType;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_customer_master_key_spec::CustomerMasterKeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_spec::KeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_origin_type::OriginType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_metadata::KeyMetadata;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_describe_key",
+    feature = "op_encrypt",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_encryption_algorithm_spec::EncryptionAlgorithmSpec;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_recipient_info::RecipientInfo;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_key_agreement_algorithm_spec::KeyAgreementAlgorithmSpec;

+#[cfg(any(feature = "op_generate_data_key", feature = "op_generate_data_key_without_plaintext"))]
 pub use crate::types::_data_key_spec::DataKeySpec;

+#[cfg(any(
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext"
+))]
 pub use crate::types::_data_key_pair_spec::DataKeyPairSpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_generate_mac",
+    feature = "op_replicate_key",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::_mac_algorithm_spec::MacAlgorithmSpec;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_data::KeyLastUsageData;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub use crate::types::_algorithm_spec::AlgorithmSpec;

+#[cfg(feature = "op_get_parameters_for_import")]
 pub use crate::types::_wrapping_key_spec::WrappingKeySpec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::_expiration_model_type::ExpirationModelType;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::_import_type::ImportType;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_include_key_material::IncludeKeyMaterial;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_replicate_key",
+    feature = "op_schedule_key_deletion"
+))]
 pub use crate::types::_key_state::KeyState;

+#[cfg(any(feature = "op_sign", feature = "op_verify"))]
 pub use crate::types::_message_type::MessageType;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key",
+    feature = "op_sign",
+    feature = "op_verify"
+))]
 pub use crate::types::_signing_algorithm_spec::SigningAlgorithmSpec;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_operation::GrantOperation;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_manager_type::KeyManagerType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_configuration::MultiRegionConfiguration;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_xks_key_configuration_type::XksKeyConfigurationType;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_key_encryption_mechanism::KeyEncryptionMechanism;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::_dry_run_modifier_type::DryRunModifierType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_custom_key_stores_list_entry::CustomKeyStoresListEntry;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_tracking_operation::KeyLastUsageTrackingOperation;

+#[cfg(feature = "op_list_aliases")]
 pub use crate::types::_alias_list_entry::AliasListEntry;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub use crate::types::_grant_list_entry::GrantListEntry;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotations_list_entry::RotationsListEntry;

+#[cfg(feature = "op_list_keys")]
 pub use crate::types::_key_list_entry::KeyListEntry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key_type::MultiRegionKeyType;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key::MultiRegionKey;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_connection_state_type::ConnectionStateType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_connection_error_code_type::ConnectionErrorCodeType;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_xks_proxy_configuration_type::XksProxyConfigurationType;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_import_state::ImportState;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_key_material_state::KeyMaterialState;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotation_type::RotationType;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod _algorithm_spec;

+#[cfg(feature = "op_list_aliases")]
 mod _alias_list_entry;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _connection_error_code_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _connection_state_type;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_describe_custom_key_stores"))]
 mod _custom_key_store_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _custom_key_stores_list_entry;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _customer_master_key_spec;

+#[cfg(any(
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext"
+))]
 mod _data_key_pair_spec;

+#[cfg(any(feature = "op_generate_data_key", feature = "op_generate_data_key_without_plaintext"))]
 mod _data_key_spec;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 mod _dry_run_modifier_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_describe_key",
+    feature = "op_encrypt",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key"
+))]
 mod _encryption_algorithm_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_replicate_key"
+))]
 mod _expiration_model_type;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 mod _grant_constraints;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 mod _grant_list_entry;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 mod _grant_operation;

+#[cfg(feature = "op_list_key_rotations")]
 mod _import_state;

+#[cfg(feature = "op_import_key_material")]
 mod _import_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _include_key_material;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_agreement_algorithm_spec;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 mod _key_encryption_mechanism;

+#[cfg(feature = "op_get_key_last_usage")]
 mod _key_last_usage_data;

+#[cfg(feature = "op_get_key_last_usage")]
 mod _key_last_usage_tracking_operation;

+#[cfg(feature = "op_list_keys")]
 mod _key_list_entry;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _key_manager_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _key_material_state;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _key_metadata;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_replicate_key",
+    feature = "op_schedule_key_deletion"
+))]
 mod _key_state;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key"
+))]
 mod _key_usage_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_generate_mac",
+    feature = "op_replicate_key",
+    feature = "op_verify_mac"
+))]
 mod _mac_algorithm_spec;

+#[cfg(any(feature = "op_sign", feature = "op_verify"))]
 mod _message_type;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_configuration;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_key;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _multi_region_key_type;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_replicate_key"
+))]
 mod _origin_type;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 mod _recipient_info;

+#[cfg(feature = "op_list_key_rotations")]
 mod _rotation_type;

+#[cfg(feature = "op_list_key_rotations")]
 mod _rotations_list_entry;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_describe_key",
+    feature = "op_get_public_key",
+    feature = "op_replicate_key",
+    feature = "op_sign",
+    feature = "op_verify"
+))]
 mod _signing_algorithm_spec;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(feature = "op_get_parameters_for_import")]
 mod _wrapping_key_spec;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 mod _xks_key_configuration_type;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_authentication_credential_type;

+#[cfg(feature = "op_describe_custom_key_stores")]
 mod _xks_proxy_configuration_type;

+#[cfg(any(
+    feature = "op_create_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_update_custom_key_store"
+))]
 mod _xks_proxy_connectivity_type;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,30 +1,60 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::_xks_proxy_authentication_credential_type::XksProxyAuthenticationCredentialTypeBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_list_grants",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::_grant_constraints::GrantConstraintsBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_key_metadata::KeyMetadataBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_random"
+))]
 pub use crate::types::_recipient_info::RecipientInfoBuilder;

+#[cfg(feature = "op_get_key_last_usage")]
 pub use crate::types::_key_last_usage_data::KeyLastUsageDataBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_list_resource_tags",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_configuration::MultiRegionConfigurationBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_xks_key_configuration_type::XksKeyConfigurationTypeBuilder;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_custom_key_stores_list_entry::CustomKeyStoresListEntryBuilder;

+#[cfg(feature = "op_list_aliases")]
 pub use crate::types::_alias_list_entry::AliasListEntryBuilder;

+#[cfg(any(feature = "op_list_grants", feature = "op_list_retirable_grants"))]
 pub use crate::types::_grant_list_entry::GrantListEntryBuilder;

+#[cfg(feature = "op_list_key_rotations")]
 pub use crate::types::_rotations_list_entry::RotationsListEntryBuilder;

+#[cfg(feature = "op_list_keys")]
 pub use crate::types::_key_list_entry::KeyListEntryBuilder;

+#[cfg(any(feature = "op_create_key", feature = "op_describe_key", feature = "op_replicate_key"))]
 pub use crate::types::_multi_region_key::MultiRegionKeyBuilder;

+#[cfg(feature = "op_describe_custom_key_stores")]
 pub use crate::types::_xks_proxy_configuration_type::XksProxyConfigurationTypeBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,194 +1,1026 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub use crate::types::error::_dependency_timeout_exception::DependencyTimeoutException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_invalid_arn_exception::InvalidArnException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_internal_exception::KmsInternalException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateException;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_invalid_configuration_exception::CloudHsmClusterInvalidConfigurationException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_not_active_exception::CloudHsmClusterNotActiveException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_invalid_state_exception::CustomKeyStoreInvalidStateException;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_not_found_exception::CustomKeyStoreNotFoundException;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsException;

+#[cfg(feature = "op_create_alias")]
 pub use crate::types::error::_invalid_alias_name_exception::InvalidAliasNameException;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_in_use_exception::CloudHsmClusterInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_cloud_hsm_cluster_not_found_exception::CloudHsmClusterNotFoundException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_custom_key_store_name_in_use_exception::CustomKeyStoreNameInUseException;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_incorrect_trust_anchor_exception::IncorrectTrustAnchorException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_incorrect_authentication_credential_exception::XksProxyIncorrectAuthenticationCredentialException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_configuration_exception::XksProxyInvalidConfigurationException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_response_exception::XksProxyInvalidResponseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_endpoint_in_use_exception::XksProxyUriEndpointInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_in_use_exception::XksProxyUriInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_unreachable_exception::XksProxyUriUnreachableException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_in_use_exception::XksProxyVpcEndpointServiceInUseException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_invalid_configuration_exception::XksProxyVpcEndpointServiceInvalidConfigurationException;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_not_found_exception::XksProxyVpcEndpointServiceNotFoundException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_disabled_exception::DisabledException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_dry_run_operation_exception::DryRunOperationException;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_grant_token_exception::InvalidGrantTokenException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_exception::TagException;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_unsupported_operation_exception::UnsupportedOperationException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_already_in_use_exception::XksKeyAlreadyInUseException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_invalid_configuration_exception::XksKeyInvalidConfigurationException;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_not_found_exception::XksKeyNotFoundException;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::error::_incorrect_key_exception::IncorrectKeyException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub use crate::types::error::_invalid_ciphertext_exception::InvalidCiphertextException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_key_usage_exception::InvalidKeyUsageException;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_key_unavailable_exception::KeyUnavailableException;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub use crate::types::error::_custom_key_store_has_cmks_exception::CustomKeyStoreHasCmKsException;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::error::_invalid_marker_exception::InvalidMarkerException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_expired_import_token_exception::ExpiredImportTokenException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_incorrect_key_material_exception::IncorrectKeyMaterialException;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_invalid_import_token_exception::InvalidImportTokenException;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub use crate::types::error::_invalid_grant_id_exception::InvalidGrantIdException;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(feature = "op_update_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_not_related_exception::CloudHsmClusterNotRelatedException;

+#[cfg(feature = "op_verify")]
 pub use crate::types::error::_kms_invalid_signature_exception::KmsInvalidSignatureException;

+#[cfg(feature = "op_verify_mac")]
 pub use crate::types::error::_kms_invalid_mac_exception::KmsInvalidMacException;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 mod _already_exists_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 mod _cloud_hsm_cluster_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 mod _cloud_hsm_cluster_invalid_configuration_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 mod _cloud_hsm_cluster_not_active_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _cloud_hsm_cluster_not_found_exception;

+#[cfg(feature = "op_update_custom_key_store")]
 mod _cloud_hsm_cluster_not_related_exception;

+#[cfg(feature = "op_rotate_key_on_demand")]
 mod _conflict_exception;

+#[cfg(feature = "op_delete_custom_key_store")]
 mod _custom_key_store_has_cmks_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 mod _custom_key_store_invalid_state_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _custom_key_store_name_in_use_exception;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 mod _custom_key_store_not_found_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 mod _dependency_timeout_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _disabled_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _dry_run_operation_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _expired_import_token_exception;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 mod _incorrect_key_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _incorrect_key_material_exception;

+#[cfg(feature = "op_create_custom_key_store")]
 mod _incorrect_trust_anchor_exception;

+#[cfg(feature = "op_create_alias")]
 mod _invalid_alias_name_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 mod _invalid_arn_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 mod _invalid_ciphertext_exception;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 mod _invalid_grant_id_exception;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _invalid_grant_token_exception;

+#[cfg(feature = "op_import_key_material")]
 mod _invalid_import_token_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _invalid_key_usage_exception;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 mod _invalid_marker_exception;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _key_unavailable_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _kms_internal_exception;

+#[cfg(feature = "op_verify_mac")]
 mod _kms_invalid_mac_exception;

+#[cfg(feature = "op_verify")]
 mod _kms_invalid_signature_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _kms_invalid_state_exception;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 mod _malformed_policy_document_exception;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 mod _not_found_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_exception;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 mod _unsupported_operation_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_already_in_use_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_invalid_configuration_exception;

+#[cfg(feature = "op_create_key")]
 mod _xks_key_not_found_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_incorrect_authentication_credential_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_invalid_response_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_endpoint_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_uri_unreachable_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_in_use_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_invalid_configuration_exception;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 mod _xks_proxy_vpc_endpoint_service_not_found_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,96 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_keys",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_verify"
+))]
 pub use crate::types::error::_dependency_timeout_exception::DependencyTimeoutExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_invalid_arn_exception::InvalidArnExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_custom_key_store",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_generate_random",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_custom_key_store",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_internal_exception::KmsInternalExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_key_deletion",
+    feature = "op_create_alias",
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_delete_alias",
+    feature = "op_delete_imported_key_material",
+    feature = "op_derive_shared_secret",
+    feature = "op_describe_key",
+    feature = "op_disable_key",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_key_last_usage",
+    feature = "op_get_key_policy",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_policies",
+    feature = "op_list_key_rotations",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants",
+    feature = "op_put_key_policy",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_schedule_key_deletion",
+    feature = "op_sign",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_alias",
+    feature = "op_update_key_description",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_invalid_configuration_exception::CloudHsmClusterInvalidConfigurationExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_custom_key_store",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_cloud_hsm_cluster_not_active_exception::CloudHsmClusterNotActiveExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_invalid_state_exception::CustomKeyStoreInvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_connect_custom_key_store",
+    feature = "op_create_key",
+    feature = "op_delete_custom_key_store",
+    feature = "op_describe_custom_key_stores",
+    feature = "op_disconnect_custom_key_store",
+    feature = "op_generate_random",
+    feature = "op_update_custom_key_store"
+))]
 pub use crate::types::error::_custom_key_store_not_found_exception::CustomKeyStoreNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_create_alias", feature = "op_replicate_key"))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_create_alias")]
 pub use crate::types::error::_invalid_alias_name_exception::InvalidAliasNameExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_alias",
+    feature = "op_create_custom_key_store",
+    feature = "op_create_grant",
+    feature = "op_create_key",
+    feature = "op_enable_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_tag_resource",
+    feature = "op_update_alias"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_in_use_exception::CloudHsmClusterInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_cloud_hsm_cluster_not_found_exception::CloudHsmClusterNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_custom_key_store_name_in_use_exception::CustomKeyStoreNameInUseExceptionBuilder;

+#[cfg(feature = "op_create_custom_key_store")]
 pub use crate::types::error::_incorrect_trust_anchor_exception::IncorrectTrustAnchorExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_incorrect_authentication_credential_exception::XksProxyIncorrectAuthenticationCredentialExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_configuration_exception::XksProxyInvalidConfigurationExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_invalid_response_exception::XksProxyInvalidResponseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_endpoint_in_use_exception::XksProxyUriEndpointInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_in_use_exception::XksProxyUriInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_uri_unreachable_exception::XksProxyUriUnreachableExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_in_use_exception::XksProxyVpcEndpointServiceInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_invalid_configuration_exception::XksProxyVpcEndpointServiceInvalidConfigurationExceptionBuilder;

+#[cfg(any(feature = "op_create_custom_key_store", feature = "op_update_custom_key_store"))]
 pub use crate::types::error::_xks_proxy_vpc_endpoint_service_not_found_exception::XksProxyVpcEndpointServiceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_sign",
+    feature = "op_update_primary_region",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_disabled_exception::DisabledExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_revoke_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_dry_run_operation_exception::DryRunOperationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_grant",
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_retire_grant",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_grant_token_exception::InvalidGrantTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key"
+))]
 pub use crate::types::error::_malformed_policy_document_exception::MalformedPolicyDocumentExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_replicate_key",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_exception::TagExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_key",
+    feature = "op_delete_imported_key_material",
+    feature = "op_disable_key_rotation",
+    feature = "op_enable_key_rotation",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_random",
+    feature = "op_get_key_rotation_status",
+    feature = "op_get_parameters_for_import",
+    feature = "op_get_public_key",
+    feature = "op_import_key_material",
+    feature = "op_list_key_rotations",
+    feature = "op_put_key_policy",
+    feature = "op_replicate_key",
+    feature = "op_rotate_key_on_demand",
+    feature = "op_update_primary_region"
+))]
 pub use crate::types::error::_unsupported_operation_exception::UnsupportedOperationExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_already_in_use_exception::XksKeyAlreadyInUseExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_invalid_configuration_exception::XksKeyInvalidConfigurationExceptionBuilder;

+#[cfg(feature = "op_create_key")]
 pub use crate::types::error::_xks_key_not_found_exception::XksKeyNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_decrypt", feature = "op_re_encrypt"))]
 pub use crate::types::error::_incorrect_key_exception::IncorrectKeyExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_import_key_material",
+    feature = "op_re_encrypt"
+))]
 pub use crate::types::error::_invalid_ciphertext_exception::InvalidCiphertextExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_invalid_key_usage_exception::InvalidKeyUsageExceptionBuilder;

+#[cfg(any(
+    feature = "op_decrypt",
+    feature = "op_derive_shared_secret",
+    feature = "op_encrypt",
+    feature = "op_generate_data_key",
+    feature = "op_generate_data_key_pair",
+    feature = "op_generate_data_key_pair_without_plaintext",
+    feature = "op_generate_data_key_without_plaintext",
+    feature = "op_generate_mac",
+    feature = "op_get_public_key",
+    feature = "op_re_encrypt",
+    feature = "op_sign",
+    feature = "op_verify",
+    feature = "op_verify_mac"
+))]
 pub use crate::types::error::_key_unavailable_exception::KeyUnavailableExceptionBuilder;

+#[cfg(feature = "op_delete_custom_key_store")]
 pub use crate::types::error::_custom_key_store_has_cmks_exception::CustomKeyStoreHasCmKsExceptionBuilder;

+#[cfg(any(
+    feature = "op_describe_custom_key_stores",
+    feature = "op_list_aliases",
+    feature = "op_list_grants",
+    feature = "op_list_key_rotations",
+    feature = "op_list_keys",
+    feature = "op_list_resource_tags",
+    feature = "op_list_retirable_grants"
+))]
 pub use crate::types::error::_invalid_marker_exception::InvalidMarkerExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_expired_import_token_exception::ExpiredImportTokenExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_incorrect_key_material_exception::IncorrectKeyMaterialExceptionBuilder;

+#[cfg(feature = "op_import_key_material")]
 pub use crate::types::error::_invalid_import_token_exception::InvalidImportTokenExceptionBuilder;

+#[cfg(any(feature = "op_list_grants", feature = "op_retire_grant", feature = "op_revoke_grant"))]
 pub use crate::types::error::_invalid_grant_id_exception::InvalidGrantIdExceptionBuilder;

+#[cfg(feature = "op_rotate_key_on_demand")]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(feature = "op_update_custom_key_store")]
 pub use crate::types::error::_cloud_hsm_cluster_not_related_exception::CloudHsmClusterNotRelatedExceptionBuilder;

+#[cfg(feature = "op_verify")]
 pub use crate::types::error::_kms_invalid_signature_exception::KmsInvalidSignatureExceptionBuilder;

+#[cfg(feature = "op_verify_mac")]
 pub use crate::types::error::_kms_invalid_mac_exception::KmsInvalidMacExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
