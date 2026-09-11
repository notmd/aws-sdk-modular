# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/sns`
- model: `aws-models/sns.json`
- package: `aws-sdk-sns`
- library: `aws_sdk_sns`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_add_permission`: `AddPermission`
- `op_check_if_phone_number_is_opted_out`: `CheckIfPhoneNumberIsOptedOut`
- `op_confirm_subscription`: `ConfirmSubscription`
- `op_create_platform_application`: `CreatePlatformApplication`
- `op_create_platform_endpoint`: `CreatePlatformEndpoint`
- `op_create_sms_sandbox_phone_number`: `CreateSMSSandboxPhoneNumber`
- `op_create_topic`: `CreateTopic`
- `op_delete_endpoint`: `DeleteEndpoint`
- `op_delete_platform_application`: `DeletePlatformApplication`
- `op_delete_sms_sandbox_phone_number`: `DeleteSMSSandboxPhoneNumber`
- `op_delete_topic`: `DeleteTopic`
- `op_get_data_protection_policy`: `GetDataProtectionPolicy`
- `op_get_endpoint_attributes`: `GetEndpointAttributes`
- `op_get_platform_application_attributes`: `GetPlatformApplicationAttributes`
- `op_get_sms_attributes`: `GetSMSAttributes`
- `op_get_sms_sandbox_account_status`: `GetSMSSandboxAccountStatus`
- `op_get_subscription_attributes`: `GetSubscriptionAttributes`
- `op_get_topic_attributes`: `GetTopicAttributes`
- `op_list_endpoints_by_platform_application`: `ListEndpointsByPlatformApplication`
- `op_list_origination_numbers`: `ListOriginationNumbers`
- `op_list_phone_numbers_opted_out`: `ListPhoneNumbersOptedOut`
- `op_list_platform_applications`: `ListPlatformApplications`
- `op_list_sms_sandbox_phone_numbers`: `ListSMSSandboxPhoneNumbers`
- `op_list_subscriptions`: `ListSubscriptions`
- `op_list_subscriptions_by_topic`: `ListSubscriptionsByTopic`
- `op_list_tags_for_resource`: `ListTagsForResource`
- `op_list_topics`: `ListTopics`
- `op_opt_in_phone_number`: `OptInPhoneNumber`
- `op_publish`: `Publish`
- `op_publish_batch`: `PublishBatch`
- `op_put_data_protection_policy`: `PutDataProtectionPolicy`
- `op_remove_permission`: `RemovePermission`
- `op_set_endpoint_attributes`: `SetEndpointAttributes`
- `op_set_platform_application_attributes`: `SetPlatformApplicationAttributes`
- `op_set_sms_attributes`: `SetSMSAttributes`
- `op_set_subscription_attributes`: `SetSubscriptionAttributes`
- `op_set_topic_attributes`: `SetTopicAttributes`
- `op_subscribe`: `Subscribe`
- `op_tag_resource`: `TagResource`
- `op_unsubscribe`: `Unsubscribe`
- `op_untag_resource`: `UntagResource`
- `op_verify_sms_sandbox_phone_number`: `VerifySMSSandboxPhoneNumber`

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
@@ -19,58 +19,45 @@
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

 [dependencies.aws-smithy-query]
-path = "../aws-smithy-query"
 version = "0.62.0"

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

 [dependencies.aws-smithy-xml]
-path = "../aws-smithy-xml"
 version = "0.62.0"

 [dependencies.aws-types]
-path = "../aws-types"
 version = "1.6.0"

 [dependencies.fastrand]
@@ -89,11 +76,9 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -112,6 +97,48 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_add_permission = []
+op_check_if_phone_number_is_opted_out = []
+op_confirm_subscription = []
+op_create_platform_application = []
+op_create_platform_endpoint = []
+op_create_sms_sandbox_phone_number = []
+op_create_topic = []
+op_delete_endpoint = []
+op_delete_platform_application = []
+op_delete_sms_sandbox_phone_number = []
+op_delete_topic = []
+op_get_data_protection_policy = []
+op_get_endpoint_attributes = []
+op_get_platform_application_attributes = []
+op_get_sms_attributes = []
+op_get_sms_sandbox_account_status = []
+op_get_subscription_attributes = []
+op_get_topic_attributes = []
+op_list_endpoints_by_platform_application = []
+op_list_origination_numbers = []
+op_list_phone_numbers_opted_out = []
+op_list_platform_applications = []
+op_list_sms_sandbox_phone_numbers = []
+op_list_subscriptions = []
+op_list_subscriptions_by_topic = []
+op_list_tags_for_resource = []
+op_list_topics = []
+op_opt_in_phone_number = []
+op_publish = []
+op_publish_batch = []
+op_put_data_protection_policy = []
+op_remove_permission = []
+op_set_endpoint_attributes = []
+op_set_platform_application_attributes = []
+op_set_sms_attributes = []
+op_set_subscription_attributes = []
+op_set_topic_attributes = []
+op_subscribe = []
+op_tag_resource = []
+op_unsubscribe = []
+op_untag_resource = []
+op_verify_sms_sandbox_phone_number = []

 [hints]
 mostly-unused = true
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,18 +136,25 @@
     }
 }

+#[cfg(feature = "op_add_permission")]
 mod add_permission;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 mod check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_confirm_subscription")]
 mod confirm_subscription;

+#[cfg(feature = "op_create_platform_application")]
 mod create_platform_application;

+#[cfg(feature = "op_create_platform_endpoint")]
 mod create_platform_endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_topic")]
 mod create_topic;

 /// Operation customization and supporting types.
@@ -177,72 +184,107 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_endpoint")]
 mod delete_endpoint;

+#[cfg(feature = "op_delete_platform_application")]
 mod delete_platform_application;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 mod delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_topic")]
 mod delete_topic;

+#[cfg(feature = "op_get_data_protection_policy")]
 mod get_data_protection_policy;

+#[cfg(feature = "op_get_endpoint_attributes")]
 mod get_endpoint_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 mod get_platform_application_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 mod get_sms_attributes;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 mod get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_subscription_attributes")]
 mod get_subscription_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 mod get_topic_attributes;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 mod list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_origination_numbers")]
 mod list_origination_numbers;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 mod list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_platform_applications")]
 mod list_platform_applications;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_subscriptions")]
 mod list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 mod list_subscriptions_by_topic;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_topics")]
 mod list_topics;

+#[cfg(feature = "op_opt_in_phone_number")]
 mod opt_in_phone_number;

+#[cfg(feature = "op_publish")]
 mod publish;

+#[cfg(feature = "op_publish_batch")]
 mod publish_batch;

+#[cfg(feature = "op_put_data_protection_policy")]
 mod put_data_protection_policy;

+#[cfg(feature = "op_remove_permission")]
 mod remove_permission;

+#[cfg(feature = "op_set_endpoint_attributes")]
 mod set_endpoint_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 mod set_platform_application_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 mod set_sms_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 mod set_subscription_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 mod set_topic_attributes;

+#[cfg(feature = "op_subscribe")]
 mod subscribe;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_unsubscribe")]
 mod unsubscribe;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 mod verify_sms_sandbox_phone_number;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,72 +3,318 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_tag_resource",
+        feature = "op_unsubscribe",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that the user has been denied access to the requested resource.</p>
     AuthorizationErrorException(crate::types::error::AuthorizationErrorException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>Two or more batch entries in the request have the same <code>Id</code>.</p>
     BatchEntryIdsNotDistinctException(crate::types::error::BatchEntryIdsNotDistinctException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The length of all the batch messages put together is more than the limit.</p>
     BatchRequestTooLongException(crate::types::error::BatchRequestTooLongException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>Can't perform multiple operations on a tag simultaneously. Perform the operations sequentially.</p>
     ConcurrentAccessException(crate::types::error::ConcurrentAccessException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The batch request doesn't contain any entries.</p>
     EmptyBatchRequestException(crate::types::error::EmptyBatchRequestException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Exception error indicating endpoint disabled.</p>
     EndpointDisabledException(crate::types::error::EndpointDisabledException),
+    #[cfg(any(
+        feature = "op_confirm_subscription",
+        feature = "op_set_subscription_attributes",
+        feature = "op_subscribe"
+    ))]
     /// <p>Indicates that the number of filter polices in your Amazon Web Services account exceeds the limit. To add more filter polices, submit an Amazon SNS Limit Increase case in the Amazon Web Services Support Center.</p>
     FilterPolicyLimitExceededException(crate::types::error::FilterPolicyLimitExceededException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates an internal service error.</p>
     InternalErrorException(crate::types::error::InternalErrorException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The <code>Id</code> of a batch entry in a batch request doesn't abide by the specification.</p>
     InvalidBatchEntryIdException(crate::types::error::InvalidBatchEntryIdException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_tag_resource",
+        feature = "op_unsubscribe",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     InvalidParameterException(crate::types::error::InvalidParameterException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     InvalidParameterValueException(crate::types::error::InvalidParameterValueException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_topic_attributes",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe"
+    ))]
     /// <p>The credential signature isn't valid. You must use an HTTPS endpoint and sign your request using Signature Version 4.</p>
     InvalidSecurityException(crate::types::error::InvalidSecurityException),
+    #[cfg(feature = "op_delete_topic")]
     /// <p>Indicates that the specified state is not a valid state for an event source.</p>
     InvalidStateException(crate::types::error::InvalidStateException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The ciphertext references a key that doesn't exist or that you don't have access to.</p>
     KmsAccessDeniedException(crate::types::error::KmsAccessDeniedException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the specified Amazon Web Services KMS key isn't enabled.</p>
     KmsDisabledException(crate::types::error::KmsDisabledException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the state of the specified resource isn't valid for this request. For more information, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/key-state.html">Key states of Amazon Web Services KMS keys</a> in the <i>Key Management Service Developer Guide</i>.</p>
     KmsInvalidStateException(crate::types::error::KmsInvalidStateException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the specified entity or resource can't be found.</p>
     KmsNotFoundException(crate::types::error::KmsNotFoundException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The Amazon Web Services access key ID needs a subscription for the service.</p>
     KmsOptInRequired(crate::types::error::KmsOptInRequired),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was denied due to request throttling. For more information about throttling, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/limits.html#requests-per-second">Limits</a> in the <i>Key Management Service Developer Guide.</i></p>
     KmsThrottlingException(crate::types::error::KmsThrottlingException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_endpoint",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe"
+    ))]
     /// <p>Indicates that the requested resource does not exist.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(feature = "op_create_sms_sandbox_phone_number")]
     /// <p>Indicates that the specified phone number opted out of receiving SMS messages from your Amazon Web Services account. You can't send SMS messages to phone numbers that opt out.</p>
     OptedOutException(crate::types::error::OptedOutException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Exception error indicating platform application disabled.</p>
     PlatformApplicationDisabledException(crate::types::error::PlatformApplicationDisabledException),
+    #[cfg(any(
+        feature = "op_confirm_subscription",
+        feature = "op_set_subscription_attributes",
+        feature = "op_subscribe"
+    ))]
     /// <p>Indicates that the request parameter has exceeded the maximum number of concurrent message replays.</p>
     ReplayLimitExceededException(crate::types::error::ReplayLimitExceededException),
+    #[cfg(any(
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Can’t perform the action on the specified resource. Make sure that the resource exists.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>A tag has been added to a resource with the same ARN as a deleted resource. Wait a short while and then retry the operation.</p>
     StaleTagException(crate::types::error::StaleTagException),
+    #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
     /// <p>Indicates that the customer already owns the maximum allowed number of subscriptions.</p>
     SubscriptionLimitExceededException(crate::types::error::SubscriptionLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>Can't add more than 50 tags to a topic.</p>
     TagLimitExceededException(crate::types::error::TagLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>The request doesn't comply with the IAM tag policy. Correct your request and then retry it.</p>
     TagPolicyException(crate::types::error::TagPolicyException),
+    #[cfg(any(
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_opt_in_phone_number",
+        feature = "op_set_sms_attributes",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that the rate at which requests have been submitted for this action exceeds the limit for your Amazon Web Services account.</p>
     ThrottledException(crate::types::error::ThrottledException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The batch request contains more entries than permissible (more than 10).</p>
     TooManyEntriesInBatchRequestException(crate::types::error::TooManyEntriesInBatchRequestException),
+    #[cfg(feature = "op_create_topic")]
     /// <p>Indicates that the customer already owns the maximum allowed number of topics.</p>
     TopicLimitExceededException(crate::types::error::TopicLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_delete_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     UserErrorException(crate::types::error::UserErrorException),
+    #[cfg(any(
+        feature = "op_list_origination_numbers",
+        feature = "op_publish",
+        feature = "op_publish_batch"
+    ))]
     /// <p>Indicates that a parameter in the request is invalid.</p>
     ValidationException(crate::types::error::ValidationException),
+    #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
     /// <p>Indicates that the one-time password (OTP) used for verification is invalid.</p>
     VerificationException(crate::types::error::VerificationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -85,39 +331,285 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::AuthorizationErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchEntryIdsNotDistinctException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchRequestTooLongException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::ConcurrentAccessException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::EmptyBatchRequestException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::EndpointDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::FilterPolicyLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InternalErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::InvalidBatchEntryIdException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InvalidParameterException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::InvalidParameterValueException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::InvalidSecurityException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_topic")]
             Error::InvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsAccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsOptInRequired(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Error::OptedOutException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::PlatformApplicationDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::ReplayLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::StaleTagException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Error::SubscriptionLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagPolicyException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ThrottledException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::TooManyEntriesInBatchRequestException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_topic")]
             Error::TopicLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Error::UserErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Error::VerificationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -142,44 +634,291 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::AuthorizationErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchEntryIdsNotDistinctException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchRequestTooLongException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::ConcurrentAccessException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::EmptyBatchRequestException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::EndpointDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::FilterPolicyLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InternalErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::InvalidBatchEntryIdException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InvalidParameterException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::InvalidParameterValueException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::InvalidSecurityException(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_topic")]
             Self::InvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsAccessDeniedException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsDisabledException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsOptInRequired(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Self::OptedOutException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::PlatformApplicationDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::ReplayLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::StaleTagException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Self::SubscriptionLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagPolicyException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ThrottledException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::TooManyEntriesInBatchRequestException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_topic")]
             Self::TopicLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Self::UserErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Self::VerificationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::add_permission::AddPermissionError, R>>
     for Error
@@ -201,6 +940,7 @@
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl From<crate::operation::add_permission::AddPermissionError> for Error {
     fn from(err: crate::operation::add_permission::AddPermissionError) -> Self {
         match err {
@@ -220,6 +960,7 @@
         }
     }
 }
+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -245,6 +986,7 @@
         }
     }
 }
+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 impl From<crate::operation::check_if_phone_number_is_opted_out::CheckIfPhoneNumberIsOptedOutError> for Error {
     fn from(err: crate::operation::check_if_phone_number_is_opted_out::CheckIfPhoneNumberIsOptedOutError) -> Self {
         match err {
@@ -264,6 +1006,7 @@
         }
     }
 }
+#[cfg(feature = "op_confirm_subscription")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -289,6 +1032,7 @@
         }
     }
 }
+#[cfg(feature = "op_confirm_subscription")]
 impl From<crate::operation::confirm_subscription::ConfirmSubscriptionError> for Error {
     fn from(err: crate::operation::confirm_subscription::ConfirmSubscriptionError) -> Self {
         match err {
@@ -319,6 +1063,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -344,6 +1089,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_application")]
 impl From<crate::operation::create_platform_application::CreatePlatformApplicationError> for Error {
     fn from(err: crate::operation::create_platform_application::CreatePlatformApplicationError) -> Self {
         match err {
@@ -360,6 +1106,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -385,6 +1132,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_endpoint")]
 impl From<crate::operation::create_platform_endpoint::CreatePlatformEndpointError> for Error {
     fn from(err: crate::operation::create_platform_endpoint::CreatePlatformEndpointError) -> Self {
         match err {
@@ -406,6 +1154,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -431,6 +1180,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 impl From<crate::operation::create_sms_sandbox_phone_number::CreateSMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::create_sms_sandbox_phone_number::CreateSMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -456,6 +1206,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_topic")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_topic::CreateTopicError, R>>
     for Error
 where
@@ -473,6 +1224,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_topic")]
 impl From<crate::operation::create_topic::CreateTopicError> for Error {
     fn from(err: crate::operation::create_topic::CreateTopicError) -> Self {
         match err {
@@ -507,6 +1259,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_endpoint")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_endpoint::DeleteEndpointError, R>>
     for Error
@@ -528,6 +1281,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_endpoint")]
 impl From<crate::operation::delete_endpoint::DeleteEndpointError> for Error {
     fn from(err: crate::operation::delete_endpoint::DeleteEndpointError) -> Self {
         match err {
@@ -544,6 +1298,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -569,6 +1324,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_platform_application")]
 impl From<crate::operation::delete_platform_application::DeletePlatformApplicationError> for Error {
     fn from(err: crate::operation::delete_platform_application::DeletePlatformApplicationError) -> Self {
         match err {
@@ -585,6 +1341,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -610,6 +1367,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 impl From<crate::operation::delete_sms_sandbox_phone_number::DeleteSMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::delete_sms_sandbox_phone_number::DeleteSMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -635,6 +1393,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_topic")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_topic::DeleteTopicError, R>>
     for Error
 where
@@ -652,6 +1411,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_topic")]
 impl From<crate::operation::delete_topic::DeleteTopicError> for Error {
     fn from(err: crate::operation::delete_topic::DeleteTopicError) -> Self {
         match err {
@@ -683,6 +1443,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -708,6 +1469,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl From<crate::operation::get_data_protection_policy::GetDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::get_data_protection_policy::GetDataProtectionPolicyError) -> Self {
         match err {
@@ -732,6 +1494,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_endpoint_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -757,6 +1520,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_endpoint_attributes")]
 impl From<crate::operation::get_endpoint_attributes::GetEndpointAttributesError> for Error {
     fn from(err: crate::operation::get_endpoint_attributes::GetEndpointAttributesError) -> Self {
         match err {
@@ -778,6 +1542,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_platform_application_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -803,6 +1568,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_platform_application_attributes")]
 impl From<crate::operation::get_platform_application_attributes::GetPlatformApplicationAttributesError> for Error {
     fn from(err: crate::operation::get_platform_application_attributes::GetPlatformApplicationAttributesError) -> Self {
         match err {
@@ -822,6 +1588,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -847,6 +1614,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_attributes")]
 impl From<crate::operation::get_sms_attributes::GetSMSAttributesError> for Error {
     fn from(err: crate::operation::get_sms_attributes::GetSMSAttributesError) -> Self {
         match err {
@@ -866,6 +1634,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -891,6 +1660,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 impl From<crate::operation::get_sms_sandbox_account_status::GetSMSSandboxAccountStatusError> for Error {
     fn from(err: crate::operation::get_sms_sandbox_account_status::GetSMSSandboxAccountStatusError) -> Self {
         match err {
@@ -907,6 +1677,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_subscription_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -932,6 +1703,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_subscription_attributes")]
 impl From<crate::operation::get_subscription_attributes::GetSubscriptionAttributesError> for Error {
     fn from(err: crate::operation::get_subscription_attributes::GetSubscriptionAttributesError) -> Self {
         match err {
@@ -951,6 +1723,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_topic_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -976,6 +1749,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_topic_attributes")]
 impl From<crate::operation::get_topic_attributes::GetTopicAttributesError> for Error {
     fn from(err: crate::operation::get_topic_attributes::GetTopicAttributesError) -> Self {
         match err {
@@ -1000,6 +1774,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1025,6 +1800,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 impl From<crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationError> for Error {
     fn from(
         err: crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationError,
@@ -1048,6 +1824,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_origination_numbers")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1073,6 +1850,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_origination_numbers")]
 impl From<crate::operation::list_origination_numbers::ListOriginationNumbersError> for Error {
     fn from(err: crate::operation::list_origination_numbers::ListOriginationNumbersError) -> Self {
         match err {
@@ -1097,6 +1875,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1122,6 +1901,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 impl From<crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutError> for Error {
     fn from(err: crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutError) -> Self {
         match err {
@@ -1141,6 +1921,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_platform_applications")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1166,6 +1947,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_platform_applications")]
 impl From<crate::operation::list_platform_applications::ListPlatformApplicationsError> for Error {
     fn from(err: crate::operation::list_platform_applications::ListPlatformApplicationsError) -> Self {
         match err {
@@ -1182,6 +1964,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1207,6 +1990,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 impl From<crate::operation::list_sms_sandbox_phone_numbers::ListSMSSandboxPhoneNumbersError> for Error {
     fn from(err: crate::operation::list_sms_sandbox_phone_numbers::ListSMSSandboxPhoneNumbersError) -> Self {
         match err {
@@ -1229,6 +2013,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1254,6 +2039,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions")]
 impl From<crate::operation::list_subscriptions::ListSubscriptionsError> for Error {
     fn from(err: crate::operation::list_subscriptions::ListSubscriptionsError) -> Self {
         match err {
@@ -1270,6 +2056,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions_by_topic")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1295,6 +2082,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions_by_topic")]
 impl From<crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicError> for Error {
     fn from(err: crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicError) -> Self {
         match err {
@@ -1312,6 +2100,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1337,6 +2126,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -1361,6 +2151,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_topics")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_topics::ListTopicsError, R>>
     for Error
 where
@@ -1378,6 +2169,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_topics")]
 impl From<crate::operation::list_topics::ListTopicsError> for Error {
     fn from(err: crate::operation::list_topics::ListTopicsError) -> Self {
         match err {
@@ -1394,6 +2186,7 @@
         }
     }
 }
+#[cfg(feature = "op_opt_in_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1419,6 +2212,7 @@
         }
     }
 }
+#[cfg(feature = "op_opt_in_phone_number")]
 impl From<crate::operation::opt_in_phone_number::OptInPhoneNumberError> for Error {
     fn from(err: crate::operation::opt_in_phone_number::OptInPhoneNumberError) -> Self {
         match err {
@@ -1438,6 +2232,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::publish::PublishError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1454,6 +2249,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish")]
 impl From<crate::operation::publish::PublishError> for Error {
     fn from(err: crate::operation::publish::PublishError) -> Self {
         match err {
@@ -1496,6 +2292,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish_batch")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::publish_batch::PublishBatchError, R>>
     for Error
 where
@@ -1513,6 +2310,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish_batch")]
 impl From<crate::operation::publish_batch::PublishBatchError> for Error {
     fn from(err: crate::operation::publish_batch::PublishBatchError) -> Self {
         match err {
@@ -1580,6 +2378,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1605,6 +2404,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl From<crate::operation::put_data_protection_policy::PutDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::put_data_protection_policy::PutDataProtectionPolicyError) -> Self {
         match err {
@@ -1629,6 +2429,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1654,6 +2455,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl From<crate::operation::remove_permission::RemovePermissionError> for Error {
     fn from(err: crate::operation::remove_permission::RemovePermissionError) -> Self {
         match err {
@@ -1673,6 +2475,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_endpoint_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1698,6 +2501,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_endpoint_attributes")]
 impl From<crate::operation::set_endpoint_attributes::SetEndpointAttributesError> for Error {
     fn from(err: crate::operation::set_endpoint_attributes::SetEndpointAttributesError) -> Self {
         match err {
@@ -1719,6 +2523,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_platform_application_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1744,6 +2549,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_platform_application_attributes")]
 impl From<crate::operation::set_platform_application_attributes::SetPlatformApplicationAttributesError> for Error {
     fn from(err: crate::operation::set_platform_application_attributes::SetPlatformApplicationAttributesError) -> Self {
         match err {
@@ -1763,6 +2569,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_sms_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1788,6 +2595,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_sms_attributes")]
 impl From<crate::operation::set_sms_attributes::SetSMSAttributesError> for Error {
     fn from(err: crate::operation::set_sms_attributes::SetSMSAttributesError) -> Self {
         match err {
@@ -1807,6 +2615,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_subscription_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1832,6 +2641,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_subscription_attributes")]
 impl From<crate::operation::set_subscription_attributes::SetSubscriptionAttributesError> for Error {
     fn from(err: crate::operation::set_subscription_attributes::SetSubscriptionAttributesError) -> Self {
         match err {
@@ -1857,6 +2667,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_topic_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1882,6 +2693,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_topic_attributes")]
 impl From<crate::operation::set_topic_attributes::SetTopicAttributesError> for Error {
     fn from(err: crate::operation::set_topic_attributes::SetTopicAttributesError) -> Self {
         match err {
@@ -1906,6 +2718,7 @@
         }
     }
 }
+#[cfg(feature = "op_subscribe")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::subscribe::SubscribeError, R>>
     for Error
 where
@@ -1923,6 +2736,7 @@
         }
     }
 }
+#[cfg(feature = "op_subscribe")]
 impl From<crate::operation::subscribe::SubscribeError> for Error {
     fn from(err: crate::operation::subscribe::SubscribeError) -> Self {
         match err {
@@ -1952,6 +2766,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -1969,6 +2784,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -1997,6 +2813,7 @@
         }
     }
 }
+#[cfg(feature = "op_unsubscribe")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::unsubscribe::UnsubscribeError, R>>
     for Error
 where
@@ -2014,6 +2831,7 @@
         }
     }
 }
+#[cfg(feature = "op_unsubscribe")]
 impl From<crate::operation::unsubscribe::UnsubscribeError> for Error {
     fn from(err: crate::operation::unsubscribe::UnsubscribeError) -> Self {
         match err {
@@ -2036,6 +2854,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2057,6 +2876,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2085,6 +2905,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2110,6 +2931,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 impl From<crate::operation::verify_sms_sandbox_phone_number::VerifySMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::verify_sms_sandbox_phone_number::VerifySMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -2138,39 +2960,285 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::AuthorizationErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchEntryIdsNotDistinctException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchRequestTooLongException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::ConcurrentAccessException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::EmptyBatchRequestException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::EndpointDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::FilterPolicyLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InternalErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::InvalidBatchEntryIdException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InvalidParameterException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::InvalidParameterValueException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::InvalidSecurityException(inner) => inner.source(),
+            #[cfg(feature = "op_delete_topic")]
             Error::InvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsAccessDeniedException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsDisabledException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsInvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsOptInRequired(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Error::OptedOutException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::PlatformApplicationDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::ReplayLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::StaleTagException(inner) => inner.source(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Error::SubscriptionLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagPolicyException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ThrottledException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::TooManyEntriesInBatchRequestException(inner) => inner.source(),
+            #[cfg(feature = "op_create_topic")]
             Error::TopicLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Error::UserErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Error::ValidationException(inner) => inner.source(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Error::VerificationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2179,39 +3247,285 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::AuthorizationErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchEntryIdsNotDistinctException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchRequestTooLongException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::ConcurrentAccessException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::EmptyBatchRequestException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::EndpointDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::FilterPolicyLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InternalErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::InvalidBatchEntryIdException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InvalidParameterException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::InvalidParameterValueException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::InvalidSecurityException(e) => e.request_id(),
+            #[cfg(feature = "op_delete_topic")]
             Self::InvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsAccessDeniedException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsDisabledException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsInvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsOptInRequired(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Self::OptedOutException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::PlatformApplicationDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::ReplayLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::StaleTagException(e) => e.request_id(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Self::SubscriptionLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagPolicyException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ThrottledException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::TooManyEntriesInBatchRequestException(e) => e.request_id(),
+            #[cfg(feature = "op_create_topic")]
             Self::TopicLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Self::UserErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Self::ValidationException(e) => e.request_id(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Self::VerificationException(e) => e.request_id(),
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
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) fn reflens_list_endpoints_by_platform_application_output_output_next_token(
     input: &crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) fn reflens_list_origination_numbers_output_output_next_token(
     input: &crate::operation::list_origination_numbers::ListOriginationNumbersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) fn reflens_list_phone_numbers_opted_out_output_output_next_token(
     input: &crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) fn reflens_list_platform_applications_output_output_next_token(
     input: &crate::operation::list_platform_applications::ListPlatformApplicationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn reflens_list_sms_sandbox_phone_numbers_output_output_next_token(
     input: &crate::operation::list_sms_sandbox_phone_numbers::ListSmsSandboxPhoneNumbersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) fn reflens_list_subscriptions_output_output_next_token(
     input: &crate::operation::list_subscriptions::ListSubscriptionsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) fn reflens_list_subscriptions_by_topic_output_output_next_token(
     input: &crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_topics")]
 pub(crate) fn reflens_list_topics_output_output_next_token(
     input: &crate::operation::list_topics::ListTopicsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) fn lens_list_endpoints_by_platform_application_output_output_endpoints(
     input: crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Endpoint>> {
@@ -86,6 +95,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) fn lens_list_origination_numbers_output_output_phone_numbers(
     input: crate::operation::list_origination_numbers::ListOriginationNumbersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::PhoneNumberInformation>> {
@@ -93,6 +103,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) fn lens_list_phone_numbers_opted_out_output_output_phone_numbers(
     input: crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -100,6 +111,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) fn lens_list_platform_applications_output_output_platform_applications(
     input: crate::operation::list_platform_applications::ListPlatformApplicationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::PlatformApplication>> {
@@ -107,6 +119,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn lens_list_sms_sandbox_phone_numbers_output_output_phone_numbers(
     input: crate::operation::list_sms_sandbox_phone_numbers::ListSmsSandboxPhoneNumbersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SmsSandboxPhoneNumber>> {
@@ -114,6 +127,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) fn lens_list_subscriptions_output_output_subscriptions(
     input: crate::operation::list_subscriptions::ListSubscriptionsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Subscription>> {
@@ -121,6 +135,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) fn lens_list_subscriptions_by_topic_output_output_subscriptions(
     input: crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Subscription>> {
@@ -128,6 +143,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_topics")]
 pub(crate) fn lens_list_topics_output_output_topics(
     input: crate::operation::list_topics::ListTopicsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Topic>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,128 +1,170 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_add_permission")]
 /// Types for the `AddPermission` operation.
 pub mod add_permission;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 /// Types for the `CheckIfPhoneNumberIsOptedOut` operation.
 pub mod check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_confirm_subscription")]
 /// Types for the `ConfirmSubscription` operation.
 pub mod confirm_subscription;

+#[cfg(feature = "op_create_platform_application")]
 /// Types for the `CreatePlatformApplication` operation.
 pub mod create_platform_application;

+#[cfg(feature = "op_create_platform_endpoint")]
 /// Types for the `CreatePlatformEndpoint` operation.
 pub mod create_platform_endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 /// Types for the `CreateSMSSandboxPhoneNumber` operation.
 pub mod create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_topic")]
 /// Types for the `CreateTopic` operation.
 pub mod create_topic;

+#[cfg(feature = "op_delete_endpoint")]
 /// Types for the `DeleteEndpoint` operation.
 pub mod delete_endpoint;

+#[cfg(feature = "op_delete_platform_application")]
 /// Types for the `DeletePlatformApplication` operation.
 pub mod delete_platform_application;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 /// Types for the `DeleteSMSSandboxPhoneNumber` operation.
 pub mod delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_topic")]
 /// Types for the `DeleteTopic` operation.
 pub mod delete_topic;

+#[cfg(feature = "op_get_data_protection_policy")]
 /// Types for the `GetDataProtectionPolicy` operation.
 pub mod get_data_protection_policy;

+#[cfg(feature = "op_get_endpoint_attributes")]
 /// Types for the `GetEndpointAttributes` operation.
 pub mod get_endpoint_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 /// Types for the `GetPlatformApplicationAttributes` operation.
 pub mod get_platform_application_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 /// Types for the `GetSMSAttributes` operation.
 pub mod get_sms_attributes;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 /// Types for the `GetSMSSandboxAccountStatus` operation.
 pub mod get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_subscription_attributes")]
 /// Types for the `GetSubscriptionAttributes` operation.
 pub mod get_subscription_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 /// Types for the `GetTopicAttributes` operation.
 pub mod get_topic_attributes;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 /// Types for the `ListEndpointsByPlatformApplication` operation.
 pub mod list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_origination_numbers")]
 /// Types for the `ListOriginationNumbers` operation.
 pub mod list_origination_numbers;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 /// Types for the `ListPhoneNumbersOptedOut` operation.
 pub mod list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_platform_applications")]
 /// Types for the `ListPlatformApplications` operation.
 pub mod list_platform_applications;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 /// Types for the `ListSMSSandboxPhoneNumbers` operation.
 pub mod list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_subscriptions")]
 /// Types for the `ListSubscriptions` operation.
 pub mod list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 /// Types for the `ListSubscriptionsByTopic` operation.
 pub mod list_subscriptions_by_topic;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_topics")]
 /// Types for the `ListTopics` operation.
 pub mod list_topics;

+#[cfg(feature = "op_opt_in_phone_number")]
 /// Types for the `OptInPhoneNumber` operation.
 pub mod opt_in_phone_number;

+#[cfg(feature = "op_publish")]
 /// Types for the `Publish` operation.
 pub mod publish;

+#[cfg(feature = "op_publish_batch")]
 /// Types for the `PublishBatch` operation.
 pub mod publish_batch;

+#[cfg(feature = "op_put_data_protection_policy")]
 /// Types for the `PutDataProtectionPolicy` operation.
 pub mod put_data_protection_policy;

+#[cfg(feature = "op_remove_permission")]
 /// Types for the `RemovePermission` operation.
 pub mod remove_permission;

+#[cfg(feature = "op_set_endpoint_attributes")]
 /// Types for the `SetEndpointAttributes` operation.
 pub mod set_endpoint_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 /// Types for the `SetPlatformApplicationAttributes` operation.
 pub mod set_platform_application_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 /// Types for the `SetSMSAttributes` operation.
 pub mod set_sms_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 /// Types for the `SetSubscriptionAttributes` operation.
 pub mod set_subscription_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 /// Types for the `SetTopicAttributes` operation.
 pub mod set_topic_attributes;

+#[cfg(feature = "op_subscribe")]
 /// Types for the `Subscribe` operation.
 pub mod subscribe;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_unsubscribe")]
 /// Types for the `Unsubscribe` operation.
 pub mod unsubscribe;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 /// Types for the `VerifySMSSandboxPhoneNumber` operation.
 pub mod verify_sms_sandbox_phone_number;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,48 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +61,50 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     _response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -25,288 +113,653 @@
     crate::rest_xml_wrapped_errors::parse_error_metadata(response_body)
 }

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission;

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission_input;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 pub(crate) mod shape_check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 pub(crate) mod shape_check_if_phone_number_is_opted_out_input;

+#[cfg(feature = "op_confirm_subscription")]
 pub(crate) mod shape_confirm_subscription;

+#[cfg(feature = "op_confirm_subscription")]
 pub(crate) mod shape_confirm_subscription_input;

+#[cfg(feature = "op_create_platform_application")]
 pub(crate) mod shape_create_platform_application;

+#[cfg(feature = "op_create_platform_application")]
 pub(crate) mod shape_create_platform_application_input;

+#[cfg(feature = "op_create_platform_endpoint")]
 pub(crate) mod shape_create_platform_endpoint;

+#[cfg(feature = "op_create_platform_endpoint")]
 pub(crate) mod shape_create_platform_endpoint_input;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_create_sms_sandbox_phone_number_input;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_create_topic;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_create_topic_input;

+#[cfg(feature = "op_delete_endpoint")]
 pub(crate) mod shape_delete_endpoint;

+#[cfg(feature = "op_delete_endpoint")]
 pub(crate) mod shape_delete_endpoint_input;

+#[cfg(feature = "op_delete_platform_application")]
 pub(crate) mod shape_delete_platform_application;

+#[cfg(feature = "op_delete_platform_application")]
 pub(crate) mod shape_delete_platform_application_input;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 pub(crate) mod shape_delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 pub(crate) mod shape_delete_sms_sandbox_phone_number_input;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_delete_topic;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_delete_topic_input;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy_input;

+#[cfg(feature = "op_get_endpoint_attributes")]
 pub(crate) mod shape_get_endpoint_attributes;

+#[cfg(feature = "op_get_endpoint_attributes")]
 pub(crate) mod shape_get_endpoint_attributes_input;

+#[cfg(feature = "op_get_platform_application_attributes")]
 pub(crate) mod shape_get_platform_application_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 pub(crate) mod shape_get_platform_application_attributes_input;

+#[cfg(feature = "op_get_sms_attributes")]
 pub(crate) mod shape_get_sms_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 pub(crate) mod shape_get_sms_attributes_input;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) mod shape_get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) mod shape_get_sms_sandbox_account_status_input;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_get_subscription_attributes;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_get_subscription_attributes_input;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_get_topic_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_get_topic_attributes_input;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_endpoints_by_platform_application_input;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_list_origination_numbers;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_list_origination_numbers_input;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_list_phone_numbers_opted_out_input;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_platform_applications;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_platform_applications_input;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_list_sms_sandbox_phone_numbers_input;

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) mod shape_list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) mod shape_list_subscriptions_by_topic;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) mod shape_list_subscriptions_by_topic_input;

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) mod shape_list_subscriptions_input;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource_input;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_list_topics;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_list_topics_input;

+#[cfg(feature = "op_opt_in_phone_number")]
 pub(crate) mod shape_opt_in_phone_number;

+#[cfg(feature = "op_opt_in_phone_number")]
 pub(crate) mod shape_opt_in_phone_number_input;

+#[cfg(feature = "op_publish")]
 pub(crate) mod shape_publish;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_input;

+#[cfg(feature = "op_publish")]
 pub(crate) mod shape_publish_input;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy_input;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission_input;

+#[cfg(feature = "op_set_endpoint_attributes")]
 pub(crate) mod shape_set_endpoint_attributes;

+#[cfg(feature = "op_set_endpoint_attributes")]
 pub(crate) mod shape_set_endpoint_attributes_input;

+#[cfg(feature = "op_set_platform_application_attributes")]
 pub(crate) mod shape_set_platform_application_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 pub(crate) mod shape_set_platform_application_attributes_input;

+#[cfg(feature = "op_set_sms_attributes")]
 pub(crate) mod shape_set_sms_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 pub(crate) mod shape_set_sms_attributes_input;

+#[cfg(feature = "op_set_subscription_attributes")]
 pub(crate) mod shape_set_subscription_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 pub(crate) mod shape_set_subscription_attributes_input;

+#[cfg(feature = "op_set_topic_attributes")]
 pub(crate) mod shape_set_topic_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 pub(crate) mod shape_set_topic_attributes_input;

+#[cfg(feature = "op_subscribe")]
 pub(crate) mod shape_subscribe;

+#[cfg(feature = "op_subscribe")]
 pub(crate) mod shape_subscribe_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_unsubscribe")]
 pub(crate) mod shape_unsubscribe;

+#[cfg(feature = "op_unsubscribe")]
 pub(crate) mod shape_unsubscribe_input;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verify_sms_sandbox_phone_number;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verify_sms_sandbox_phone_number_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_authorization_error_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_entry_ids_not_distinct_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_request_too_long_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_concurrent_access_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_empty_batch_request_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_endpoint_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub(crate) mod shape_filter_policy_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_internal_error_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_invalid_batch_entry_id_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_invalid_parameter_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_invalid_parameter_value_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub(crate) mod shape_invalid_security_exception;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_access_denied_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_disabled_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_not_found_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_opt_in_required;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_throttling_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_message_attribute_value;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_opted_out_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_platform_application_disabled_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_request_entry;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub(crate) mod shape_replay_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_stale_tag_exception;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub(crate) mod shape_subscription_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_policy_exception;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_throttled_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_too_many_entries_in_batch_request_exception;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_topic_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_user_error_exception;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verification_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_result_error_entry_list;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_of_endpoints;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_of_platform_applications;

+#[cfg(any(
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_platform_applications"
+))]
 pub(crate) mod shape_map_string_to_string;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_phone_number_information_list;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_phone_number_list;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_result_entry_list;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_sms_sandbox_phone_number_list;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_subscription_attributes_map;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub(crate) mod shape_subscriptions_list;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_tag_list;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_topic_attributes_map;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_topics_list;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_result_error_entry;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_endpoint;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_phone_number_information;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_platform_application;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_result_entry;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_sms_sandbox_phone_number;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub(crate) mod shape_subscription;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_topic;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_number_capability_list;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) fn get_sms_sandbox_account_status_output_output_correct_errors(
     mut builder: crate::operation::get_sms_sandbox_account_status::builders::GetSmsSandboxAccountStatusOutputBuilder,
 ) -> crate::operation::get_sms_sandbox_account_status::builders::GetSmsSandboxAccountStatusOutputBuilder {
@@ -8,6 +9,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub(crate) fn validation_exception_correct_errors(
     mut builder: crate::types::error::builders::ValidationExceptionBuilder,
 ) -> crate::types::error::builders::ValidationExceptionBuilder {
@@ -17,6 +23,7 @@
     builder
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn list_sms_sandbox_phone_numbers_output_output_correct_errors(
     mut builder: crate::operation::list_sms_sandbox_phone_numbers::builders::ListSmsSandboxPhoneNumbersOutputBuilder,
 ) -> crate::operation::list_sms_sandbox_phone_numbers::builders::ListSmsSandboxPhoneNumbersOutputBuilder {
@@ -26,6 +33,7 @@
     builder
 }

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) fn verification_exception_correct_errors(
     mut builder: crate::types::error::builders::VerificationExceptionBuilder,
 ) -> crate::types::error::builders::VerificationExceptionBuilder {
@@ -38,6 +46,7 @@
     builder
 }

+#[cfg(feature = "op_publish_batch")]
 pub(crate) fn batch_result_error_entry_correct_errors(
     mut builder: crate::types::builders::BatchResultErrorEntryBuilder,
 ) -> crate::types::builders::BatchResultErrorEntryBuilder {
@@ -53,6 +62,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
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
@@ -1,62 +1,100 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::_language_code_string::LanguageCodeString;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub use crate::types::_endpoint::Endpoint;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_phone_number_information::PhoneNumberInformation;

+#[cfg(feature = "op_list_platform_applications")]
 pub use crate::types::_platform_application::PlatformApplication;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number::SmsSandboxPhoneNumber;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub use crate::types::_subscription::Subscription;

+#[cfg(feature = "op_list_topics")]
 pub use crate::types::_topic::Topic;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::_message_attribute_value::MessageAttributeValue;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_request_entry::PublishBatchRequestEntry;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_result_entry::PublishBatchResultEntry;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntry;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_route_type::RouteType;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number_verification_status::SmsSandboxPhoneNumberVerificationStatus;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_number_capability::NumberCapability;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_result_error_entry;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 mod _endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod _language_code_string;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _message_attribute_value;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _number_capability;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _phone_number_information;

+#[cfg(feature = "op_list_platform_applications")]
 mod _platform_application;

+#[cfg(feature = "op_publish_batch")]
 mod _publish_batch_request_entry;

+#[cfg(feature = "op_publish_batch")]
 mod _publish_batch_result_entry;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _route_type;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod _sms_sandbox_phone_number;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod _sms_sandbox_phone_number_verification_status;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 mod _subscription;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(feature = "op_list_topics")]
 mod _topic;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,22 +1,37 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub use crate::types::_endpoint::EndpointBuilder;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_phone_number_information::PhoneNumberInformationBuilder;

+#[cfg(feature = "op_list_platform_applications")]
 pub use crate::types::_platform_application::PlatformApplicationBuilder;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number::SmsSandboxPhoneNumberBuilder;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub use crate::types::_subscription::SubscriptionBuilder;

+#[cfg(feature = "op_list_topics")]
 pub use crate::types::_topic::TopicBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::_message_attribute_value::MessageAttributeValueBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_request_entry::PublishBatchRequestEntryBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_result_entry::PublishBatchResultEntryBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntryBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,138 +1,630 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_authorization_error_exception::AuthorizationErrorException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_internal_error_exception::InternalErrorException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_throttled_exception::ThrottledException;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_filter_policy_limit_exceeded_exception::FilterPolicyLimitExceededException;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_replay_limit_exceeded_exception::ReplayLimitExceededException;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub use crate::types::error::_subscription_limit_exceeded_exception::SubscriptionLimitExceededException;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::error::_opted_out_exception::OptedOutException;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_user_error_exception::UserErrorException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_concurrent_access_exception::ConcurrentAccessException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_invalid_security_exception::InvalidSecurityException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_stale_tag_exception::StaleTagException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_limit_exceeded_exception::TagLimitExceededException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_policy_exception::TagPolicyException;

+#[cfg(feature = "op_create_topic")]
 pub use crate::types::error::_topic_limit_exceeded_exception::TopicLimitExceededException;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(feature = "op_delete_topic")]
 pub use crate::types::error::_invalid_state_exception::InvalidStateException;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_endpoint_disabled_exception::EndpointDisabledException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_invalid_parameter_value_exception::InvalidParameterValueException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_access_denied_exception::KmsAccessDeniedException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_disabled_exception::KmsDisabledException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_not_found_exception::KmsNotFoundException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequired;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_throttling_exception::KmsThrottlingException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_platform_application_disabled_exception::PlatformApplicationDisabledException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_entry_ids_not_distinct_exception::BatchEntryIdsNotDistinctException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_request_too_long_exception::BatchRequestTooLongException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_empty_batch_request_exception::EmptyBatchRequestException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_invalid_batch_entry_id_exception::InvalidBatchEntryIdException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_too_many_entries_in_batch_request_exception::TooManyEntriesInBatchRequestException;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub use crate::types::error::_verification_exception::VerificationException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _authorization_error_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_entry_ids_not_distinct_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_request_too_long_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _concurrent_access_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _empty_batch_request_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _endpoint_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 mod _filter_policy_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _internal_error_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _invalid_batch_entry_id_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _invalid_parameter_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _invalid_parameter_value_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 mod _invalid_security_exception;

+#[cfg(feature = "op_delete_topic")]
 mod _invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_access_denied_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_disabled_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_not_found_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_opt_in_required;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_throttling_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 mod _not_found_exception;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod _opted_out_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _platform_application_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 mod _replay_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _stale_tag_exception;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 mod _subscription_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_policy_exception;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _throttled_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _too_many_entries_in_batch_request_exception;

+#[cfg(feature = "op_create_topic")]
 mod _topic_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 mod _user_error_exception;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 mod _validation_exception;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 mod _verification_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,68 +1,314 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_authorization_error_exception::AuthorizationErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_internal_error_exception::InternalErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_throttled_exception::ThrottledExceptionBuilder;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_filter_policy_limit_exceeded_exception::FilterPolicyLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_replay_limit_exceeded_exception::ReplayLimitExceededExceptionBuilder;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub use crate::types::error::_subscription_limit_exceeded_exception::SubscriptionLimitExceededExceptionBuilder;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::error::_opted_out_exception::OptedOutExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_user_error_exception::UserErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_concurrent_access_exception::ConcurrentAccessExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_invalid_security_exception::InvalidSecurityExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_stale_tag_exception::StaleTagExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_limit_exceeded_exception::TagLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_policy_exception::TagPolicyExceptionBuilder;

+#[cfg(feature = "op_create_topic")]
 pub use crate::types::error::_topic_limit_exceeded_exception::TopicLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(feature = "op_delete_topic")]
 pub use crate::types::error::_invalid_state_exception::InvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_endpoint_disabled_exception::EndpointDisabledExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_invalid_parameter_value_exception::InvalidParameterValueExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_access_denied_exception::KmsAccessDeniedExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_disabled_exception::KmsDisabledExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_not_found_exception::KmsNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequiredBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_throttling_exception::KmsThrottlingExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_platform_application_disabled_exception::PlatformApplicationDisabledExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_entry_ids_not_distinct_exception::BatchEntryIdsNotDistinctExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_request_too_long_exception::BatchRequestTooLongExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_empty_batch_request_exception::EmptyBatchRequestExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_invalid_batch_entry_id_exception::InvalidBatchEntryIdExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_too_many_entries_in_batch_request_exception::TooManyEntriesInBatchRequestExceptionBuilder;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub use crate::types::error::_verification_exception::VerificationExceptionBuilder;
```

