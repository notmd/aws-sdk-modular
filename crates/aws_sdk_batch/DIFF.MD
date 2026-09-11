# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/batch`
- model: `aws-models/batch.json`
- package: `aws-sdk-batch`
- library: `aws_sdk_batch`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_cancel_job`: `CancelJob`
- `op_create_compute_environment`: `CreateComputeEnvironment`
- `op_create_consumable_resource`: `CreateConsumableResource`
- `op_create_job_queue`: `CreateJobQueue`
- `op_create_quota_share`: `CreateQuotaShare`
- `op_create_scheduling_policy`: `CreateSchedulingPolicy`
- `op_create_service_environment`: `CreateServiceEnvironment`
- `op_delete_compute_environment`: `DeleteComputeEnvironment`
- `op_delete_consumable_resource`: `DeleteConsumableResource`
- `op_delete_job_queue`: `DeleteJobQueue`
- `op_delete_quota_share`: `DeleteQuotaShare`
- `op_delete_scheduling_policy`: `DeleteSchedulingPolicy`
- `op_delete_service_environment`: `DeleteServiceEnvironment`
- `op_deregister_job_definition`: `DeregisterJobDefinition`
- `op_describe_compute_environments`: `DescribeComputeEnvironments`
- `op_describe_consumable_resource`: `DescribeConsumableResource`
- `op_describe_job_definitions`: `DescribeJobDefinitions`
- `op_describe_job_queues`: `DescribeJobQueues`
- `op_describe_jobs`: `DescribeJobs`
- `op_describe_quota_share`: `DescribeQuotaShare`
- `op_describe_scheduling_policies`: `DescribeSchedulingPolicies`
- `op_describe_service_environments`: `DescribeServiceEnvironments`
- `op_describe_service_job`: `DescribeServiceJob`
- `op_get_job_queue_snapshot`: `GetJobQueueSnapshot`
- `op_list_consumable_resources`: `ListConsumableResources`
- `op_list_jobs`: `ListJobs`
- `op_list_jobs_by_consumable_resource`: `ListJobsByConsumableResource`
- `op_list_quota_shares`: `ListQuotaShares`
- `op_list_scheduling_policies`: `ListSchedulingPolicies`
- `op_list_service_jobs`: `ListServiceJobs`
- `op_list_tags_for_resource`: `ListTagsForResource`
- `op_register_job_definition`: `RegisterJobDefinition`
- `op_submit_job`: `SubmitJob`
- `op_submit_service_job`: `SubmitServiceJob`
- `op_tag_resource`: `TagResource`
- `op_terminate_job`: `TerminateJob`
- `op_terminate_service_job`: `TerminateServiceJob`
- `op_untag_resource`: `UntagResource`
- `op_update_compute_environment`: `UpdateComputeEnvironment`
- `op_update_consumable_resource`: `UpdateConsumableResource`
- `op_update_job_queue`: `UpdateJobQueue`
- `op_update_quota_share`: `UpdateQuotaShare`
- `op_update_scheduling_policy`: `UpdateSchedulingPolicy`
- `op_update_service_environment`: `UpdateServiceEnvironment`
- `op_update_service_job`: `UpdateServiceJob`

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
@@ -84,16 +73,13 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-smithy-protocol-test]
-path = "../aws-smithy-protocol-test"
 version = "0.64.0"

 [dev-dependencies.pretty_assertions]
@@ -118,3 +104,48 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_cancel_job = []
+op_create_compute_environment = []
+op_create_consumable_resource = []
+op_create_job_queue = []
+op_create_quota_share = []
+op_create_scheduling_policy = []
+op_create_service_environment = []
+op_delete_compute_environment = []
+op_delete_consumable_resource = []
+op_delete_job_queue = []
+op_delete_quota_share = []
+op_delete_scheduling_policy = []
+op_delete_service_environment = []
+op_deregister_job_definition = []
+op_describe_compute_environments = []
+op_describe_consumable_resource = []
+op_describe_job_definitions = []
+op_describe_job_queues = []
+op_describe_jobs = []
+op_describe_quota_share = []
+op_describe_scheduling_policies = []
+op_describe_service_environments = []
+op_describe_service_job = []
+op_get_job_queue_snapshot = []
+op_list_consumable_resources = []
+op_list_jobs = []
+op_list_jobs_by_consumable_resource = []
+op_list_quota_shares = []
+op_list_scheduling_policies = []
+op_list_service_jobs = []
+op_list_tags_for_resource = []
+op_register_job_definition = []
+op_submit_job = []
+op_submit_service_job = []
+op_tag_resource = []
+op_terminate_job = []
+op_terminate_service_job = []
+op_untag_resource = []
+op_update_compute_environment = []
+op_update_consumable_resource = []
+op_update_job_queue = []
+op_update_quota_share = []
+op_update_scheduling_policy = []
+op_update_service_environment = []
+op_update_service_job = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,18 +136,25 @@
     }
 }

+#[cfg(feature = "op_cancel_job")]
 mod cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 mod create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 mod create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 mod create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 mod create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 mod create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 mod create_service_environment;

 /// Operation customization and supporting types.
@@ -177,78 +184,116 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_compute_environment")]
 mod delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 mod delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 mod delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 mod delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 mod delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 mod delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 mod deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 mod describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 mod describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 mod describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 mod describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 mod describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 mod describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 mod describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 mod describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 mod describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 mod list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 mod list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 mod list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 mod list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 mod list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 mod list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 mod register_job_definition;

+#[cfg(feature = "op_submit_job")]
 mod submit_job;

+#[cfg(feature = "op_submit_service_job")]
 mod submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_terminate_job")]
 mod terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 mod terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 mod update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 mod update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 mod update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 mod update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 mod update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 mod update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 mod update_service_job;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,8 +3,102 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_cancel_job",
+        feature = "op_create_compute_environment",
+        feature = "op_create_consumable_resource",
+        feature = "op_create_job_queue",
+        feature = "op_create_quota_share",
+        feature = "op_create_scheduling_policy",
+        feature = "op_create_service_environment",
+        feature = "op_delete_compute_environment",
+        feature = "op_delete_consumable_resource",
+        feature = "op_delete_job_queue",
+        feature = "op_delete_quota_share",
+        feature = "op_delete_scheduling_policy",
+        feature = "op_delete_service_environment",
+        feature = "op_deregister_job_definition",
+        feature = "op_describe_compute_environments",
+        feature = "op_describe_consumable_resource",
+        feature = "op_describe_job_definitions",
+        feature = "op_describe_job_queues",
+        feature = "op_describe_jobs",
+        feature = "op_describe_quota_share",
+        feature = "op_describe_scheduling_policies",
+        feature = "op_describe_service_environments",
+        feature = "op_describe_service_job",
+        feature = "op_get_job_queue_snapshot",
+        feature = "op_list_consumable_resources",
+        feature = "op_list_jobs",
+        feature = "op_list_jobs_by_consumable_resource",
+        feature = "op_list_quota_shares",
+        feature = "op_list_scheduling_policies",
+        feature = "op_list_service_jobs",
+        feature = "op_list_tags_for_resource",
+        feature = "op_register_job_definition",
+        feature = "op_submit_job",
+        feature = "op_submit_service_job",
+        feature = "op_tag_resource",
+        feature = "op_terminate_job",
+        feature = "op_terminate_service_job",
+        feature = "op_untag_resource",
+        feature = "op_update_compute_environment",
+        feature = "op_update_consumable_resource",
+        feature = "op_update_job_queue",
+        feature = "op_update_quota_share",
+        feature = "op_update_scheduling_policy",
+        feature = "op_update_service_environment",
+        feature = "op_update_service_job"
+    ))]
     /// <p>These errors are usually caused by a client action. One example cause is using an action or resource on behalf of a user that doesn't have permissions to use the action or resource. Another cause is specifying an identifier that's not valid.</p>
     ClientException(crate::types::error::ClientException),
+    #[cfg(any(
+        feature = "op_cancel_job",
+        feature = "op_create_compute_environment",
+        feature = "op_create_consumable_resource",
+        feature = "op_create_job_queue",
+        feature = "op_create_quota_share",
+        feature = "op_create_scheduling_policy",
+        feature = "op_create_service_environment",
+        feature = "op_delete_compute_environment",
+        feature = "op_delete_consumable_resource",
+        feature = "op_delete_job_queue",
+        feature = "op_delete_quota_share",
+        feature = "op_delete_scheduling_policy",
+        feature = "op_delete_service_environment",
+        feature = "op_deregister_job_definition",
+        feature = "op_describe_compute_environments",
+        feature = "op_describe_consumable_resource",
+        feature = "op_describe_job_definitions",
+        feature = "op_describe_job_queues",
+        feature = "op_describe_jobs",
+        feature = "op_describe_quota_share",
+        feature = "op_describe_scheduling_policies",
+        feature = "op_describe_service_environments",
+        feature = "op_describe_service_job",
+        feature = "op_get_job_queue_snapshot",
+        feature = "op_list_consumable_resources",
+        feature = "op_list_jobs",
+        feature = "op_list_jobs_by_consumable_resource",
+        feature = "op_list_quota_shares",
+        feature = "op_list_scheduling_policies",
+        feature = "op_list_service_jobs",
+        feature = "op_list_tags_for_resource",
+        feature = "op_register_job_definition",
+        feature = "op_submit_job",
+        feature = "op_submit_service_job",
+        feature = "op_tag_resource",
+        feature = "op_terminate_job",
+        feature = "op_terminate_service_job",
+        feature = "op_untag_resource",
+        feature = "op_update_compute_environment",
+        feature = "op_update_consumable_resource",
+        feature = "op_update_job_queue",
+        feature = "op_update_quota_share",
+        feature = "op_update_scheduling_policy",
+        feature = "op_update_service_environment",
+        feature = "op_update_service_job"
+    ))]
     /// <p>These errors are usually caused by a server issue.</p>
     ServerException(crate::types::error::ServerException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -21,7 +115,101 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ClientException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ServerException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -46,12 +234,107 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ClientException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ServerException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_cancel_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::cancel_job::CancelJobError, R>>
     for Error
 where
@@ -69,6 +352,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_job")]
 impl From<crate::operation::cancel_job::CancelJobError> for Error {
     fn from(err: crate::operation::cancel_job::CancelJobError) -> Self {
         match err {
@@ -78,6 +362,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -103,6 +388,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_compute_environment")]
 impl From<crate::operation::create_compute_environment::CreateComputeEnvironmentError> for Error {
     fn from(err: crate::operation::create_compute_environment::CreateComputeEnvironmentError) -> Self {
         match err {
@@ -118,6 +404,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -143,6 +430,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_consumable_resource")]
 impl From<crate::operation::create_consumable_resource::CreateConsumableResourceError> for Error {
     fn from(err: crate::operation::create_consumable_resource::CreateConsumableResourceError) -> Self {
         match err {
@@ -158,6 +446,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_job_queue::CreateJobQueueError, R>>
     for Error
@@ -179,6 +468,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_job_queue")]
 impl From<crate::operation::create_job_queue::CreateJobQueueError> for Error {
     fn from(err: crate::operation::create_job_queue::CreateJobQueueError) -> Self {
         match err {
@@ -192,6 +482,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -217,6 +508,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_quota_share")]
 impl From<crate::operation::create_quota_share::CreateQuotaShareError> for Error {
     fn from(err: crate::operation::create_quota_share::CreateQuotaShareError) -> Self {
         match err {
@@ -230,6 +522,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -255,6 +548,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduling_policy")]
 impl From<crate::operation::create_scheduling_policy::CreateSchedulingPolicyError> for Error {
     fn from(err: crate::operation::create_scheduling_policy::CreateSchedulingPolicyError) -> Self {
         match err {
@@ -270,6 +564,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -295,6 +590,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_service_environment")]
 impl From<crate::operation::create_service_environment::CreateServiceEnvironmentError> for Error {
     fn from(err: crate::operation::create_service_environment::CreateServiceEnvironmentError) -> Self {
         match err {
@@ -310,6 +606,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -335,6 +632,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_compute_environment")]
 impl From<crate::operation::delete_compute_environment::DeleteComputeEnvironmentError> for Error {
     fn from(err: crate::operation::delete_compute_environment::DeleteComputeEnvironmentError) -> Self {
         match err {
@@ -350,6 +648,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -375,6 +674,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_consumable_resource")]
 impl From<crate::operation::delete_consumable_resource::DeleteConsumableResourceError> for Error {
     fn from(err: crate::operation::delete_consumable_resource::DeleteConsumableResourceError) -> Self {
         match err {
@@ -390,6 +690,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_job_queue::DeleteJobQueueError, R>>
     for Error
@@ -411,6 +712,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_job_queue")]
 impl From<crate::operation::delete_job_queue::DeleteJobQueueError> for Error {
     fn from(err: crate::operation::delete_job_queue::DeleteJobQueueError) -> Self {
         match err {
@@ -424,6 +726,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -449,6 +752,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_quota_share")]
 impl From<crate::operation::delete_quota_share::DeleteQuotaShareError> for Error {
     fn from(err: crate::operation::delete_quota_share::DeleteQuotaShareError) -> Self {
         match err {
@@ -462,6 +766,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -487,6 +792,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduling_policy")]
 impl From<crate::operation::delete_scheduling_policy::DeleteSchedulingPolicyError> for Error {
     fn from(err: crate::operation::delete_scheduling_policy::DeleteSchedulingPolicyError) -> Self {
         match err {
@@ -502,6 +808,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -527,6 +834,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_service_environment")]
 impl From<crate::operation::delete_service_environment::DeleteServiceEnvironmentError> for Error {
     fn from(err: crate::operation::delete_service_environment::DeleteServiceEnvironmentError) -> Self {
         match err {
@@ -542,6 +850,7 @@
         }
     }
 }
+#[cfg(feature = "op_deregister_job_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -567,6 +876,7 @@
         }
     }
 }
+#[cfg(feature = "op_deregister_job_definition")]
 impl From<crate::operation::deregister_job_definition::DeregisterJobDefinitionError> for Error {
     fn from(err: crate::operation::deregister_job_definition::DeregisterJobDefinitionError) -> Self {
         match err {
@@ -582,6 +892,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_compute_environments")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -607,6 +918,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_compute_environments")]
 impl From<crate::operation::describe_compute_environments::DescribeComputeEnvironmentsError> for Error {
     fn from(err: crate::operation::describe_compute_environments::DescribeComputeEnvironmentsError) -> Self {
         match err {
@@ -622,6 +934,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -647,6 +960,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_consumable_resource")]
 impl From<crate::operation::describe_consumable_resource::DescribeConsumableResourceError> for Error {
     fn from(err: crate::operation::describe_consumable_resource::DescribeConsumableResourceError) -> Self {
         match err {
@@ -662,6 +976,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_definitions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -687,6 +1002,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_definitions")]
 impl From<crate::operation::describe_job_definitions::DescribeJobDefinitionsError> for Error {
     fn from(err: crate::operation::describe_job_definitions::DescribeJobDefinitionsError) -> Self {
         match err {
@@ -702,6 +1018,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_queues")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -727,6 +1044,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_queues")]
 impl From<crate::operation::describe_job_queues::DescribeJobQueuesError> for Error {
     fn from(err: crate::operation::describe_job_queues::DescribeJobQueuesError) -> Self {
         match err {
@@ -740,6 +1058,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_jobs")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_jobs::DescribeJobsError, R>>
     for Error
 where
@@ -757,6 +1076,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_jobs")]
 impl From<crate::operation::describe_jobs::DescribeJobsError> for Error {
     fn from(err: crate::operation::describe_jobs::DescribeJobsError) -> Self {
         match err {
@@ -766,6 +1086,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -791,6 +1112,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_quota_share")]
 impl From<crate::operation::describe_quota_share::DescribeQuotaShareError> for Error {
     fn from(err: crate::operation::describe_quota_share::DescribeQuotaShareError) -> Self {
         match err {
@@ -806,6 +1128,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_scheduling_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -831,6 +1154,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_scheduling_policies")]
 impl From<crate::operation::describe_scheduling_policies::DescribeSchedulingPoliciesError> for Error {
     fn from(err: crate::operation::describe_scheduling_policies::DescribeSchedulingPoliciesError) -> Self {
         match err {
@@ -846,6 +1170,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_environments")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -871,6 +1196,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_environments")]
 impl From<crate::operation::describe_service_environments::DescribeServiceEnvironmentsError> for Error {
     fn from(err: crate::operation::describe_service_environments::DescribeServiceEnvironmentsError) -> Self {
         match err {
@@ -886,6 +1212,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -911,6 +1238,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_job")]
 impl From<crate::operation::describe_service_job::DescribeServiceJobError> for Error {
     fn from(err: crate::operation::describe_service_job::DescribeServiceJobError) -> Self {
         match err {
@@ -926,6 +1254,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_job_queue_snapshot")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -951,6 +1280,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_job_queue_snapshot")]
 impl From<crate::operation::get_job_queue_snapshot::GetJobQueueSnapshotError> for Error {
     fn from(err: crate::operation::get_job_queue_snapshot::GetJobQueueSnapshotError) -> Self {
         match err {
@@ -966,6 +1296,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_consumable_resources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -991,6 +1322,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_consumable_resources")]
 impl From<crate::operation::list_consumable_resources::ListConsumableResourcesError> for Error {
     fn from(err: crate::operation::list_consumable_resources::ListConsumableResourcesError) -> Self {
         match err {
@@ -1006,6 +1338,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_jobs::ListJobsError, R>>
     for Error
 where
@@ -1023,6 +1356,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs")]
 impl From<crate::operation::list_jobs::ListJobsError> for Error {
     fn from(err: crate::operation::list_jobs::ListJobsError) -> Self {
         match err {
@@ -1032,6 +1366,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1057,6 +1392,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 impl From<crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceError> for Error {
     fn from(err: crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceError) -> Self {
         match err {
@@ -1072,6 +1408,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_quota_shares")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1097,6 +1434,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_quota_shares")]
 impl From<crate::operation::list_quota_shares::ListQuotaSharesError> for Error {
     fn from(err: crate::operation::list_quota_shares::ListQuotaSharesError) -> Self {
         match err {
@@ -1110,6 +1448,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduling_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1135,6 +1474,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduling_policies")]
 impl From<crate::operation::list_scheduling_policies::ListSchedulingPoliciesError> for Error {
     fn from(err: crate::operation::list_scheduling_policies::ListSchedulingPoliciesError) -> Self {
         match err {
@@ -1150,6 +1490,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_service_jobs")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1175,6 +1516,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_service_jobs")]
 impl From<crate::operation::list_service_jobs::ListServiceJobsError> for Error {
     fn from(err: crate::operation::list_service_jobs::ListServiceJobsError) -> Self {
         match err {
@@ -1188,6 +1530,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1213,6 +1556,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -1228,6 +1572,7 @@
         }
     }
 }
+#[cfg(feature = "op_register_job_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1253,6 +1598,7 @@
         }
     }
 }
+#[cfg(feature = "op_register_job_definition")]
 impl From<crate::operation::register_job_definition::RegisterJobDefinitionError> for Error {
     fn from(err: crate::operation::register_job_definition::RegisterJobDefinitionError) -> Self {
         match err {
@@ -1268,6 +1614,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::submit_job::SubmitJobError, R>>
     for Error
 where
@@ -1285,6 +1632,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_job")]
 impl From<crate::operation::submit_job::SubmitJobError> for Error {
     fn from(err: crate::operation::submit_job::SubmitJobError) -> Self {
         match err {
@@ -1294,6 +1642,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1319,6 +1668,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_service_job")]
 impl From<crate::operation::submit_service_job::SubmitServiceJobError> for Error {
     fn from(err: crate::operation::submit_service_job::SubmitServiceJobError) -> Self {
         match err {
@@ -1332,6 +1682,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -1349,6 +1700,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -1358,6 +1710,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::terminate_job::TerminateJobError, R>>
     for Error
 where
@@ -1375,6 +1728,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_job")]
 impl From<crate::operation::terminate_job::TerminateJobError> for Error {
     fn from(err: crate::operation::terminate_job::TerminateJobError) -> Self {
         match err {
@@ -1384,6 +1738,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1409,6 +1764,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_service_job")]
 impl From<crate::operation::terminate_service_job::TerminateServiceJobError> for Error {
     fn from(err: crate::operation::terminate_service_job::TerminateServiceJobError) -> Self {
         match err {
@@ -1424,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -1445,6 +1802,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -1458,6 +1816,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1483,6 +1842,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_compute_environment")]
 impl From<crate::operation::update_compute_environment::UpdateComputeEnvironmentError> for Error {
     fn from(err: crate::operation::update_compute_environment::UpdateComputeEnvironmentError) -> Self {
         match err {
@@ -1498,6 +1858,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1523,6 +1884,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_consumable_resource")]
 impl From<crate::operation::update_consumable_resource::UpdateConsumableResourceError> for Error {
     fn from(err: crate::operation::update_consumable_resource::UpdateConsumableResourceError) -> Self {
         match err {
@@ -1538,6 +1900,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_job_queue::UpdateJobQueueError, R>>
     for Error
@@ -1559,6 +1922,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_job_queue")]
 impl From<crate::operation::update_job_queue::UpdateJobQueueError> for Error {
     fn from(err: crate::operation::update_job_queue::UpdateJobQueueError) -> Self {
         match err {
@@ -1572,6 +1936,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1597,6 +1962,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_quota_share")]
 impl From<crate::operation::update_quota_share::UpdateQuotaShareError> for Error {
     fn from(err: crate::operation::update_quota_share::UpdateQuotaShareError) -> Self {
         match err {
@@ -1610,6 +1976,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1635,6 +2002,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduling_policy")]
 impl From<crate::operation::update_scheduling_policy::UpdateSchedulingPolicyError> for Error {
     fn from(err: crate::operation::update_scheduling_policy::UpdateSchedulingPolicyError) -> Self {
         match err {
@@ -1650,6 +2018,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1675,6 +2044,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_environment")]
 impl From<crate::operation::update_service_environment::UpdateServiceEnvironmentError> for Error {
     fn from(err: crate::operation::update_service_environment::UpdateServiceEnvironmentError) -> Self {
         match err {
@@ -1690,6 +2060,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1715,6 +2086,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_job")]
 impl From<crate::operation::update_service_job::UpdateServiceJobError> for Error {
     fn from(err: crate::operation::update_service_job::UpdateServiceJobError) -> Self {
         match err {
@@ -1731,7 +2103,101 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ClientException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ServerException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -1740,7 +2206,101 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ClientException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ServerException(e) => e.request_id(),
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
+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn reflens_describe_compute_environments_output_output_next_token(
     input: &crate::operation::describe_compute_environments::DescribeComputeEnvironmentsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn reflens_describe_job_definitions_output_output_next_token(
     input: &crate::operation::describe_job_definitions::DescribeJobDefinitionsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn reflens_describe_job_queues_output_output_next_token(
     input: &crate::operation::describe_job_queues::DescribeJobQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn reflens_describe_service_environments_output_output_next_token(
     input: &crate::operation::describe_service_environments::DescribeServiceEnvironmentsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn reflens_list_consumable_resources_output_output_next_token(
     input: &crate::operation::list_consumable_resources::ListConsumableResourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn reflens_list_jobs_output_output_next_token(
     input: &crate::operation::list_jobs::ListJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn reflens_list_jobs_by_consumable_resource_output_output_next_token(
     input: &crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) fn reflens_list_quota_shares_output_output_next_token(
     input: &crate::operation::list_quota_shares::ListQuotaSharesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn reflens_list_scheduling_policies_output_output_next_token(
     input: &crate::operation::list_scheduling_policies::ListSchedulingPoliciesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn reflens_list_service_jobs_output_output_next_token(
     input: &crate::operation::list_service_jobs::ListServiceJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn lens_describe_compute_environments_output_output_compute_environments(
     input: crate::operation::describe_compute_environments::DescribeComputeEnvironmentsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ComputeEnvironmentDetail>> {
@@ -106,6 +117,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn lens_describe_job_definitions_output_output_job_definitions(
     input: crate::operation::describe_job_definitions::DescribeJobDefinitionsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobDefinition>> {
@@ -113,6 +125,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn lens_describe_job_queues_output_output_job_queues(
     input: crate::operation::describe_job_queues::DescribeJobQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobQueueDetail>> {
@@ -120,6 +133,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn lens_describe_service_environments_output_output_service_environments(
     input: crate::operation::describe_service_environments::DescribeServiceEnvironmentsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ServiceEnvironmentDetail>> {
@@ -127,6 +141,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn lens_list_consumable_resources_output_output_consumable_resources(
     input: crate::operation::list_consumable_resources::ListConsumableResourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ConsumableResourceSummary>> {
@@ -134,6 +149,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn lens_list_jobs_output_output_job_summary_list(
     input: crate::operation::list_jobs::ListJobsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobSummary>> {
@@ -141,6 +157,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn lens_list_jobs_by_consumable_resource_output_output_jobs(
     input: crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ListJobsByConsumableResourceSummary>> {
@@ -148,6 +165,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) fn lens_list_quota_shares_output_output_quota_shares(
     input: crate::operation::list_quota_shares::ListQuotaSharesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::QuotaShareDetail>> {
@@ -155,6 +173,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn lens_list_scheduling_policies_output_output_scheduling_policies(
     input: crate::operation::list_scheduling_policies::ListSchedulingPoliciesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SchedulingPolicyListingDetail>> {
@@ -162,6 +181,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn lens_list_service_jobs_output_output_job_summary_list(
     input: crate::operation::list_service_jobs::ListServiceJobsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ServiceJobSummary>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,137 +1,182 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_cancel_job")]
 /// Types for the `CancelJob` operation.
 pub mod cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 /// Types for the `CreateComputeEnvironment` operation.
 pub mod create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 /// Types for the `CreateConsumableResource` operation.
 pub mod create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 /// Types for the `CreateJobQueue` operation.
 pub mod create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 /// Types for the `CreateQuotaShare` operation.
 pub mod create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 /// Types for the `CreateSchedulingPolicy` operation.
 pub mod create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 /// Types for the `CreateServiceEnvironment` operation.
 pub mod create_service_environment;

+#[cfg(feature = "op_delete_compute_environment")]
 /// Types for the `DeleteComputeEnvironment` operation.
 pub mod delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 /// Types for the `DeleteConsumableResource` operation.
 pub mod delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 /// Types for the `DeleteJobQueue` operation.
 pub mod delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 /// Types for the `DeleteQuotaShare` operation.
 pub mod delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 /// Types for the `DeleteSchedulingPolicy` operation.
 pub mod delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 /// Types for the `DeleteServiceEnvironment` operation.
 pub mod delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 /// Types for the `DeregisterJobDefinition` operation.
 pub mod deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 /// Types for the `DescribeComputeEnvironments` operation.
 pub mod describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 /// Types for the `DescribeConsumableResource` operation.
 pub mod describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 /// Types for the `DescribeJobDefinitions` operation.
 pub mod describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 /// Types for the `DescribeJobQueues` operation.
 pub mod describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 /// Types for the `DescribeJobs` operation.
 pub mod describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 /// Types for the `DescribeQuotaShare` operation.
 pub mod describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 /// Types for the `DescribeSchedulingPolicies` operation.
 pub mod describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 /// Types for the `DescribeServiceEnvironments` operation.
 pub mod describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 /// Types for the `DescribeServiceJob` operation.
 pub mod describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 /// Types for the `GetJobQueueSnapshot` operation.
 pub mod get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 /// Types for the `ListConsumableResources` operation.
 pub mod list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 /// Types for the `ListJobs` operation.
 pub mod list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 /// Types for the `ListJobsByConsumableResource` operation.
 pub mod list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 /// Types for the `ListQuotaShares` operation.
 pub mod list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 /// Types for the `ListSchedulingPolicies` operation.
 pub mod list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 /// Types for the `ListServiceJobs` operation.
 pub mod list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 /// Types for the `RegisterJobDefinition` operation.
 pub mod register_job_definition;

+#[cfg(feature = "op_submit_job")]
 /// Types for the `SubmitJob` operation.
 pub mod submit_job;

+#[cfg(feature = "op_submit_service_job")]
 /// Types for the `SubmitServiceJob` operation.
 pub mod submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_terminate_job")]
 /// Types for the `TerminateJob` operation.
 pub mod terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 /// Types for the `TerminateServiceJob` operation.
 pub mod terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 /// Types for the `UpdateComputeEnvironment` operation.
 pub mod update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 /// Types for the `UpdateConsumableResource` operation.
 pub mod update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 /// Types for the `UpdateJobQueue` operation.
 pub mod update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 /// Types for the `UpdateQuotaShare` operation.
 pub mod update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 /// Types for the `UpdateSchedulingPolicy` operation.
 pub mod update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 /// Types for the `UpdateServiceEnvironment` operation.
 pub mod update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 /// Types for the `UpdateServiceJob` operation.
 pub mod update_service_job;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,51 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +64,53 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,98 +122,191 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_cancel_job")]
 pub(crate) mod shape_cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 pub(crate) mod shape_create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) mod shape_create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) mod shape_create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 pub(crate) mod shape_create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) mod shape_create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) mod shape_create_service_environment;

+#[cfg(feature = "op_delete_compute_environment")]
 pub(crate) mod shape_delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 pub(crate) mod shape_delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 pub(crate) mod shape_delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 pub(crate) mod shape_delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 pub(crate) mod shape_delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 pub(crate) mod shape_delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 pub(crate) mod shape_deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) mod shape_describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 pub(crate) mod shape_describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) mod shape_register_job_definition;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_submit_job;

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) mod shape_submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_terminate_job")]
 pub(crate) mod shape_terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 pub(crate) mod shape_terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) mod shape_update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 pub(crate) mod shape_update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 pub(crate) mod shape_update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 pub(crate) mod shape_update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) mod shape_update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 pub(crate) mod shape_update_service_job;

+#[cfg(feature = "op_cancel_job")]
 pub(crate) mod shape_cancel_job_input;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -128,526 +315,1327 @@
     }
 }

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) mod shape_client_exception;

+#[cfg(feature = "op_create_compute_environment")]
 pub(crate) mod shape_create_compute_environment_input;

+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) mod shape_create_consumable_resource_input;

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) mod shape_create_job_queue_input;

+#[cfg(feature = "op_create_quota_share")]
 pub(crate) mod shape_create_quota_share_input;

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) mod shape_create_scheduling_policy_input;

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) mod shape_create_service_environment_input;

+#[cfg(feature = "op_delete_compute_environment")]
 pub(crate) mod shape_delete_compute_environment_input;

+#[cfg(feature = "op_delete_consumable_resource")]
 pub(crate) mod shape_delete_consumable_resource_input;

+#[cfg(feature = "op_delete_job_queue")]
 pub(crate) mod shape_delete_job_queue_input;

+#[cfg(feature = "op_delete_quota_share")]
 pub(crate) mod shape_delete_quota_share_input;

+#[cfg(feature = "op_delete_scheduling_policy")]
 pub(crate) mod shape_delete_scheduling_policy_input;

+#[cfg(feature = "op_delete_service_environment")]
 pub(crate) mod shape_delete_service_environment_input;

+#[cfg(feature = "op_deregister_job_definition")]
 pub(crate) mod shape_deregister_job_definition_input;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_describe_compute_environments_input;

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) mod shape_describe_consumable_resource_input;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_describe_job_definitions_input;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_describe_job_queues_input;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_describe_jobs_input;

+#[cfg(feature = "op_describe_quota_share")]
 pub(crate) mod shape_describe_quota_share_input;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_describe_scheduling_policies_input;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_describe_service_environments_input;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_describe_service_job_input;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_get_job_queue_snapshot_input;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_list_consumable_resources_input;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_input;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_list_jobs_input;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_list_quota_shares_input;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_list_scheduling_policies_input;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_list_service_jobs_input;

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) mod shape_register_job_definition_input;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) mod shape_server_exception;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_submit_job_input;

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) mod shape_submit_service_job_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_terminate_job")]
 pub(crate) mod shape_terminate_job_input;

+#[cfg(feature = "op_terminate_service_job")]
 pub(crate) mod shape_terminate_service_job_input;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_compute_environment_input;

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) mod shape_update_consumable_resource_input;

+#[cfg(feature = "op_update_job_queue")]
 pub(crate) mod shape_update_job_queue_input;

+#[cfg(feature = "op_update_quota_share")]
 pub(crate) mod shape_update_quota_share_input;

+#[cfg(feature = "op_update_scheduling_policy")]
 pub(crate) mod shape_update_scheduling_policy_input;

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) mod shape_update_service_environment_input;

+#[cfg(feature = "op_update_service_job")]
 pub(crate) mod shape_update_service_job_input;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_array_properties;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub(crate) mod shape_capacity_limit;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_compute_environment_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_compute_environment_order;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_compute_resource;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_compute_resource_update;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_properties;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_consumable_resource_summary_list;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_container_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ecs_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_ecs_properties_override;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_ecs_settings;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_eks_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_properties_override;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_fairshare_policy;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_shares_detail;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_job_definition_list;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub(crate) mod shape_job_dependency;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_detail_list;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_queue_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_job_state_time_limit_action;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_summary_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_job_timeout;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub(crate) mod shape_key_values_pair;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) mod shape_latest_service_job_attempt;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_summary_list;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_node_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_utilization_detail;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_capacity_limit;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 pub(crate) mod shape_quota_share_capacity_limits;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_quota_share_list;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_quota_share_policy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_preemption_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_resource_sharing_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_retry_strategy;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_detail_list;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_listing_detail_list;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_service_environment_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_service_environment_order;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_attempt_details;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_capacity_usage_detail_list;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_preemption_configuration;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_preemption_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_retry_strategy;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_summary_list;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_timeout;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_list_tags_for_resource"
+))]
 pub(crate) mod shape_tagris_tags_map;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_update_policy;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_compute_environment_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_compute_scaling_policy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_requirement;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_ec2_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ecs_task_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_pod_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_pod_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ephemeral_storage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_evaluate_on_exit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_fargate_platform_configuration;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_job_summary_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_shares_job_summary_map;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_job_definition;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_detail;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_queue_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_key_value_pair;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_linux_parameters;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_log_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_managed_instances_provider;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_mount_point;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_network_configuration;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_node_property_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_range_property;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_capacity_usage_list;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_quota_share_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_repository_credentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_resource_requirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_runtime_platform;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_detail;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_listing_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_secret;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_service_environment_detail;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_attempt_detail;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_capacity_usage_detail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_evaluate_on_exit;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_evaluate_on_exit_list;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_recent_preempted_attempt_list;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) mod shape_service_resource_id;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_share_attributes;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_task_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ulimit;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_managed_instances_provider_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_volume;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_array_properties_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_array_properties_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_details;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_capacity_limits;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_compute_environment_orders;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_container_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_container_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_device;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_ecs_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_efs_volume_configuration;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_container_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_metadata;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_volume;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_utilization_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_share_job_summary_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_image_pull_secret;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_infrastructure_optimization;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_instance_launch_template;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_instance_launch_template_update;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_capacity_usage_summary_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_dependency_list;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_state_time_limit_actions;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification_override;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_node_details;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_node_properties_summary;

+#[cfg(any(feature = "op_describe_job_definitions", feature = "op_describe_jobs"))]
 pub(crate) mod shape_parameters_map;

+#[cfg(any(feature = "op_describe_job_definitions", feature = "op_describe_jobs"))]
 pub(crate) mod shape_platform_capability_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_utilization_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_s3_files_volume_configuration;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_service_environment_orders;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_capacity_usage_summary_list;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_preempted_attempt;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_task_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_tmpfs;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 pub(crate) mod shape_array_job_status_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_capacity_reservation_request;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_ec2_configuration_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_efs_authorization_config;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_container_environment_variable;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_container_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_security_context;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_volume_mount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_empty_dir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_host_path;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_persistent_volume_claim;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_pod_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_environment_variables;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_evaluate_on_exit_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_utilization;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_firelens_configuration;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_share_job_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_instance_requirements_request;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_capacity_usage_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_list_ecs_task_properties;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_local_storage_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_network_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_storage_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_mount_points;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_network_interface_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_range_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_utilization;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_secret_list;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_capacity_usage_summary;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_share_attributes_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_string_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_tags_map;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_dependency;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ulimits;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_volumes;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_devices_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_ecs_task_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_containers;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_volumes;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_usage_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_image_pull_secrets;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification_override_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_attempt_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_log_configuration_options_map;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_network_interface;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_usage_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_tmpfs_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_annotations_map;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_labels_map;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_usage;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_task_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_list_task_container_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_usage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_device_cgroup_permissions;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_environment_variables;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_volume_mounts;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_attempt_task_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_task_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_task_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_limits;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_requests;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_dependency_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_firelens_configuration_options_map;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) fn create_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::create_consumable_resource::builders::CreateConsumableResourceOutputBuilder,
 ) -> crate::operation::create_consumable_resource::builders::CreateConsumableResourceOutputBuilder {
@@ -11,6 +12,7 @@
     builder
 }

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) fn create_job_queue_output_output_correct_errors(
     mut builder: crate::operation::create_job_queue::builders::CreateJobQueueOutputBuilder,
 ) -> crate::operation::create_job_queue::builders::CreateJobQueueOutputBuilder {
@@ -23,6 +25,7 @@
     builder
 }

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) fn create_scheduling_policy_output_output_correct_errors(
     mut builder: crate::operation::create_scheduling_policy::builders::CreateSchedulingPolicyOutputBuilder,
 ) -> crate::operation::create_scheduling_policy::builders::CreateSchedulingPolicyOutputBuilder {
@@ -35,6 +38,7 @@
     builder
 }

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) fn create_service_environment_output_output_correct_errors(
     mut builder: crate::operation::create_service_environment::builders::CreateServiceEnvironmentOutputBuilder,
 ) -> crate::operation::create_service_environment::builders::CreateServiceEnvironmentOutputBuilder {
@@ -47,6 +51,7 @@
     builder
 }

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) fn describe_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::describe_consumable_resource::builders::DescribeConsumableResourceOutputBuilder,
 ) -> crate::operation::describe_consumable_resource::builders::DescribeConsumableResourceOutputBuilder {
@@ -59,6 +64,7 @@
     builder
 }

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) fn describe_service_job_output_output_correct_errors(
     mut builder: crate::operation::describe_service_job::builders::DescribeServiceJobOutputBuilder,
 ) -> crate::operation::describe_service_job::builders::DescribeServiceJobOutputBuilder {
@@ -83,6 +89,7 @@
     builder
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn list_consumable_resources_output_output_correct_errors(
     mut builder: crate::operation::list_consumable_resources::builders::ListConsumableResourcesOutputBuilder,
 ) -> crate::operation::list_consumable_resources::builders::ListConsumableResourcesOutputBuilder {
@@ -92,6 +99,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn list_jobs_output_output_correct_errors(
     mut builder: crate::operation::list_jobs::builders::ListJobsOutputBuilder,
 ) -> crate::operation::list_jobs::builders::ListJobsOutputBuilder {
@@ -101,6 +109,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn list_jobs_by_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::list_jobs_by_consumable_resource::builders::ListJobsByConsumableResourceOutputBuilder,
 ) -> crate::operation::list_jobs_by_consumable_resource::builders::ListJobsByConsumableResourceOutputBuilder {
@@ -110,6 +119,7 @@
     builder
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn list_service_jobs_output_output_correct_errors(
     mut builder: crate::operation::list_service_jobs::builders::ListServiceJobsOutputBuilder,
 ) -> crate::operation::list_service_jobs::builders::ListServiceJobsOutputBuilder {
@@ -119,6 +129,7 @@
     builder
 }

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) fn register_job_definition_output_output_correct_errors(
     mut builder: crate::operation::register_job_definition::builders::RegisterJobDefinitionOutputBuilder,
 ) -> crate::operation::register_job_definition::builders::RegisterJobDefinitionOutputBuilder {
@@ -134,6 +145,7 @@
     builder
 }

+#[cfg(feature = "op_submit_job")]
 pub(crate) fn submit_job_output_output_correct_errors(
     mut builder: crate::operation::submit_job::builders::SubmitJobOutputBuilder,
 ) -> crate::operation::submit_job::builders::SubmitJobOutputBuilder {
@@ -146,6 +158,7 @@
     builder
 }

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) fn submit_service_job_output_output_correct_errors(
     mut builder: crate::operation::submit_service_job::builders::SubmitServiceJobOutputBuilder,
 ) -> crate::operation::submit_service_job::builders::SubmitServiceJobOutputBuilder {
@@ -158,6 +171,7 @@
     builder
 }

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) fn update_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::update_consumable_resource::builders::UpdateConsumableResourceOutputBuilder,
 ) -> crate::operation::update_consumable_resource::builders::UpdateConsumableResourceOutputBuilder {
@@ -170,6 +184,7 @@
     builder
 }

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) fn update_service_environment_output_output_correct_errors(
     mut builder: crate::operation::update_service_environment::builders::UpdateServiceEnvironmentOutputBuilder,
 ) -> crate::operation::update_service_environment::builders::UpdateServiceEnvironmentOutputBuilder {
@@ -182,6 +197,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_preemption_configuration_correct_errors(
     mut builder: crate::types::builders::QuotaSharePreemptionConfigurationBuilder,
 ) -> crate::types::builders::QuotaSharePreemptionConfigurationBuilder {
@@ -193,6 +214,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_resource_sharing_configuration_correct_errors(
     mut builder: crate::types::builders::QuotaShareResourceSharingConfigurationBuilder,
 ) -> crate::types::builders::QuotaShareResourceSharingConfigurationBuilder {
@@ -204,6 +231,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) fn service_job_retry_strategy_correct_errors(
     mut builder: crate::types::builders::ServiceJobRetryStrategyBuilder,
 ) -> crate::types::builders::ServiceJobRetryStrategyBuilder {
@@ -213,6 +241,7 @@
     builder
 }

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn compute_environment_detail_correct_errors(
     mut builder: crate::types::builders::ComputeEnvironmentDetailBuilder,
 ) -> crate::types::builders::ComputeEnvironmentDetailBuilder {
@@ -225,6 +254,7 @@
     builder
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn consumable_resource_summary_correct_errors(
     mut builder: crate::types::builders::ConsumableResourceSummaryBuilder,
 ) -> crate::types::builders::ConsumableResourceSummaryBuilder {
@@ -237,6 +267,7 @@
     builder
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn job_definition_correct_errors(
     mut builder: crate::types::builders::JobDefinitionBuilder,
 ) -> crate::types::builders::JobDefinitionBuilder {
@@ -255,6 +286,7 @@
     builder
 }

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) fn job_detail_correct_errors(
     mut builder: crate::types::builders::JobDetailBuilder,
 ) -> crate::types::builders::JobDetailBuilder {
@@ -279,6 +311,7 @@
     builder
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn job_queue_detail_correct_errors(
     mut builder: crate::types::builders::JobQueueDetailBuilder,
 ) -> crate::types::builders::JobQueueDetailBuilder {
@@ -300,6 +333,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn job_summary_correct_errors(
     mut builder: crate::types::builders::JobSummaryBuilder,
 ) -> crate::types::builders::JobSummaryBuilder {
@@ -312,6 +346,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn list_jobs_by_consumable_resource_summary_correct_errors(
     mut builder: crate::types::builders::ListJobsByConsumableResourceSummaryBuilder,
 ) -> crate::types::builders::ListJobsByConsumableResourceSummaryBuilder {
@@ -342,6 +377,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_capacity_limit_correct_errors(
     mut builder: crate::types::builders::QuotaShareCapacityLimitBuilder,
 ) -> crate::types::builders::QuotaShareCapacityLimitBuilder {
@@ -354,6 +395,7 @@
     builder
 }

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) fn scheduling_policy_detail_correct_errors(
     mut builder: crate::types::builders::SchedulingPolicyDetailBuilder,
 ) -> crate::types::builders::SchedulingPolicyDetailBuilder {
@@ -366,6 +408,7 @@
     builder
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn scheduling_policy_listing_detail_correct_errors(
     mut builder: crate::types::builders::SchedulingPolicyListingDetailBuilder,
 ) -> crate::types::builders::SchedulingPolicyListingDetailBuilder {
@@ -375,6 +418,7 @@
     builder
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn service_environment_detail_correct_errors(
     mut builder: crate::types::builders::ServiceEnvironmentDetailBuilder,
 ) -> crate::types::builders::ServiceEnvironmentDetailBuilder {
@@ -393,6 +437,7 @@
     builder
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn service_job_summary_correct_errors(
     mut builder: crate::types::builders::ServiceJobSummaryBuilder,
 ) -> crate::types::builders::ServiceJobSummaryBuilder {
@@ -408,6 +453,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) fn service_resource_id_correct_errors(
     mut builder: crate::types::builders::ServiceResourceIdBuilder,
 ) -> crate::types::builders::ServiceResourceIdBuilder {
@@ -420,6 +466,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn compute_resource_correct_errors(
     mut builder: crate::types::builders::ComputeResourceBuilder,
 ) -> crate::types::builders::ComputeResourceBuilder {
@@ -432,6 +482,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ecs_properties_correct_errors(
     mut builder: crate::types::builders::EcsPropertiesBuilder,
 ) -> crate::types::builders::EcsPropertiesBuilder {
@@ -441,6 +496,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn eks_configuration_correct_errors(
     mut builder: crate::types::builders::EksConfigurationBuilder,
 ) -> crate::types::builders::EksConfigurationBuilder {
@@ -453,6 +512,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn node_properties_correct_errors(
     mut builder: crate::types::builders::NodePropertiesBuilder,
 ) -> crate::types::builders::NodePropertiesBuilder {
@@ -468,6 +532,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) fn quota_share_policy_correct_errors(
     mut builder: crate::types::builders::QuotaSharePolicyBuilder,
 ) -> crate::types::builders::QuotaSharePolicyBuilder {
@@ -479,6 +548,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn compute_environment_order_correct_errors(
     mut builder: crate::types::builders::ComputeEnvironmentOrderBuilder,
 ) -> crate::types::builders::ComputeEnvironmentOrderBuilder {
@@ -491,6 +565,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ephemeral_storage_correct_errors(
     mut builder: crate::types::builders::EphemeralStorageBuilder,
 ) -> crate::types::builders::EphemeralStorageBuilder {
@@ -500,6 +579,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn job_state_time_limit_action_correct_errors(
     mut builder: crate::types::builders::JobStateTimeLimitActionBuilder,
 ) -> crate::types::builders::JobStateTimeLimitActionBuilder {
@@ -522,6 +606,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn log_configuration_correct_errors(
     mut builder: crate::types::builders::LogConfigurationBuilder,
 ) -> crate::types::builders::LogConfigurationBuilder {
@@ -531,6 +620,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn managed_instances_provider_correct_errors(
     mut builder: crate::types::builders::ManagedInstancesProviderBuilder,
 ) -> crate::types::builders::ManagedInstancesProviderBuilder {
@@ -546,6 +639,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn repository_credentials_correct_errors(
     mut builder: crate::types::builders::RepositoryCredentialsBuilder,
 ) -> crate::types::builders::RepositoryCredentialsBuilder {
@@ -555,6 +653,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn service_environment_order_correct_errors(
     mut builder: crate::types::builders::ServiceEnvironmentOrderBuilder,
 ) -> crate::types::builders::ServiceEnvironmentOrderBuilder {
@@ -567,6 +670,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) fn ec2_configuration_correct_errors(
     mut builder: crate::types::builders::Ec2ConfigurationBuilder,
 ) -> crate::types::builders::Ec2ConfigurationBuilder {
@@ -576,6 +684,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ecs_task_properties_correct_errors(
     mut builder: crate::types::builders::EcsTaskPropertiesBuilder,
 ) -> crate::types::builders::EcsTaskPropertiesBuilder {
@@ -585,6 +698,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn evaluate_on_exit_correct_errors(
     mut builder: crate::types::builders::EvaluateOnExitBuilder,
 ) -> crate::types::builders::EvaluateOnExitBuilder {
@@ -594,6 +713,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn instance_launch_template_correct_errors(
     mut builder: crate::types::builders::InstanceLaunchTemplateBuilder,
 ) -> crate::types::builders::InstanceLaunchTemplateBuilder {
@@ -609,6 +732,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn node_range_property_correct_errors(
     mut builder: crate::types::builders::NodeRangePropertyBuilder,
 ) -> crate::types::builders::NodeRangePropertyBuilder {
@@ -618,6 +746,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn resource_requirement_correct_errors(
     mut builder: crate::types::builders::ResourceRequirementBuilder,
 ) -> crate::types::builders::ResourceRequirementBuilder {
@@ -630,6 +764,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn secret_correct_errors(
     mut builder: crate::types::builders::SecretBuilder,
 ) -> crate::types::builders::SecretBuilder {
@@ -642,6 +781,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) fn share_attributes_correct_errors(
     mut builder: crate::types::builders::ShareAttributesBuilder,
 ) -> crate::types::builders::ShareAttributesBuilder {
@@ -651,6 +795,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ulimit_correct_errors(
     mut builder: crate::types::builders::UlimitBuilder,
 ) -> crate::types::builders::UlimitBuilder {
@@ -666,6 +815,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn device_correct_errors(
     mut builder: crate::types::builders::DeviceBuilder,
 ) -> crate::types::builders::DeviceBuilder {
@@ -675,6 +829,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn efs_volume_configuration_correct_errors(
     mut builder: crate::types::builders::EfsVolumeConfigurationBuilder,
 ) -> crate::types::builders::EfsVolumeConfigurationBuilder {
@@ -684,6 +843,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_container_correct_errors(
     mut builder: crate::types::builders::EksContainerBuilder,
 ) -> crate::types::builders::EksContainerBuilder {
@@ -693,6 +857,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_volume_correct_errors(
     mut builder: crate::types::builders::EksVolumeBuilder,
 ) -> crate::types::builders::EksVolumeBuilder {
@@ -702,6 +871,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn image_pull_secret_correct_errors(
     mut builder: crate::types::builders::ImagePullSecretBuilder,
 ) -> crate::types::builders::ImagePullSecretBuilder {
@@ -711,6 +885,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) fn managed_instances_network_configuration_correct_errors(
     mut builder: crate::types::builders::ManagedInstancesNetworkConfigurationBuilder,
 ) -> crate::types::builders::ManagedInstancesNetworkConfigurationBuilder {
@@ -723,6 +902,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn s3_files_volume_configuration_correct_errors(
     mut builder: crate::types::builders::S3FilesVolumeConfigurationBuilder,
 ) -> crate::types::builders::S3FilesVolumeConfigurationBuilder {
@@ -732,6 +916,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn tmpfs_correct_errors(
     mut builder: crate::types::builders::TmpfsBuilder,
 ) -> crate::types::builders::TmpfsBuilder {
@@ -744,6 +933,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_persistent_volume_claim_correct_errors(
     mut builder: crate::types::builders::EksPersistentVolumeClaimBuilder,
 ) -> crate::types::builders::EksPersistentVolumeClaimBuilder {
@@ -753,6 +947,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_secret_correct_errors(
     mut builder: crate::types::builders::EksSecretBuilder,
 ) -> crate::types::builders::EksSecretBuilder {
@@ -762,6 +961,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn task_container_properties_correct_errors(
     mut builder: crate::types::builders::TaskContainerPropertiesBuilder,
 ) -> crate::types::builders::TaskContainerPropertiesBuilder {
@@ -771,6 +975,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn eks_container_environment_variable_correct_errors(
     mut builder: crate::types::builders::EksContainerEnvironmentVariableBuilder,
 ) -> crate::types::builders::EksContainerEnvironmentVariableBuilder {
@@ -780,6 +990,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn firelens_configuration_correct_errors(
     mut builder: crate::types::builders::FirelensConfigurationBuilder,
 ) -> crate::types::builders::FirelensConfigurationBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,722 +1,1898 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_ce_type::CeType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ce_state::CeState;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_compute_resource::ComputeResource;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_eks_configuration::EksConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ecs_settings::EcsSettings;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_jq_state::JqState;

+#[cfg(any(feature = "op_create_job_queue", feature = "op_describe_job_queues"))]
 pub use crate::types::_job_queue_type::JobQueueType;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_configuration::QuotaShareResourceSharingConfiguration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_preemption_configuration::QuotaSharePreemptionConfiguration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_state::QuotaShareState;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_policy::QuotaSharePolicy;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_fairshare_policy::FairsharePolicy;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments"
+))]
 pub use crate::types::_service_environment_type::ServiceEnvironmentType;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_service_environment_state::ServiceEnvironmentState;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 pub use crate::types::_quota_share_status::QuotaShareStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_latest_service_job_attempt::LatestServiceJobAttempt;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_strategy::ServiceJobRetryStrategy;

+#[cfg(any(
+    feature = "op_describe_service_job",
+    feature = "op_list_service_jobs",
+    feature = "op_submit_service_job"
+))]
 pub use crate::types::_service_job_type::ServiceJobType;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_preemption_configuration::ServiceJobPreemptionConfiguration;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preemption_summary::ServiceJobPreemptionSummary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_job_status::ServiceJobStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_timeout::ServiceJobTimeout;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_detail::FrontOfQueueDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_shares_detail::FrontOfQuotaSharesDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_utilization_detail::QueueSnapshotUtilizationDetail;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 pub use crate::types::_job_status::JobStatus;

+#[cfg(feature = "op_register_job_definition")]
 pub use crate::types::_job_definition_type::JobDefinitionType;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_container_properties::ContainerProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_properties::NodeProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_strategy::RetryStrategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_job_timeout::JobTimeout;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_properties::EksProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_properties::EcsProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_properties::ConsumableResourceProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_array_properties::ArrayProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_container_overrides::ContainerOverrides;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_overrides::NodeOverrides;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_properties_override::EksPropertiesOverride;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_ecs_properties_override::EcsPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_compute_resource_update::ComputeResourceUpdate;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_update_policy::UpdatePolicy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_cr_type::CrType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_cr_allocation_strategy::CrAllocationStrategy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification::LaunchTemplateSpecification;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_compute_scaling_policy::ComputeScalingPolicy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_managed_instances_provider::ManagedInstancesProvider;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_container_insights::ContainerInsights;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_compute_environment_order::ComputeEnvironmentOrder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_service_environment_order::ServiceEnvironmentOrder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_action::JobStateTimeLimitAction;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_capacity_limit::QuotaShareCapacityLimit;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_strategy::QuotaShareResourceSharingStrategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_in_share_preemption_state::QuotaShareInSharePreemptionState;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_idle_resource_assignment_strategy::QuotaShareIdleResourceAssignmentStrategy;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_capacity_limit::CapacityLimit;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_compute_environment_detail::ComputeEnvironmentDetail;

+#[cfg(feature = "op_describe_job_definitions")]
 pub use crate::types::_job_definition::JobDefinition;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_job_queue_detail::JobQueueDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_job_detail::JobDetail;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub use crate::types::_scheduling_policy_detail::SchedulingPolicyDetail;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_detail::ServiceEnvironmentDetail;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_attempt_detail::ServiceJobAttemptDetail;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_capacity_usage_detail::ServiceJobCapacityUsageDetail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id::ServiceResourceId;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_utilization_detail::FairshareUtilizationDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_utilization_detail::QuotaShareUtilizationDetail;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub use crate::types::_key_values_pair::KeyValuesPair;

+#[cfg(feature = "op_list_consumable_resources")]
 pub use crate::types::_consumable_resource_summary::ConsumableResourceSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_summary::JobSummary;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub use crate::types::_list_jobs_by_consumable_resource_summary::ListJobsByConsumableResourceSummary;

+#[cfg(feature = "op_list_quota_shares")]
 pub use crate::types::_quota_share_detail::QuotaShareDetail;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub use crate::types::_scheduling_policy_listing_detail::SchedulingPolicyListingDetail;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_summary::ServiceJobSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_linux_parameters::LinuxParameters;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_configuration::LogConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_network_configuration::NetworkConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_fargate_platform_configuration::FargatePlatformConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ephemeral_storage::EphemeralStorage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_runtime_platform::RuntimePlatform;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_repository_credentials::RepositoryCredentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_platform_capability::PlatformCapability;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_pod_properties::EksPodProperties;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_job_dependency::JobDependency;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_pod_properties_override::EksPodPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_cr_update_allocation_strategy::CrUpdateAllocationStrategy;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_update_managed_instances_provider_configuration::UpdateManagedInstancesProviderConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_userdata_type::UserdataType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ec2_configuration::Ec2Configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_instance_launch_template::InstanceLaunchTemplate;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_infrastructure_optimization::InfrastructureOptimization;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_actions_state::JobStateTimeLimitActionsState;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_actions_action::JobStateTimeLimitActionsAction;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_share_attributes::ShareAttributes;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_ce_status::CeStatus;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions"
+))]
 pub use crate::types::_orchestration_type::OrchestrationType;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_jq_status::JqStatus;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_container_detail::ContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_node_details::NodeDetails;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_array_properties_detail::ArrayPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_properties_detail::EksPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_properties_detail::EcsPropertiesDetail;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_status::ServiceEnvironmentStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id_name::ServiceResourceIdName;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_evaluate_on_exit::ServiceJobEvaluateOnExit;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preempted_attempt::ServiceJobPreemptedAttempt;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_job_summary::FrontOfQueueJobSummary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_capacity_usage::QueueSnapshotCapacityUsage;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_container_summary::ContainerSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_array_properties_summary::ArrayPropertiesSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_node_properties_summary::NodePropertiesSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_volume::Volume;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_key_value_pair::KeyValuePair;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_mount_point::MountPoint;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ulimit::Ulimit;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_requirement::ResourceRequirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_driver::LogDriver;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_secret::Secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_assign_public_ip::AssignPublicIp;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_range_property::NodeRangeProperty;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_evaluate_on_exit::EvaluateOnExit;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_metadata::EksMetadata;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_task_properties::EcsTaskProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_requirement::ConsumableResourceRequirement;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_array_job_dependency::ArrayJobDependency;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_property_override::NodePropertyOverride;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_properties_override::TaskPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_instance_launch_template_update::InstanceLaunchTemplateUpdate;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification_override::LaunchTemplateSpecificationOverride;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_network_configuration::ManagedInstancesNetworkConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_instance_requirements_request::InstanceRequirementsRequest;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_storage_configuration::ManagedInstancesStorageConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_capacity_reservation_request::CapacityReservationRequest;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_local_storage_configuration::ManagedInstancesLocalStorageConfiguration;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_detail::AttemptDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_pod_properties_detail::EksPodPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_detail::EksAttemptDetail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_action::ServiceJobRetryAction;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_share_job_summary::FrontOfQuotaShareJobSummary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_utilization::FairshareCapacityUtilization;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_utilization::QuotaShareCapacityUtilization;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_capacity_usage_summary::JobCapacityUsageSummary;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_capacity_usage_summary::ServiceJobCapacityUsageSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_host::Host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_volume_configuration::EfsVolumeConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_s3_files_volume_configuration::S3FilesVolumeConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_type::ResourceType;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device::Device;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_tmpfs::Tmpfs;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_action::RetryAction;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_image_pull_secret::ImagePullSecret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container::EksContainer;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_volume::EksVolume;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_container_override::EksContainerOverride;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_container_detail::AttemptContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_network_interface::NetworkInterface;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_task_details::EcsTaskDetails;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_transit_encryption::EfsTransitEncryption;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config::EfsAuthorizationConfig;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_resource_requirements::EksContainerResourceRequirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_security_context::EksContainerSecurityContext;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_host_path::EksHostPath;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_empty_dir::EksEmptyDir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_secret::EksSecret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_persistent_volume_claim::EksPersistentVolumeClaim;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_properties::TaskContainerProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_container_overrides::TaskContainerOverrides;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_ecs_task_details::AttemptEcsTaskDetails;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_container_detail::EksContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_container_detail::EksAttemptContainerDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_usage::FairshareCapacityUsage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_usage::QuotaShareCapacityUsage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config_iam::EfsAuthorizationConfigIam;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device_cgroup_permission::DeviceCgroupPermission;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_environment_variable::EksContainerEnvironmentVariable;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_volume_mount::EksContainerVolumeMount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration::FirelensConfiguration;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_task_container_details::TaskContainerDetails;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_dependency::TaskContainerDependency;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration_type::FirelensConfigurationType;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_task_container_details::AttemptTaskContainerDetails;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 mod _array_job_dependency;

+#[cfg(feature = "op_submit_job")]
 mod _array_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _array_properties_detail;

+#[cfg(feature = "op_list_jobs")]
 mod _array_properties_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _assign_public_ip;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_ecs_task_details;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_task_container_details;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 mod _capacity_limit;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _capacity_reservation_request;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ce_state;

+#[cfg(feature = "op_describe_compute_environments")]
 mod _ce_status;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _ce_type;

+#[cfg(feature = "op_describe_compute_environments")]
 mod _compute_environment_detail;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _compute_environment_order;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _compute_resource;

+#[cfg(feature = "op_update_compute_environment")]
 mod _compute_resource_update;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _compute_scaling_policy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _consumable_resource_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _consumable_resource_requirement;

+#[cfg(feature = "op_list_consumable_resources")]
 mod _consumable_resource_summary;

+#[cfg(feature = "op_describe_jobs")]
 mod _container_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _container_insights;

+#[cfg(feature = "op_submit_job")]
 mod _container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _container_properties;

+#[cfg(feature = "op_list_jobs")]
 mod _container_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _cr_allocation_strategy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _cr_type;

+#[cfg(feature = "op_update_compute_environment")]
 mod _cr_update_allocation_strategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _device;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _device_cgroup_permission;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ec2_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ecs_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _ecs_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _ecs_properties_override;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ecs_settings;

+#[cfg(feature = "op_describe_jobs")]
 mod _ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ecs_task_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_authorization_config;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_authorization_config_iam;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_transit_encryption;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_volume_configuration;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_attempt_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _eks_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_container_environment_variable;

+#[cfg(feature = "op_submit_job")]
 mod _eks_container_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_container_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container_security_context;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container_volume_mount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_empty_dir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_host_path;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_metadata;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_persistent_volume_claim;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_pod_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_pod_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _eks_pod_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _eks_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_volume;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ephemeral_storage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _evaluate_on_exit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_capacity_utilization;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _fairshare_policy;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _fargate_platform_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _firelens_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _firelens_configuration_type;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_queue_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_queue_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_quota_share_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_quota_shares_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _image_pull_secret;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _infrastructure_optimization;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _instance_launch_template;

+#[cfg(feature = "op_update_compute_environment")]
 mod _instance_launch_template_update;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _instance_requirements_request;

+#[cfg(feature = "op_list_jobs")]
 mod _job_capacity_usage_summary;

+#[cfg(feature = "op_describe_job_definitions")]
 mod _job_definition;

+#[cfg(feature = "op_register_job_definition")]
 mod _job_definition_type;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 mod _job_dependency;

+#[cfg(feature = "op_describe_jobs")]
 mod _job_detail;

+#[cfg(feature = "op_describe_job_queues")]
 mod _job_queue_detail;

+#[cfg(any(feature = "op_create_job_queue", feature = "op_describe_job_queues"))]
 mod _job_queue_type;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_action;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_actions_action;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_actions_state;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 mod _job_status;

+#[cfg(feature = "op_list_jobs")]
 mod _job_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _job_timeout;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _jq_state;

+#[cfg(feature = "op_describe_job_queues")]
 mod _jq_status;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _key_value_pair;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 mod _key_values_pair;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _latest_service_job_attempt;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _launch_template_specification;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _launch_template_specification_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _linux_parameters;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 mod _list_jobs_by_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _log_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _log_driver;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_local_storage_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_network_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _managed_instances_provider;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_storage_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _mount_point;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _network_configuration;

+#[cfg(feature = "op_describe_jobs")]
 mod _network_interface;

+#[cfg(feature = "op_describe_jobs")]
 mod _node_details;

+#[cfg(feature = "op_submit_job")]
 mod _node_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _node_properties;

+#[cfg(feature = "op_list_jobs")]
 mod _node_properties_summary;

+#[cfg(feature = "op_submit_job")]
 mod _node_property_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _node_range_property;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions"
+))]
 mod _orchestration_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _platform_capability;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _queue_snapshot_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _queue_snapshot_utilization_detail;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_capacity_limit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_capacity_utilization;

+#[cfg(feature = "op_list_quota_shares")]
 mod _quota_share_detail;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _quota_share_idle_resource_assignment_strategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_in_share_preemption_state;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _quota_share_policy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_preemption_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_resource_sharing_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_resource_sharing_strategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_state;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 mod _quota_share_status;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _repository_credentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _resource_requirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _resource_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _retry_action;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _retry_strategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _runtime_platform;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _s3_files_volume_configuration;

+#[cfg(feature = "op_describe_scheduling_policies")]
 mod _scheduling_policy_detail;

+#[cfg(feature = "op_list_scheduling_policies")]
 mod _scheduling_policy_listing_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _secret;

+#[cfg(feature = "op_describe_service_environments")]
 mod _service_environment_detail;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _service_environment_order;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 mod _service_environment_state;

+#[cfg(feature = "op_describe_service_environments")]
 mod _service_environment_status;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments"
+))]
 mod _service_environment_type;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_attempt_detail;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_capacity_usage_detail;

+#[cfg(feature = "op_list_service_jobs")]
 mod _service_job_capacity_usage_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_evaluate_on_exit;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_preempted_attempt;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_preemption_configuration;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_preemption_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_retry_action;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_retry_strategy;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_job_status;

+#[cfg(feature = "op_list_service_jobs")]
 mod _service_job_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_timeout;

+#[cfg(any(
+    feature = "op_describe_service_job",
+    feature = "op_list_service_jobs",
+    feature = "op_submit_service_job"
+))]
 mod _service_job_type;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_resource_id;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_resource_id_name;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _share_attributes;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _task_container_dependency;

+#[cfg(feature = "op_describe_jobs")]
 mod _task_container_details;

+#[cfg(feature = "op_submit_job")]
 mod _task_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _task_container_properties;

+#[cfg(feature = "op_submit_job")]
 mod _task_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _tmpfs;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ulimit;

+#[cfg(feature = "op_update_compute_environment")]
 mod _update_managed_instances_provider_configuration;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _update_policy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _userdata_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _volume;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,284 +1,729 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_compute_resource::ComputeResourceBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_eks_configuration::EksConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ecs_settings::EcsSettingsBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_configuration::QuotaShareResourceSharingConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_preemption_configuration::QuotaSharePreemptionConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_policy::QuotaSharePolicyBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_fairshare_policy::FairsharePolicyBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_latest_service_job_attempt::LatestServiceJobAttemptBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_strategy::ServiceJobRetryStrategyBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_preemption_configuration::ServiceJobPreemptionConfigurationBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preemption_summary::ServiceJobPreemptionSummaryBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_timeout::ServiceJobTimeoutBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_detail::FrontOfQueueDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_shares_detail::FrontOfQuotaSharesDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_utilization_detail::QueueSnapshotUtilizationDetailBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_container_properties::ContainerPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_properties::NodePropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_strategy::RetryStrategyBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_job_timeout::JobTimeoutBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_properties::EksPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_properties::EcsPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_properties::ConsumableResourcePropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_array_properties::ArrayPropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_container_overrides::ContainerOverridesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_overrides::NodeOverridesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_properties_override::EksPropertiesOverrideBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_ecs_properties_override::EcsPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_compute_resource_update::ComputeResourceUpdateBuilder;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_update_policy::UpdatePolicyBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification::LaunchTemplateSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_compute_scaling_policy::ComputeScalingPolicyBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_managed_instances_provider::ManagedInstancesProviderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_compute_environment_order::ComputeEnvironmentOrderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_service_environment_order::ServiceEnvironmentOrderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_action::JobStateTimeLimitActionBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_capacity_limit::QuotaShareCapacityLimitBuilder;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_capacity_limit::CapacityLimitBuilder;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_compute_environment_detail::ComputeEnvironmentDetailBuilder;

+#[cfg(feature = "op_describe_job_definitions")]
 pub use crate::types::_job_definition::JobDefinitionBuilder;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_job_queue_detail::JobQueueDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_job_detail::JobDetailBuilder;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub use crate::types::_scheduling_policy_detail::SchedulingPolicyDetailBuilder;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_detail::ServiceEnvironmentDetailBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_attempt_detail::ServiceJobAttemptDetailBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_capacity_usage_detail::ServiceJobCapacityUsageDetailBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id::ServiceResourceIdBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_utilization_detail::FairshareUtilizationDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_utilization_detail::QuotaShareUtilizationDetailBuilder;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub use crate::types::_key_values_pair::KeyValuesPairBuilder;

+#[cfg(feature = "op_list_consumable_resources")]
 pub use crate::types::_consumable_resource_summary::ConsumableResourceSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_summary::JobSummaryBuilder;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub use crate::types::_list_jobs_by_consumable_resource_summary::ListJobsByConsumableResourceSummaryBuilder;

+#[cfg(feature = "op_list_quota_shares")]
 pub use crate::types::_quota_share_detail::QuotaShareDetailBuilder;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub use crate::types::_scheduling_policy_listing_detail::SchedulingPolicyListingDetailBuilder;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_summary::ServiceJobSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_linux_parameters::LinuxParametersBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_configuration::LogConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_network_configuration::NetworkConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_fargate_platform_configuration::FargatePlatformConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ephemeral_storage::EphemeralStorageBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_runtime_platform::RuntimePlatformBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_repository_credentials::RepositoryCredentialsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_pod_properties::EksPodPropertiesBuilder;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_job_dependency::JobDependencyBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_pod_properties_override::EksPodPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_update_managed_instances_provider_configuration::UpdateManagedInstancesProviderConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ec2_configuration::Ec2ConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_instance_launch_template::InstanceLaunchTemplateBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_infrastructure_optimization::InfrastructureOptimizationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_share_attributes::ShareAttributesBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_container_detail::ContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_node_details::NodeDetailsBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_array_properties_detail::ArrayPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_properties_detail::EksPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_properties_detail::EcsPropertiesDetailBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_evaluate_on_exit::ServiceJobEvaluateOnExitBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preempted_attempt::ServiceJobPreemptedAttemptBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_job_summary::FrontOfQueueJobSummaryBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_capacity_usage::QueueSnapshotCapacityUsageBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_container_summary::ContainerSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_array_properties_summary::ArrayPropertiesSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_node_properties_summary::NodePropertiesSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_volume::VolumeBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_key_value_pair::KeyValuePairBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_mount_point::MountPointBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ulimit::UlimitBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_requirement::ResourceRequirementBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_secret::SecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_range_property::NodeRangePropertyBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_evaluate_on_exit::EvaluateOnExitBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_metadata::EksMetadataBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_task_properties::EcsTaskPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_requirement::ConsumableResourceRequirementBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_property_override::NodePropertyOverrideBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_properties_override::TaskPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_instance_launch_template_update::InstanceLaunchTemplateUpdateBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification_override::LaunchTemplateSpecificationOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_network_configuration::ManagedInstancesNetworkConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_instance_requirements_request::InstanceRequirementsRequestBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_storage_configuration::ManagedInstancesStorageConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_capacity_reservation_request::CapacityReservationRequestBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_local_storage_configuration::ManagedInstancesLocalStorageConfigurationBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_detail::AttemptDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_pod_properties_detail::EksPodPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_detail::EksAttemptDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_share_job_summary::FrontOfQuotaShareJobSummaryBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_utilization::FairshareCapacityUtilizationBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_utilization::QuotaShareCapacityUtilizationBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_capacity_usage_summary::JobCapacityUsageSummaryBuilder;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_capacity_usage_summary::ServiceJobCapacityUsageSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_host::HostBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_volume_configuration::EfsVolumeConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_s3_files_volume_configuration::S3FilesVolumeConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device::DeviceBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_tmpfs::TmpfsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_image_pull_secret::ImagePullSecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container::EksContainerBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_volume::EksVolumeBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_container_override::EksContainerOverrideBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_container_detail::AttemptContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_network_interface::NetworkInterfaceBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_task_details::EcsTaskDetailsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config::EfsAuthorizationConfigBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_resource_requirements::EksContainerResourceRequirementsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_security_context::EksContainerSecurityContextBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_host_path::EksHostPathBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_empty_dir::EksEmptyDirBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_secret::EksSecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_persistent_volume_claim::EksPersistentVolumeClaimBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_properties::TaskContainerPropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_container_overrides::TaskContainerOverridesBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_ecs_task_details::AttemptEcsTaskDetailsBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_container_detail::EksContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_container_detail::EksAttemptContainerDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_usage::FairshareCapacityUsageBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_usage::QuotaShareCapacityUsageBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_environment_variable::EksContainerEnvironmentVariableBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_volume_mount::EksContainerVolumeMountBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration::FirelensConfigurationBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_task_container_details::TaskContainerDetailsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_dependency::TaskContainerDependencyBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_task_container_details::AttemptTaskContainerDetailsBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,10 +1,198 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_client_exception::ClientException;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_server_exception::ServerException;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 mod _client_exception;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 mod _server_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,4 +1,98 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_client_exception::ClientExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_server_exception::ServerExceptionBuilder;
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
@@ -84,16 +73,13 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

 [dev-dependencies.aws-smithy-protocol-test]
-path = "../aws-smithy-protocol-test"
 version = "0.64.0"

 [dev-dependencies.pretty_assertions]
@@ -118,3 +104,48 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_cancel_job = []
+op_create_compute_environment = []
+op_create_consumable_resource = []
+op_create_job_queue = []
+op_create_quota_share = []
+op_create_scheduling_policy = []
+op_create_service_environment = []
+op_delete_compute_environment = []
+op_delete_consumable_resource = []
+op_delete_job_queue = []
+op_delete_quota_share = []
+op_delete_scheduling_policy = []
+op_delete_service_environment = []
+op_deregister_job_definition = []
+op_describe_compute_environments = []
+op_describe_consumable_resource = []
+op_describe_job_definitions = []
+op_describe_job_queues = []
+op_describe_jobs = []
+op_describe_quota_share = []
+op_describe_scheduling_policies = []
+op_describe_service_environments = []
+op_describe_service_job = []
+op_get_job_queue_snapshot = []
+op_list_consumable_resources = []
+op_list_jobs = []
+op_list_jobs_by_consumable_resource = []
+op_list_quota_shares = []
+op_list_scheduling_policies = []
+op_list_service_jobs = []
+op_list_tags_for_resource = []
+op_register_job_definition = []
+op_submit_job = []
+op_submit_service_job = []
+op_tag_resource = []
+op_terminate_job = []
+op_terminate_service_job = []
+op_untag_resource = []
+op_update_compute_environment = []
+op_update_consumable_resource = []
+op_update_job_queue = []
+op_update_quota_share = []
+op_update_scheduling_policy = []
+op_update_service_environment = []
+op_update_service_job = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,18 +136,25 @@
     }
 }

+#[cfg(feature = "op_cancel_job")]
 mod cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 mod create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 mod create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 mod create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 mod create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 mod create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 mod create_service_environment;

 /// Operation customization and supporting types.
@@ -177,78 +184,116 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_compute_environment")]
 mod delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 mod delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 mod delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 mod delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 mod delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 mod delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 mod deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 mod describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 mod describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 mod describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 mod describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 mod describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 mod describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 mod describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 mod describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 mod describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 mod list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 mod list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 mod list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 mod list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 mod list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 mod list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 mod register_job_definition;

+#[cfg(feature = "op_submit_job")]
 mod submit_job;

+#[cfg(feature = "op_submit_service_job")]
 mod submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_terminate_job")]
 mod terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 mod terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 mod update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 mod update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 mod update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 mod update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 mod update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 mod update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 mod update_service_job;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,8 +3,102 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_cancel_job",
+        feature = "op_create_compute_environment",
+        feature = "op_create_consumable_resource",
+        feature = "op_create_job_queue",
+        feature = "op_create_quota_share",
+        feature = "op_create_scheduling_policy",
+        feature = "op_create_service_environment",
+        feature = "op_delete_compute_environment",
+        feature = "op_delete_consumable_resource",
+        feature = "op_delete_job_queue",
+        feature = "op_delete_quota_share",
+        feature = "op_delete_scheduling_policy",
+        feature = "op_delete_service_environment",
+        feature = "op_deregister_job_definition",
+        feature = "op_describe_compute_environments",
+        feature = "op_describe_consumable_resource",
+        feature = "op_describe_job_definitions",
+        feature = "op_describe_job_queues",
+        feature = "op_describe_jobs",
+        feature = "op_describe_quota_share",
+        feature = "op_describe_scheduling_policies",
+        feature = "op_describe_service_environments",
+        feature = "op_describe_service_job",
+        feature = "op_get_job_queue_snapshot",
+        feature = "op_list_consumable_resources",
+        feature = "op_list_jobs",
+        feature = "op_list_jobs_by_consumable_resource",
+        feature = "op_list_quota_shares",
+        feature = "op_list_scheduling_policies",
+        feature = "op_list_service_jobs",
+        feature = "op_list_tags_for_resource",
+        feature = "op_register_job_definition",
+        feature = "op_submit_job",
+        feature = "op_submit_service_job",
+        feature = "op_tag_resource",
+        feature = "op_terminate_job",
+        feature = "op_terminate_service_job",
+        feature = "op_untag_resource",
+        feature = "op_update_compute_environment",
+        feature = "op_update_consumable_resource",
+        feature = "op_update_job_queue",
+        feature = "op_update_quota_share",
+        feature = "op_update_scheduling_policy",
+        feature = "op_update_service_environment",
+        feature = "op_update_service_job"
+    ))]
     /// <p>These errors are usually caused by a client action. One example cause is using an action or resource on behalf of a user that doesn't have permissions to use the action or resource. Another cause is specifying an identifier that's not valid.</p>
     ClientException(crate::types::error::ClientException),
+    #[cfg(any(
+        feature = "op_cancel_job",
+        feature = "op_create_compute_environment",
+        feature = "op_create_consumable_resource",
+        feature = "op_create_job_queue",
+        feature = "op_create_quota_share",
+        feature = "op_create_scheduling_policy",
+        feature = "op_create_service_environment",
+        feature = "op_delete_compute_environment",
+        feature = "op_delete_consumable_resource",
+        feature = "op_delete_job_queue",
+        feature = "op_delete_quota_share",
+        feature = "op_delete_scheduling_policy",
+        feature = "op_delete_service_environment",
+        feature = "op_deregister_job_definition",
+        feature = "op_describe_compute_environments",
+        feature = "op_describe_consumable_resource",
+        feature = "op_describe_job_definitions",
+        feature = "op_describe_job_queues",
+        feature = "op_describe_jobs",
+        feature = "op_describe_quota_share",
+        feature = "op_describe_scheduling_policies",
+        feature = "op_describe_service_environments",
+        feature = "op_describe_service_job",
+        feature = "op_get_job_queue_snapshot",
+        feature = "op_list_consumable_resources",
+        feature = "op_list_jobs",
+        feature = "op_list_jobs_by_consumable_resource",
+        feature = "op_list_quota_shares",
+        feature = "op_list_scheduling_policies",
+        feature = "op_list_service_jobs",
+        feature = "op_list_tags_for_resource",
+        feature = "op_register_job_definition",
+        feature = "op_submit_job",
+        feature = "op_submit_service_job",
+        feature = "op_tag_resource",
+        feature = "op_terminate_job",
+        feature = "op_terminate_service_job",
+        feature = "op_untag_resource",
+        feature = "op_update_compute_environment",
+        feature = "op_update_consumable_resource",
+        feature = "op_update_job_queue",
+        feature = "op_update_quota_share",
+        feature = "op_update_scheduling_policy",
+        feature = "op_update_service_environment",
+        feature = "op_update_service_job"
+    ))]
     /// <p>These errors are usually caused by a server issue.</p>
     ServerException(crate::types::error::ServerException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -21,7 +115,101 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ClientException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ServerException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -46,12 +234,107 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ClientException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ServerException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_cancel_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::cancel_job::CancelJobError, R>>
     for Error
 where
@@ -69,6 +352,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_job")]
 impl From<crate::operation::cancel_job::CancelJobError> for Error {
     fn from(err: crate::operation::cancel_job::CancelJobError) -> Self {
         match err {
@@ -78,6 +362,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -103,6 +388,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_compute_environment")]
 impl From<crate::operation::create_compute_environment::CreateComputeEnvironmentError> for Error {
     fn from(err: crate::operation::create_compute_environment::CreateComputeEnvironmentError) -> Self {
         match err {
@@ -118,6 +404,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -143,6 +430,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_consumable_resource")]
 impl From<crate::operation::create_consumable_resource::CreateConsumableResourceError> for Error {
     fn from(err: crate::operation::create_consumable_resource::CreateConsumableResourceError) -> Self {
         match err {
@@ -158,6 +446,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_job_queue::CreateJobQueueError, R>>
     for Error
@@ -179,6 +468,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_job_queue")]
 impl From<crate::operation::create_job_queue::CreateJobQueueError> for Error {
     fn from(err: crate::operation::create_job_queue::CreateJobQueueError) -> Self {
         match err {
@@ -192,6 +482,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -217,6 +508,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_quota_share")]
 impl From<crate::operation::create_quota_share::CreateQuotaShareError> for Error {
     fn from(err: crate::operation::create_quota_share::CreateQuotaShareError) -> Self {
         match err {
@@ -230,6 +522,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -255,6 +548,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduling_policy")]
 impl From<crate::operation::create_scheduling_policy::CreateSchedulingPolicyError> for Error {
     fn from(err: crate::operation::create_scheduling_policy::CreateSchedulingPolicyError) -> Self {
         match err {
@@ -270,6 +564,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -295,6 +590,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_service_environment")]
 impl From<crate::operation::create_service_environment::CreateServiceEnvironmentError> for Error {
     fn from(err: crate::operation::create_service_environment::CreateServiceEnvironmentError) -> Self {
         match err {
@@ -310,6 +606,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -335,6 +632,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_compute_environment")]
 impl From<crate::operation::delete_compute_environment::DeleteComputeEnvironmentError> for Error {
     fn from(err: crate::operation::delete_compute_environment::DeleteComputeEnvironmentError) -> Self {
         match err {
@@ -350,6 +648,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -375,6 +674,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_consumable_resource")]
 impl From<crate::operation::delete_consumable_resource::DeleteConsumableResourceError> for Error {
     fn from(err: crate::operation::delete_consumable_resource::DeleteConsumableResourceError) -> Self {
         match err {
@@ -390,6 +690,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_job_queue::DeleteJobQueueError, R>>
     for Error
@@ -411,6 +712,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_job_queue")]
 impl From<crate::operation::delete_job_queue::DeleteJobQueueError> for Error {
     fn from(err: crate::operation::delete_job_queue::DeleteJobQueueError) -> Self {
         match err {
@@ -424,6 +726,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -449,6 +752,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_quota_share")]
 impl From<crate::operation::delete_quota_share::DeleteQuotaShareError> for Error {
     fn from(err: crate::operation::delete_quota_share::DeleteQuotaShareError) -> Self {
         match err {
@@ -462,6 +766,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -487,6 +792,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduling_policy")]
 impl From<crate::operation::delete_scheduling_policy::DeleteSchedulingPolicyError> for Error {
     fn from(err: crate::operation::delete_scheduling_policy::DeleteSchedulingPolicyError) -> Self {
         match err {
@@ -502,6 +808,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -527,6 +834,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_service_environment")]
 impl From<crate::operation::delete_service_environment::DeleteServiceEnvironmentError> for Error {
     fn from(err: crate::operation::delete_service_environment::DeleteServiceEnvironmentError) -> Self {
         match err {
@@ -542,6 +850,7 @@
         }
     }
 }
+#[cfg(feature = "op_deregister_job_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -567,6 +876,7 @@
         }
     }
 }
+#[cfg(feature = "op_deregister_job_definition")]
 impl From<crate::operation::deregister_job_definition::DeregisterJobDefinitionError> for Error {
     fn from(err: crate::operation::deregister_job_definition::DeregisterJobDefinitionError) -> Self {
         match err {
@@ -582,6 +892,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_compute_environments")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -607,6 +918,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_compute_environments")]
 impl From<crate::operation::describe_compute_environments::DescribeComputeEnvironmentsError> for Error {
     fn from(err: crate::operation::describe_compute_environments::DescribeComputeEnvironmentsError) -> Self {
         match err {
@@ -622,6 +934,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -647,6 +960,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_consumable_resource")]
 impl From<crate::operation::describe_consumable_resource::DescribeConsumableResourceError> for Error {
     fn from(err: crate::operation::describe_consumable_resource::DescribeConsumableResourceError) -> Self {
         match err {
@@ -662,6 +976,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_definitions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -687,6 +1002,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_definitions")]
 impl From<crate::operation::describe_job_definitions::DescribeJobDefinitionsError> for Error {
     fn from(err: crate::operation::describe_job_definitions::DescribeJobDefinitionsError) -> Self {
         match err {
@@ -702,6 +1018,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_queues")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -727,6 +1044,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_job_queues")]
 impl From<crate::operation::describe_job_queues::DescribeJobQueuesError> for Error {
     fn from(err: crate::operation::describe_job_queues::DescribeJobQueuesError) -> Self {
         match err {
@@ -740,6 +1058,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_jobs")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_jobs::DescribeJobsError, R>>
     for Error
 where
@@ -757,6 +1076,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_jobs")]
 impl From<crate::operation::describe_jobs::DescribeJobsError> for Error {
     fn from(err: crate::operation::describe_jobs::DescribeJobsError) -> Self {
         match err {
@@ -766,6 +1086,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -791,6 +1112,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_quota_share")]
 impl From<crate::operation::describe_quota_share::DescribeQuotaShareError> for Error {
     fn from(err: crate::operation::describe_quota_share::DescribeQuotaShareError) -> Self {
         match err {
@@ -806,6 +1128,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_scheduling_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -831,6 +1154,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_scheduling_policies")]
 impl From<crate::operation::describe_scheduling_policies::DescribeSchedulingPoliciesError> for Error {
     fn from(err: crate::operation::describe_scheduling_policies::DescribeSchedulingPoliciesError) -> Self {
         match err {
@@ -846,6 +1170,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_environments")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -871,6 +1196,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_environments")]
 impl From<crate::operation::describe_service_environments::DescribeServiceEnvironmentsError> for Error {
     fn from(err: crate::operation::describe_service_environments::DescribeServiceEnvironmentsError) -> Self {
         match err {
@@ -886,6 +1212,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -911,6 +1238,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_service_job")]
 impl From<crate::operation::describe_service_job::DescribeServiceJobError> for Error {
     fn from(err: crate::operation::describe_service_job::DescribeServiceJobError) -> Self {
         match err {
@@ -926,6 +1254,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_job_queue_snapshot")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -951,6 +1280,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_job_queue_snapshot")]
 impl From<crate::operation::get_job_queue_snapshot::GetJobQueueSnapshotError> for Error {
     fn from(err: crate::operation::get_job_queue_snapshot::GetJobQueueSnapshotError) -> Self {
         match err {
@@ -966,6 +1296,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_consumable_resources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -991,6 +1322,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_consumable_resources")]
 impl From<crate::operation::list_consumable_resources::ListConsumableResourcesError> for Error {
     fn from(err: crate::operation::list_consumable_resources::ListConsumableResourcesError) -> Self {
         match err {
@@ -1006,6 +1338,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_jobs::ListJobsError, R>>
     for Error
 where
@@ -1023,6 +1356,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs")]
 impl From<crate::operation::list_jobs::ListJobsError> for Error {
     fn from(err: crate::operation::list_jobs::ListJobsError) -> Self {
         match err {
@@ -1032,6 +1366,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1057,6 +1392,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 impl From<crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceError> for Error {
     fn from(err: crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceError) -> Self {
         match err {
@@ -1072,6 +1408,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_quota_shares")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1097,6 +1434,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_quota_shares")]
 impl From<crate::operation::list_quota_shares::ListQuotaSharesError> for Error {
     fn from(err: crate::operation::list_quota_shares::ListQuotaSharesError) -> Self {
         match err {
@@ -1110,6 +1448,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduling_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1135,6 +1474,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduling_policies")]
 impl From<crate::operation::list_scheduling_policies::ListSchedulingPoliciesError> for Error {
     fn from(err: crate::operation::list_scheduling_policies::ListSchedulingPoliciesError) -> Self {
         match err {
@@ -1150,6 +1490,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_service_jobs")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1175,6 +1516,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_service_jobs")]
 impl From<crate::operation::list_service_jobs::ListServiceJobsError> for Error {
     fn from(err: crate::operation::list_service_jobs::ListServiceJobsError) -> Self {
         match err {
@@ -1188,6 +1530,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1213,6 +1556,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -1228,6 +1572,7 @@
         }
     }
 }
+#[cfg(feature = "op_register_job_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1253,6 +1598,7 @@
         }
     }
 }
+#[cfg(feature = "op_register_job_definition")]
 impl From<crate::operation::register_job_definition::RegisterJobDefinitionError> for Error {
     fn from(err: crate::operation::register_job_definition::RegisterJobDefinitionError) -> Self {
         match err {
@@ -1268,6 +1614,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::submit_job::SubmitJobError, R>>
     for Error
 where
@@ -1285,6 +1632,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_job")]
 impl From<crate::operation::submit_job::SubmitJobError> for Error {
     fn from(err: crate::operation::submit_job::SubmitJobError) -> Self {
         match err {
@@ -1294,6 +1642,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1319,6 +1668,7 @@
         }
     }
 }
+#[cfg(feature = "op_submit_service_job")]
 impl From<crate::operation::submit_service_job::SubmitServiceJobError> for Error {
     fn from(err: crate::operation::submit_service_job::SubmitServiceJobError) -> Self {
         match err {
@@ -1332,6 +1682,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -1349,6 +1700,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -1358,6 +1710,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::terminate_job::TerminateJobError, R>>
     for Error
 where
@@ -1375,6 +1728,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_job")]
 impl From<crate::operation::terminate_job::TerminateJobError> for Error {
     fn from(err: crate::operation::terminate_job::TerminateJobError) -> Self {
         match err {
@@ -1384,6 +1738,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1409,6 +1764,7 @@
         }
     }
 }
+#[cfg(feature = "op_terminate_service_job")]
 impl From<crate::operation::terminate_service_job::TerminateServiceJobError> for Error {
     fn from(err: crate::operation::terminate_service_job::TerminateServiceJobError) -> Self {
         match err {
@@ -1424,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -1445,6 +1802,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -1458,6 +1816,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_compute_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1483,6 +1842,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_compute_environment")]
 impl From<crate::operation::update_compute_environment::UpdateComputeEnvironmentError> for Error {
     fn from(err: crate::operation::update_compute_environment::UpdateComputeEnvironmentError) -> Self {
         match err {
@@ -1498,6 +1858,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_consumable_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1523,6 +1884,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_consumable_resource")]
 impl From<crate::operation::update_consumable_resource::UpdateConsumableResourceError> for Error {
     fn from(err: crate::operation::update_consumable_resource::UpdateConsumableResourceError) -> Self {
         match err {
@@ -1538,6 +1900,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_job_queue")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_job_queue::UpdateJobQueueError, R>>
     for Error
@@ -1559,6 +1922,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_job_queue")]
 impl From<crate::operation::update_job_queue::UpdateJobQueueError> for Error {
     fn from(err: crate::operation::update_job_queue::UpdateJobQueueError) -> Self {
         match err {
@@ -1572,6 +1936,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_quota_share")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1597,6 +1962,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_quota_share")]
 impl From<crate::operation::update_quota_share::UpdateQuotaShareError> for Error {
     fn from(err: crate::operation::update_quota_share::UpdateQuotaShareError) -> Self {
         match err {
@@ -1610,6 +1976,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduling_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1635,6 +2002,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduling_policy")]
 impl From<crate::operation::update_scheduling_policy::UpdateSchedulingPolicyError> for Error {
     fn from(err: crate::operation::update_scheduling_policy::UpdateSchedulingPolicyError) -> Self {
         match err {
@@ -1650,6 +2018,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_environment")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1675,6 +2044,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_environment")]
 impl From<crate::operation::update_service_environment::UpdateServiceEnvironmentError> for Error {
     fn from(err: crate::operation::update_service_environment::UpdateServiceEnvironmentError) -> Self {
         match err {
@@ -1690,6 +2060,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1715,6 +2086,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_service_job")]
 impl From<crate::operation::update_service_job::UpdateServiceJobError> for Error {
     fn from(err: crate::operation::update_service_job::UpdateServiceJobError) -> Self {
         match err {
@@ -1731,7 +2103,101 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ClientException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Error::ServerException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -1740,7 +2206,101 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ClientException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_job",
+                feature = "op_create_compute_environment",
+                feature = "op_create_consumable_resource",
+                feature = "op_create_job_queue",
+                feature = "op_create_quota_share",
+                feature = "op_create_scheduling_policy",
+                feature = "op_create_service_environment",
+                feature = "op_delete_compute_environment",
+                feature = "op_delete_consumable_resource",
+                feature = "op_delete_job_queue",
+                feature = "op_delete_quota_share",
+                feature = "op_delete_scheduling_policy",
+                feature = "op_delete_service_environment",
+                feature = "op_deregister_job_definition",
+                feature = "op_describe_compute_environments",
+                feature = "op_describe_consumable_resource",
+                feature = "op_describe_job_definitions",
+                feature = "op_describe_job_queues",
+                feature = "op_describe_jobs",
+                feature = "op_describe_quota_share",
+                feature = "op_describe_scheduling_policies",
+                feature = "op_describe_service_environments",
+                feature = "op_describe_service_job",
+                feature = "op_get_job_queue_snapshot",
+                feature = "op_list_consumable_resources",
+                feature = "op_list_jobs",
+                feature = "op_list_jobs_by_consumable_resource",
+                feature = "op_list_quota_shares",
+                feature = "op_list_scheduling_policies",
+                feature = "op_list_service_jobs",
+                feature = "op_list_tags_for_resource",
+                feature = "op_register_job_definition",
+                feature = "op_submit_job",
+                feature = "op_submit_service_job",
+                feature = "op_tag_resource",
+                feature = "op_terminate_job",
+                feature = "op_terminate_service_job",
+                feature = "op_untag_resource",
+                feature = "op_update_compute_environment",
+                feature = "op_update_consumable_resource",
+                feature = "op_update_job_queue",
+                feature = "op_update_quota_share",
+                feature = "op_update_scheduling_policy",
+                feature = "op_update_service_environment",
+                feature = "op_update_service_job"
+            ))]
             Self::ServerException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn reflens_describe_compute_environments_output_output_next_token(
     input: &crate::operation::describe_compute_environments::DescribeComputeEnvironmentsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn reflens_describe_job_definitions_output_output_next_token(
     input: &crate::operation::describe_job_definitions::DescribeJobDefinitionsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn reflens_describe_job_queues_output_output_next_token(
     input: &crate::operation::describe_job_queues::DescribeJobQueuesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn reflens_describe_service_environments_output_output_next_token(
     input: &crate::operation::describe_service_environments::DescribeServiceEnvironmentsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn reflens_list_consumable_resources_output_output_next_token(
     input: &crate::operation::list_consumable_resources::ListConsumableResourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn reflens_list_jobs_output_output_next_token(
     input: &crate::operation::list_jobs::ListJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn reflens_list_jobs_by_consumable_resource_output_output_next_token(
     input: &crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) fn reflens_list_quota_shares_output_output_next_token(
     input: &crate::operation::list_quota_shares::ListQuotaSharesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn reflens_list_scheduling_policies_output_output_next_token(
     input: &crate::operation::list_scheduling_policies::ListSchedulingPoliciesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn reflens_list_service_jobs_output_output_next_token(
     input: &crate::operation::list_service_jobs::ListServiceJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn lens_describe_compute_environments_output_output_compute_environments(
     input: crate::operation::describe_compute_environments::DescribeComputeEnvironmentsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ComputeEnvironmentDetail>> {
@@ -106,6 +117,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn lens_describe_job_definitions_output_output_job_definitions(
     input: crate::operation::describe_job_definitions::DescribeJobDefinitionsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobDefinition>> {
@@ -113,6 +125,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn lens_describe_job_queues_output_output_job_queues(
     input: crate::operation::describe_job_queues::DescribeJobQueuesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobQueueDetail>> {
@@ -120,6 +133,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn lens_describe_service_environments_output_output_service_environments(
     input: crate::operation::describe_service_environments::DescribeServiceEnvironmentsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ServiceEnvironmentDetail>> {
@@ -127,6 +141,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn lens_list_consumable_resources_output_output_consumable_resources(
     input: crate::operation::list_consumable_resources::ListConsumableResourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ConsumableResourceSummary>> {
@@ -134,6 +149,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn lens_list_jobs_output_output_job_summary_list(
     input: crate::operation::list_jobs::ListJobsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::JobSummary>> {
@@ -141,6 +157,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn lens_list_jobs_by_consumable_resource_output_output_jobs(
     input: crate::operation::list_jobs_by_consumable_resource::ListJobsByConsumableResourceOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ListJobsByConsumableResourceSummary>> {
@@ -148,6 +165,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) fn lens_list_quota_shares_output_output_quota_shares(
     input: crate::operation::list_quota_shares::ListQuotaSharesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::QuotaShareDetail>> {
@@ -155,6 +173,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn lens_list_scheduling_policies_output_output_scheduling_policies(
     input: crate::operation::list_scheduling_policies::ListSchedulingPoliciesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SchedulingPolicyListingDetail>> {
@@ -162,6 +181,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn lens_list_service_jobs_output_output_job_summary_list(
     input: crate::operation::list_service_jobs::ListServiceJobsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ServiceJobSummary>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,137 +1,182 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_cancel_job")]
 /// Types for the `CancelJob` operation.
 pub mod cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 /// Types for the `CreateComputeEnvironment` operation.
 pub mod create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 /// Types for the `CreateConsumableResource` operation.
 pub mod create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 /// Types for the `CreateJobQueue` operation.
 pub mod create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 /// Types for the `CreateQuotaShare` operation.
 pub mod create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 /// Types for the `CreateSchedulingPolicy` operation.
 pub mod create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 /// Types for the `CreateServiceEnvironment` operation.
 pub mod create_service_environment;

+#[cfg(feature = "op_delete_compute_environment")]
 /// Types for the `DeleteComputeEnvironment` operation.
 pub mod delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 /// Types for the `DeleteConsumableResource` operation.
 pub mod delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 /// Types for the `DeleteJobQueue` operation.
 pub mod delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 /// Types for the `DeleteQuotaShare` operation.
 pub mod delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 /// Types for the `DeleteSchedulingPolicy` operation.
 pub mod delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 /// Types for the `DeleteServiceEnvironment` operation.
 pub mod delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 /// Types for the `DeregisterJobDefinition` operation.
 pub mod deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 /// Types for the `DescribeComputeEnvironments` operation.
 pub mod describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 /// Types for the `DescribeConsumableResource` operation.
 pub mod describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 /// Types for the `DescribeJobDefinitions` operation.
 pub mod describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 /// Types for the `DescribeJobQueues` operation.
 pub mod describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 /// Types for the `DescribeJobs` operation.
 pub mod describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 /// Types for the `DescribeQuotaShare` operation.
 pub mod describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 /// Types for the `DescribeSchedulingPolicies` operation.
 pub mod describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 /// Types for the `DescribeServiceEnvironments` operation.
 pub mod describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 /// Types for the `DescribeServiceJob` operation.
 pub mod describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 /// Types for the `GetJobQueueSnapshot` operation.
 pub mod get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 /// Types for the `ListConsumableResources` operation.
 pub mod list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 /// Types for the `ListJobs` operation.
 pub mod list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 /// Types for the `ListJobsByConsumableResource` operation.
 pub mod list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 /// Types for the `ListQuotaShares` operation.
 pub mod list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 /// Types for the `ListSchedulingPolicies` operation.
 pub mod list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 /// Types for the `ListServiceJobs` operation.
 pub mod list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 /// Types for the `RegisterJobDefinition` operation.
 pub mod register_job_definition;

+#[cfg(feature = "op_submit_job")]
 /// Types for the `SubmitJob` operation.
 pub mod submit_job;

+#[cfg(feature = "op_submit_service_job")]
 /// Types for the `SubmitServiceJob` operation.
 pub mod submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_terminate_job")]
 /// Types for the `TerminateJob` operation.
 pub mod terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 /// Types for the `TerminateServiceJob` operation.
 pub mod terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 /// Types for the `UpdateComputeEnvironment` operation.
 pub mod update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 /// Types for the `UpdateConsumableResource` operation.
 pub mod update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 /// Types for the `UpdateJobQueue` operation.
 pub mod update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 /// Types for the `UpdateQuotaShare` operation.
 pub mod update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 /// Types for the `UpdateSchedulingPolicy` operation.
 pub mod update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 /// Types for the `UpdateServiceEnvironment` operation.
 pub mod update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 /// Types for the `UpdateServiceJob` operation.
 pub mod update_service_job;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,51 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +64,53 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,98 +122,191 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_cancel_job")]
 pub(crate) mod shape_cancel_job;

+#[cfg(feature = "op_create_compute_environment")]
 pub(crate) mod shape_create_compute_environment;

+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) mod shape_create_consumable_resource;

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) mod shape_create_job_queue;

+#[cfg(feature = "op_create_quota_share")]
 pub(crate) mod shape_create_quota_share;

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) mod shape_create_scheduling_policy;

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) mod shape_create_service_environment;

+#[cfg(feature = "op_delete_compute_environment")]
 pub(crate) mod shape_delete_compute_environment;

+#[cfg(feature = "op_delete_consumable_resource")]
 pub(crate) mod shape_delete_consumable_resource;

+#[cfg(feature = "op_delete_job_queue")]
 pub(crate) mod shape_delete_job_queue;

+#[cfg(feature = "op_delete_quota_share")]
 pub(crate) mod shape_delete_quota_share;

+#[cfg(feature = "op_delete_scheduling_policy")]
 pub(crate) mod shape_delete_scheduling_policy;

+#[cfg(feature = "op_delete_service_environment")]
 pub(crate) mod shape_delete_service_environment;

+#[cfg(feature = "op_deregister_job_definition")]
 pub(crate) mod shape_deregister_job_definition;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_describe_compute_environments;

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) mod shape_describe_consumable_resource;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_describe_job_definitions;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_describe_job_queues;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_describe_jobs;

+#[cfg(feature = "op_describe_quota_share")]
 pub(crate) mod shape_describe_quota_share;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_describe_scheduling_policies;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_describe_service_environments;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_describe_service_job;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_get_job_queue_snapshot;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_list_consumable_resources;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_list_jobs;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_list_quota_shares;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_list_scheduling_policies;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_list_service_jobs;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) mod shape_register_job_definition;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_submit_job;

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) mod shape_submit_service_job;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_terminate_job")]
 pub(crate) mod shape_terminate_job;

+#[cfg(feature = "op_terminate_service_job")]
 pub(crate) mod shape_terminate_service_job;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_compute_environment;

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) mod shape_update_consumable_resource;

+#[cfg(feature = "op_update_job_queue")]
 pub(crate) mod shape_update_job_queue;

+#[cfg(feature = "op_update_quota_share")]
 pub(crate) mod shape_update_quota_share;

+#[cfg(feature = "op_update_scheduling_policy")]
 pub(crate) mod shape_update_scheduling_policy;

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) mod shape_update_service_environment;

+#[cfg(feature = "op_update_service_job")]
 pub(crate) mod shape_update_service_job;

+#[cfg(feature = "op_cancel_job")]
 pub(crate) mod shape_cancel_job_input;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -128,526 +315,1327 @@
     }
 }

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) mod shape_client_exception;

+#[cfg(feature = "op_create_compute_environment")]
 pub(crate) mod shape_create_compute_environment_input;

+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) mod shape_create_consumable_resource_input;

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) mod shape_create_job_queue_input;

+#[cfg(feature = "op_create_quota_share")]
 pub(crate) mod shape_create_quota_share_input;

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) mod shape_create_scheduling_policy_input;

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) mod shape_create_service_environment_input;

+#[cfg(feature = "op_delete_compute_environment")]
 pub(crate) mod shape_delete_compute_environment_input;

+#[cfg(feature = "op_delete_consumable_resource")]
 pub(crate) mod shape_delete_consumable_resource_input;

+#[cfg(feature = "op_delete_job_queue")]
 pub(crate) mod shape_delete_job_queue_input;

+#[cfg(feature = "op_delete_quota_share")]
 pub(crate) mod shape_delete_quota_share_input;

+#[cfg(feature = "op_delete_scheduling_policy")]
 pub(crate) mod shape_delete_scheduling_policy_input;

+#[cfg(feature = "op_delete_service_environment")]
 pub(crate) mod shape_delete_service_environment_input;

+#[cfg(feature = "op_deregister_job_definition")]
 pub(crate) mod shape_deregister_job_definition_input;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_describe_compute_environments_input;

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) mod shape_describe_consumable_resource_input;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_describe_job_definitions_input;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_describe_job_queues_input;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_describe_jobs_input;

+#[cfg(feature = "op_describe_quota_share")]
 pub(crate) mod shape_describe_quota_share_input;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_describe_scheduling_policies_input;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_describe_service_environments_input;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_describe_service_job_input;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_get_job_queue_snapshot_input;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_list_consumable_resources_input;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_input;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_list_jobs_input;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_list_quota_shares_input;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_list_scheduling_policies_input;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_list_service_jobs_input;

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) mod shape_register_job_definition_input;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub(crate) mod shape_server_exception;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_submit_job_input;

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) mod shape_submit_service_job_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_terminate_job")]
 pub(crate) mod shape_terminate_job_input;

+#[cfg(feature = "op_terminate_service_job")]
 pub(crate) mod shape_terminate_service_job_input;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_compute_environment_input;

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) mod shape_update_consumable_resource_input;

+#[cfg(feature = "op_update_job_queue")]
 pub(crate) mod shape_update_job_queue_input;

+#[cfg(feature = "op_update_quota_share")]
 pub(crate) mod shape_update_quota_share_input;

+#[cfg(feature = "op_update_scheduling_policy")]
 pub(crate) mod shape_update_scheduling_policy_input;

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) mod shape_update_service_environment_input;

+#[cfg(feature = "op_update_service_job")]
 pub(crate) mod shape_update_service_job_input;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_array_properties;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub(crate) mod shape_capacity_limit;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_compute_environment_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_compute_environment_order;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_compute_resource;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_compute_resource_update;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_properties;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_consumable_resource_summary_list;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_container_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ecs_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_ecs_properties_override;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_ecs_settings;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_eks_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_properties_override;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_fairshare_policy;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_shares_detail;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_job_definition_list;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub(crate) mod shape_job_dependency;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_detail_list;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_queue_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_job_state_time_limit_action;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_summary_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_job_timeout;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub(crate) mod shape_key_values_pair;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) mod shape_latest_service_job_attempt;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_summary_list;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_node_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_utilization_detail;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_capacity_limit;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 pub(crate) mod shape_quota_share_capacity_limits;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_quota_share_list;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_quota_share_policy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_preemption_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) mod shape_quota_share_resource_sharing_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_retry_strategy;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_detail_list;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_listing_detail_list;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_service_environment_detail_list;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) mod shape_service_environment_order;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_attempt_details;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_capacity_usage_detail_list;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_preemption_configuration;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_preemption_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_retry_strategy;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_summary_list;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_timeout;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_list_tags_for_resource"
+))]
 pub(crate) mod shape_tagris_tags_map;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_update_policy;

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) mod shape_compute_environment_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_compute_scaling_policy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_requirement;

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) mod shape_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_ec2_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ecs_task_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_pod_properties;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_pod_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ephemeral_storage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_evaluate_on_exit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_fargate_platform_configuration;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_job_summary_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_shares_job_summary_map;

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) mod shape_job_definition;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_detail;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_queue_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_key_value_pair;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_linux_parameters;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) mod shape_list_jobs_by_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_log_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_managed_instances_provider;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_mount_point;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_network_configuration;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_node_property_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_range_property;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_capacity_usage_list;

+#[cfg(feature = "op_list_quota_shares")]
 pub(crate) mod shape_quota_share_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_repository_credentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_resource_requirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_runtime_platform;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_detail;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) mod shape_scheduling_policy_listing_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_secret;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_service_environment_detail;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_attempt_detail;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_capacity_usage_detail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_evaluate_on_exit;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) mod shape_service_job_evaluate_on_exit_list;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_recent_preempted_attempt_list;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) mod shape_service_resource_id;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_share_attributes;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_task_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ulimit;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_update_managed_instances_provider_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_volume;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_array_properties_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_array_properties_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_details;

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) mod shape_capacity_limits;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_compute_environment_orders;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_container_detail;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_container_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_device;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_ecs_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_efs_volume_configuration;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_eks_container_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_metadata;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_volume;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_utilization_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_queue_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_share_job_summary_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_image_pull_secret;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_infrastructure_optimization;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_instance_launch_template;

+#[cfg(feature = "op_update_compute_environment")]
 pub(crate) mod shape_instance_launch_template_update;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_capacity_usage_summary_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_job_dependency_list;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_job_state_time_limit_actions;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification_override;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_node_details;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_node_properties_summary;

+#[cfg(any(feature = "op_describe_job_definitions", feature = "op_describe_jobs"))]
 pub(crate) mod shape_parameters_map;

+#[cfg(any(feature = "op_describe_job_definitions", feature = "op_describe_jobs"))]
 pub(crate) mod shape_platform_capability_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_queue_snapshot_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_utilization_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_s3_files_volume_configuration;

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) mod shape_service_environment_orders;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_capacity_usage_summary_list;

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) mod shape_service_job_preempted_attempt;

+#[cfg(feature = "op_submit_job")]
 pub(crate) mod shape_task_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_tmpfs;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 pub(crate) mod shape_array_job_status_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_capacity_reservation_request;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_consumable_resource_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_ec2_configuration_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_efs_authorization_config;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_container_environment_variable;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_container_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_security_context;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_volume_mount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_empty_dir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_host_path;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_persistent_volume_claim;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_pod_properties_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_environment_variables;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_evaluate_on_exit_list;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_utilization;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_firelens_configuration;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_front_of_quota_share_job_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_instance_requirements_request;

+#[cfg(feature = "op_list_jobs")]
 pub(crate) mod shape_job_capacity_usage_summary;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_list_ecs_task_properties;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_local_storage_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_network_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_managed_instances_storage_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_mount_points;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_network_interface_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_node_range_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_utilization;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_secret_list;

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) mod shape_service_job_capacity_usage_summary;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) mod shape_share_attributes_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_string_list;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) mod shape_tags_map;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_dependency;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_ulimits;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_volumes;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_devices_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_ecs_task_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_containers;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_volumes;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_usage_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_image_pull_secrets;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) mod shape_launch_template_specification_override_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_attempt_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_log_configuration_options_map;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_network_interface;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_usage_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_tmpfs_list;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_annotations_map;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_eks_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_labels_map;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_fairshare_capacity_usage;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_task_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_list_task_container_properties;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub(crate) mod shape_quota_share_capacity_usage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_device_cgroup_permissions;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_environment_variables;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_eks_container_volume_mounts;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_list_attempt_task_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_task_container_details;

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) mod shape_attempt_task_container_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_limits;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) mod shape_eks_requests;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_task_container_dependency_list;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) mod shape_firelens_configuration_options_map;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_consumable_resource")]
 pub(crate) fn create_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::create_consumable_resource::builders::CreateConsumableResourceOutputBuilder,
 ) -> crate::operation::create_consumable_resource::builders::CreateConsumableResourceOutputBuilder {
@@ -11,6 +12,7 @@
     builder
 }

+#[cfg(feature = "op_create_job_queue")]
 pub(crate) fn create_job_queue_output_output_correct_errors(
     mut builder: crate::operation::create_job_queue::builders::CreateJobQueueOutputBuilder,
 ) -> crate::operation::create_job_queue::builders::CreateJobQueueOutputBuilder {
@@ -23,6 +25,7 @@
     builder
 }

+#[cfg(feature = "op_create_scheduling_policy")]
 pub(crate) fn create_scheduling_policy_output_output_correct_errors(
     mut builder: crate::operation::create_scheduling_policy::builders::CreateSchedulingPolicyOutputBuilder,
 ) -> crate::operation::create_scheduling_policy::builders::CreateSchedulingPolicyOutputBuilder {
@@ -35,6 +38,7 @@
     builder
 }

+#[cfg(feature = "op_create_service_environment")]
 pub(crate) fn create_service_environment_output_output_correct_errors(
     mut builder: crate::operation::create_service_environment::builders::CreateServiceEnvironmentOutputBuilder,
 ) -> crate::operation::create_service_environment::builders::CreateServiceEnvironmentOutputBuilder {
@@ -47,6 +51,7 @@
     builder
 }

+#[cfg(feature = "op_describe_consumable_resource")]
 pub(crate) fn describe_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::describe_consumable_resource::builders::DescribeConsumableResourceOutputBuilder,
 ) -> crate::operation::describe_consumable_resource::builders::DescribeConsumableResourceOutputBuilder {
@@ -59,6 +64,7 @@
     builder
 }

+#[cfg(feature = "op_describe_service_job")]
 pub(crate) fn describe_service_job_output_output_correct_errors(
     mut builder: crate::operation::describe_service_job::builders::DescribeServiceJobOutputBuilder,
 ) -> crate::operation::describe_service_job::builders::DescribeServiceJobOutputBuilder {
@@ -83,6 +89,7 @@
     builder
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn list_consumable_resources_output_output_correct_errors(
     mut builder: crate::operation::list_consumable_resources::builders::ListConsumableResourcesOutputBuilder,
 ) -> crate::operation::list_consumable_resources::builders::ListConsumableResourcesOutputBuilder {
@@ -92,6 +99,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn list_jobs_output_output_correct_errors(
     mut builder: crate::operation::list_jobs::builders::ListJobsOutputBuilder,
 ) -> crate::operation::list_jobs::builders::ListJobsOutputBuilder {
@@ -101,6 +109,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn list_jobs_by_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::list_jobs_by_consumable_resource::builders::ListJobsByConsumableResourceOutputBuilder,
 ) -> crate::operation::list_jobs_by_consumable_resource::builders::ListJobsByConsumableResourceOutputBuilder {
@@ -110,6 +119,7 @@
     builder
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn list_service_jobs_output_output_correct_errors(
     mut builder: crate::operation::list_service_jobs::builders::ListServiceJobsOutputBuilder,
 ) -> crate::operation::list_service_jobs::builders::ListServiceJobsOutputBuilder {
@@ -119,6 +129,7 @@
     builder
 }

+#[cfg(feature = "op_register_job_definition")]
 pub(crate) fn register_job_definition_output_output_correct_errors(
     mut builder: crate::operation::register_job_definition::builders::RegisterJobDefinitionOutputBuilder,
 ) -> crate::operation::register_job_definition::builders::RegisterJobDefinitionOutputBuilder {
@@ -134,6 +145,7 @@
     builder
 }

+#[cfg(feature = "op_submit_job")]
 pub(crate) fn submit_job_output_output_correct_errors(
     mut builder: crate::operation::submit_job::builders::SubmitJobOutputBuilder,
 ) -> crate::operation::submit_job::builders::SubmitJobOutputBuilder {
@@ -146,6 +158,7 @@
     builder
 }

+#[cfg(feature = "op_submit_service_job")]
 pub(crate) fn submit_service_job_output_output_correct_errors(
     mut builder: crate::operation::submit_service_job::builders::SubmitServiceJobOutputBuilder,
 ) -> crate::operation::submit_service_job::builders::SubmitServiceJobOutputBuilder {
@@ -158,6 +171,7 @@
     builder
 }

+#[cfg(feature = "op_update_consumable_resource")]
 pub(crate) fn update_consumable_resource_output_output_correct_errors(
     mut builder: crate::operation::update_consumable_resource::builders::UpdateConsumableResourceOutputBuilder,
 ) -> crate::operation::update_consumable_resource::builders::UpdateConsumableResourceOutputBuilder {
@@ -170,6 +184,7 @@
     builder
 }

+#[cfg(feature = "op_update_service_environment")]
 pub(crate) fn update_service_environment_output_output_correct_errors(
     mut builder: crate::operation::update_service_environment::builders::UpdateServiceEnvironmentOutputBuilder,
 ) -> crate::operation::update_service_environment::builders::UpdateServiceEnvironmentOutputBuilder {
@@ -182,6 +197,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_preemption_configuration_correct_errors(
     mut builder: crate::types::builders::QuotaSharePreemptionConfigurationBuilder,
 ) -> crate::types::builders::QuotaSharePreemptionConfigurationBuilder {
@@ -193,6 +214,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_resource_sharing_configuration_correct_errors(
     mut builder: crate::types::builders::QuotaShareResourceSharingConfigurationBuilder,
 ) -> crate::types::builders::QuotaShareResourceSharingConfigurationBuilder {
@@ -204,6 +231,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub(crate) fn service_job_retry_strategy_correct_errors(
     mut builder: crate::types::builders::ServiceJobRetryStrategyBuilder,
 ) -> crate::types::builders::ServiceJobRetryStrategyBuilder {
@@ -213,6 +241,7 @@
     builder
 }

+#[cfg(feature = "op_describe_compute_environments")]
 pub(crate) fn compute_environment_detail_correct_errors(
     mut builder: crate::types::builders::ComputeEnvironmentDetailBuilder,
 ) -> crate::types::builders::ComputeEnvironmentDetailBuilder {
@@ -225,6 +254,7 @@
     builder
 }

+#[cfg(feature = "op_list_consumable_resources")]
 pub(crate) fn consumable_resource_summary_correct_errors(
     mut builder: crate::types::builders::ConsumableResourceSummaryBuilder,
 ) -> crate::types::builders::ConsumableResourceSummaryBuilder {
@@ -237,6 +267,7 @@
     builder
 }

+#[cfg(feature = "op_describe_job_definitions")]
 pub(crate) fn job_definition_correct_errors(
     mut builder: crate::types::builders::JobDefinitionBuilder,
 ) -> crate::types::builders::JobDefinitionBuilder {
@@ -255,6 +286,7 @@
     builder
 }

+#[cfg(feature = "op_describe_jobs")]
 pub(crate) fn job_detail_correct_errors(
     mut builder: crate::types::builders::JobDetailBuilder,
 ) -> crate::types::builders::JobDetailBuilder {
@@ -279,6 +311,7 @@
     builder
 }

+#[cfg(feature = "op_describe_job_queues")]
 pub(crate) fn job_queue_detail_correct_errors(
     mut builder: crate::types::builders::JobQueueDetailBuilder,
 ) -> crate::types::builders::JobQueueDetailBuilder {
@@ -300,6 +333,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs")]
 pub(crate) fn job_summary_correct_errors(
     mut builder: crate::types::builders::JobSummaryBuilder,
 ) -> crate::types::builders::JobSummaryBuilder {
@@ -312,6 +346,7 @@
     builder
 }

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub(crate) fn list_jobs_by_consumable_resource_summary_correct_errors(
     mut builder: crate::types::builders::ListJobsByConsumableResourceSummaryBuilder,
 ) -> crate::types::builders::ListJobsByConsumableResourceSummaryBuilder {
@@ -342,6 +377,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub(crate) fn quota_share_capacity_limit_correct_errors(
     mut builder: crate::types::builders::QuotaShareCapacityLimitBuilder,
 ) -> crate::types::builders::QuotaShareCapacityLimitBuilder {
@@ -354,6 +395,7 @@
     builder
 }

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub(crate) fn scheduling_policy_detail_correct_errors(
     mut builder: crate::types::builders::SchedulingPolicyDetailBuilder,
 ) -> crate::types::builders::SchedulingPolicyDetailBuilder {
@@ -366,6 +408,7 @@
     builder
 }

+#[cfg(feature = "op_list_scheduling_policies")]
 pub(crate) fn scheduling_policy_listing_detail_correct_errors(
     mut builder: crate::types::builders::SchedulingPolicyListingDetailBuilder,
 ) -> crate::types::builders::SchedulingPolicyListingDetailBuilder {
@@ -375,6 +418,7 @@
     builder
 }

+#[cfg(feature = "op_describe_service_environments")]
 pub(crate) fn service_environment_detail_correct_errors(
     mut builder: crate::types::builders::ServiceEnvironmentDetailBuilder,
 ) -> crate::types::builders::ServiceEnvironmentDetailBuilder {
@@ -393,6 +437,7 @@
     builder
 }

+#[cfg(feature = "op_list_service_jobs")]
 pub(crate) fn service_job_summary_correct_errors(
     mut builder: crate::types::builders::ServiceJobSummaryBuilder,
 ) -> crate::types::builders::ServiceJobSummaryBuilder {
@@ -408,6 +453,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub(crate) fn service_resource_id_correct_errors(
     mut builder: crate::types::builders::ServiceResourceIdBuilder,
 ) -> crate::types::builders::ServiceResourceIdBuilder {
@@ -420,6 +466,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn compute_resource_correct_errors(
     mut builder: crate::types::builders::ComputeResourceBuilder,
 ) -> crate::types::builders::ComputeResourceBuilder {
@@ -432,6 +482,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ecs_properties_correct_errors(
     mut builder: crate::types::builders::EcsPropertiesBuilder,
 ) -> crate::types::builders::EcsPropertiesBuilder {
@@ -441,6 +496,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn eks_configuration_correct_errors(
     mut builder: crate::types::builders::EksConfigurationBuilder,
 ) -> crate::types::builders::EksConfigurationBuilder {
@@ -453,6 +512,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn node_properties_correct_errors(
     mut builder: crate::types::builders::NodePropertiesBuilder,
 ) -> crate::types::builders::NodePropertiesBuilder {
@@ -468,6 +532,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) fn quota_share_policy_correct_errors(
     mut builder: crate::types::builders::QuotaSharePolicyBuilder,
 ) -> crate::types::builders::QuotaSharePolicyBuilder {
@@ -479,6 +548,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn compute_environment_order_correct_errors(
     mut builder: crate::types::builders::ComputeEnvironmentOrderBuilder,
 ) -> crate::types::builders::ComputeEnvironmentOrderBuilder {
@@ -491,6 +565,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ephemeral_storage_correct_errors(
     mut builder: crate::types::builders::EphemeralStorageBuilder,
 ) -> crate::types::builders::EphemeralStorageBuilder {
@@ -500,6 +579,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn job_state_time_limit_action_correct_errors(
     mut builder: crate::types::builders::JobStateTimeLimitActionBuilder,
 ) -> crate::types::builders::JobStateTimeLimitActionBuilder {
@@ -522,6 +606,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn log_configuration_correct_errors(
     mut builder: crate::types::builders::LogConfigurationBuilder,
 ) -> crate::types::builders::LogConfigurationBuilder {
@@ -531,6 +620,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn managed_instances_provider_correct_errors(
     mut builder: crate::types::builders::ManagedInstancesProviderBuilder,
 ) -> crate::types::builders::ManagedInstancesProviderBuilder {
@@ -546,6 +639,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn repository_credentials_correct_errors(
     mut builder: crate::types::builders::RepositoryCredentialsBuilder,
 ) -> crate::types::builders::RepositoryCredentialsBuilder {
@@ -555,6 +653,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub(crate) fn service_environment_order_correct_errors(
     mut builder: crate::types::builders::ServiceEnvironmentOrderBuilder,
 ) -> crate::types::builders::ServiceEnvironmentOrderBuilder {
@@ -567,6 +670,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) fn ec2_configuration_correct_errors(
     mut builder: crate::types::builders::Ec2ConfigurationBuilder,
 ) -> crate::types::builders::Ec2ConfigurationBuilder {
@@ -576,6 +684,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ecs_task_properties_correct_errors(
     mut builder: crate::types::builders::EcsTaskPropertiesBuilder,
 ) -> crate::types::builders::EcsTaskPropertiesBuilder {
@@ -585,6 +698,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn evaluate_on_exit_correct_errors(
     mut builder: crate::types::builders::EvaluateOnExitBuilder,
 ) -> crate::types::builders::EvaluateOnExitBuilder {
@@ -594,6 +713,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub(crate) fn instance_launch_template_correct_errors(
     mut builder: crate::types::builders::InstanceLaunchTemplateBuilder,
 ) -> crate::types::builders::InstanceLaunchTemplateBuilder {
@@ -609,6 +732,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn node_range_property_correct_errors(
     mut builder: crate::types::builders::NodeRangePropertyBuilder,
 ) -> crate::types::builders::NodeRangePropertyBuilder {
@@ -618,6 +746,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn resource_requirement_correct_errors(
     mut builder: crate::types::builders::ResourceRequirementBuilder,
 ) -> crate::types::builders::ResourceRequirementBuilder {
@@ -630,6 +764,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn secret_correct_errors(
     mut builder: crate::types::builders::SecretBuilder,
 ) -> crate::types::builders::SecretBuilder {
@@ -642,6 +781,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub(crate) fn share_attributes_correct_errors(
     mut builder: crate::types::builders::ShareAttributesBuilder,
 ) -> crate::types::builders::ShareAttributesBuilder {
@@ -651,6 +795,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn ulimit_correct_errors(
     mut builder: crate::types::builders::UlimitBuilder,
 ) -> crate::types::builders::UlimitBuilder {
@@ -666,6 +815,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn device_correct_errors(
     mut builder: crate::types::builders::DeviceBuilder,
 ) -> crate::types::builders::DeviceBuilder {
@@ -675,6 +829,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn efs_volume_configuration_correct_errors(
     mut builder: crate::types::builders::EfsVolumeConfigurationBuilder,
 ) -> crate::types::builders::EfsVolumeConfigurationBuilder {
@@ -684,6 +843,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_container_correct_errors(
     mut builder: crate::types::builders::EksContainerBuilder,
 ) -> crate::types::builders::EksContainerBuilder {
@@ -693,6 +857,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_volume_correct_errors(
     mut builder: crate::types::builders::EksVolumeBuilder,
 ) -> crate::types::builders::EksVolumeBuilder {
@@ -702,6 +871,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn image_pull_secret_correct_errors(
     mut builder: crate::types::builders::ImagePullSecretBuilder,
 ) -> crate::types::builders::ImagePullSecretBuilder {
@@ -711,6 +885,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub(crate) fn managed_instances_network_configuration_correct_errors(
     mut builder: crate::types::builders::ManagedInstancesNetworkConfigurationBuilder,
 ) -> crate::types::builders::ManagedInstancesNetworkConfigurationBuilder {
@@ -723,6 +902,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn s3_files_volume_configuration_correct_errors(
     mut builder: crate::types::builders::S3FilesVolumeConfigurationBuilder,
 ) -> crate::types::builders::S3FilesVolumeConfigurationBuilder {
@@ -732,6 +916,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn tmpfs_correct_errors(
     mut builder: crate::types::builders::TmpfsBuilder,
 ) -> crate::types::builders::TmpfsBuilder {
@@ -744,6 +933,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_persistent_volume_claim_correct_errors(
     mut builder: crate::types::builders::EksPersistentVolumeClaimBuilder,
 ) -> crate::types::builders::EksPersistentVolumeClaimBuilder {
@@ -753,6 +947,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn eks_secret_correct_errors(
     mut builder: crate::types::builders::EksSecretBuilder,
 ) -> crate::types::builders::EksSecretBuilder {
@@ -762,6 +961,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn task_container_properties_correct_errors(
     mut builder: crate::types::builders::TaskContainerPropertiesBuilder,
 ) -> crate::types::builders::TaskContainerPropertiesBuilder {
@@ -771,6 +975,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub(crate) fn eks_container_environment_variable_correct_errors(
     mut builder: crate::types::builders::EksContainerEnvironmentVariableBuilder,
 ) -> crate::types::builders::EksContainerEnvironmentVariableBuilder {
@@ -780,6 +990,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub(crate) fn firelens_configuration_correct_errors(
     mut builder: crate::types::builders::FirelensConfigurationBuilder,
 ) -> crate::types::builders::FirelensConfigurationBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,722 +1,1898 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_ce_type::CeType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ce_state::CeState;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_compute_resource::ComputeResource;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_eks_configuration::EksConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ecs_settings::EcsSettings;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_jq_state::JqState;

+#[cfg(any(feature = "op_create_job_queue", feature = "op_describe_job_queues"))]
 pub use crate::types::_job_queue_type::JobQueueType;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_configuration::QuotaShareResourceSharingConfiguration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_preemption_configuration::QuotaSharePreemptionConfiguration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_state::QuotaShareState;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_policy::QuotaSharePolicy;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_fairshare_policy::FairsharePolicy;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments"
+))]
 pub use crate::types::_service_environment_type::ServiceEnvironmentType;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_service_environment_state::ServiceEnvironmentState;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 pub use crate::types::_quota_share_status::QuotaShareStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_latest_service_job_attempt::LatestServiceJobAttempt;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_strategy::ServiceJobRetryStrategy;

+#[cfg(any(
+    feature = "op_describe_service_job",
+    feature = "op_list_service_jobs",
+    feature = "op_submit_service_job"
+))]
 pub use crate::types::_service_job_type::ServiceJobType;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_preemption_configuration::ServiceJobPreemptionConfiguration;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preemption_summary::ServiceJobPreemptionSummary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_job_status::ServiceJobStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_timeout::ServiceJobTimeout;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_detail::FrontOfQueueDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_shares_detail::FrontOfQuotaSharesDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_utilization_detail::QueueSnapshotUtilizationDetail;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 pub use crate::types::_job_status::JobStatus;

+#[cfg(feature = "op_register_job_definition")]
 pub use crate::types::_job_definition_type::JobDefinitionType;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_container_properties::ContainerProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_properties::NodeProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_strategy::RetryStrategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_job_timeout::JobTimeout;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_properties::EksProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_properties::EcsProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_properties::ConsumableResourceProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_array_properties::ArrayProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_container_overrides::ContainerOverrides;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_overrides::NodeOverrides;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_properties_override::EksPropertiesOverride;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_ecs_properties_override::EcsPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_compute_resource_update::ComputeResourceUpdate;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_update_policy::UpdatePolicy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_cr_type::CrType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_cr_allocation_strategy::CrAllocationStrategy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification::LaunchTemplateSpecification;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_compute_scaling_policy::ComputeScalingPolicy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_managed_instances_provider::ManagedInstancesProvider;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_container_insights::ContainerInsights;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_compute_environment_order::ComputeEnvironmentOrder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_service_environment_order::ServiceEnvironmentOrder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_action::JobStateTimeLimitAction;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_capacity_limit::QuotaShareCapacityLimit;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_strategy::QuotaShareResourceSharingStrategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_in_share_preemption_state::QuotaShareInSharePreemptionState;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_idle_resource_assignment_strategy::QuotaShareIdleResourceAssignmentStrategy;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_capacity_limit::CapacityLimit;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_compute_environment_detail::ComputeEnvironmentDetail;

+#[cfg(feature = "op_describe_job_definitions")]
 pub use crate::types::_job_definition::JobDefinition;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_job_queue_detail::JobQueueDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_job_detail::JobDetail;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub use crate::types::_scheduling_policy_detail::SchedulingPolicyDetail;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_detail::ServiceEnvironmentDetail;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_attempt_detail::ServiceJobAttemptDetail;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_capacity_usage_detail::ServiceJobCapacityUsageDetail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id::ServiceResourceId;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_utilization_detail::FairshareUtilizationDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_utilization_detail::QuotaShareUtilizationDetail;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub use crate::types::_key_values_pair::KeyValuesPair;

+#[cfg(feature = "op_list_consumable_resources")]
 pub use crate::types::_consumable_resource_summary::ConsumableResourceSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_summary::JobSummary;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub use crate::types::_list_jobs_by_consumable_resource_summary::ListJobsByConsumableResourceSummary;

+#[cfg(feature = "op_list_quota_shares")]
 pub use crate::types::_quota_share_detail::QuotaShareDetail;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub use crate::types::_scheduling_policy_listing_detail::SchedulingPolicyListingDetail;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_summary::ServiceJobSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_linux_parameters::LinuxParameters;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_configuration::LogConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_network_configuration::NetworkConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_fargate_platform_configuration::FargatePlatformConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ephemeral_storage::EphemeralStorage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_runtime_platform::RuntimePlatform;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_repository_credentials::RepositoryCredentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_platform_capability::PlatformCapability;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_pod_properties::EksPodProperties;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_job_dependency::JobDependency;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_pod_properties_override::EksPodPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_cr_update_allocation_strategy::CrUpdateAllocationStrategy;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_update_managed_instances_provider_configuration::UpdateManagedInstancesProviderConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_userdata_type::UserdataType;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ec2_configuration::Ec2Configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_instance_launch_template::InstanceLaunchTemplate;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_infrastructure_optimization::InfrastructureOptimization;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_actions_state::JobStateTimeLimitActionsState;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_actions_action::JobStateTimeLimitActionsAction;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_share_attributes::ShareAttributes;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_ce_status::CeStatus;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions"
+))]
 pub use crate::types::_orchestration_type::OrchestrationType;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_jq_status::JqStatus;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_container_detail::ContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_node_details::NodeDetails;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_array_properties_detail::ArrayPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_properties_detail::EksPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_properties_detail::EcsPropertiesDetail;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_status::ServiceEnvironmentStatus;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id_name::ServiceResourceIdName;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_evaluate_on_exit::ServiceJobEvaluateOnExit;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preempted_attempt::ServiceJobPreemptedAttempt;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_job_summary::FrontOfQueueJobSummary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_capacity_usage::QueueSnapshotCapacityUsage;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_container_summary::ContainerSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_array_properties_summary::ArrayPropertiesSummary;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_node_properties_summary::NodePropertiesSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_volume::Volume;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_key_value_pair::KeyValuePair;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_mount_point::MountPoint;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ulimit::Ulimit;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_requirement::ResourceRequirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_driver::LogDriver;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_secret::Secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_assign_public_ip::AssignPublicIp;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_range_property::NodeRangeProperty;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_evaluate_on_exit::EvaluateOnExit;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_metadata::EksMetadata;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_task_properties::EcsTaskProperties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_requirement::ConsumableResourceRequirement;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_array_job_dependency::ArrayJobDependency;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_property_override::NodePropertyOverride;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_properties_override::TaskPropertiesOverride;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_instance_launch_template_update::InstanceLaunchTemplateUpdate;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification_override::LaunchTemplateSpecificationOverride;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_network_configuration::ManagedInstancesNetworkConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_instance_requirements_request::InstanceRequirementsRequest;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_storage_configuration::ManagedInstancesStorageConfiguration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_capacity_reservation_request::CapacityReservationRequest;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_local_storage_configuration::ManagedInstancesLocalStorageConfiguration;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_detail::AttemptDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_pod_properties_detail::EksPodPropertiesDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_detail::EksAttemptDetail;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_action::ServiceJobRetryAction;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_share_job_summary::FrontOfQuotaShareJobSummary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_utilization::FairshareCapacityUtilization;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_utilization::QuotaShareCapacityUtilization;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_capacity_usage_summary::JobCapacityUsageSummary;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_capacity_usage_summary::ServiceJobCapacityUsageSummary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_host::Host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_volume_configuration::EfsVolumeConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_s3_files_volume_configuration::S3FilesVolumeConfiguration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_type::ResourceType;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device::Device;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_tmpfs::Tmpfs;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_action::RetryAction;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_image_pull_secret::ImagePullSecret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container::EksContainer;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_volume::EksVolume;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_container_override::EksContainerOverride;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_container_detail::AttemptContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_network_interface::NetworkInterface;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_task_details::EcsTaskDetails;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_transit_encryption::EfsTransitEncryption;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config::EfsAuthorizationConfig;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_resource_requirements::EksContainerResourceRequirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_security_context::EksContainerSecurityContext;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_host_path::EksHostPath;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_empty_dir::EksEmptyDir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_secret::EksSecret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_persistent_volume_claim::EksPersistentVolumeClaim;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_properties::TaskContainerProperties;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_container_overrides::TaskContainerOverrides;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_ecs_task_details::AttemptEcsTaskDetails;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_container_detail::EksContainerDetail;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_container_detail::EksAttemptContainerDetail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_usage::FairshareCapacityUsage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_usage::QuotaShareCapacityUsage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config_iam::EfsAuthorizationConfigIam;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device_cgroup_permission::DeviceCgroupPermission;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_environment_variable::EksContainerEnvironmentVariable;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_volume_mount::EksContainerVolumeMount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration::FirelensConfiguration;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_task_container_details::TaskContainerDetails;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_dependency::TaskContainerDependency;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration_type::FirelensConfigurationType;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_task_container_details::AttemptTaskContainerDetails;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 mod _array_job_dependency;

+#[cfg(feature = "op_submit_job")]
 mod _array_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _array_properties_detail;

+#[cfg(feature = "op_list_jobs")]
 mod _array_properties_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _assign_public_ip;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_ecs_task_details;

+#[cfg(feature = "op_describe_jobs")]
 mod _attempt_task_container_details;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 mod _capacity_limit;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _capacity_reservation_request;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ce_state;

+#[cfg(feature = "op_describe_compute_environments")]
 mod _ce_status;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _ce_type;

+#[cfg(feature = "op_describe_compute_environments")]
 mod _compute_environment_detail;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _compute_environment_order;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _compute_resource;

+#[cfg(feature = "op_update_compute_environment")]
 mod _compute_resource_update;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _compute_scaling_policy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _consumable_resource_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _consumable_resource_requirement;

+#[cfg(feature = "op_list_consumable_resources")]
 mod _consumable_resource_summary;

+#[cfg(feature = "op_describe_jobs")]
 mod _container_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _container_insights;

+#[cfg(feature = "op_submit_job")]
 mod _container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _container_properties;

+#[cfg(feature = "op_list_jobs")]
 mod _container_summary;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _cr_allocation_strategy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _cr_type;

+#[cfg(feature = "op_update_compute_environment")]
 mod _cr_update_allocation_strategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _device;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _device_cgroup_permission;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ec2_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ecs_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _ecs_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _ecs_properties_override;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _ecs_settings;

+#[cfg(feature = "op_describe_jobs")]
 mod _ecs_task_details;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ecs_task_properties;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_authorization_config;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_authorization_config_iam;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_transit_encryption;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _efs_volume_configuration;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_attempt_container_detail;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_attempt_detail;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _eks_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_container_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_container_environment_variable;

+#[cfg(feature = "op_submit_job")]
 mod _eks_container_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_container_resource_requirements;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container_security_context;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_container_volume_mount;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_empty_dir;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_host_path;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _eks_metadata;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_persistent_volume_claim;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_pod_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_pod_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _eks_pod_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_properties;

+#[cfg(feature = "op_describe_jobs")]
 mod _eks_properties_detail;

+#[cfg(feature = "op_submit_job")]
 mod _eks_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_secret;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _eks_volume;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ephemeral_storage;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _evaluate_on_exit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_capacity_utilization;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _fairshare_policy;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _fairshare_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _fargate_platform_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _firelens_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _firelens_configuration_type;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_queue_detail;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_queue_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_quota_share_job_summary;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _front_of_quota_shares_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _host;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _image_pull_secret;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _infrastructure_optimization;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _instance_launch_template;

+#[cfg(feature = "op_update_compute_environment")]
 mod _instance_launch_template_update;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _instance_requirements_request;

+#[cfg(feature = "op_list_jobs")]
 mod _job_capacity_usage_summary;

+#[cfg(feature = "op_describe_job_definitions")]
 mod _job_definition;

+#[cfg(feature = "op_register_job_definition")]
 mod _job_definition_type;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 mod _job_dependency;

+#[cfg(feature = "op_describe_jobs")]
 mod _job_detail;

+#[cfg(feature = "op_describe_job_queues")]
 mod _job_queue_detail;

+#[cfg(any(feature = "op_create_job_queue", feature = "op_describe_job_queues"))]
 mod _job_queue_type;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_action;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_actions_action;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _job_state_time_limit_actions_state;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_list_jobs"))]
 mod _job_status;

+#[cfg(feature = "op_list_jobs")]
 mod _job_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _job_timeout;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _jq_state;

+#[cfg(feature = "op_describe_job_queues")]
 mod _jq_status;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _key_value_pair;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 mod _key_values_pair;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _latest_service_job_attempt;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _launch_template_specification;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _launch_template_specification_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _linux_parameters;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 mod _list_jobs_by_consumable_resource_summary;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _log_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _log_driver;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_local_storage_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_network_configuration;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 mod _managed_instances_provider;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _managed_instances_storage_configuration;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _mount_point;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _network_configuration;

+#[cfg(feature = "op_describe_jobs")]
 mod _network_interface;

+#[cfg(feature = "op_describe_jobs")]
 mod _node_details;

+#[cfg(feature = "op_submit_job")]
 mod _node_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _node_properties;

+#[cfg(feature = "op_list_jobs")]
 mod _node_properties_summary;

+#[cfg(feature = "op_submit_job")]
 mod _node_property_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _node_range_property;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_job_definitions"
+))]
 mod _orchestration_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _platform_capability;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _queue_snapshot_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _queue_snapshot_utilization_detail;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_capacity_limit;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_capacity_usage;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_capacity_utilization;

+#[cfg(feature = "op_list_quota_shares")]
 mod _quota_share_detail;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _quota_share_idle_resource_assignment_strategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_in_share_preemption_state;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _quota_share_policy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_preemption_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_resource_sharing_configuration;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_resource_sharing_strategy;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 mod _quota_share_state;

+#[cfg(any(feature = "op_describe_quota_share", feature = "op_list_quota_shares"))]
 mod _quota_share_status;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 mod _quota_share_utilization_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _repository_credentials;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _resource_requirement;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _resource_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _retry_action;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 mod _retry_strategy;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _runtime_platform;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _s3_files_volume_configuration;

+#[cfg(feature = "op_describe_scheduling_policies")]
 mod _scheduling_policy_detail;

+#[cfg(feature = "op_list_scheduling_policies")]
 mod _scheduling_policy_listing_detail;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _secret;

+#[cfg(feature = "op_describe_service_environments")]
 mod _service_environment_detail;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 mod _service_environment_order;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 mod _service_environment_state;

+#[cfg(feature = "op_describe_service_environments")]
 mod _service_environment_status;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments"
+))]
 mod _service_environment_type;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_attempt_detail;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_capacity_usage_detail;

+#[cfg(feature = "op_list_service_jobs")]
 mod _service_job_capacity_usage_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_evaluate_on_exit;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_preempted_attempt;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_preemption_configuration;

+#[cfg(feature = "op_describe_service_job")]
 mod _service_job_preemption_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_retry_action;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_retry_strategy;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_job_status;

+#[cfg(feature = "op_list_service_jobs")]
 mod _service_job_summary;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 mod _service_job_timeout;

+#[cfg(any(
+    feature = "op_describe_service_job",
+    feature = "op_list_service_jobs",
+    feature = "op_submit_service_job"
+))]
 mod _service_job_type;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_resource_id;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 mod _service_resource_id_name;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 mod _share_attributes;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _task_container_dependency;

+#[cfg(feature = "op_describe_jobs")]
 mod _task_container_details;

+#[cfg(feature = "op_submit_job")]
 mod _task_container_overrides;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _task_container_properties;

+#[cfg(feature = "op_submit_job")]
 mod _task_properties_override;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _tmpfs;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _ulimit;

+#[cfg(feature = "op_update_compute_environment")]
 mod _update_managed_instances_provider_configuration;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _update_policy;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 mod _userdata_type;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 mod _volume;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,284 +1,729 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_compute_resource::ComputeResourceBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_eks_configuration::EksConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ecs_settings::EcsSettingsBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_resource_sharing_configuration::QuotaShareResourceSharingConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_preemption_configuration::QuotaSharePreemptionConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_quota_share_policy::QuotaSharePolicyBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_fairshare_policy::FairsharePolicyBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_latest_service_job_attempt::LatestServiceJobAttemptBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_retry_strategy::ServiceJobRetryStrategyBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_preemption_configuration::ServiceJobPreemptionConfigurationBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preemption_summary::ServiceJobPreemptionSummaryBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_timeout::ServiceJobTimeoutBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_detail::FrontOfQueueDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_shares_detail::FrontOfQuotaSharesDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_utilization_detail::QueueSnapshotUtilizationDetailBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_container_properties::ContainerPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_properties::NodePropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_retry_strategy::RetryStrategyBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_job_timeout::JobTimeoutBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_properties::EksPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_properties::EcsPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_properties::ConsumableResourcePropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_array_properties::ArrayPropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_container_overrides::ContainerOverridesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_overrides::NodeOverridesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_properties_override::EksPropertiesOverrideBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_ecs_properties_override::EcsPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_compute_resource_update::ComputeResourceUpdateBuilder;

+#[cfg(any(
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_update_policy::UpdatePolicyBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification::LaunchTemplateSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_compute_scaling_policy::ComputeScalingPolicyBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_managed_instances_provider::ManagedInstancesProviderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_compute_environment_order::ComputeEnvironmentOrderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_service_environment_order::ServiceEnvironmentOrderBuilder;

+#[cfg(any(
+    feature = "op_create_job_queue",
+    feature = "op_describe_job_queues",
+    feature = "op_update_job_queue"
+))]
 pub use crate::types::_job_state_time_limit_action::JobStateTimeLimitActionBuilder;

+#[cfg(any(
+    feature = "op_create_quota_share",
+    feature = "op_describe_quota_share",
+    feature = "op_list_quota_shares",
+    feature = "op_update_quota_share"
+))]
 pub use crate::types::_quota_share_capacity_limit::QuotaShareCapacityLimitBuilder;

+#[cfg(any(
+    feature = "op_create_service_environment",
+    feature = "op_describe_service_environments",
+    feature = "op_update_service_environment"
+))]
 pub use crate::types::_capacity_limit::CapacityLimitBuilder;

+#[cfg(feature = "op_describe_compute_environments")]
 pub use crate::types::_compute_environment_detail::ComputeEnvironmentDetailBuilder;

+#[cfg(feature = "op_describe_job_definitions")]
 pub use crate::types::_job_definition::JobDefinitionBuilder;

+#[cfg(feature = "op_describe_job_queues")]
 pub use crate::types::_job_queue_detail::JobQueueDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_job_detail::JobDetailBuilder;

+#[cfg(feature = "op_describe_scheduling_policies")]
 pub use crate::types::_scheduling_policy_detail::SchedulingPolicyDetailBuilder;

+#[cfg(feature = "op_describe_service_environments")]
 pub use crate::types::_service_environment_detail::ServiceEnvironmentDetailBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_attempt_detail::ServiceJobAttemptDetailBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_capacity_usage_detail::ServiceJobCapacityUsageDetailBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_list_service_jobs"))]
 pub use crate::types::_service_resource_id::ServiceResourceIdBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_utilization_detail::FairshareUtilizationDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_utilization_detail::QuotaShareUtilizationDetailBuilder;

+#[cfg(any(
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_service_jobs"
+))]
 pub use crate::types::_key_values_pair::KeyValuesPairBuilder;

+#[cfg(feature = "op_list_consumable_resources")]
 pub use crate::types::_consumable_resource_summary::ConsumableResourceSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_summary::JobSummaryBuilder;

+#[cfg(feature = "op_list_jobs_by_consumable_resource")]
 pub use crate::types::_list_jobs_by_consumable_resource_summary::ListJobsByConsumableResourceSummaryBuilder;

+#[cfg(feature = "op_list_quota_shares")]
 pub use crate::types::_quota_share_detail::QuotaShareDetailBuilder;

+#[cfg(feature = "op_list_scheduling_policies")]
 pub use crate::types::_scheduling_policy_listing_detail::SchedulingPolicyListingDetailBuilder;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_summary::ServiceJobSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_linux_parameters::LinuxParametersBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_log_configuration::LogConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_network_configuration::NetworkConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_fargate_platform_configuration::FargatePlatformConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ephemeral_storage::EphemeralStorageBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_runtime_platform::RuntimePlatformBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_repository_credentials::RepositoryCredentialsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_pod_properties::EksPodPropertiesBuilder;

+#[cfg(any(feature = "op_describe_jobs", feature = "op_submit_job"))]
 pub use crate::types::_job_dependency::JobDependencyBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_pod_properties_override::EksPodPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_update_managed_instances_provider_configuration::UpdateManagedInstancesProviderConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_ec2_configuration::Ec2ConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments"
+))]
 pub use crate::types::_instance_launch_template::InstanceLaunchTemplateBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_infrastructure_optimization::InfrastructureOptimizationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduling_policy",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_update_scheduling_policy"
+))]
 pub use crate::types::_share_attributes::ShareAttributesBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_container_detail::ContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_node_details::NodeDetailsBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_array_properties_detail::ArrayPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_properties_detail::EksPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_properties_detail::EcsPropertiesDetailBuilder;

+#[cfg(any(feature = "op_describe_service_job", feature = "op_submit_service_job"))]
 pub use crate::types::_service_job_evaluate_on_exit::ServiceJobEvaluateOnExitBuilder;

+#[cfg(feature = "op_describe_service_job")]
 pub use crate::types::_service_job_preempted_attempt::ServiceJobPreemptedAttemptBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_queue_job_summary::FrontOfQueueJobSummaryBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_queue_snapshot_capacity_usage::QueueSnapshotCapacityUsageBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_container_summary::ContainerSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_array_properties_summary::ArrayPropertiesSummaryBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_node_properties_summary::NodePropertiesSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_volume::VolumeBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_key_value_pair::KeyValuePairBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_mount_point::MountPointBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ulimit::UlimitBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_resource_requirement::ResourceRequirementBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_secret::SecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_node_range_property::NodeRangePropertyBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_evaluate_on_exit::EvaluateOnExitBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_metadata::EksMetadataBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_ecs_task_properties::EcsTaskPropertiesBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_consumable_resource_requirement::ConsumableResourceRequirementBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_node_property_override::NodePropertyOverrideBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_properties_override::TaskPropertiesOverrideBuilder;

+#[cfg(feature = "op_update_compute_environment")]
 pub use crate::types::_instance_launch_template_update::InstanceLaunchTemplateUpdateBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_launch_template_specification_override::LaunchTemplateSpecificationOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_network_configuration::ManagedInstancesNetworkConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_instance_requirements_request::InstanceRequirementsRequestBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_storage_configuration::ManagedInstancesStorageConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_capacity_reservation_request::CapacityReservationRequestBuilder;

+#[cfg(any(
+    feature = "op_create_compute_environment",
+    feature = "op_describe_compute_environments",
+    feature = "op_update_compute_environment"
+))]
 pub use crate::types::_managed_instances_local_storage_configuration::ManagedInstancesLocalStorageConfigurationBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_detail::AttemptDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_pod_properties_detail::EksPodPropertiesDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_detail::EksAttemptDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_front_of_quota_share_job_summary::FrontOfQuotaShareJobSummaryBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_utilization::FairshareCapacityUtilizationBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_utilization::QuotaShareCapacityUtilizationBuilder;

+#[cfg(feature = "op_list_jobs")]
 pub use crate::types::_job_capacity_usage_summary::JobCapacityUsageSummaryBuilder;

+#[cfg(feature = "op_list_service_jobs")]
 pub use crate::types::_service_job_capacity_usage_summary::ServiceJobCapacityUsageSummaryBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_host::HostBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_volume_configuration::EfsVolumeConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_s3_files_volume_configuration::S3FilesVolumeConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_device::DeviceBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_tmpfs::TmpfsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_image_pull_secret::ImagePullSecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container::EksContainerBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_volume::EksVolumeBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_eks_container_override::EksContainerOverrideBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_container_detail::AttemptContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_network_interface::NetworkInterfaceBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_ecs_task_details::EcsTaskDetailsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_efs_authorization_config::EfsAuthorizationConfigBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_resource_requirements::EksContainerResourceRequirementsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_security_context::EksContainerSecurityContextBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_host_path::EksHostPathBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_empty_dir::EksEmptyDirBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_secret::EksSecretBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_persistent_volume_claim::EksPersistentVolumeClaimBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_properties::TaskContainerPropertiesBuilder;

+#[cfg(feature = "op_submit_job")]
 pub use crate::types::_task_container_overrides::TaskContainerOverridesBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_ecs_task_details::AttemptEcsTaskDetailsBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_container_detail::EksContainerDetailBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_eks_attempt_container_detail::EksAttemptContainerDetailBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_fairshare_capacity_usage::FairshareCapacityUsageBuilder;

+#[cfg(feature = "op_get_job_queue_snapshot")]
 pub use crate::types::_quota_share_capacity_usage::QuotaShareCapacityUsageBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job"
+))]
 pub use crate::types::_eks_container_environment_variable::EksContainerEnvironmentVariableBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_eks_container_volume_mount::EksContainerVolumeMountBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_firelens_configuration::FirelensConfigurationBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_task_container_details::TaskContainerDetailsBuilder;

+#[cfg(any(
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_jobs",
+    feature = "op_register_job_definition"
+))]
 pub use crate::types::_task_container_dependency::TaskContainerDependencyBuilder;

+#[cfg(feature = "op_describe_jobs")]
 pub use crate::types::_attempt_task_container_details::AttemptTaskContainerDetailsBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,10 +1,198 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_client_exception::ClientException;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_server_exception::ServerException;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 mod _client_exception;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 mod _server_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,4 +1,98 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_client_exception::ClientExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_job",
+    feature = "op_create_compute_environment",
+    feature = "op_create_consumable_resource",
+    feature = "op_create_job_queue",
+    feature = "op_create_quota_share",
+    feature = "op_create_scheduling_policy",
+    feature = "op_create_service_environment",
+    feature = "op_delete_compute_environment",
+    feature = "op_delete_consumable_resource",
+    feature = "op_delete_job_queue",
+    feature = "op_delete_quota_share",
+    feature = "op_delete_scheduling_policy",
+    feature = "op_delete_service_environment",
+    feature = "op_deregister_job_definition",
+    feature = "op_describe_compute_environments",
+    feature = "op_describe_consumable_resource",
+    feature = "op_describe_job_definitions",
+    feature = "op_describe_job_queues",
+    feature = "op_describe_jobs",
+    feature = "op_describe_quota_share",
+    feature = "op_describe_scheduling_policies",
+    feature = "op_describe_service_environments",
+    feature = "op_describe_service_job",
+    feature = "op_get_job_queue_snapshot",
+    feature = "op_list_consumable_resources",
+    feature = "op_list_jobs",
+    feature = "op_list_jobs_by_consumable_resource",
+    feature = "op_list_quota_shares",
+    feature = "op_list_scheduling_policies",
+    feature = "op_list_service_jobs",
+    feature = "op_list_tags_for_resource",
+    feature = "op_register_job_definition",
+    feature = "op_submit_job",
+    feature = "op_submit_service_job",
+    feature = "op_tag_resource",
+    feature = "op_terminate_job",
+    feature = "op_terminate_service_job",
+    feature = "op_untag_resource",
+    feature = "op_update_compute_environment",
+    feature = "op_update_consumable_resource",
+    feature = "op_update_job_queue",
+    feature = "op_update_quota_share",
+    feature = "op_update_scheduling_policy",
+    feature = "op_update_service_environment",
+    feature = "op_update_service_job"
+))]
 pub use crate::types::error::_server_exception::ServerExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