## Unified diff

```diff
diff --git a/Cargo.toml b/Cargo.toml
--- a/Cargo.toml
+++ b/Cargo.toml
@@ -19,58 +19,45 @@
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

 [dependencies.aws-smithy-query]
-path = "../aws-smithy-query"
 version = "0.62.0"

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

 [dependencies.aws-smithy-xml]
-path = "../aws-smithy-xml"
 version = "0.62.0"

 [dependencies.aws-types]
-path = "../aws-types"
 version = "1.6.0"

 [dependencies.fastrand]
@@ -89,11 +76,9 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -112,6 +97,48 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_add_permission = []
+op_check_if_phone_number_is_opted_out = []
+op_confirm_subscription = []
+op_create_platform_application = []
+op_create_platform_endpoint = []
+op_create_sms_sandbox_phone_number = []
+op_create_topic = []
+op_delete_endpoint = []
+op_delete_platform_application = []
+op_delete_sms_sandbox_phone_number = []
+op_delete_topic = []
+op_get_data_protection_policy = []
+op_get_endpoint_attributes = []
+op_get_platform_application_attributes = []
+op_get_sms_attributes = []
+op_get_sms_sandbox_account_status = []
+op_get_subscription_attributes = []
+op_get_topic_attributes = []
+op_list_endpoints_by_platform_application = []
+op_list_origination_numbers = []
+op_list_phone_numbers_opted_out = []
+op_list_platform_applications = []
+op_list_sms_sandbox_phone_numbers = []
+op_list_subscriptions = []
+op_list_subscriptions_by_topic = []
+op_list_tags_for_resource = []
+op_list_topics = []
+op_opt_in_phone_number = []
+op_publish = []
+op_publish_batch = []
+op_put_data_protection_policy = []
+op_remove_permission = []
+op_set_endpoint_attributes = []
+op_set_platform_application_attributes = []
+op_set_sms_attributes = []
+op_set_subscription_attributes = []
+op_set_topic_attributes = []
+op_subscribe = []
+op_tag_resource = []
+op_unsubscribe = []
+op_untag_resource = []
+op_verify_sms_sandbox_phone_number = []

 [hints]
 mostly-unused = true
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,18 +136,25 @@
     }
 }

+#[cfg(feature = "op_add_permission")]
 mod add_permission;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 mod check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_confirm_subscription")]
 mod confirm_subscription;

+#[cfg(feature = "op_create_platform_application")]
 mod create_platform_application;

+#[cfg(feature = "op_create_platform_endpoint")]
 mod create_platform_endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_topic")]
 mod create_topic;

 /// Operation customization and supporting types.
@@ -177,72 +184,107 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_endpoint")]
 mod delete_endpoint;

+#[cfg(feature = "op_delete_platform_application")]
 mod delete_platform_application;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 mod delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_topic")]
 mod delete_topic;

+#[cfg(feature = "op_get_data_protection_policy")]
 mod get_data_protection_policy;

+#[cfg(feature = "op_get_endpoint_attributes")]
 mod get_endpoint_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 mod get_platform_application_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 mod get_sms_attributes;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 mod get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_subscription_attributes")]
 mod get_subscription_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 mod get_topic_attributes;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 mod list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_origination_numbers")]
 mod list_origination_numbers;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 mod list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_platform_applications")]
 mod list_platform_applications;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_subscriptions")]
 mod list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 mod list_subscriptions_by_topic;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_topics")]
 mod list_topics;

+#[cfg(feature = "op_opt_in_phone_number")]
 mod opt_in_phone_number;

+#[cfg(feature = "op_publish")]
 mod publish;

+#[cfg(feature = "op_publish_batch")]
 mod publish_batch;

+#[cfg(feature = "op_put_data_protection_policy")]
 mod put_data_protection_policy;

+#[cfg(feature = "op_remove_permission")]
 mod remove_permission;

+#[cfg(feature = "op_set_endpoint_attributes")]
 mod set_endpoint_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 mod set_platform_application_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 mod set_sms_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 mod set_subscription_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 mod set_topic_attributes;

+#[cfg(feature = "op_subscribe")]
 mod subscribe;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_unsubscribe")]
 mod unsubscribe;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 mod verify_sms_sandbox_phone_number;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,72 +3,318 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_tag_resource",
+        feature = "op_unsubscribe",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that the user has been denied access to the requested resource.</p>
     AuthorizationErrorException(crate::types::error::AuthorizationErrorException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>Two or more batch entries in the request have the same <code>Id</code>.</p>
     BatchEntryIdsNotDistinctException(crate::types::error::BatchEntryIdsNotDistinctException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The length of all the batch messages put together is more than the limit.</p>
     BatchRequestTooLongException(crate::types::error::BatchRequestTooLongException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>Can't perform multiple operations on a tag simultaneously. Perform the operations sequentially.</p>
     ConcurrentAccessException(crate::types::error::ConcurrentAccessException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The batch request doesn't contain any entries.</p>
     EmptyBatchRequestException(crate::types::error::EmptyBatchRequestException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Exception error indicating endpoint disabled.</p>
     EndpointDisabledException(crate::types::error::EndpointDisabledException),
+    #[cfg(any(
+        feature = "op_confirm_subscription",
+        feature = "op_set_subscription_attributes",
+        feature = "op_subscribe"
+    ))]
     /// <p>Indicates that the number of filter polices in your Amazon Web Services account exceeds the limit. To add more filter polices, submit an Amazon SNS Limit Increase case in the Amazon Web Services Support Center.</p>
     FilterPolicyLimitExceededException(crate::types::error::FilterPolicyLimitExceededException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates an internal service error.</p>
     InternalErrorException(crate::types::error::InternalErrorException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The <code>Id</code> of a batch entry in a batch request doesn't abide by the specification.</p>
     InvalidBatchEntryIdException(crate::types::error::InvalidBatchEntryIdException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_application",
+        feature = "op_create_platform_endpoint",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_create_topic",
+        feature = "op_delete_endpoint",
+        feature = "op_delete_platform_application",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_platform_applications",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_subscriptions",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_topics",
+        feature = "op_opt_in_phone_number",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_sms_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_tag_resource",
+        feature = "op_unsubscribe",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     InvalidParameterException(crate::types::error::InvalidParameterException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     InvalidParameterValueException(crate::types::error::InvalidParameterValueException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_topic_attributes",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe"
+    ))]
     /// <p>The credential signature isn't valid. You must use an HTTPS endpoint and sign your request using Signature Version 4.</p>
     InvalidSecurityException(crate::types::error::InvalidSecurityException),
+    #[cfg(feature = "op_delete_topic")]
     /// <p>Indicates that the specified state is not a valid state for an event source.</p>
     InvalidStateException(crate::types::error::InvalidStateException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The ciphertext references a key that doesn't exist or that you don't have access to.</p>
     KmsAccessDeniedException(crate::types::error::KmsAccessDeniedException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the specified Amazon Web Services KMS key isn't enabled.</p>
     KmsDisabledException(crate::types::error::KmsDisabledException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the state of the specified resource isn't valid for this request. For more information, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/key-state.html">Key states of Amazon Web Services KMS keys</a> in the <i>Key Management Service Developer Guide</i>.</p>
     KmsInvalidStateException(crate::types::error::KmsInvalidStateException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was rejected because the specified entity or resource can't be found.</p>
     KmsNotFoundException(crate::types::error::KmsNotFoundException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The Amazon Web Services access key ID needs a subscription for the service.</p>
     KmsOptInRequired(crate::types::error::KmsOptInRequired),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>The request was denied due to request throttling. For more information about throttling, see <a href="https://docs.aws.amazon.com/kms/latest/developerguide/limits.html#requests-per-second">Limits</a> in the <i>Key Management Service Developer Guide.</i></p>
     KmsThrottlingException(crate::types::error::KmsThrottlingException),
+    #[cfg(any(
+        feature = "op_add_permission",
+        feature = "op_confirm_subscription",
+        feature = "op_create_platform_endpoint",
+        feature = "op_delete_topic",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_endpoint_attributes",
+        feature = "op_get_platform_application_attributes",
+        feature = "op_get_subscription_attributes",
+        feature = "op_get_topic_attributes",
+        feature = "op_list_endpoints_by_platform_application",
+        feature = "op_list_subscriptions_by_topic",
+        feature = "op_publish",
+        feature = "op_publish_batch",
+        feature = "op_put_data_protection_policy",
+        feature = "op_remove_permission",
+        feature = "op_set_endpoint_attributes",
+        feature = "op_set_platform_application_attributes",
+        feature = "op_set_subscription_attributes",
+        feature = "op_set_topic_attributes",
+        feature = "op_subscribe",
+        feature = "op_unsubscribe"
+    ))]
     /// <p>Indicates that the requested resource does not exist.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(feature = "op_create_sms_sandbox_phone_number")]
     /// <p>Indicates that the specified phone number opted out of receiving SMS messages from your Amazon Web Services account. You can't send SMS messages to phone numbers that opt out.</p>
     OptedOutException(crate::types::error::OptedOutException),
+    #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
     /// <p>Exception error indicating platform application disabled.</p>
     PlatformApplicationDisabledException(crate::types::error::PlatformApplicationDisabledException),
+    #[cfg(any(
+        feature = "op_confirm_subscription",
+        feature = "op_set_subscription_attributes",
+        feature = "op_subscribe"
+    ))]
     /// <p>Indicates that the request parameter has exceeded the maximum number of concurrent message replays.</p>
     ReplayLimitExceededException(crate::types::error::ReplayLimitExceededException),
+    #[cfg(any(
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Can’t perform the action on the specified resource. Make sure that the resource exists.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>A tag has been added to a resource with the same ARN as a deleted resource. Wait a short while and then retry the operation.</p>
     StaleTagException(crate::types::error::StaleTagException),
+    #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
     /// <p>Indicates that the customer already owns the maximum allowed number of subscriptions.</p>
     SubscriptionLimitExceededException(crate::types::error::SubscriptionLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>Can't add more than 50 tags to a topic.</p>
     TagLimitExceededException(crate::types::error::TagLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_topic",
+        feature = "op_delete_topic",
+        feature = "op_list_tags_for_resource",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource"
+    ))]
     /// <p>The request doesn't comply with the IAM tag policy. Correct your request and then retry it.</p>
     TagPolicyException(crate::types::error::TagPolicyException),
+    #[cfg(any(
+        feature = "op_check_if_phone_number_is_opted_out",
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_delete_sms_sandbox_phone_number",
+        feature = "op_get_sms_attributes",
+        feature = "op_get_sms_sandbox_account_status",
+        feature = "op_list_origination_numbers",
+        feature = "op_list_phone_numbers_opted_out",
+        feature = "op_list_sms_sandbox_phone_numbers",
+        feature = "op_opt_in_phone_number",
+        feature = "op_set_sms_attributes",
+        feature = "op_verify_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that the rate at which requests have been submitted for this action exceeds the limit for your Amazon Web Services account.</p>
     ThrottledException(crate::types::error::ThrottledException),
+    #[cfg(feature = "op_publish_batch")]
     /// <p>The batch request contains more entries than permissible (more than 10).</p>
     TooManyEntriesInBatchRequestException(crate::types::error::TooManyEntriesInBatchRequestException),
+    #[cfg(feature = "op_create_topic")]
     /// <p>Indicates that the customer already owns the maximum allowed number of topics.</p>
     TopicLimitExceededException(crate::types::error::TopicLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_sms_sandbox_phone_number",
+        feature = "op_delete_sms_sandbox_phone_number"
+    ))]
     /// <p>Indicates that a request parameter does not comply with the associated constraints.</p>
     UserErrorException(crate::types::error::UserErrorException),
+    #[cfg(any(
+        feature = "op_list_origination_numbers",
+        feature = "op_publish",
+        feature = "op_publish_batch"
+    ))]
     /// <p>Indicates that a parameter in the request is invalid.</p>
     ValidationException(crate::types::error::ValidationException),
+    #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
     /// <p>Indicates that the one-time password (OTP) used for verification is invalid.</p>
     VerificationException(crate::types::error::VerificationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -85,39 +331,285 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::AuthorizationErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchEntryIdsNotDistinctException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchRequestTooLongException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::ConcurrentAccessException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::EmptyBatchRequestException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::EndpointDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::FilterPolicyLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InternalErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::InvalidBatchEntryIdException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InvalidParameterException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::InvalidParameterValueException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::InvalidSecurityException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_delete_topic")]
             Error::InvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsAccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsInvalidStateException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsOptInRequired(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Error::OptedOutException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::PlatformApplicationDisabledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::ReplayLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::StaleTagException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Error::SubscriptionLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagPolicyException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ThrottledException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_publish_batch")]
             Error::TooManyEntriesInBatchRequestException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_topic")]
             Error::TopicLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Error::UserErrorException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Error::VerificationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -142,44 +634,291 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::AuthorizationErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchEntryIdsNotDistinctException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchRequestTooLongException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::ConcurrentAccessException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::EmptyBatchRequestException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::EndpointDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::FilterPolicyLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InternalErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::InvalidBatchEntryIdException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InvalidParameterException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::InvalidParameterValueException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::InvalidSecurityException(inner) => inner.meta(),
+            #[cfg(feature = "op_delete_topic")]
             Self::InvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsAccessDeniedException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsDisabledException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsInvalidStateException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsOptInRequired(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Self::OptedOutException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::PlatformApplicationDisabledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::ReplayLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::StaleTagException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Self::SubscriptionLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagPolicyException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ThrottledException(inner) => inner.meta(),
+            #[cfg(feature = "op_publish_batch")]
             Self::TooManyEntriesInBatchRequestException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_topic")]
             Self::TopicLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Self::UserErrorException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Self::VerificationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::add_permission::AddPermissionError, R>>
     for Error
@@ -201,6 +940,7 @@
         }
     }
 }
+#[cfg(feature = "op_add_permission")]
 impl From<crate::operation::add_permission::AddPermissionError> for Error {
     fn from(err: crate::operation::add_permission::AddPermissionError) -> Self {
         match err {
@@ -220,6 +960,7 @@
         }
     }
 }
+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -245,6 +986,7 @@
         }
     }
 }
+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 impl From<crate::operation::check_if_phone_number_is_opted_out::CheckIfPhoneNumberIsOptedOutError> for Error {
     fn from(err: crate::operation::check_if_phone_number_is_opted_out::CheckIfPhoneNumberIsOptedOutError) -> Self {
         match err {
@@ -264,6 +1006,7 @@
         }
     }
 }
+#[cfg(feature = "op_confirm_subscription")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -289,6 +1032,7 @@
         }
     }
 }
+#[cfg(feature = "op_confirm_subscription")]
 impl From<crate::operation::confirm_subscription::ConfirmSubscriptionError> for Error {
     fn from(err: crate::operation::confirm_subscription::ConfirmSubscriptionError) -> Self {
         match err {
@@ -319,6 +1063,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -344,6 +1089,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_application")]
 impl From<crate::operation::create_platform_application::CreatePlatformApplicationError> for Error {
     fn from(err: crate::operation::create_platform_application::CreatePlatformApplicationError) -> Self {
         match err {
@@ -360,6 +1106,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -385,6 +1132,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_platform_endpoint")]
 impl From<crate::operation::create_platform_endpoint::CreatePlatformEndpointError> for Error {
     fn from(err: crate::operation::create_platform_endpoint::CreatePlatformEndpointError) -> Self {
         match err {
@@ -406,6 +1154,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -431,6 +1180,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 impl From<crate::operation::create_sms_sandbox_phone_number::CreateSMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::create_sms_sandbox_phone_number::CreateSMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -456,6 +1206,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_topic")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_topic::CreateTopicError, R>>
     for Error
 where
@@ -473,6 +1224,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_topic")]
 impl From<crate::operation::create_topic::CreateTopicError> for Error {
     fn from(err: crate::operation::create_topic::CreateTopicError) -> Self {
         match err {
@@ -507,6 +1259,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_endpoint")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_endpoint::DeleteEndpointError, R>>
     for Error
@@ -528,6 +1281,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_endpoint")]
 impl From<crate::operation::delete_endpoint::DeleteEndpointError> for Error {
     fn from(err: crate::operation::delete_endpoint::DeleteEndpointError) -> Self {
         match err {
@@ -544,6 +1298,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -569,6 +1324,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_platform_application")]
 impl From<crate::operation::delete_platform_application::DeletePlatformApplicationError> for Error {
     fn from(err: crate::operation::delete_platform_application::DeletePlatformApplicationError) -> Self {
         match err {
@@ -585,6 +1341,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -610,6 +1367,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 impl From<crate::operation::delete_sms_sandbox_phone_number::DeleteSMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::delete_sms_sandbox_phone_number::DeleteSMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -635,6 +1393,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_topic")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_topic::DeleteTopicError, R>>
     for Error
 where
@@ -652,6 +1411,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_topic")]
 impl From<crate::operation::delete_topic::DeleteTopicError> for Error {
     fn from(err: crate::operation::delete_topic::DeleteTopicError) -> Self {
         match err {
@@ -683,6 +1443,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -708,6 +1469,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl From<crate::operation::get_data_protection_policy::GetDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::get_data_protection_policy::GetDataProtectionPolicyError) -> Self {
         match err {
@@ -732,6 +1494,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_endpoint_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -757,6 +1520,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_endpoint_attributes")]
 impl From<crate::operation::get_endpoint_attributes::GetEndpointAttributesError> for Error {
     fn from(err: crate::operation::get_endpoint_attributes::GetEndpointAttributesError) -> Self {
         match err {
@@ -778,6 +1542,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_platform_application_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -803,6 +1568,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_platform_application_attributes")]
 impl From<crate::operation::get_platform_application_attributes::GetPlatformApplicationAttributesError> for Error {
     fn from(err: crate::operation::get_platform_application_attributes::GetPlatformApplicationAttributesError) -> Self {
         match err {
@@ -822,6 +1588,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -847,6 +1614,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_attributes")]
 impl From<crate::operation::get_sms_attributes::GetSMSAttributesError> for Error {
     fn from(err: crate::operation::get_sms_attributes::GetSMSAttributesError) -> Self {
         match err {
@@ -866,6 +1634,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -891,6 +1660,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 impl From<crate::operation::get_sms_sandbox_account_status::GetSMSSandboxAccountStatusError> for Error {
     fn from(err: crate::operation::get_sms_sandbox_account_status::GetSMSSandboxAccountStatusError) -> Self {
         match err {
@@ -907,6 +1677,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_subscription_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -932,6 +1703,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_subscription_attributes")]
 impl From<crate::operation::get_subscription_attributes::GetSubscriptionAttributesError> for Error {
     fn from(err: crate::operation::get_subscription_attributes::GetSubscriptionAttributesError) -> Self {
         match err {
@@ -951,6 +1723,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_topic_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -976,6 +1749,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_topic_attributes")]
 impl From<crate::operation::get_topic_attributes::GetTopicAttributesError> for Error {
     fn from(err: crate::operation::get_topic_attributes::GetTopicAttributesError) -> Self {
         match err {
@@ -1000,6 +1774,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1025,6 +1800,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 impl From<crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationError> for Error {
     fn from(
         err: crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationError,
@@ -1048,6 +1824,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_origination_numbers")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1073,6 +1850,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_origination_numbers")]
 impl From<crate::operation::list_origination_numbers::ListOriginationNumbersError> for Error {
     fn from(err: crate::operation::list_origination_numbers::ListOriginationNumbersError) -> Self {
         match err {
@@ -1097,6 +1875,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1122,6 +1901,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 impl From<crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutError> for Error {
     fn from(err: crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutError) -> Self {
         match err {
@@ -1141,6 +1921,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_platform_applications")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1166,6 +1947,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_platform_applications")]
 impl From<crate::operation::list_platform_applications::ListPlatformApplicationsError> for Error {
     fn from(err: crate::operation::list_platform_applications::ListPlatformApplicationsError) -> Self {
         match err {
@@ -1182,6 +1964,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1207,6 +1990,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 impl From<crate::operation::list_sms_sandbox_phone_numbers::ListSMSSandboxPhoneNumbersError> for Error {
     fn from(err: crate::operation::list_sms_sandbox_phone_numbers::ListSMSSandboxPhoneNumbersError) -> Self {
         match err {
@@ -1229,6 +2013,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1254,6 +2039,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions")]
 impl From<crate::operation::list_subscriptions::ListSubscriptionsError> for Error {
     fn from(err: crate::operation::list_subscriptions::ListSubscriptionsError) -> Self {
         match err {
@@ -1270,6 +2056,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions_by_topic")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1295,6 +2082,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_subscriptions_by_topic")]
 impl From<crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicError> for Error {
     fn from(err: crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicError) -> Self {
         match err {
@@ -1312,6 +2100,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1337,6 +2126,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -1361,6 +2151,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_topics")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_topics::ListTopicsError, R>>
     for Error
 where
@@ -1378,6 +2169,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_topics")]
 impl From<crate::operation::list_topics::ListTopicsError> for Error {
     fn from(err: crate::operation::list_topics::ListTopicsError) -> Self {
         match err {
@@ -1394,6 +2186,7 @@
         }
     }
 }
+#[cfg(feature = "op_opt_in_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1419,6 +2212,7 @@
         }
     }
 }
+#[cfg(feature = "op_opt_in_phone_number")]
 impl From<crate::operation::opt_in_phone_number::OptInPhoneNumberError> for Error {
     fn from(err: crate::operation::opt_in_phone_number::OptInPhoneNumberError) -> Self {
         match err {
@@ -1438,6 +2232,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::publish::PublishError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1454,6 +2249,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish")]
 impl From<crate::operation::publish::PublishError> for Error {
     fn from(err: crate::operation::publish::PublishError) -> Self {
         match err {
@@ -1496,6 +2292,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish_batch")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::publish_batch::PublishBatchError, R>>
     for Error
 where
@@ -1513,6 +2310,7 @@
         }
     }
 }
+#[cfg(feature = "op_publish_batch")]
 impl From<crate::operation::publish_batch::PublishBatchError> for Error {
     fn from(err: crate::operation::publish_batch::PublishBatchError) -> Self {
         match err {
@@ -1580,6 +2378,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1605,6 +2404,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl From<crate::operation::put_data_protection_policy::PutDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::put_data_protection_policy::PutDataProtectionPolicyError) -> Self {
         match err {
@@ -1629,6 +2429,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1654,6 +2455,7 @@
         }
     }
 }
+#[cfg(feature = "op_remove_permission")]
 impl From<crate::operation::remove_permission::RemovePermissionError> for Error {
     fn from(err: crate::operation::remove_permission::RemovePermissionError) -> Self {
         match err {
@@ -1673,6 +2475,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_endpoint_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1698,6 +2501,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_endpoint_attributes")]
 impl From<crate::operation::set_endpoint_attributes::SetEndpointAttributesError> for Error {
     fn from(err: crate::operation::set_endpoint_attributes::SetEndpointAttributesError) -> Self {
         match err {
@@ -1719,6 +2523,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_platform_application_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1744,6 +2549,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_platform_application_attributes")]
 impl From<crate::operation::set_platform_application_attributes::SetPlatformApplicationAttributesError> for Error {
     fn from(err: crate::operation::set_platform_application_attributes::SetPlatformApplicationAttributesError) -> Self {
         match err {
@@ -1763,6 +2569,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_sms_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1788,6 +2595,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_sms_attributes")]
 impl From<crate::operation::set_sms_attributes::SetSMSAttributesError> for Error {
     fn from(err: crate::operation::set_sms_attributes::SetSMSAttributesError) -> Self {
         match err {
@@ -1807,6 +2615,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_subscription_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1832,6 +2641,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_subscription_attributes")]
 impl From<crate::operation::set_subscription_attributes::SetSubscriptionAttributesError> for Error {
     fn from(err: crate::operation::set_subscription_attributes::SetSubscriptionAttributesError) -> Self {
         match err {
@@ -1857,6 +2667,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_topic_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1882,6 +2693,7 @@
         }
     }
 }
+#[cfg(feature = "op_set_topic_attributes")]
 impl From<crate::operation::set_topic_attributes::SetTopicAttributesError> for Error {
     fn from(err: crate::operation::set_topic_attributes::SetTopicAttributesError) -> Self {
         match err {
@@ -1906,6 +2718,7 @@
         }
     }
 }
+#[cfg(feature = "op_subscribe")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::subscribe::SubscribeError, R>>
     for Error
 where
@@ -1923,6 +2736,7 @@
         }
     }
 }
+#[cfg(feature = "op_subscribe")]
 impl From<crate::operation::subscribe::SubscribeError> for Error {
     fn from(err: crate::operation::subscribe::SubscribeError) -> Self {
         match err {
@@ -1952,6 +2766,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -1969,6 +2784,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -1997,6 +2813,7 @@
         }
     }
 }
+#[cfg(feature = "op_unsubscribe")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::unsubscribe::UnsubscribeError, R>>
     for Error
 where
@@ -2014,6 +2831,7 @@
         }
     }
 }
+#[cfg(feature = "op_unsubscribe")]
 impl From<crate::operation::unsubscribe::UnsubscribeError> for Error {
     fn from(err: crate::operation::unsubscribe::UnsubscribeError) -> Self {
         match err {
@@ -2036,6 +2854,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2057,6 +2876,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2085,6 +2905,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2110,6 +2931,7 @@
         }
     }
 }
+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 impl From<crate::operation::verify_sms_sandbox_phone_number::VerifySMSSandboxPhoneNumberError> for Error {
     fn from(err: crate::operation::verify_sms_sandbox_phone_number::VerifySMSSandboxPhoneNumberError) -> Self {
         match err {
@@ -2138,39 +2960,285 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::AuthorizationErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchEntryIdsNotDistinctException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::BatchRequestTooLongException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::ConcurrentAccessException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::EmptyBatchRequestException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::EndpointDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::FilterPolicyLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InternalErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::InvalidBatchEntryIdException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::InvalidParameterException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::InvalidParameterValueException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::InvalidSecurityException(inner) => inner.source(),
+            #[cfg(feature = "op_delete_topic")]
             Error::InvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsAccessDeniedException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsDisabledException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsInvalidStateException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsOptInRequired(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::KmsThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Error::OptedOutException(inner) => inner.source(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Error::PlatformApplicationDisabledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Error::ReplayLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::StaleTagException(inner) => inner.source(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Error::SubscriptionLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Error::TagPolicyException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Error::ThrottledException(inner) => inner.source(),
+            #[cfg(feature = "op_publish_batch")]
             Error::TooManyEntriesInBatchRequestException(inner) => inner.source(),
+            #[cfg(feature = "op_create_topic")]
             Error::TopicLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Error::UserErrorException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Error::ValidationException(inner) => inner.source(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Error::VerificationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2179,39 +3247,285 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::AuthorizationErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchEntryIdsNotDistinctException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::BatchRequestTooLongException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::ConcurrentAccessException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::EmptyBatchRequestException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::EndpointDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::FilterPolicyLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InternalErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::InvalidBatchEntryIdException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_application",
+                feature = "op_create_platform_endpoint",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_create_topic",
+                feature = "op_delete_endpoint",
+                feature = "op_delete_platform_application",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_platform_applications",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_subscriptions",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_topics",
+                feature = "op_opt_in_phone_number",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_sms_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_tag_resource",
+                feature = "op_unsubscribe",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::InvalidParameterException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::InvalidParameterValueException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_topic_attributes",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::InvalidSecurityException(e) => e.request_id(),
+            #[cfg(feature = "op_delete_topic")]
             Self::InvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsAccessDeniedException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsDisabledException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsInvalidStateException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsOptInRequired(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::KmsThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_add_permission",
+                feature = "op_confirm_subscription",
+                feature = "op_create_platform_endpoint",
+                feature = "op_delete_topic",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_endpoint_attributes",
+                feature = "op_get_platform_application_attributes",
+                feature = "op_get_subscription_attributes",
+                feature = "op_get_topic_attributes",
+                feature = "op_list_endpoints_by_platform_application",
+                feature = "op_list_subscriptions_by_topic",
+                feature = "op_publish",
+                feature = "op_publish_batch",
+                feature = "op_put_data_protection_policy",
+                feature = "op_remove_permission",
+                feature = "op_set_endpoint_attributes",
+                feature = "op_set_platform_application_attributes",
+                feature = "op_set_subscription_attributes",
+                feature = "op_set_topic_attributes",
+                feature = "op_subscribe",
+                feature = "op_unsubscribe"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_create_sms_sandbox_phone_number")]
             Self::OptedOutException(e) => e.request_id(),
+            #[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
             Self::PlatformApplicationDisabledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_confirm_subscription",
+                feature = "op_set_subscription_attributes",
+                feature = "op_subscribe"
+            ))]
             Self::ReplayLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::StaleTagException(e) => e.request_id(),
+            #[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
             Self::SubscriptionLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_topic",
+                feature = "op_delete_topic",
+                feature = "op_list_tags_for_resource",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource"
+            ))]
             Self::TagPolicyException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_check_if_phone_number_is_opted_out",
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number",
+                feature = "op_get_sms_attributes",
+                feature = "op_get_sms_sandbox_account_status",
+                feature = "op_list_origination_numbers",
+                feature = "op_list_phone_numbers_opted_out",
+                feature = "op_list_sms_sandbox_phone_numbers",
+                feature = "op_opt_in_phone_number",
+                feature = "op_set_sms_attributes",
+                feature = "op_verify_sms_sandbox_phone_number"
+            ))]
             Self::ThrottledException(e) => e.request_id(),
+            #[cfg(feature = "op_publish_batch")]
             Self::TooManyEntriesInBatchRequestException(e) => e.request_id(),
+            #[cfg(feature = "op_create_topic")]
             Self::TopicLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_sms_sandbox_phone_number",
+                feature = "op_delete_sms_sandbox_phone_number"
+            ))]
             Self::UserErrorException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_list_origination_numbers",
+                feature = "op_publish",
+                feature = "op_publish_batch"
+            ))]
             Self::ValidationException(e) => e.request_id(),
+            #[cfg(feature = "op_verify_sms_sandbox_phone_number")]
             Self::VerificationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) fn reflens_list_endpoints_by_platform_application_output_output_next_token(
     input: &crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) fn reflens_list_origination_numbers_output_output_next_token(
     input: &crate::operation::list_origination_numbers::ListOriginationNumbersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) fn reflens_list_phone_numbers_opted_out_output_output_next_token(
     input: &crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) fn reflens_list_platform_applications_output_output_next_token(
     input: &crate::operation::list_platform_applications::ListPlatformApplicationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn reflens_list_sms_sandbox_phone_numbers_output_output_next_token(
     input: &crate::operation::list_sms_sandbox_phone_numbers::ListSmsSandboxPhoneNumbersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) fn reflens_list_subscriptions_output_output_next_token(
     input: &crate::operation::list_subscriptions::ListSubscriptionsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) fn reflens_list_subscriptions_by_topic_output_output_next_token(
     input: &crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_topics")]
 pub(crate) fn reflens_list_topics_output_output_next_token(
     input: &crate::operation::list_topics::ListTopicsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) fn lens_list_endpoints_by_platform_application_output_output_endpoints(
     input: crate::operation::list_endpoints_by_platform_application::ListEndpointsByPlatformApplicationOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Endpoint>> {
@@ -86,6 +95,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) fn lens_list_origination_numbers_output_output_phone_numbers(
     input: crate::operation::list_origination_numbers::ListOriginationNumbersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::PhoneNumberInformation>> {
@@ -93,6 +103,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) fn lens_list_phone_numbers_opted_out_output_output_phone_numbers(
     input: crate::operation::list_phone_numbers_opted_out::ListPhoneNumbersOptedOutOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -100,6 +111,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) fn lens_list_platform_applications_output_output_platform_applications(
     input: crate::operation::list_platform_applications::ListPlatformApplicationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::PlatformApplication>> {
@@ -107,6 +119,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn lens_list_sms_sandbox_phone_numbers_output_output_phone_numbers(
     input: crate::operation::list_sms_sandbox_phone_numbers::ListSmsSandboxPhoneNumbersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SmsSandboxPhoneNumber>> {
@@ -114,6 +127,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) fn lens_list_subscriptions_output_output_subscriptions(
     input: crate::operation::list_subscriptions::ListSubscriptionsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Subscription>> {
@@ -121,6 +135,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) fn lens_list_subscriptions_by_topic_output_output_subscriptions(
     input: crate::operation::list_subscriptions_by_topic::ListSubscriptionsByTopicOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Subscription>> {
@@ -128,6 +143,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_topics")]
 pub(crate) fn lens_list_topics_output_output_topics(
     input: crate::operation::list_topics::ListTopicsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Topic>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,128 +1,170 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_add_permission")]
 /// Types for the `AddPermission` operation.
 pub mod add_permission;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 /// Types for the `CheckIfPhoneNumberIsOptedOut` operation.
 pub mod check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_confirm_subscription")]
 /// Types for the `ConfirmSubscription` operation.
 pub mod confirm_subscription;

+#[cfg(feature = "op_create_platform_application")]
 /// Types for the `CreatePlatformApplication` operation.
 pub mod create_platform_application;

+#[cfg(feature = "op_create_platform_endpoint")]
 /// Types for the `CreatePlatformEndpoint` operation.
 pub mod create_platform_endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 /// Types for the `CreateSMSSandboxPhoneNumber` operation.
 pub mod create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_topic")]
 /// Types for the `CreateTopic` operation.
 pub mod create_topic;

+#[cfg(feature = "op_delete_endpoint")]
 /// Types for the `DeleteEndpoint` operation.
 pub mod delete_endpoint;

+#[cfg(feature = "op_delete_platform_application")]
 /// Types for the `DeletePlatformApplication` operation.
 pub mod delete_platform_application;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 /// Types for the `DeleteSMSSandboxPhoneNumber` operation.
 pub mod delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_topic")]
 /// Types for the `DeleteTopic` operation.
 pub mod delete_topic;

+#[cfg(feature = "op_get_data_protection_policy")]
 /// Types for the `GetDataProtectionPolicy` operation.
 pub mod get_data_protection_policy;

+#[cfg(feature = "op_get_endpoint_attributes")]
 /// Types for the `GetEndpointAttributes` operation.
 pub mod get_endpoint_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 /// Types for the `GetPlatformApplicationAttributes` operation.
 pub mod get_platform_application_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 /// Types for the `GetSMSAttributes` operation.
 pub mod get_sms_attributes;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 /// Types for the `GetSMSSandboxAccountStatus` operation.
 pub mod get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_subscription_attributes")]
 /// Types for the `GetSubscriptionAttributes` operation.
 pub mod get_subscription_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 /// Types for the `GetTopicAttributes` operation.
 pub mod get_topic_attributes;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 /// Types for the `ListEndpointsByPlatformApplication` operation.
 pub mod list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_origination_numbers")]
 /// Types for the `ListOriginationNumbers` operation.
 pub mod list_origination_numbers;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 /// Types for the `ListPhoneNumbersOptedOut` operation.
 pub mod list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_platform_applications")]
 /// Types for the `ListPlatformApplications` operation.
 pub mod list_platform_applications;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 /// Types for the `ListSMSSandboxPhoneNumbers` operation.
 pub mod list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_subscriptions")]
 /// Types for the `ListSubscriptions` operation.
 pub mod list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 /// Types for the `ListSubscriptionsByTopic` operation.
 pub mod list_subscriptions_by_topic;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_topics")]
 /// Types for the `ListTopics` operation.
 pub mod list_topics;

+#[cfg(feature = "op_opt_in_phone_number")]
 /// Types for the `OptInPhoneNumber` operation.
 pub mod opt_in_phone_number;

+#[cfg(feature = "op_publish")]
 /// Types for the `Publish` operation.
 pub mod publish;

+#[cfg(feature = "op_publish_batch")]
 /// Types for the `PublishBatch` operation.
 pub mod publish_batch;

+#[cfg(feature = "op_put_data_protection_policy")]
 /// Types for the `PutDataProtectionPolicy` operation.
 pub mod put_data_protection_policy;

+#[cfg(feature = "op_remove_permission")]
 /// Types for the `RemovePermission` operation.
 pub mod remove_permission;

+#[cfg(feature = "op_set_endpoint_attributes")]
 /// Types for the `SetEndpointAttributes` operation.
 pub mod set_endpoint_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 /// Types for the `SetPlatformApplicationAttributes` operation.
 pub mod set_platform_application_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 /// Types for the `SetSMSAttributes` operation.
 pub mod set_sms_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 /// Types for the `SetSubscriptionAttributes` operation.
 pub mod set_subscription_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 /// Types for the `SetTopicAttributes` operation.
 pub mod set_topic_attributes;

+#[cfg(feature = "op_subscribe")]
 /// Types for the `Subscribe` operation.
 pub mod subscribe;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_unsubscribe")]
 /// Types for the `Unsubscribe` operation.
 pub mod unsubscribe;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 /// Types for the `VerifySMSSandboxPhoneNumber` operation.
 pub mod verify_sms_sandbox_phone_number;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,48 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +61,50 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     _response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -25,288 +113,653 @@
     crate::rest_xml_wrapped_errors::parse_error_metadata(response_body)
 }

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission;

+#[cfg(feature = "op_add_permission")]
 pub(crate) mod shape_add_permission_input;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 pub(crate) mod shape_check_if_phone_number_is_opted_out;

+#[cfg(feature = "op_check_if_phone_number_is_opted_out")]
 pub(crate) mod shape_check_if_phone_number_is_opted_out_input;

+#[cfg(feature = "op_confirm_subscription")]
 pub(crate) mod shape_confirm_subscription;

+#[cfg(feature = "op_confirm_subscription")]
 pub(crate) mod shape_confirm_subscription_input;

+#[cfg(feature = "op_create_platform_application")]
 pub(crate) mod shape_create_platform_application;

+#[cfg(feature = "op_create_platform_application")]
 pub(crate) mod shape_create_platform_application_input;

+#[cfg(feature = "op_create_platform_endpoint")]
 pub(crate) mod shape_create_platform_endpoint;

+#[cfg(feature = "op_create_platform_endpoint")]
 pub(crate) mod shape_create_platform_endpoint_input;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_create_sms_sandbox_phone_number;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_create_sms_sandbox_phone_number_input;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_create_topic;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_create_topic_input;

+#[cfg(feature = "op_delete_endpoint")]
 pub(crate) mod shape_delete_endpoint;

+#[cfg(feature = "op_delete_endpoint")]
 pub(crate) mod shape_delete_endpoint_input;

+#[cfg(feature = "op_delete_platform_application")]
 pub(crate) mod shape_delete_platform_application;

+#[cfg(feature = "op_delete_platform_application")]
 pub(crate) mod shape_delete_platform_application_input;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 pub(crate) mod shape_delete_sms_sandbox_phone_number;

+#[cfg(feature = "op_delete_sms_sandbox_phone_number")]
 pub(crate) mod shape_delete_sms_sandbox_phone_number_input;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_delete_topic;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_delete_topic_input;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy_input;

+#[cfg(feature = "op_get_endpoint_attributes")]
 pub(crate) mod shape_get_endpoint_attributes;

+#[cfg(feature = "op_get_endpoint_attributes")]
 pub(crate) mod shape_get_endpoint_attributes_input;

+#[cfg(feature = "op_get_platform_application_attributes")]
 pub(crate) mod shape_get_platform_application_attributes;

+#[cfg(feature = "op_get_platform_application_attributes")]
 pub(crate) mod shape_get_platform_application_attributes_input;

+#[cfg(feature = "op_get_sms_attributes")]
 pub(crate) mod shape_get_sms_attributes;

+#[cfg(feature = "op_get_sms_attributes")]
 pub(crate) mod shape_get_sms_attributes_input;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) mod shape_get_sms_sandbox_account_status;

+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) mod shape_get_sms_sandbox_account_status_input;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_get_subscription_attributes;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_get_subscription_attributes_input;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_get_topic_attributes;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_get_topic_attributes_input;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_endpoints_by_platform_application;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_endpoints_by_platform_application_input;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_list_origination_numbers;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_list_origination_numbers_input;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_list_phone_numbers_opted_out;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_list_phone_numbers_opted_out_input;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_platform_applications;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_platform_applications_input;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_list_sms_sandbox_phone_numbers;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_list_sms_sandbox_phone_numbers_input;

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) mod shape_list_subscriptions;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) mod shape_list_subscriptions_by_topic;

+#[cfg(feature = "op_list_subscriptions_by_topic")]
 pub(crate) mod shape_list_subscriptions_by_topic_input;

+#[cfg(feature = "op_list_subscriptions")]
 pub(crate) mod shape_list_subscriptions_input;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource_input;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_list_topics;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_list_topics_input;

+#[cfg(feature = "op_opt_in_phone_number")]
 pub(crate) mod shape_opt_in_phone_number;

+#[cfg(feature = "op_opt_in_phone_number")]
 pub(crate) mod shape_opt_in_phone_number_input;

+#[cfg(feature = "op_publish")]
 pub(crate) mod shape_publish;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_input;

+#[cfg(feature = "op_publish")]
 pub(crate) mod shape_publish_input;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy_input;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission;

+#[cfg(feature = "op_remove_permission")]
 pub(crate) mod shape_remove_permission_input;

+#[cfg(feature = "op_set_endpoint_attributes")]
 pub(crate) mod shape_set_endpoint_attributes;

+#[cfg(feature = "op_set_endpoint_attributes")]
 pub(crate) mod shape_set_endpoint_attributes_input;

+#[cfg(feature = "op_set_platform_application_attributes")]
 pub(crate) mod shape_set_platform_application_attributes;

+#[cfg(feature = "op_set_platform_application_attributes")]
 pub(crate) mod shape_set_platform_application_attributes_input;

+#[cfg(feature = "op_set_sms_attributes")]
 pub(crate) mod shape_set_sms_attributes;

+#[cfg(feature = "op_set_sms_attributes")]
 pub(crate) mod shape_set_sms_attributes_input;

+#[cfg(feature = "op_set_subscription_attributes")]
 pub(crate) mod shape_set_subscription_attributes;

+#[cfg(feature = "op_set_subscription_attributes")]
 pub(crate) mod shape_set_subscription_attributes_input;

+#[cfg(feature = "op_set_topic_attributes")]
 pub(crate) mod shape_set_topic_attributes;

+#[cfg(feature = "op_set_topic_attributes")]
 pub(crate) mod shape_set_topic_attributes_input;

+#[cfg(feature = "op_subscribe")]
 pub(crate) mod shape_subscribe;

+#[cfg(feature = "op_subscribe")]
 pub(crate) mod shape_subscribe_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_unsubscribe")]
 pub(crate) mod shape_unsubscribe;

+#[cfg(feature = "op_unsubscribe")]
 pub(crate) mod shape_unsubscribe_input;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verify_sms_sandbox_phone_number;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verify_sms_sandbox_phone_number_input;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_authorization_error_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_entry_ids_not_distinct_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_request_too_long_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_concurrent_access_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_empty_batch_request_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_endpoint_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub(crate) mod shape_filter_policy_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_internal_error_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_invalid_batch_entry_id_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_invalid_parameter_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_invalid_parameter_value_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub(crate) mod shape_invalid_security_exception;

+#[cfg(feature = "op_delete_topic")]
 pub(crate) mod shape_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_access_denied_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_disabled_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_not_found_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_opt_in_required;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_kms_throttling_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_message_attribute_value;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub(crate) mod shape_opted_out_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub(crate) mod shape_platform_application_disabled_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_request_entry;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub(crate) mod shape_replay_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_stale_tag_exception;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub(crate) mod shape_subscription_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub(crate) mod shape_tag_policy_exception;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_throttled_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_too_many_entries_in_batch_request_exception;

+#[cfg(feature = "op_create_topic")]
 pub(crate) mod shape_topic_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub(crate) mod shape_user_error_exception;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) mod shape_verification_exception;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_result_error_entry_list;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_list_of_endpoints;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_list_of_platform_applications;

+#[cfg(any(
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_platform_applications"
+))]
 pub(crate) mod shape_map_string_to_string;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_phone_number_information_list;

+#[cfg(feature = "op_list_phone_numbers_opted_out")]
 pub(crate) mod shape_phone_number_list;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_result_entry_list;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_sms_sandbox_phone_number_list;

+#[cfg(feature = "op_get_subscription_attributes")]
 pub(crate) mod shape_subscription_attributes_map;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub(crate) mod shape_subscriptions_list;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_tag_list;

+#[cfg(feature = "op_get_topic_attributes")]
 pub(crate) mod shape_topic_attributes_map;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_topics_list;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_batch_result_error_entry;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub(crate) mod shape_endpoint;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_phone_number_information;

+#[cfg(feature = "op_list_platform_applications")]
 pub(crate) mod shape_platform_application;

+#[cfg(feature = "op_publish_batch")]
 pub(crate) mod shape_publish_batch_result_entry;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) mod shape_sms_sandbox_phone_number;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub(crate) mod shape_subscription;

+#[cfg(feature = "op_list_topics")]
 pub(crate) mod shape_topic;

+#[cfg(feature = "op_list_origination_numbers")]
 pub(crate) mod shape_number_capability_list;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_sms_sandbox_account_status")]
 pub(crate) fn get_sms_sandbox_account_status_output_output_correct_errors(
     mut builder: crate::operation::get_sms_sandbox_account_status::builders::GetSmsSandboxAccountStatusOutputBuilder,
 ) -> crate::operation::get_sms_sandbox_account_status::builders::GetSmsSandboxAccountStatusOutputBuilder {
@@ -8,6 +9,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub(crate) fn validation_exception_correct_errors(
     mut builder: crate::types::error::builders::ValidationExceptionBuilder,
 ) -> crate::types::error::builders::ValidationExceptionBuilder {
@@ -17,6 +23,7 @@
     builder
 }

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub(crate) fn list_sms_sandbox_phone_numbers_output_output_correct_errors(
     mut builder: crate::operation::list_sms_sandbox_phone_numbers::builders::ListSmsSandboxPhoneNumbersOutputBuilder,
 ) -> crate::operation::list_sms_sandbox_phone_numbers::builders::ListSmsSandboxPhoneNumbersOutputBuilder {
@@ -26,6 +33,7 @@
     builder
 }

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub(crate) fn verification_exception_correct_errors(
     mut builder: crate::types::error::builders::VerificationExceptionBuilder,
 ) -> crate::types::error::builders::VerificationExceptionBuilder {
@@ -38,6 +46,7 @@
     builder
 }

+#[cfg(feature = "op_publish_batch")]
 pub(crate) fn batch_result_error_entry_correct_errors(
     mut builder: crate::types::builders::BatchResultErrorEntryBuilder,
 ) -> crate::types::builders::BatchResultErrorEntryBuilder {
@@ -53,6 +62,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,62 +1,100 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::_language_code_string::LanguageCodeString;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub use crate::types::_endpoint::Endpoint;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_phone_number_information::PhoneNumberInformation;

+#[cfg(feature = "op_list_platform_applications")]
 pub use crate::types::_platform_application::PlatformApplication;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number::SmsSandboxPhoneNumber;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub use crate::types::_subscription::Subscription;

+#[cfg(feature = "op_list_topics")]
 pub use crate::types::_topic::Topic;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::_message_attribute_value::MessageAttributeValue;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_request_entry::PublishBatchRequestEntry;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_result_entry::PublishBatchResultEntry;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntry;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_route_type::RouteType;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number_verification_status::SmsSandboxPhoneNumberVerificationStatus;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_number_capability::NumberCapability;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_result_error_entry;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 mod _endpoint;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod _language_code_string;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _message_attribute_value;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _number_capability;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _phone_number_information;

+#[cfg(feature = "op_list_platform_applications")]
 mod _platform_application;

+#[cfg(feature = "op_publish_batch")]
 mod _publish_batch_request_entry;

+#[cfg(feature = "op_publish_batch")]
 mod _publish_batch_result_entry;

+#[cfg(feature = "op_list_origination_numbers")]
 mod _route_type;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod _sms_sandbox_phone_number;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 mod _sms_sandbox_phone_number_verification_status;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 mod _subscription;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(feature = "op_list_topics")]
 mod _topic;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,22 +1,37 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(feature = "op_list_endpoints_by_platform_application")]
 pub use crate::types::_endpoint::EndpointBuilder;

+#[cfg(feature = "op_list_origination_numbers")]
 pub use crate::types::_phone_number_information::PhoneNumberInformationBuilder;

+#[cfg(feature = "op_list_platform_applications")]
 pub use crate::types::_platform_application::PlatformApplicationBuilder;

+#[cfg(feature = "op_list_sms_sandbox_phone_numbers")]
 pub use crate::types::_sms_sandbox_phone_number::SmsSandboxPhoneNumberBuilder;

+#[cfg(any(feature = "op_list_subscriptions", feature = "op_list_subscriptions_by_topic"))]
 pub use crate::types::_subscription::SubscriptionBuilder;

+#[cfg(feature = "op_list_topics")]
 pub use crate::types::_topic::TopicBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::_message_attribute_value::MessageAttributeValueBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_request_entry::PublishBatchRequestEntryBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_publish_batch_result_entry::PublishBatchResultEntryBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::_batch_result_error_entry::BatchResultErrorEntryBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,138 +1,630 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_authorization_error_exception::AuthorizationErrorException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_internal_error_exception::InternalErrorException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_throttled_exception::ThrottledException;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_filter_policy_limit_exceeded_exception::FilterPolicyLimitExceededException;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_replay_limit_exceeded_exception::ReplayLimitExceededException;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub use crate::types::error::_subscription_limit_exceeded_exception::SubscriptionLimitExceededException;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::error::_opted_out_exception::OptedOutException;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_user_error_exception::UserErrorException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_concurrent_access_exception::ConcurrentAccessException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_invalid_security_exception::InvalidSecurityException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_stale_tag_exception::StaleTagException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_limit_exceeded_exception::TagLimitExceededException;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_policy_exception::TagPolicyException;

+#[cfg(feature = "op_create_topic")]
 pub use crate::types::error::_topic_limit_exceeded_exception::TopicLimitExceededException;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(feature = "op_delete_topic")]
 pub use crate::types::error::_invalid_state_exception::InvalidStateException;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_endpoint_disabled_exception::EndpointDisabledException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_invalid_parameter_value_exception::InvalidParameterValueException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_access_denied_exception::KmsAccessDeniedException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_disabled_exception::KmsDisabledException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_not_found_exception::KmsNotFoundException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequired;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_throttling_exception::KmsThrottlingException;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_platform_application_disabled_exception::PlatformApplicationDisabledException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_entry_ids_not_distinct_exception::BatchEntryIdsNotDistinctException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_request_too_long_exception::BatchRequestTooLongException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_empty_batch_request_exception::EmptyBatchRequestException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_invalid_batch_entry_id_exception::InvalidBatchEntryIdException;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_too_many_entries_in_batch_request_exception::TooManyEntriesInBatchRequestException;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub use crate::types::error::_verification_exception::VerificationException;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _authorization_error_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_entry_ids_not_distinct_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _batch_request_too_long_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _concurrent_access_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _empty_batch_request_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _endpoint_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 mod _filter_policy_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _internal_error_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _invalid_batch_entry_id_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _invalid_parameter_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _invalid_parameter_value_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 mod _invalid_security_exception;

+#[cfg(feature = "op_delete_topic")]
 mod _invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_access_denied_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_disabled_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_invalid_state_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_not_found_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_opt_in_required;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _kms_throttling_exception;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 mod _not_found_exception;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 mod _opted_out_exception;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 mod _platform_application_disabled_exception;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 mod _replay_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _stale_tag_exception;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 mod _subscription_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 mod _tag_policy_exception;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 mod _throttled_exception;

+#[cfg(feature = "op_publish_batch")]
 mod _too_many_entries_in_batch_request_exception;

+#[cfg(feature = "op_create_topic")]
 mod _topic_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 mod _user_error_exception;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 mod _validation_exception;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 mod _verification_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,68 +1,314 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_authorization_error_exception::AuthorizationErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_internal_error_exception::InternalErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_application",
+    feature = "op_create_platform_endpoint",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_create_topic",
+    feature = "op_delete_endpoint",
+    feature = "op_delete_platform_application",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_platform_applications",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_subscriptions",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_topics",
+    feature = "op_opt_in_phone_number",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_sms_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_tag_resource",
+    feature = "op_unsubscribe",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterExceptionBuilder;

+#[cfg(any(
+    feature = "op_add_permission",
+    feature = "op_confirm_subscription",
+    feature = "op_create_platform_endpoint",
+    feature = "op_delete_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_endpoint_attributes",
+    feature = "op_get_platform_application_attributes",
+    feature = "op_get_subscription_attributes",
+    feature = "op_get_topic_attributes",
+    feature = "op_list_endpoints_by_platform_application",
+    feature = "op_list_subscriptions_by_topic",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_remove_permission",
+    feature = "op_set_endpoint_attributes",
+    feature = "op_set_platform_application_attributes",
+    feature = "op_set_subscription_attributes",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_check_if_phone_number_is_opted_out",
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_get_sms_attributes",
+    feature = "op_get_sms_sandbox_account_status",
+    feature = "op_list_origination_numbers",
+    feature = "op_list_phone_numbers_opted_out",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_opt_in_phone_number",
+    feature = "op_set_sms_attributes",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_throttled_exception::ThrottledExceptionBuilder;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_filter_policy_limit_exceeded_exception::FilterPolicyLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_confirm_subscription",
+    feature = "op_set_subscription_attributes",
+    feature = "op_subscribe"
+))]
 pub use crate::types::error::_replay_limit_exceeded_exception::ReplayLimitExceededExceptionBuilder;

+#[cfg(any(feature = "op_confirm_subscription", feature = "op_subscribe"))]
 pub use crate::types::error::_subscription_limit_exceeded_exception::SubscriptionLimitExceededExceptionBuilder;

+#[cfg(feature = "op_create_sms_sandbox_phone_number")]
 pub use crate::types::error::_opted_out_exception::OptedOutExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_sms_sandbox_phone_number",
+    feature = "op_delete_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_user_error_exception::UserErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_concurrent_access_exception::ConcurrentAccessExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_topic_attributes",
+    feature = "op_publish",
+    feature = "op_publish_batch",
+    feature = "op_put_data_protection_policy",
+    feature = "op_set_topic_attributes",
+    feature = "op_subscribe",
+    feature = "op_unsubscribe"
+))]
 pub use crate::types::error::_invalid_security_exception::InvalidSecurityExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_stale_tag_exception::StaleTagExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_limit_exceeded_exception::TagLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_topic",
+    feature = "op_delete_topic",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource"
+))]
 pub use crate::types::error::_tag_policy_exception::TagPolicyExceptionBuilder;

+#[cfg(feature = "op_create_topic")]
 pub use crate::types::error::_topic_limit_exceeded_exception::TopicLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_sms_sandbox_phone_number",
+    feature = "op_list_sms_sandbox_phone_numbers",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_verify_sms_sandbox_phone_number"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(feature = "op_delete_topic")]
 pub use crate::types::error::_invalid_state_exception::InvalidStateExceptionBuilder;

+#[cfg(any(
+    feature = "op_list_origination_numbers",
+    feature = "op_publish",
+    feature = "op_publish_batch"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_endpoint_disabled_exception::EndpointDisabledExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_invalid_parameter_value_exception::InvalidParameterValueExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_access_denied_exception::KmsAccessDeniedExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_disabled_exception::KmsDisabledExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_invalid_state_exception::KmsInvalidStateExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_not_found_exception::KmsNotFoundExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_opt_in_required::KmsOptInRequiredBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_kms_throttling_exception::KmsThrottlingExceptionBuilder;

+#[cfg(any(feature = "op_publish", feature = "op_publish_batch"))]
 pub use crate::types::error::_platform_application_disabled_exception::PlatformApplicationDisabledExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_entry_ids_not_distinct_exception::BatchEntryIdsNotDistinctExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_batch_request_too_long_exception::BatchRequestTooLongExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_empty_batch_request_exception::EmptyBatchRequestExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_invalid_batch_entry_id_exception::InvalidBatchEntryIdExceptionBuilder;

+#[cfg(feature = "op_publish_batch")]
 pub use crate::types::error::_too_many_entries_in_batch_request_exception::TooManyEntriesInBatchRequestExceptionBuilder;

+#[cfg(feature = "op_verify_sms_sandbox_phone_number")]
 pub use crate::types::error::_verification_exception::VerificationExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
