# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/dynamodb`
- model: `aws-models/dynamodb.json`
- package: `aws-sdk-dynamodb`
- library: `aws_sdk_dynamodb`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_batch_execute_statement`: `BatchExecuteStatement`
- `op_batch_get_item`: `BatchGetItem`
- `op_batch_write_item`: `BatchWriteItem`
- `op_create_backup`: `CreateBackup`
- `op_create_global_table`: `CreateGlobalTable`
- `op_create_table`: `CreateTable`
- `op_delete_backup`: `DeleteBackup`
- `op_delete_item`: `DeleteItem`
- `op_delete_resource_policy`: `DeleteResourcePolicy`
- `op_delete_table`: `DeleteTable`
- `op_describe_backup`: `DescribeBackup`
- `op_describe_continuous_backups`: `DescribeContinuousBackups`
- `op_describe_contributor_insights`: `DescribeContributorInsights`
- `op_describe_endpoints`: `DescribeEndpoints`
- `op_describe_export`: `DescribeExport`
- `op_describe_global_table`: `DescribeGlobalTable`
- `op_describe_global_table_settings`: `DescribeGlobalTableSettings`
- `op_describe_import`: `DescribeImport`
- `op_describe_kinesis_streaming_destination`: `DescribeKinesisStreamingDestination`
- `op_describe_limits`: `DescribeLimits`
- `op_describe_table`: `DescribeTable`
- `op_describe_table_replica_auto_scaling`: `DescribeTableReplicaAutoScaling`
- `op_describe_time_to_live`: `DescribeTimeToLive`
- `op_disable_kinesis_streaming_destination`: `DisableKinesisStreamingDestination`
- `op_enable_kinesis_streaming_destination`: `EnableKinesisStreamingDestination`
- `op_execute_statement`: `ExecuteStatement`
- `op_execute_transaction`: `ExecuteTransaction`
- `op_export_table_to_point_in_time`: `ExportTableToPointInTime`
- `op_get_item`: `GetItem`
- `op_get_resource_policy`: `GetResourcePolicy`
- `op_import_table`: `ImportTable`
- `op_list_backups`: `ListBackups`
- `op_list_contributor_insights`: `ListContributorInsights`
- `op_list_exports`: `ListExports`
- `op_list_global_tables`: `ListGlobalTables`
- `op_list_imports`: `ListImports`
- `op_list_tables`: `ListTables`
- `op_list_tags_of_resource`: `ListTagsOfResource`
- `op_put_item`: `PutItem`
- `op_put_resource_policy`: `PutResourcePolicy`
- `op_query`: `Query`
- `op_restore_table_from_backup`: `RestoreTableFromBackup`
- `op_restore_table_to_point_in_time`: `RestoreTableToPointInTime`
- `op_scan`: `Scan`
- `op_search_vectors`: `SearchVectors`
- `op_tag_resource`: `TagResource`
- `op_transact_get_items`: `TransactGetItems`
- `op_transact_write_items`: `TransactWriteItems`
- `op_untag_resource`: `UntagResource`
- `op_update_continuous_backups`: `UpdateContinuousBackups`
- `op_update_contributor_insights`: `UpdateContributorInsights`
- `op_update_global_table`: `UpdateGlobalTable`
- `op_update_global_table_settings`: `UpdateGlobalTableSettings`
- `op_update_item`: `UpdateItem`
- `op_update_kinesis_streaming_destination`: `UpdateKinesisStreamingDestination`
- `op_update_table`: `UpdateTable`
- `op_update_table_replica_auto_scaling`: `UpdateTableReplicaAutoScaling`
- `op_update_time_to_live`: `UpdateTimeToLive`

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
- `src/waiters.rs`
- `src/waiters/matchers.rs`

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
@@ -90,51 +79,41 @@
 version = "0.5.1"

 [dev-dependencies.aws-config]
-path = "../aws-config"
 features = ["test-util"]
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

 [dev-dependencies.aws-smithy-xml]
-path = "../aws-smithy-xml"
 version = "0.62.0"

 [dev-dependencies.criterion]
@@ -167,6 +146,64 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_batch_execute_statement = []
+op_batch_get_item = []
+op_batch_write_item = []
+op_create_backup = []
+op_create_global_table = []
+op_create_table = []
+op_delete_backup = []
+op_delete_item = []
+op_delete_resource_policy = []
+op_delete_table = []
+op_describe_backup = []
+op_describe_continuous_backups = []
+op_describe_contributor_insights = []
+op_describe_endpoints = []
+op_describe_export = []
+op_describe_global_table = []
+op_describe_global_table_settings = []
+op_describe_import = []
+op_describe_kinesis_streaming_destination = []
+op_describe_limits = []
+op_describe_table = []
+op_describe_table_replica_auto_scaling = []
+op_describe_time_to_live = []
+op_disable_kinesis_streaming_destination = []
+op_enable_kinesis_streaming_destination = []
+op_execute_statement = []
+op_execute_transaction = []
+op_export_table_to_point_in_time = []
+op_get_item = []
+op_get_resource_policy = []
+op_import_table = []
+op_list_backups = []
+op_list_contributor_insights = []
+op_list_exports = []
+op_list_global_tables = []
+op_list_imports = []
+op_list_tables = []
+op_list_tags_of_resource = []
+op_put_item = []
+op_put_resource_policy = []
+op_query = []
+op_restore_table_from_backup = []
+op_restore_table_to_point_in_time = []
+op_scan = []
+op_search_vectors = []
+op_tag_resource = []
+op_transact_get_items = []
+op_transact_write_items = []
+op_untag_resource = []
+op_update_continuous_backups = []
+op_update_contributor_insights = []
+op_update_global_table = []
+op_update_global_table_settings = []
+op_update_item = []
+op_update_kinesis_streaming_destination = []
+op_update_table = []
+op_update_table_replica_auto_scaling = []
+op_update_time_to_live = []

 [hints]
 mostly-unused = true
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -140,35 +140,45 @@
 /// Import this trait to get `wait_until` methods on the client.
 ///
 pub trait Waiters {
+    #[cfg(feature = "op_describe_contributor_insights")]
     /// Wait for `contributor_insights_enabled`
     fn wait_until_contributor_insights_enabled(
         &self,
     ) -> crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder;
+    #[cfg(feature = "op_describe_export")]
     /// Wait for `export_completed`
     fn wait_until_export_completed(&self) -> crate::waiters::export_completed::ExportCompletedFluentBuilder;
+    #[cfg(feature = "op_describe_import")]
     /// Wait for `import_completed`
     fn wait_until_import_completed(&self) -> crate::waiters::import_completed::ImportCompletedFluentBuilder;
+    #[cfg(feature = "op_describe_kinesis_streaming_destination")]
     /// Wait for `kinesis_streaming_destination_active`
     fn wait_until_kinesis_streaming_destination_active(
         &self,
     ) -> crate::waiters::kinesis_streaming_destination_active::KinesisStreamingDestinationActiveFluentBuilder;
+    #[cfg(feature = "op_describe_table")]
     /// Wait for `table_exists`
     fn wait_until_table_exists(&self) -> crate::waiters::table_exists::TableExistsFluentBuilder;
+    #[cfg(feature = "op_describe_table")]
     /// Wait for `table_not_exists`
     fn wait_until_table_not_exists(&self) -> crate::waiters::table_not_exists::TableNotExistsFluentBuilder;
 }
 impl Waiters for Client {
+    #[cfg(feature = "op_describe_contributor_insights")]
     fn wait_until_contributor_insights_enabled(
         &self,
     ) -> crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder {
         crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_export")]
     fn wait_until_export_completed(&self) -> crate::waiters::export_completed::ExportCompletedFluentBuilder {
         crate::waiters::export_completed::ExportCompletedFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_import")]
     fn wait_until_import_completed(&self) -> crate::waiters::import_completed::ImportCompletedFluentBuilder {
         crate::waiters::import_completed::ImportCompletedFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_kinesis_streaming_destination")]
     fn wait_until_kinesis_streaming_destination_active(
         &self,
     ) -> crate::waiters::kinesis_streaming_destination_active::KinesisStreamingDestinationActiveFluentBuilder {
@@ -176,9 +186,11 @@
             self.handle.clone(),
         )
     }
+    #[cfg(feature = "op_describe_table")]
     fn wait_until_table_exists(&self) -> crate::waiters::table_exists::TableExistsFluentBuilder {
         crate::waiters::table_exists::TableExistsFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_table")]
     fn wait_until_table_not_exists(&self) -> crate::waiters::table_not_exists::TableNotExistsFluentBuilder {
         crate::waiters::table_not_exists::TableNotExistsFluentBuilder::new(self.handle.clone())
     }
@@ -200,16 +212,22 @@
     }
 }

+#[cfg(feature = "op_batch_execute_statement")]
 mod batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 mod batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 mod batch_write_item;

+#[cfg(feature = "op_create_backup")]
 mod create_backup;

+#[cfg(feature = "op_create_global_table")]
 mod create_global_table;

+#[cfg(feature = "op_create_table")]
 mod create_table;

 /// Operation customization and supporting types.
@@ -239,106 +257,158 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_backup")]
 mod delete_backup;

+#[cfg(feature = "op_delete_item")]
 mod delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 mod delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 mod delete_table;

+#[cfg(feature = "op_describe_backup")]
 mod describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 mod describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 mod describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 mod describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 mod describe_export;

+#[cfg(feature = "op_describe_global_table")]
 mod describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 mod describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 mod describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 mod describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 mod describe_limits;

+#[cfg(feature = "op_describe_table")]
 mod describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 mod describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 mod describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 mod disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 mod enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 mod execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 mod execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 mod get_item;

+#[cfg(feature = "op_get_resource_policy")]
 mod get_resource_policy;

+#[cfg(feature = "op_import_table")]
 mod import_table;

+#[cfg(feature = "op_list_backups")]
 mod list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 mod list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 mod list_exports;

+#[cfg(feature = "op_list_global_tables")]
 mod list_global_tables;

+#[cfg(feature = "op_list_imports")]
 mod list_imports;

+#[cfg(feature = "op_list_tables")]
 mod list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 mod list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 mod put_item;

+#[cfg(feature = "op_put_resource_policy")]
 mod put_resource_policy;

+#[cfg(feature = "op_query")]
 mod query;

+#[cfg(feature = "op_restore_table_from_backup")]
 mod restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 mod restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 mod scan;

+#[cfg(feature = "op_search_vectors")]
 mod search_vectors;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 mod transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 mod transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 mod update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 mod update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 mod update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 mod update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 mod update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 mod update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 mod update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 mod update_time_to_live;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,42 +3,207 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_delete_backup",
+        feature = "op_restore_table_from_backup"
+    ))]
     /// <p>There is another ongoing conflicting backup control plane operation on the table. The backup is either being created, deleted or restored to a table.</p>
     BackupInUseException(crate::types::error::BackupInUseException),
+    #[cfg(any(
+        feature = "op_delete_backup",
+        feature = "op_describe_backup",
+        feature = "op_restore_table_from_backup"
+    ))]
     /// <p>Backup not found for the given BackupARN.</p>
     BackupNotFoundException(crate::types::error::BackupNotFoundException),
+    #[cfg(any(
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>A condition specified in the operation failed to be evaluated.</p>
     ConditionalCheckFailedException(crate::types::error::ConditionalCheckFailedException),
+    #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
     /// <p>Backups have not yet been enabled for this table.</p>
     ContinuousBackupsUnavailableException(crate::types::error::ContinuousBackupsUnavailableException),
+    #[cfg(feature = "op_execute_statement")]
     /// <p>There was an attempt to insert an item with the same primary key as an item that already exists in the DynamoDB table.</p>
     DuplicateItemException(crate::types::error::DuplicateItemException),
+    #[cfg(feature = "op_export_table_to_point_in_time")]
     /// <p>There was a conflict when writing to the specified S3 bucket.</p>
     ExportConflictException(crate::types::error::ExportConflictException),
+    #[cfg(feature = "op_describe_export")]
     /// <p>The specified export was not found.</p>
     ExportNotFoundException(crate::types::error::ExportNotFoundException),
+    #[cfg(feature = "op_create_global_table")]
     /// <p>The specified global table already exists.</p>
     GlobalTableAlreadyExistsException(crate::types::error::GlobalTableAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings"
+    ))]
     /// <p>The specified global table does not exist.</p>
     GlobalTableNotFoundException(crate::types::error::GlobalTableNotFoundException),
+    #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
     /// <p>DynamoDB rejected the request because you retried a request with a different payload but with an idempotent token that was already used.</p>
     IdempotentParameterMismatchException(crate::types::error::IdempotentParameterMismatchException),
+    #[cfg(feature = "op_import_table")]
     /// <p>There was a conflict when importing from the specified S3 source. This can occur when the current import conflicts with a previous import request that had the same client token.</p>
     ImportConflictException(crate::types::error::ImportConflictException),
+    #[cfg(feature = "op_describe_import")]
     /// <p>The specified import was not found.</p>
     ImportNotFoundException(crate::types::error::ImportNotFoundException),
+    #[cfg(feature = "op_update_global_table_settings")]
     /// <p>The operation tried to access a nonexistent index.</p>
     IndexNotFoundException(crate::types::error::IndexNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_backup",
+        feature = "op_describe_continuous_backups",
+        feature = "op_describe_contributor_insights",
+        feature = "op_describe_export",
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_limits",
+        feature = "op_describe_table",
+        feature = "op_describe_table_replica_auto_scaling",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_backups",
+        feature = "op_list_contributor_insights",
+        feature = "op_list_exports",
+        feature = "op_list_global_tables",
+        feature = "op_list_tables",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_contributor_insights",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>An error occurred on the server side.</p>
     InternalServerError(crate::types::error::InternalServerError),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_backup",
+        feature = "op_describe_continuous_backups",
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_limits",
+        feature = "op_describe_table",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_backups",
+        feature = "op_list_global_tables",
+        feature = "op_list_tables",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_scan",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_time_to_live"
+    ))]
     #[allow(missing_docs)] // documentation missing in model
     InvalidEndpointException(crate::types::error::InvalidEndpointException),
+    #[cfg(feature = "op_export_table_to_point_in_time")]
     /// <p>The specified <code>ExportTime</code> is outside of the point in time recovery window.</p>
     InvalidExportTimeException(crate::types::error::InvalidExportTimeException),
+    #[cfg(feature = "op_restore_table_to_point_in_time")]
     /// <p>An invalid restore time was specified. RestoreDateTime must be between EarliestRestorableDateTime and LatestRestorableDateTime.</p>
     InvalidRestoreTimeException(crate::types::error::InvalidRestoreTimeException),
+    #[cfg(any(
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>An item collection is too large. This exception is only returned for tables that have one or more local secondary indexes.</p>
     ItemCollectionSizeLimitExceededException(crate::types::error::ItemCollectionSizeLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_export",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_import_table",
+        feature = "op_list_exports",
+        feature = "op_list_imports",
+        feature = "op_put_resource_policy",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>There is no limit to the number of daily on-demand backups that can be taken.</p>
     /// <p>For most purposes, up to 500 simultaneous table operations are allowed per account. These operations include <code>CreateTable</code>, <code>UpdateTable</code>, <code>DeleteTable</code>,<code>UpdateTimeToLive</code>, <code>RestoreTableFromBackup</code>, and <code>RestoreTableToPointInTime</code>.</p>
     /// <p>When you are creating a table with one or more secondary indexes, you can have up to 250 such requests running at a time. However, if the table or index specifications are complex, then DynamoDB might temporarily reduce the number of concurrent operations.</p>
@@ -47,21 +212,84 @@
     /// <p>GetRecords was called with a value of more than 1000 for the limit request parameter.</p>
     /// <p>More than 2 processes are reading from the same streams shard at the same time. Exceeding this limit may result in request throttling.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>Point in time recovery has not yet been enabled for this source table.</p>
     PointInTimeRecoveryUnavailableException(crate::types::error::PointInTimeRecoveryUnavailableException),
+    #[cfg(any(
+        feature = "op_delete_resource_policy",
+        feature = "op_get_resource_policy",
+        feature = "op_put_resource_policy"
+    ))]
     /// <p>The operation tried to access a nonexistent resource-based policy.</p>
     /// <p>If you specified an <code>ExpectedRevisionId</code>, it's possible that a policy is present for the resource but its revision ID didn't match the expected value.</p>
     PolicyNotFoundException(crate::types::error::PolicyNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was denied due to request throttling. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception. The Amazon Web Services SDKs for DynamoDB automatically retry requests that receive this exception. Your request is eventually successful, unless your retry queue is too large to finish. Reduce the frequency of requests and use exponential backoff. For more information, go to <a href="https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Programming.Errors.html#Programming.Errors.RetryAndBackoff">Error Retries and Exponential Backoff</a> in the <i>Amazon DynamoDB Developer Guide</i>.</p>
     ProvisionedThroughputExceededException(crate::types::error::ProvisionedThroughputExceededException),
+    #[cfg(feature = "op_update_global_table")]
     /// <p>The specified replica is already part of the global table.</p>
     ReplicaAlreadyExistsException(crate::types::error::ReplicaAlreadyExistsException),
+    #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
     /// <p>The specified replica is no longer part of the global table.</p>
     ReplicaNotFoundException(crate::types::error::ReplicaNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was rejected because one or more items in the request are being modified by a request in another Region.</p>
     ReplicatedWriteConflictException(crate::types::error::ReplicatedWriteConflictException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>Throughput exceeds the current throughput quota for your account. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception. Contact <a href="https://aws.amazon.com/support">Amazon Web Services Support</a> to request a quota increase.</p>
     RequestLimitExceeded(crate::types::error::RequestLimitExceeded),
+    #[cfg(any(
+        feature = "op_create_table",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_import_table",
+        feature = "op_put_resource_policy",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>The operation conflicts with the resource's availability. For example:</p>
     /// <ul>
     /// <li>
@@ -73,16 +301,90 @@
     /// </ul>
     /// <p>When appropriate, wait for the ongoing update to complete and attempt the request again.</p>
     ResourceInUseException(crate::types::error::ResourceInUseException),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_contributor_insights",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_table",
+        feature = "op_describe_table_replica_auto_scaling",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_contributor_insights",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_contributor_insights",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>The operation tried to access a nonexistent table or index. The resource might not be specified correctly, or its status might not be <code>ACTIVE</code>.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>A target table with the specified name already exists.</p>
     TableAlreadyExistsException(crate::types::error::TableAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>A target table with the specified name is either being created or deleted.</p>
     TableInUseException(crate::types::error::TableInUseException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_describe_continuous_backups",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_global_table"
+    ))]
     /// <p>A source table with the name <code>TableName</code> does not currently exist within the subscriber's account or the subscriber is operating in the wrong Amazon Web Services Region.</p>
     TableNotFoundException(crate::types::error::TableNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was denied due to request throttling. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception.</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(any(
+        feature = "op_execute_transaction",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items"
+    ))]
     /// <p>The entire transaction request was canceled.</p>
     /// <p>DynamoDB cancels a <code>TransactWriteItems</code> request under the following circumstances:</p>
     /// <ul>
@@ -216,8 +518,15 @@
     /// </ul></li>
     /// </ul>
     TransactionCanceledException(crate::types::error::TransactionCanceledException),
+    #[cfg(any(
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>Operation was rejected because there is an ongoing transaction for the item.</p>
     TransactionConflictException(crate::types::error::TransactionConflictException),
+    #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
     /// <p>The transaction with the given request token is already in progress.</p>
     /// <p>Recommended Settings</p><note>
     /// <p>This is a general recommendation for handling the <code>TransactionInProgressException</code>. These settings help ensure that the client retries will trigger completion of the ongoing <code>TransactWriteItems</code> request.</p>
@@ -265,40 +574,349 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ConditionalCheckFailedException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Error::ContinuousBackupsUnavailableException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_execute_statement")]
             Error::DuplicateItemException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::ExportConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_describe_export")]
             Error::ExportNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_global_table")]
             Error::GlobalTableAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Error::GlobalTableNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::IdempotentParameterMismatchException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_table")]
             Error::ImportConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_describe_import")]
             Error::ImportNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_global_table_settings")]
             Error::IndexNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InternalServerError(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InvalidEndpointException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::InvalidExportTimeException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Error::InvalidRestoreTimeException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ItemCollectionSizeLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::PointInTimeRecoveryUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Error::PolicyNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ProvisionedThroughputExceededException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_global_table")]
             Error::ReplicaAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Error::ReplicaNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ReplicatedWriteConflictException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::RequestLimitExceeded(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Error::TableNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Error::TransactionCanceledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::TransactionConflictException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::TransactionInProgressException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -323,45 +941,355 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ConditionalCheckFailedException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Self::ContinuousBackupsUnavailableException(inner) => inner.meta(),
+            #[cfg(feature = "op_execute_statement")]
             Self::DuplicateItemException(inner) => inner.meta(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::ExportConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_describe_export")]
             Self::ExportNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_global_table")]
             Self::GlobalTableAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Self::GlobalTableNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::IdempotentParameterMismatchException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_table")]
             Self::ImportConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_describe_import")]
             Self::ImportNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Self::IndexNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InternalServerError(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InvalidEndpointException(inner) => inner.meta(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::InvalidExportTimeException(inner) => inner.meta(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Self::InvalidRestoreTimeException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ItemCollectionSizeLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::PointInTimeRecoveryUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Self::PolicyNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ProvisionedThroughputExceededException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_global_table")]
             Self::ReplicaAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Self::ReplicaNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ReplicatedWriteConflictException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::RequestLimitExceeded(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Self::TableNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Self::TransactionCanceledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::TransactionConflictException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::TransactionInProgressException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_batch_execute_statement")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -387,6 +1315,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_execute_statement")]
 impl From<crate::operation::batch_execute_statement::BatchExecuteStatementError> for Error {
     fn from(err: crate::operation::batch_execute_statement::BatchExecuteStatementError) -> Self {
         match err {
@@ -405,6 +1334,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::batch_get_item::BatchGetItemError, R>>
     for Error
 where
@@ -422,6 +1352,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_item")]
 impl From<crate::operation::batch_get_item::BatchGetItemError> for Error {
     fn from(err: crate::operation::batch_get_item::BatchGetItemError) -> Self {
         match err {
@@ -447,6 +1378,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_write_item")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::batch_write_item::BatchWriteItemError, R>>
     for Error
@@ -468,6 +1400,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_write_item")]
 impl From<crate::operation::batch_write_item::BatchWriteItemError> for Error {
     fn from(err: crate::operation::batch_write_item::BatchWriteItemError) -> Self {
         match err {
@@ -499,6 +1432,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_backup")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_backup::CreateBackupError, R>>
     for Error
 where
@@ -516,6 +1450,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_backup")]
 impl From<crate::operation::create_backup::CreateBackupError> for Error {
     fn from(err: crate::operation::create_backup::CreateBackupError) -> Self {
         match err {
@@ -544,6 +1479,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -569,6 +1505,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_global_table")]
 impl From<crate::operation::create_global_table::CreateGlobalTableError> for Error {
     fn from(err: crate::operation::create_global_table::CreateGlobalTableError) -> Self {
         match err {
@@ -591,6 +1528,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_table::CreateTableError, R>>
     for Error
 where
@@ -608,6 +1546,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_table")]
 impl From<crate::operation::create_table::CreateTableError> for Error {
     fn from(err: crate::operation::create_table::CreateTableError) -> Self {
         match err {
@@ -627,6 +1566,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_backup")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_backup::DeleteBackupError, R>>
     for Error
 where
@@ -644,6 +1584,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_backup")]
 impl From<crate::operation::delete_backup::DeleteBackupError> for Error {
     fn from(err: crate::operation::delete_backup::DeleteBackupError) -> Self {
         match err {
@@ -666,6 +1607,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_item::DeleteItemError, R>>
     for Error
 where
@@ -683,6 +1625,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_item")]
 impl From<crate::operation::delete_item::DeleteItemError> for Error {
     fn from(err: crate::operation::delete_item::DeleteItemError) -> Self {
         match err {
@@ -720,6 +1663,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -745,6 +1689,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl From<crate::operation::delete_resource_policy::DeleteResourcePolicyError> for Error {
     fn from(err: crate::operation::delete_resource_policy::DeleteResourcePolicyError) -> Self {
         match err {
@@ -772,6 +1717,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_table::DeleteTableError, R>>
     for Error
 where
@@ -789,6 +1735,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_table")]
 impl From<crate::operation::delete_table::DeleteTableError> for Error {
     fn from(err: crate::operation::delete_table::DeleteTableError) -> Self {
         match err {
@@ -811,6 +1758,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_backup")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_backup::DescribeBackupError, R>>
     for Error
@@ -832,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_backup")]
 impl From<crate::operation::describe_backup::DescribeBackupError> for Error {
     fn from(err: crate::operation::describe_backup::DescribeBackupError) -> Self {
         match err {
@@ -848,6 +1797,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_continuous_backups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -873,6 +1823,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_continuous_backups")]
 impl From<crate::operation::describe_continuous_backups::DescribeContinuousBackupsError> for Error {
     fn from(err: crate::operation::describe_continuous_backups::DescribeContinuousBackupsError) -> Self {
         match err {
@@ -891,6 +1842,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -916,6 +1868,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_contributor_insights")]
 impl From<crate::operation::describe_contributor_insights::DescribeContributorInsightsError> for Error {
     fn from(err: crate::operation::describe_contributor_insights::DescribeContributorInsightsError) -> Self {
         match err {
@@ -929,6 +1882,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_endpoints")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -954,6 +1908,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_endpoints")]
 impl From<crate::operation::describe_endpoints::DescribeEndpointsError> for Error {
     fn from(err: crate::operation::describe_endpoints::DescribeEndpointsError) -> Self {
         match err {
@@ -961,6 +1916,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_export::DescribeExportError, R>>
     for Error
@@ -982,6 +1938,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export")]
 impl From<crate::operation::describe_export::DescribeExportError> for Error {
     fn from(err: crate::operation::describe_export::DescribeExportError) -> Self {
         match err {
@@ -998,6 +1955,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1023,6 +1981,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table")]
 impl From<crate::operation::describe_global_table::DescribeGlobalTableError> for Error {
     fn from(err: crate::operation::describe_global_table::DescribeGlobalTableError) -> Self {
         match err {
@@ -1041,6 +2000,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table_settings")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1066,6 +2026,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table_settings")]
 impl From<crate::operation::describe_global_table_settings::DescribeGlobalTableSettingsError> for Error {
     fn from(err: crate::operation::describe_global_table_settings::DescribeGlobalTableSettingsError) -> Self {
         match err {
@@ -1082,6 +2043,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_import::DescribeImportError, R>>
     for Error
@@ -1103,6 +2065,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import")]
 impl From<crate::operation::describe_import::DescribeImportError> for Error {
     fn from(err: crate::operation::describe_import::DescribeImportError) -> Self {
         match err {
@@ -1113,6 +2076,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1138,6 +2102,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 impl From<crate::operation::describe_kinesis_streaming_destination::DescribeKinesisStreamingDestinationError>
     for Error
 {
@@ -1160,6 +2125,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_limits")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_limits::DescribeLimitsError, R>>
     for Error
@@ -1181,6 +2147,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_limits")]
 impl From<crate::operation::describe_limits::DescribeLimitsError> for Error {
     fn from(err: crate::operation::describe_limits::DescribeLimitsError) -> Self {
         match err {
@@ -1194,6 +2161,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_table::DescribeTableError, R>>
     for Error
@@ -1215,6 +2183,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table")]
 impl From<crate::operation::describe_table::DescribeTableError> for Error {
     fn from(err: crate::operation::describe_table::DescribeTableError) -> Self {
         match err {
@@ -1231,6 +2200,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1256,6 +2226,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 impl From<crate::operation::describe_table_replica_auto_scaling::DescribeTableReplicaAutoScalingError> for Error {
     fn from(err: crate::operation::describe_table_replica_auto_scaling::DescribeTableReplicaAutoScalingError) -> Self {
         match err {
@@ -1269,6 +2240,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_time_to_live")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1294,6 +2266,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_time_to_live")]
 impl From<crate::operation::describe_time_to_live::DescribeTimeToLiveError> for Error {
     fn from(err: crate::operation::describe_time_to_live::DescribeTimeToLiveError) -> Self {
         match err {
@@ -1312,6 +2285,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1337,6 +2311,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 impl From<crate::operation::disable_kinesis_streaming_destination::DisableKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::disable_kinesis_streaming_destination::DisableKinesisStreamingDestinationError,
@@ -1363,6 +2338,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1388,6 +2364,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 impl From<crate::operation::enable_kinesis_streaming_destination::EnableKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::enable_kinesis_streaming_destination::EnableKinesisStreamingDestinationError,
@@ -1414,6 +2391,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_statement")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1439,6 +2417,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_statement")]
 impl From<crate::operation::execute_statement::ExecuteStatementError> for Error {
     fn from(err: crate::operation::execute_statement::ExecuteStatementError) -> Self {
         match err {
@@ -1473,6 +2452,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_transaction")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1498,6 +2478,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_transaction")]
 impl From<crate::operation::execute_transaction::ExecuteTransactionError> for Error {
     fn from(err: crate::operation::execute_transaction::ExecuteTransactionError) -> Self {
         match err {
@@ -1529,6 +2510,7 @@
         }
     }
 }
+#[cfg(feature = "op_export_table_to_point_in_time")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1554,6 +2536,7 @@
         }
     }
 }
+#[cfg(feature = "op_export_table_to_point_in_time")]
 impl From<crate::operation::export_table_to_point_in_time::ExportTableToPointInTimeError> for Error {
     fn from(err: crate::operation::export_table_to_point_in_time::ExportTableToPointInTimeError) -> Self {
         match err {
@@ -1579,6 +2562,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_item::GetItemError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1595,6 +2579,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_item")]
 impl From<crate::operation::get_item::GetItemError> for Error {
     fn from(err: crate::operation::get_item::GetItemError) -> Self {
         match err {
@@ -1614,6 +2599,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1639,6 +2625,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_resource_policy")]
 impl From<crate::operation::get_resource_policy::GetResourcePolicyError> for Error {
     fn from(err: crate::operation::get_resource_policy::GetResourcePolicyError) -> Self {
         match err {
@@ -1658,6 +2645,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::import_table::ImportTableError, R>>
     for Error
 where
@@ -1675,6 +2663,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_table")]
 impl From<crate::operation::import_table::ImportTableError> for Error {
     fn from(err: crate::operation::import_table::ImportTableError) -> Self {
         match err {
@@ -1691,6 +2680,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_backups")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_backups::ListBackupsError, R>>
     for Error
 where
@@ -1708,6 +2698,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_backups")]
 impl From<crate::operation::list_backups::ListBackupsError> for Error {
     fn from(err: crate::operation::list_backups::ListBackupsError) -> Self {
         match err {
@@ -1721,6 +2712,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1746,6 +2738,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contributor_insights")]
 impl From<crate::operation::list_contributor_insights::ListContributorInsightsError> for Error {
     fn from(err: crate::operation::list_contributor_insights::ListContributorInsightsError) -> Self {
         match err {
@@ -1761,6 +2754,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_exports")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_exports::ListExportsError, R>>
     for Error
 where
@@ -1778,6 +2772,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_exports")]
 impl From<crate::operation::list_exports::ListExportsError> for Error {
     fn from(err: crate::operation::list_exports::ListExportsError) -> Self {
         match err {
@@ -1791,6 +2786,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_global_tables")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1816,6 +2812,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_global_tables")]
 impl From<crate::operation::list_global_tables::ListGlobalTablesError> for Error {
     fn from(err: crate::operation::list_global_tables::ListGlobalTablesError) -> Self {
         match err {
@@ -1829,6 +2826,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_imports")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_imports::ListImportsError, R>>
     for Error
 where
@@ -1846,6 +2844,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_imports")]
 impl From<crate::operation::list_imports::ListImportsError> for Error {
     fn from(err: crate::operation::list_imports::ListImportsError) -> Self {
         match err {
@@ -1856,6 +2855,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tables")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_tables::ListTablesError, R>>
     for Error
 where
@@ -1873,6 +2873,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tables")]
 impl From<crate::operation::list_tables::ListTablesError> for Error {
     fn from(err: crate::operation::list_tables::ListTablesError) -> Self {
         match err {
@@ -1886,6 +2887,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_of_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1911,6 +2913,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_of_resource")]
 impl From<crate::operation::list_tags_of_resource::ListTagsOfResourceError> for Error {
     fn from(err: crate::operation::list_tags_of_resource::ListTagsOfResourceError) -> Self {
         match err {
@@ -1929,6 +2932,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_item::PutItemError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1945,6 +2949,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_item")]
 impl From<crate::operation::put_item::PutItemError> for Error {
     fn from(err: crate::operation::put_item::PutItemError) -> Self {
         match err {
@@ -1976,6 +2981,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2001,6 +3007,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl From<crate::operation::put_resource_policy::PutResourcePolicyError> for Error {
     fn from(err: crate::operation::put_resource_policy::PutResourcePolicyError) -> Self {
         match err {
@@ -2026,6 +3033,7 @@
         }
     }
 }
+#[cfg(feature = "op_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::query::QueryError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2040,6 +3048,7 @@
         }
     }
 }
+#[cfg(feature = "op_query")]
 impl From<crate::operation::query::QueryError> for Error {
     fn from(err: crate::operation::query::QueryError) -> Self {
         match err {
@@ -2059,6 +3068,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_from_backup")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2084,6 +3094,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_from_backup")]
 impl From<crate::operation::restore_table_from_backup::RestoreTableFromBackupError> for Error {
     fn from(err: crate::operation::restore_table_from_backup::RestoreTableFromBackupError) -> Self {
         match err {
@@ -2114,6 +3125,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_to_point_in_time")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2139,6 +3151,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_to_point_in_time")]
 impl From<crate::operation::restore_table_to_point_in_time::RestoreTableToPointInTimeError> for Error {
     fn from(err: crate::operation::restore_table_to_point_in_time::RestoreTableToPointInTimeError) -> Self {
         match err {
@@ -2170,6 +3183,7 @@
         }
     }
 }
+#[cfg(feature = "op_scan")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::scan::ScanError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2184,6 +3198,7 @@
         }
     }
 }
+#[cfg(feature = "op_scan")]
 impl From<crate::operation::scan::ScanError> for Error {
     fn from(err: crate::operation::scan::ScanError) -> Self {
         match err {
@@ -2203,6 +3218,7 @@
         }
     }
 }
+#[cfg(feature = "op_search_vectors")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::search_vectors::SearchVectorsError, R>>
     for Error
@@ -2224,6 +3240,7 @@
         }
     }
 }
+#[cfg(feature = "op_search_vectors")]
 impl From<crate::operation::search_vectors::SearchVectorsError> for Error {
     fn from(err: crate::operation::search_vectors::SearchVectorsError) -> Self {
         match err {
@@ -2243,6 +3260,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -2260,6 +3278,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -2282,6 +3301,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_get_items")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2307,6 +3327,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_get_items")]
 impl From<crate::operation::transact_get_items::TransactGetItemsError> for Error {
     fn from(err: crate::operation::transact_get_items::TransactGetItemsError) -> Self {
         match err {
@@ -2335,6 +3356,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_write_items")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2360,6 +3382,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_write_items")]
 impl From<crate::operation::transact_write_items::TransactWriteItemsError> for Error {
     fn from(err: crate::operation::transact_write_items::TransactWriteItemsError) -> Self {
         match err {
@@ -2396,6 +3419,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2417,6 +3441,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2439,6 +3464,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_continuous_backups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2464,6 +3490,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_continuous_backups")]
 impl From<crate::operation::update_continuous_backups::UpdateContinuousBackupsError> for Error {
     fn from(err: crate::operation::update_continuous_backups::UpdateContinuousBackupsError) -> Self {
         match err {
@@ -2483,6 +3510,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2508,6 +3536,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contributor_insights")]
 impl From<crate::operation::update_contributor_insights::UpdateContributorInsightsError> for Error {
     fn from(err: crate::operation::update_contributor_insights::UpdateContributorInsightsError) -> Self {
         match err {
@@ -2521,6 +3550,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2546,6 +3576,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table")]
 impl From<crate::operation::update_global_table::UpdateGlobalTableError> for Error {
     fn from(err: crate::operation::update_global_table::UpdateGlobalTableError) -> Self {
         match err {
@@ -2571,6 +3602,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table_settings")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2596,6 +3628,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table_settings")]
 impl From<crate::operation::update_global_table_settings::UpdateGlobalTableSettingsError> for Error {
     fn from(err: crate::operation::update_global_table_settings::UpdateGlobalTableSettingsError) -> Self {
         match err {
@@ -2624,6 +3657,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_item::UpdateItemError, R>>
     for Error
 where
@@ -2641,6 +3675,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_item")]
 impl From<crate::operation::update_item::UpdateItemError> for Error {
     fn from(err: crate::operation::update_item::UpdateItemError) -> Self {
         match err {
@@ -2678,6 +3713,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2703,6 +3739,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 impl From<crate::operation::update_kinesis_streaming_destination::UpdateKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::update_kinesis_streaming_destination::UpdateKinesisStreamingDestinationError,
@@ -2729,6 +3766,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_table::UpdateTableError, R>>
     for Error
 where
@@ -2746,6 +3784,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table")]
 impl From<crate::operation::update_table::UpdateTableError> for Error {
     fn from(err: crate::operation::update_table::UpdateTableError) -> Self {
         match err {
@@ -2768,6 +3807,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2793,6 +3833,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 impl From<crate::operation::update_table_replica_auto_scaling::UpdateTableReplicaAutoScalingError> for Error {
     fn from(err: crate::operation::update_table_replica_auto_scaling::UpdateTableReplicaAutoScalingError) -> Self {
         match err {
@@ -2812,6 +3853,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_time_to_live")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2837,6 +3879,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_time_to_live")]
 impl From<crate::operation::update_time_to_live::UpdateTimeToLiveError> for Error {
     fn from(err: crate::operation::update_time_to_live::UpdateTimeToLiveError) -> Self {
         match err {
@@ -2874,40 +3917,349 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ConditionalCheckFailedException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Error::ContinuousBackupsUnavailableException(inner) => inner.source(),
+            #[cfg(feature = "op_execute_statement")]
             Error::DuplicateItemException(inner) => inner.source(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::ExportConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_describe_export")]
             Error::ExportNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_create_global_table")]
             Error::GlobalTableAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Error::GlobalTableNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::IdempotentParameterMismatchException(inner) => inner.source(),
+            #[cfg(feature = "op_import_table")]
             Error::ImportConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_describe_import")]
             Error::ImportNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Error::IndexNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InternalServerError(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InvalidEndpointException(inner) => inner.source(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::InvalidExportTimeException(inner) => inner.source(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Error::InvalidRestoreTimeException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ItemCollectionSizeLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::PointInTimeRecoveryUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Error::PolicyNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ProvisionedThroughputExceededException(inner) => inner.source(),
+            #[cfg(feature = "op_update_global_table")]
             Error::ReplicaAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Error::ReplicaNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ReplicatedWriteConflictException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::RequestLimitExceeded(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Error::TableNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Error::TransactionCanceledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::TransactionConflictException(inner) => inner.source(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::TransactionInProgressException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2916,40 +4268,349 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ConditionalCheckFailedException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Self::ContinuousBackupsUnavailableException(e) => e.request_id(),
+            #[cfg(feature = "op_execute_statement")]
             Self::DuplicateItemException(e) => e.request_id(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::ExportConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_describe_export")]
             Self::ExportNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_create_global_table")]
             Self::GlobalTableAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Self::GlobalTableNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::IdempotentParameterMismatchException(e) => e.request_id(),
+            #[cfg(feature = "op_import_table")]
             Self::ImportConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_describe_import")]
             Self::ImportNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Self::IndexNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InternalServerError(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InvalidEndpointException(e) => e.request_id(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::InvalidExportTimeException(e) => e.request_id(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Self::InvalidRestoreTimeException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ItemCollectionSizeLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::PointInTimeRecoveryUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Self::PolicyNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ProvisionedThroughputExceededException(e) => e.request_id(),
+            #[cfg(feature = "op_update_global_table")]
             Self::ReplicaAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Self::ReplicaNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ReplicatedWriteConflictException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::RequestLimitExceeded(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Self::TableNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Self::TransactionCanceledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::TransactionConflictException(e) => e.request_id(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::TransactionInProgressException(e) => e.request_id(),
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
+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) fn reflens_list_contributor_insights_output_output_next_token(
     input: &crate::operation::list_contributor_insights::ListContributorInsightsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_exports")]
 pub(crate) fn reflens_list_exports_output_output_next_token(
     input: &crate::operation::list_exports::ListExportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_imports")]
 pub(crate) fn reflens_list_imports_output_output_next_token(
     input: &crate::operation::list_imports::ListImportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tables")]
 pub(crate) fn reflens_list_tables_output_output_last_evaluated_table_name(
     input: &crate::operation::list_tables::ListTablesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_query")]
 pub(crate) fn reflens_query_output_output_last_evaluated_key(
     input: &crate::operation::query::QueryOutput,
 ) -> ::std::option::Option<&::std::collections::HashMap<::std::string::String, crate::types::AttributeValue>> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_scan")]
 pub(crate) fn reflens_scan_output_output_last_evaluated_key(
     input: &crate::operation::scan::ScanOutput,
 ) -> ::std::option::Option<&::std::collections::HashMap<::std::string::String, crate::types::AttributeValue>> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tables")]
 pub(crate) fn lens_list_tables_output_output_table_names(
     input: crate::operation::list_tables::ListTablesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -66,6 +73,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_query")]
 pub(crate) fn lens_query_output_output_items(
     input: crate::operation::query::QueryOutput,
 ) -> ::std::option::Option<
@@ -75,6 +83,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_scan")]
 pub(crate) fn lens_scan_output_output_items(
     input: crate::operation::scan::ScanOutput,
 ) -> ::std::option::Option<
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,176 +1,234 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_batch_execute_statement")]
 /// Types for the `BatchExecuteStatement` operation.
 pub mod batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 /// Types for the `BatchGetItem` operation.
 pub mod batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 /// Types for the `BatchWriteItem` operation.
 pub mod batch_write_item;

+#[cfg(feature = "op_create_backup")]
 /// Types for the `CreateBackup` operation.
 pub mod create_backup;

+#[cfg(feature = "op_create_global_table")]
 /// Types for the `CreateGlobalTable` operation.
 pub mod create_global_table;

+#[cfg(feature = "op_create_table")]
 /// Types for the `CreateTable` operation.
 pub mod create_table;

+#[cfg(feature = "op_delete_backup")]
 /// Types for the `DeleteBackup` operation.
 pub mod delete_backup;

+#[cfg(feature = "op_delete_item")]
 /// Types for the `DeleteItem` operation.
 pub mod delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 /// Types for the `DeleteResourcePolicy` operation.
 pub mod delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 /// Types for the `DeleteTable` operation.
 pub mod delete_table;

+#[cfg(feature = "op_describe_backup")]
 /// Types for the `DescribeBackup` operation.
 pub mod describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 /// Types for the `DescribeContinuousBackups` operation.
 pub mod describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Types for the `DescribeContributorInsights` operation.
 pub mod describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 /// Types for the `DescribeEndpoints` operation.
 pub mod describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 /// Types for the `DescribeExport` operation.
 pub mod describe_export;

+#[cfg(feature = "op_describe_global_table")]
 /// Types for the `DescribeGlobalTable` operation.
 pub mod describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 /// Types for the `DescribeGlobalTableSettings` operation.
 pub mod describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 /// Types for the `DescribeImport` operation.
 pub mod describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Types for the `DescribeKinesisStreamingDestination` operation.
 pub mod describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 /// Types for the `DescribeLimits` operation.
 pub mod describe_limits;

+#[cfg(feature = "op_describe_table")]
 /// Types for the `DescribeTable` operation.
 pub mod describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 /// Types for the `DescribeTableReplicaAutoScaling` operation.
 pub mod describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 /// Types for the `DescribeTimeToLive` operation.
 pub mod describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 /// Types for the `DisableKinesisStreamingDestination` operation.
 pub mod disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 /// Types for the `EnableKinesisStreamingDestination` operation.
 pub mod enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 /// Types for the `ExecuteStatement` operation.
 pub mod execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 /// Types for the `ExecuteTransaction` operation.
 pub mod execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 /// Types for the `ExportTableToPointInTime` operation.
 pub mod export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 /// Types for the `GetItem` operation.
 pub mod get_item;

+#[cfg(feature = "op_get_resource_policy")]
 /// Types for the `GetResourcePolicy` operation.
 pub mod get_resource_policy;

+#[cfg(feature = "op_import_table")]
 /// Types for the `ImportTable` operation.
 pub mod import_table;

+#[cfg(feature = "op_list_backups")]
 /// Types for the `ListBackups` operation.
 pub mod list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 /// Types for the `ListContributorInsights` operation.
 pub mod list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 /// Types for the `ListExports` operation.
 pub mod list_exports;

+#[cfg(feature = "op_list_global_tables")]
 /// Types for the `ListGlobalTables` operation.
 pub mod list_global_tables;

+#[cfg(feature = "op_list_imports")]
 /// Types for the `ListImports` operation.
 pub mod list_imports;

+#[cfg(feature = "op_list_tables")]
 /// Types for the `ListTables` operation.
 pub mod list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 /// Types for the `ListTagsOfResource` operation.
 pub mod list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 /// Types for the `PutItem` operation.
 pub mod put_item;

+#[cfg(feature = "op_put_resource_policy")]
 /// Types for the `PutResourcePolicy` operation.
 pub mod put_resource_policy;

+#[cfg(feature = "op_query")]
 /// Types for the `Query` operation.
 pub mod query;

+#[cfg(feature = "op_restore_table_from_backup")]
 /// Types for the `RestoreTableFromBackup` operation.
 pub mod restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 /// Types for the `RestoreTableToPointInTime` operation.
 pub mod restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 /// Types for the `Scan` operation.
 pub mod scan;

+#[cfg(feature = "op_search_vectors")]
 /// Types for the `SearchVectors` operation.
 pub mod search_vectors;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 /// Types for the `TransactGetItems` operation.
 pub mod transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 /// Types for the `TransactWriteItems` operation.
 pub mod transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 /// Types for the `UpdateContinuousBackups` operation.
 pub mod update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 /// Types for the `UpdateContributorInsights` operation.
 pub mod update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 /// Types for the `UpdateGlobalTable` operation.
 pub mod update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 /// Types for the `UpdateGlobalTableSettings` operation.
 pub mod update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 /// Types for the `UpdateItem` operation.
 pub mod update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 /// Types for the `UpdateKinesisStreamingDestination` operation.
 pub mod update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 /// Types for the `UpdateTable` operation.
 pub mod update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 /// Types for the `UpdateTableReplicaAutoScaling` operation.
 pub mod update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 /// Types for the `UpdateTimeToLive` operation.
 pub mod update_time_to_live;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,64 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +77,66 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,122 +148,240 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item;

+#[cfg(feature = "op_create_backup")]
 pub(crate) mod shape_create_backup;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_create_global_table;

+#[cfg(feature = "op_create_table")]
 pub(crate) mod shape_create_table;

+#[cfg(feature = "op_delete_backup")]
 pub(crate) mod shape_delete_backup;

+#[cfg(feature = "op_delete_item")]
 pub(crate) mod shape_delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 pub(crate) mod shape_delete_table;

+#[cfg(feature = "op_describe_backup")]
 pub(crate) mod shape_describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 pub(crate) mod shape_describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_describe_export;

+#[cfg(feature = "op_describe_global_table")]
 pub(crate) mod shape_describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 pub(crate) mod shape_describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 pub(crate) mod shape_describe_limits;

+#[cfg(feature = "op_describe_table")]
 pub(crate) mod shape_describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 pub(crate) mod shape_describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 pub(crate) mod shape_describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 pub(crate) mod shape_disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 pub(crate) mod shape_enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 pub(crate) mod shape_get_item;

+#[cfg(feature = "op_get_resource_policy")]
 pub(crate) mod shape_get_resource_policy;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_table;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_list_exports;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_list_global_tables;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_list_imports;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 pub(crate) mod shape_put_item;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy;

+#[cfg(feature = "op_query")]
 pub(crate) mod shape_query;

+#[cfg(feature = "op_restore_table_from_backup")]
 pub(crate) mod shape_restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 pub(crate) mod shape_scan;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_vectors;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 pub(crate) mod shape_update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_update_time_to_live;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -152,552 +390,1803 @@
     }
 }

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub(crate) mod shape_backup_in_use_exception;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub(crate) mod shape_backup_not_found_exception;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_execute_statement_input;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_item_input;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item_input;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_conditional_check_failed_exception;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_continuous_backups_unavailable_exception;

+#[cfg(feature = "op_create_backup")]
 pub(crate) mod shape_create_backup_input;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_create_global_table_input;

+#[cfg(feature = "op_create_table")]
 pub(crate) mod shape_create_table_input;

+#[cfg(feature = "op_delete_backup")]
 pub(crate) mod shape_delete_backup_input;

+#[cfg(feature = "op_delete_item")]
 pub(crate) mod shape_delete_item_input;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy_input;

+#[cfg(feature = "op_delete_table")]
 pub(crate) mod shape_delete_table_input;

+#[cfg(feature = "op_describe_backup")]
 pub(crate) mod shape_describe_backup_input;

+#[cfg(feature = "op_describe_continuous_backups")]
 pub(crate) mod shape_describe_continuous_backups_input;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_describe_contributor_insights_input;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_describe_export_input;

+#[cfg(feature = "op_describe_global_table")]
 pub(crate) mod shape_describe_global_table_input;

+#[cfg(feature = "op_describe_global_table_settings")]
 pub(crate) mod shape_describe_global_table_settings_input;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_describe_import_input;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_describe_kinesis_streaming_destination_input;

+#[cfg(feature = "op_describe_table")]
 pub(crate) mod shape_describe_table_input;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 pub(crate) mod shape_describe_table_replica_auto_scaling_input;

+#[cfg(feature = "op_describe_time_to_live")]
 pub(crate) mod shape_describe_time_to_live_input;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 pub(crate) mod shape_disable_kinesis_streaming_destination_input;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_duplicate_item_exception;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 pub(crate) mod shape_enable_kinesis_streaming_destination_input;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_execute_statement_input;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_execute_transaction_input;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_conflict_exception;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_export_not_found_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_table_to_point_in_time_input;

+#[cfg(feature = "op_get_item")]
 pub(crate) mod shape_get_item_input;

+#[cfg(feature = "op_get_resource_policy")]
 pub(crate) mod shape_get_resource_policy_input;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_global_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_global_table_not_found_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub(crate) mod shape_idempotent_parameter_mismatch_exception;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_conflict_exception;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_import_not_found_exception;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_table_input;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_index_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_internal_server_error;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_invalid_endpoint_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_invalid_export_time_exception;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_invalid_restore_time_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_size_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_list_backups_input;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_list_contributor_insights_input;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_list_exports_input;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_list_global_tables_input;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_list_imports_input;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_list_tables_input;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_list_tags_of_resource_input;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_point_in_time_recovery_unavailable_exception;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub(crate) mod shape_policy_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_provisioned_throughput_exceeded_exception;

+#[cfg(feature = "op_put_item")]
 pub(crate) mod shape_put_item_input;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy_input;

+#[cfg(feature = "op_query")]
 pub(crate) mod shape_query_input;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_replica_already_exists_exception;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub(crate) mod shape_replica_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_replicated_write_conflict_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_request_limit_exceeded;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_resource_in_use_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(feature = "op_restore_table_from_backup")]
 pub(crate) mod shape_restore_table_from_backup_input;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_restore_table_to_point_in_time_input;

+#[cfg(feature = "op_scan")]
 pub(crate) mod shape_scan_input;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_vectors_input;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_table_in_use_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub(crate) mod shape_table_not_found_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_items_input;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_items_input;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_transaction_canceled_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_transaction_conflict_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub(crate) mod shape_transaction_in_progress_exception;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_update_continuous_backups_input;

+#[cfg(feature = "op_update_contributor_insights")]
 pub(crate) mod shape_update_contributor_insights_input;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_update_global_table_input;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_update_global_table_settings_input;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_update_item_input;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_destination_input;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_table_input;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_update_table_replica_auto_scaling_input;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_update_time_to_live_input;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_attribute_map;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_attribute_value;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_attribute_value_update;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_settings_update;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_backup_description;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub(crate) mod shape_backup_details;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_backup_summaries;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_request_map;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_response_map;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_request;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item_request_map;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_cancellation_reason_list;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub(crate) mod shape_condition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_consumed_capacity;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_consumed_capacity_multiple;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_continuous_backups_description;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_contributor_insights_rule_list;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_contributor_insights_summaries;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub(crate) mod shape_enable_kinesis_streaming_configuration;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_endpoints;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub(crate) mod shape_expected_attribute_value;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub(crate) mod shape_export_description;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_export_summaries;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_failure_exception;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_global_secondary_index;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_global_secondary_index_auto_scaling_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_global_secondary_index_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub(crate) mod shape_global_table_description;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_global_table_global_secondary_index_settings_update;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_global_table_list;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_global_table_witness_group_update;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_import_summary_list;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_import_table_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub(crate) mod shape_incremental_export_specification;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_input_format_options;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_metrics;

+#[cfg(any(feature = "op_batch_write_item", feature = "op_transact_write_items"))]
 pub(crate) mod shape_item_collection_metrics_per_table;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_list;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub(crate) mod shape_item_response_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_key;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_key_schema_element;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_keys_and_attributes;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_kinesis_data_stream_destinations;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_local_secondary_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_on_demand_throughput;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_parameterized_statement;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_parti_ql_batch_response;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_point_in_time_recovery_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub(crate) mod shape_replica;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_replica_auto_scaling_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_settings_description_list;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_replica_settings_update;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_replica_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_replication_group_update;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub(crate) mod shape_s3_bucket_source;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_result_list;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_sse_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_stream_specification;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_table_auto_scaling_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_table_creation_parameters;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_description;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_table_name_list;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_tag_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_reason_list;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub(crate) mod shape_time_to_live_description;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_time_to_live_specification;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_item;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_configuration;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_vector_capacity;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_vector_index;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_vector_index_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_warm_throughput;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_write_request;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_archival_summary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_attribute_definitions;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_update;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_backup_summary;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_billing_mode_summary;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_cancellation_reason;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_capacity;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_condition_check;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_contributor_insights_summary;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_create_replica_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_replication_group_member_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_vector_index_action;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_csv_options;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_delete;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_delete_replica_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_replication_group_member_action;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_delete_request;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_vector_index_action;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_endpoint;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_export_summary;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_get;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_description_list;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_global_table;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_table_witness_description_list;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_import_summary;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_key_attribute_map;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_metrics_multiple;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_size_estimate_range;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub(crate) mod shape_item_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_key_schema;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_kinesis_data_stream_destination;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_local_secondary_index_description_list;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_point_in_time_recovery_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput_description;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_put;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_put_request;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_auto_scaling_description_list;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_description_list;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_update;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_replica_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_settings_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_restore_summary;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_result_item;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_search_schema_element;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_secondary_indexes_capacity_map;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_source_table_details;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_source_table_feature_details;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_sse_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_class_summary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_warm_throughput_description;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_reason;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_replication_group_member_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_attribute_definition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_index_description_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_vector_indexes_capacity_map;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_write_requests;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_attribute_name_list;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_settings_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_target_tracking_scaling_policy_configuration_update;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_error;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_binary_set_attribute_value;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_expression_attribute_name_map;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_global_secondary_index_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_global_secondary_indexes;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_table_witness_description;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_key_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_list_attribute_value;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_local_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_local_secondary_indexes;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_map_attribute_value;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_number_set_attribute_value;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_on_demand_throughput_override;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput_override;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_description;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_replica_global_secondary_index;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_global_secondary_index_settings_description_list;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_replica_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_string_set_attribute_value;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_index_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_vector_index_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_vector_indexes;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_description_list;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_csv_header_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_global_secondary_index_info;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_warm_throughput_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_local_secondary_index_info;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_description_list;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_global_secondary_index_description_list;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_global_secondary_index_settings_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_search_schema;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_vector_index_info;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_non_key_attribute_name_list;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_put_item_input_attribute_map;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_global_secondary_index_description;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_target_tracking_scaling_policy_configuration_description;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) fn describe_endpoints_output_output_correct_errors(
     mut builder: crate::operation::describe_endpoints::builders::DescribeEndpointsOutputBuilder,
 ) -> crate::operation::describe_endpoints::builders::DescribeEndpointsOutputBuilder {
@@ -8,6 +9,7 @@
     builder
 }

+#[cfg(feature = "op_describe_import")]
 pub(crate) fn describe_import_output_output_correct_errors(
     mut builder: crate::operation::describe_import::builders::DescribeImportOutputBuilder,
 ) -> crate::operation::describe_import::builders::DescribeImportOutputBuilder {
@@ -20,6 +22,7 @@
     builder
 }

+#[cfg(feature = "op_import_table")]
 pub(crate) fn import_table_output_output_correct_errors(
     mut builder: crate::operation::import_table::builders::ImportTableOutputBuilder,
 ) -> crate::operation::import_table::builders::ImportTableOutputBuilder {
@@ -32,6 +35,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub(crate) fn backup_details_correct_errors(
     mut builder: crate::types::builders::BackupDetailsBuilder,
 ) -> crate::types::builders::BackupDetailsBuilder {
@@ -53,6 +61,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) fn continuous_backups_description_correct_errors(
     mut builder: crate::types::builders::ContinuousBackupsDescriptionBuilder,
 ) -> crate::types::builders::ContinuousBackupsDescriptionBuilder {
@@ -62,6 +71,7 @@
     builder
 }

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) fn time_to_live_specification_correct_errors(
     mut builder: crate::types::builders::TimeToLiveSpecificationBuilder,
 ) -> crate::types::builders::TimeToLiveSpecificationBuilder {
@@ -74,6 +84,7 @@
     builder
 }

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) fn endpoint_correct_errors(
     mut builder: crate::types::builders::EndpointBuilder,
 ) -> crate::types::builders::EndpointBuilder {
@@ -86,6 +97,7 @@
     builder
 }

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) fn keys_and_attributes_correct_errors(
     mut builder: crate::types::builders::KeysAndAttributesBuilder,
 ) -> crate::types::builders::KeysAndAttributesBuilder {
@@ -95,6 +107,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) fn replica_settings_description_correct_errors(
     mut builder: crate::types::builders::ReplicaSettingsDescriptionBuilder,
 ) -> crate::types::builders::ReplicaSettingsDescriptionBuilder {
@@ -104,6 +120,14 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn restore_summary_correct_errors(
     mut builder: crate::types::builders::RestoreSummaryBuilder,
 ) -> crate::types::builders::RestoreSummaryBuilder {
@@ -116,6 +140,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub(crate) fn s3_bucket_source_correct_errors(
     mut builder: crate::types::builders::S3BucketSourceBuilder,
 ) -> crate::types::builders::S3BucketSourceBuilder {
@@ -125,6 +154,7 @@
     builder
 }

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) fn source_table_details_correct_errors(
     mut builder: crate::types::builders::SourceTableDetailsBuilder,
 ) -> crate::types::builders::SourceTableDetailsBuilder {
@@ -151,6 +181,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn stream_specification_correct_errors(
     mut builder: crate::types::builders::StreamSpecificationBuilder,
 ) -> crate::types::builders::StreamSpecificationBuilder {
@@ -160,6 +200,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) fn table_creation_parameters_correct_errors(
     mut builder: crate::types::builders::TableCreationParametersBuilder,
 ) -> crate::types::builders::TableCreationParametersBuilder {
@@ -175,6 +216,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
@@ -187,6 +233,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn attribute_definition_correct_errors(
     mut builder: crate::types::builders::AttributeDefinitionBuilder,
 ) -> crate::types::builders::AttributeDefinitionBuilder {
@@ -199,6 +255,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn key_schema_element_correct_errors(
     mut builder: crate::types::builders::KeySchemaElementBuilder,
 ) -> crate::types::builders::KeySchemaElementBuilder {
@@ -211,6 +279,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn provisioned_throughput_correct_errors(
     mut builder: crate::types::builders::ProvisionedThroughputBuilder,
 ) -> crate::types::builders::ProvisionedThroughputBuilder {
@@ -223,6 +301,7 @@
     builder
 }

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) fn delete_request_correct_errors(
     mut builder: crate::types::builders::DeleteRequestBuilder,
 ) -> crate::types::builders::DeleteRequestBuilder {
@@ -232,6 +311,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) fn global_secondary_index_correct_errors(
     mut builder: crate::types::builders::GlobalSecondaryIndexBuilder,
 ) -> crate::types::builders::GlobalSecondaryIndexBuilder {
@@ -250,6 +336,7 @@
     builder
 }

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) fn put_request_correct_errors(
     mut builder: crate::types::builders::PutRequestBuilder,
 ) -> crate::types::builders::PutRequestBuilder {
@@ -259,6 +346,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) fn replica_global_secondary_index_settings_description_correct_errors(
     mut builder: crate::types::builders::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder,
 ) -> crate::types::builders::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder {
@@ -268,6 +359,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn vector_attribute_definition_correct_errors(
     mut builder: crate::types::builders::VectorAttributeDefinitionBuilder,
 ) -> crate::types::builders::VectorAttributeDefinitionBuilder {
@@ -277,6 +380,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) fn vector_index_correct_errors(
     mut builder: crate::types::builders::VectorIndexBuilder,
 ) -> crate::types::builders::VectorIndexBuilder {
@@ -306,6 +416,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn search_schema_element_correct_errors(
     mut builder: crate::types::builders::SearchSchemaElementBuilder,
 ) -> crate::types::builders::SearchSchemaElementBuilder {
@@ -318,6 +440,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) fn auto_scaling_target_tracking_scaling_policy_configuration_description_correct_errors(
     mut builder: crate::types::builders::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder,
 ) -> crate::types::builders::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,678 +1,2350 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_consumed_capacity::ReturnConsumedCapacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_item_collection_metrics::ReturnItemCollectionMetrics;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub use crate::types::_backup_details::BackupDetails;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_description::GlobalTableDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode::BillingMode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput::ProvisionedThroughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_specification::StreamSpecification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_specification::SseSpecification;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class::TableClass;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_warm_throughput::WarmThroughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput::OnDemandThroughput;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_settings_replication_mode::GlobalTableSettingsReplicationMode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_description::TableDescription;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_backup_description::BackupDescription;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 pub use crate::types::_conditional_operator::ConditionalOperator;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_return_value::ReturnValue;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_values_on_condition_check_failure::ReturnValuesOnConditionCheckFailure;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_consumed_capacity::ConsumedCapacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_item_collection_metrics::ItemCollectionMetrics;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_description::ContinuousBackupsDescription;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 pub use crate::types::_contributor_insights_status::ContributorInsightsStatus;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub use crate::types::_failure_exception::FailureException;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 pub use crate::types::_contributor_insights_mode::ContributorInsightsMode;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_description::ExportDescription;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_import_table_description::ImportTableDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_auto_scaling_description::TableAutoScalingDescription;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_description::TimeToLiveDescription;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub use crate::types::_enable_kinesis_streaming_configuration::EnableKinesisStreamingConfiguration;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 pub use crate::types::_destination_status::DestinationStatus;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_s3_sse_algorithm::S3SseAlgorithm;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_format::ExportFormat;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 pub use crate::types::_export_type::ExportType;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_incremental_export_specification::IncrementalExportSpecification;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_s3_bucket_source::S3BucketSource;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_input_format::InputFormat;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_format_options::InputFormatOptions;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_compression_type::InputCompressionType;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_table_creation_parameters::TableCreationParameters;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_type_filter::BackupTypeFilter;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_select::Select;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_vector_capacity::VectorCapacity;

+#[cfg(feature = "op_update_continuous_backups")]
 pub use crate::types::_point_in_time_recovery_specification::PointInTimeRecoverySpecification;

+#[cfg(feature = "op_update_contributor_insights")]
 pub use crate::types::_contributor_insights_action::ContributorInsightsAction;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_update::AutoScalingSettingsUpdate;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub use crate::types::_update_kinesis_streaming_configuration::UpdateKinesisStreamingConfiguration;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_multi_region_consistency::MultiRegionConsistency;

+#[cfg(feature = "op_update_time_to_live")]
 pub use crate::types::_time_to_live_specification::TimeToLiveSpecification;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_request::BatchStatementRequest;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_response::BatchStatementResponse;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_throttling_reason::ThrottlingReason;

+#[cfg(feature = "op_batch_get_item")]
 pub use crate::types::_keys_and_attributes::KeysAndAttributes;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 pub use crate::types::_backup_status::BackupStatus;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 pub use crate::types::_backup_type::BackupType;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub use crate::types::_replica::Replica;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_status::GlobalTableStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_attribute_definition::AttributeDefinition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_schema_element::KeySchemaElement;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_local_secondary_index::LocalSecondaryIndex;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_global_secondary_index::GlobalSecondaryIndex;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_view_type::StreamViewType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_type::SseType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_vector_index::VectorIndex;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_status::TableStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_description::ProvisionedThroughputDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode_summary::BillingModeSummary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_restore_summary::RestoreSummary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_description::SseDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_archival_summary::ArchivalSummary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class_summary::TableClassSummary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_warm_throughput_description::TableWarmThroughputDescription;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_details::SourceTableDetails;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_feature_details::SourceTableFeatureDetails;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_attribute_value::AttributeValue;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_expected_attribute_value::ExpectedAttributeValue;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_capacity::Capacity;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_status::ContinuousBackupsStatus;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_description::PointInTimeRecoveryDescription;

+#[cfg(feature = "op_describe_endpoints")]
 pub use crate::types::_endpoint::Endpoint;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 pub use crate::types::_export_status::ExportStatus;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_settings_description::ReplicaSettingsDescription;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_import_status::ImportStatus;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub use crate::types::_kinesis_data_stream_destination::KinesisDataStreamDestination;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_status::TimeToLiveStatus;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 pub use crate::types::_approximate_creation_date_time_precision::ApproximateCreationDateTimePrecision;

+#[cfg(feature = "op_execute_transaction")]
 pub use crate::types::_parameterized_statement::ParameterizedStatement;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub use crate::types::_item_response::ItemResponse;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::_cancellation_reason::CancellationReason;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_view_type::ExportViewType;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_csv_options::CsvOptions;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_summary::BackupSummary;

+#[cfg(feature = "op_list_contributor_insights")]
 pub use crate::types::_contributor_insights_summary::ContributorInsightsSummary;

+#[cfg(feature = "op_list_exports")]
 pub use crate::types::_export_summary::ExportSummary;

+#[cfg(feature = "op_list_global_tables")]
 pub use crate::types::_global_table::GlobalTable;

+#[cfg(feature = "op_list_imports")]
 pub use crate::types::_import_summary::ImportSummary;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_condition::Condition;

+#[cfg(feature = "op_search_vectors")]
 pub use crate::types::_search_result_item::SearchResultItem;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_transact_get_item::TransactGetItem;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_transact_write_item::TransactWriteItem;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_replica_update::ReplicaUpdate;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_update::AutoScalingPolicyUpdate;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_global_table_global_secondary_index_settings_update::GlobalTableGlobalSecondaryIndexSettingsUpdate;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_settings_update::ReplicaSettingsUpdate;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_value_update::AttributeValueUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_secondary_index_update::GlobalSecondaryIndexUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replication_group_update::ReplicationGroupUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_table_witness_group_update::GlobalTableWitnessGroupUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_vector_index_update::VectorIndexUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_global_secondary_index_auto_scaling_update::GlobalSecondaryIndexAutoScalingUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_auto_scaling_update::ReplicaAutoScalingUpdate;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error::BatchStatementError;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_write_request::WriteRequest;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_description::ReplicaDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_scalar_attribute_type::ScalarAttributeType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_type::KeyType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection::Projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_attribute_definition::VectorAttributeDefinition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_distance_function::VectorDistanceFunction;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_local_secondary_index_description::LocalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_description::GlobalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_witness_description::GlobalTableWitnessDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_status::SseStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_index_description::VectorIndexDescription;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 pub use crate::types::_comparison_operator::ComparisonOperator;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_status::PointInTimeRecoveryStatus;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_status::ReplicaStatus;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_description::AutoScalingSettingsDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_auto_scaling_description::ReplicaAutoScalingDescription;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_get::Get;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_condition_check::ConditionCheck;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_put::Put;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_delete::Delete;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_update::Update;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_create_replica_action::CreateReplicaAction;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_delete_replica_action::DeleteReplicaAction;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_update::AutoScalingTargetTrackingScalingPolicyConfigurationUpdate;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_action::AttributeAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_global_secondary_index_action::UpdateGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_secondary_index_action::CreateGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_secondary_index_action::DeleteGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_replication_group_member_action::CreateReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_replication_group_member_action::UpdateReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_replication_group_member_action::DeleteReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_table_witness_group_member_action::CreateGlobalTableWitnessGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_table_witness_group_member_action::DeleteGlobalTableWitnessGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_vector_index_action::CreateVectorIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_vector_index_action::DeleteVectorIndexAction;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error_code_enum::BatchStatementErrorCodeEnum;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_put_request::PutRequest;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_delete_request::DeleteRequest;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_override::ProvisionedThroughputOverride;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput_override::OnDemandThroughputOverride;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection_type::ProjectionType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element::SearchSchemaElement;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_index_status::IndexStatus;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_warm_throughput_description::GlobalSecondaryIndexWarmThroughputDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_witness_status::WitnessStatus;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_local_secondary_index_info::LocalSecondaryIndexInfo;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_global_secondary_index_info::GlobalSecondaryIndexInfo;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_vector_index_info::VectorIndexInfo;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_global_secondary_index_settings_description::ReplicaGlobalSecondaryIndexSettingsDescription;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_global_secondary_index_settings_update::ReplicaGlobalSecondaryIndexSettingsUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_update::ReplicaGlobalSecondaryIndexAutoScalingUpdate;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_global_secondary_index_description::ReplicaGlobalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element_type::SearchSchemaElementType;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_description::AutoScalingPolicyDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_description::ReplicaGlobalSecondaryIndexAutoScalingDescription;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replica_global_secondary_index::ReplicaGlobalSecondaryIndex;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_description::AutoScalingTargetTrackingScalingPolicyConfigurationDescription;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 mod _approximate_creation_date_time_precision;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _archival_summary;

+#[cfg(feature = "op_update_item")]
 mod _attribute_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _attribute_value;

+#[cfg(feature = "op_update_item")]
 mod _attribute_value_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_policy_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_policy_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_settings_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_target_tracking_scaling_policy_configuration_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_target_tracking_scaling_policy_configuration_update;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _backup_description;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 mod _backup_details;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 mod _backup_status;

+#[cfg(feature = "op_list_backups")]
 mod _backup_summary;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 mod _backup_type;

+#[cfg(feature = "op_list_backups")]
 mod _backup_type_filter;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_error;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_error_code_enum;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_request;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _billing_mode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _billing_mode_summary;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 mod _cancellation_reason;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _capacity;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 mod _comparison_operator;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 mod _condition;

+#[cfg(feature = "op_transact_write_items")]
 mod _condition_check;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 mod _conditional_operator;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _consumed_capacity;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_description;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_status;

+#[cfg(feature = "op_update_contributor_insights")]
 mod _contributor_insights_action;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 mod _contributor_insights_mode;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 mod _contributor_insights_status;

+#[cfg(feature = "op_list_contributor_insights")]
 mod _contributor_insights_summary;

+#[cfg(feature = "op_update_table")]
 mod _create_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 mod _create_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 mod _create_replica_action;

+#[cfg(feature = "op_update_table")]
 mod _create_replication_group_member_action;

+#[cfg(feature = "op_update_table")]
 mod _create_vector_index_action;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _csv_options;

+#[cfg(feature = "op_transact_write_items")]
 mod _delete;

+#[cfg(feature = "op_update_table")]
 mod _delete_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 mod _delete_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 mod _delete_replica_action;

+#[cfg(feature = "op_update_table")]
 mod _delete_replication_group_member_action;

+#[cfg(feature = "op_batch_write_item")]
 mod _delete_request;

+#[cfg(feature = "op_update_table")]
 mod _delete_vector_index_action;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 mod _destination_status;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 mod _enable_kinesis_streaming_configuration;

+#[cfg(feature = "op_describe_endpoints")]
 mod _endpoint;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 mod _expected_attribute_value;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_format;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 mod _export_status;

+#[cfg(feature = "op_list_exports")]
 mod _export_summary;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 mod _export_type;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_view_type;

+#[cfg(feature = "op_describe_contributor_insights")]
 mod _failure_exception;

+#[cfg(feature = "op_transact_get_items")]
 mod _get;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _global_secondary_index;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _global_secondary_index_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _global_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _global_secondary_index_info;

+#[cfg(feature = "op_update_table")]
 mod _global_secondary_index_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _global_secondary_index_warm_throughput_description;

+#[cfg(feature = "op_list_global_tables")]
 mod _global_table;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 mod _global_table_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _global_table_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _global_table_settings_replication_mode;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 mod _global_table_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _global_table_witness_description;

+#[cfg(feature = "op_update_table")]
 mod _global_table_witness_group_update;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _import_status;

+#[cfg(feature = "op_list_imports")]
 mod _import_summary;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _import_table_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _incremental_export_specification;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _index_status;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _input_compression_type;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _input_format;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _input_format_options;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _item_collection_metrics;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 mod _item_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _key_schema_element;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _key_type;

+#[cfg(feature = "op_batch_get_item")]
 mod _keys_and_attributes;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 mod _kinesis_data_stream_destination;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _local_secondary_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _local_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _local_secondary_index_info;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _multi_region_consistency;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _on_demand_throughput;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _on_demand_throughput_override;

+#[cfg(feature = "op_execute_transaction")]
 mod _parameterized_statement;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _point_in_time_recovery_description;

+#[cfg(feature = "op_update_continuous_backups")]
 mod _point_in_time_recovery_specification;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _point_in_time_recovery_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _projection_type;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput_override;

+#[cfg(feature = "op_transact_write_items")]
 mod _put;

+#[cfg(feature = "op_batch_write_item")]
 mod _put_request;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 mod _replica;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_auto_scaling_description;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _replica_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _replica_description;

+#[cfg(feature = "op_update_table")]
 mod _replica_global_secondary_index;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_global_secondary_index_auto_scaling_description;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _replica_global_secondary_index_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _replica_global_secondary_index_description;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 mod _replica_global_secondary_index_settings_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _replica_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 mod _replica_settings_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _replica_settings_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_status;

+#[cfg(feature = "op_update_global_table")]
 mod _replica_update;

+#[cfg(feature = "op_update_table")]
 mod _replication_group_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _restore_summary;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_consumed_capacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_item_collection_metrics;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 mod _return_value;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_values_on_condition_check_failure;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _s3_bucket_source;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _s3_sse_algorithm;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _scalar_attribute_type;

+#[cfg(feature = "op_search_vectors")]
 mod _search_result_item;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _search_schema_element;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _search_schema_element_type;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 mod _select;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _source_table_details;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _source_table_feature_details;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_type;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _stream_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _stream_view_type;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _table_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _table_class;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _table_class_summary;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _table_creation_parameters;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _table_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _table_status;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _table_warm_throughput_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _throttling_reason;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 mod _time_to_live_description;

+#[cfg(feature = "op_update_time_to_live")]
 mod _time_to_live_specification;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 mod _time_to_live_status;

+#[cfg(feature = "op_transact_get_items")]
 mod _transact_get_item;

+#[cfg(feature = "op_transact_write_items")]
 mod _transact_write_item;

+#[cfg(feature = "op_transact_write_items")]
 mod _update;

+#[cfg(feature = "op_update_table")]
 mod _update_global_secondary_index_action;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 mod _update_kinesis_streaming_configuration;

+#[cfg(feature = "op_update_table")]
 mod _update_replication_group_member_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _vector_capacity;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_distance_function;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _vector_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _vector_index_info;

+#[cfg(feature = "op_update_table")]
 mod _vector_index_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _warm_throughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _witness_status;

+#[cfg(feature = "op_batch_write_item")]
 mod _write_request;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,246 +1,757 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub use crate::types::_backup_details::BackupDetailsBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_description::GlobalTableDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput::ProvisionedThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_specification::StreamSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_specification::SseSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_warm_throughput::WarmThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput::OnDemandThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_description::TableDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_backup_description::BackupDescriptionBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_consumed_capacity::ConsumedCapacityBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_item_collection_metrics::ItemCollectionMetricsBuilder;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_description::ContinuousBackupsDescriptionBuilder;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub use crate::types::_failure_exception::FailureExceptionBuilder;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_description::ExportDescriptionBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_import_table_description::ImportTableDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_auto_scaling_description::TableAutoScalingDescriptionBuilder;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_description::TimeToLiveDescriptionBuilder;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub use crate::types::_enable_kinesis_streaming_configuration::EnableKinesisStreamingConfigurationBuilder;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_incremental_export_specification::IncrementalExportSpecificationBuilder;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_s3_bucket_source::S3BucketSourceBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_format_options::InputFormatOptionsBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_table_creation_parameters::TableCreationParametersBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_vector_capacity::VectorCapacityBuilder;

+#[cfg(feature = "op_update_continuous_backups")]
 pub use crate::types::_point_in_time_recovery_specification::PointInTimeRecoverySpecificationBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_update::AutoScalingSettingsUpdateBuilder;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub use crate::types::_update_kinesis_streaming_configuration::UpdateKinesisStreamingConfigurationBuilder;

+#[cfg(feature = "op_update_time_to_live")]
 pub use crate::types::_time_to_live_specification::TimeToLiveSpecificationBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_request::BatchStatementRequestBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_response::BatchStatementResponseBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_throttling_reason::ThrottlingReasonBuilder;

+#[cfg(feature = "op_batch_get_item")]
 pub use crate::types::_keys_and_attributes::KeysAndAttributesBuilder;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub use crate::types::_replica::ReplicaBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_attribute_definition::AttributeDefinitionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_schema_element::KeySchemaElementBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_local_secondary_index::LocalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_global_secondary_index::GlobalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_vector_index::VectorIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_description::ProvisionedThroughputDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode_summary::BillingModeSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_restore_summary::RestoreSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_description::SseDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_archival_summary::ArchivalSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class_summary::TableClassSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_warm_throughput_description::TableWarmThroughputDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_details::SourceTableDetailsBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_feature_details::SourceTableFeatureDetailsBuilder;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_expected_attribute_value::ExpectedAttributeValueBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_capacity::CapacityBuilder;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_description::PointInTimeRecoveryDescriptionBuilder;

+#[cfg(feature = "op_describe_endpoints")]
 pub use crate::types::_endpoint::EndpointBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_settings_description::ReplicaSettingsDescriptionBuilder;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub use crate::types::_kinesis_data_stream_destination::KinesisDataStreamDestinationBuilder;

+#[cfg(feature = "op_execute_transaction")]
 pub use crate::types::_parameterized_statement::ParameterizedStatementBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub use crate::types::_item_response::ItemResponseBuilder;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::_cancellation_reason::CancellationReasonBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_csv_options::CsvOptionsBuilder;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_summary::BackupSummaryBuilder;

+#[cfg(feature = "op_list_contributor_insights")]
 pub use crate::types::_contributor_insights_summary::ContributorInsightsSummaryBuilder;

+#[cfg(feature = "op_list_exports")]
 pub use crate::types::_export_summary::ExportSummaryBuilder;

+#[cfg(feature = "op_list_global_tables")]
 pub use crate::types::_global_table::GlobalTableBuilder;

+#[cfg(feature = "op_list_imports")]
 pub use crate::types::_import_summary::ImportSummaryBuilder;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_condition::ConditionBuilder;

+#[cfg(feature = "op_search_vectors")]
 pub use crate::types::_search_result_item::SearchResultItemBuilder;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_transact_get_item::TransactGetItemBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_transact_write_item::TransactWriteItemBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_replica_update::ReplicaUpdateBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_update::AutoScalingPolicyUpdateBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_global_table_global_secondary_index_settings_update::GlobalTableGlobalSecondaryIndexSettingsUpdateBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_settings_update::ReplicaSettingsUpdateBuilder;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_value_update::AttributeValueUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_secondary_index_update::GlobalSecondaryIndexUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replication_group_update::ReplicationGroupUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_table_witness_group_update::GlobalTableWitnessGroupUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_vector_index_update::VectorIndexUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_global_secondary_index_auto_scaling_update::GlobalSecondaryIndexAutoScalingUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_auto_scaling_update::ReplicaAutoScalingUpdateBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error::BatchStatementErrorBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_write_request::WriteRequestBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_description::ReplicaDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection::ProjectionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_attribute_definition::VectorAttributeDefinitionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_local_secondary_index_description::LocalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_description::GlobalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_witness_description::GlobalTableWitnessDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_index_description::VectorIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_description::AutoScalingSettingsDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_auto_scaling_description::ReplicaAutoScalingDescriptionBuilder;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_get::GetBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_condition_check::ConditionCheckBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_put::PutBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_delete::DeleteBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_update::UpdateBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_create_replica_action::CreateReplicaActionBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_delete_replica_action::DeleteReplicaActionBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_update::AutoScalingTargetTrackingScalingPolicyConfigurationUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_global_secondary_index_action::UpdateGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_secondary_index_action::CreateGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_secondary_index_action::DeleteGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_replication_group_member_action::CreateReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_replication_group_member_action::UpdateReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_replication_group_member_action::DeleteReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_table_witness_group_member_action::CreateGlobalTableWitnessGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_table_witness_group_member_action::DeleteGlobalTableWitnessGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_vector_index_action::CreateVectorIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_vector_index_action::DeleteVectorIndexActionBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_put_request::PutRequestBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_delete_request::DeleteRequestBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_override::ProvisionedThroughputOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput_override::OnDemandThroughputOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element::SearchSchemaElementBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_warm_throughput_description::GlobalSecondaryIndexWarmThroughputDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_local_secondary_index_info::LocalSecondaryIndexInfoBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_global_secondary_index_info::GlobalSecondaryIndexInfoBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_vector_index_info::VectorIndexInfoBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_global_secondary_index_settings_description::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_global_secondary_index_settings_update::ReplicaGlobalSecondaryIndexSettingsUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_update::ReplicaGlobalSecondaryIndexAutoScalingUpdateBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_global_secondary_index_description::ReplicaGlobalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_description::AutoScalingPolicyDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_description::ReplicaGlobalSecondaryIndexAutoScalingDescriptionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replica_global_secondary_index::ReplicaGlobalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_description::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,142 +1,760 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_internal_server_error::InternalServerError;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_request_limit_exceeded::RequestLimitExceeded;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_invalid_endpoint_exception::InvalidEndpointException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_provisioned_throughput_exceeded_exception::ProvisionedThroughputExceededException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_item_collection_size_limit_exceeded_exception::ItemCollectionSizeLimitExceededException;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_replicated_write_conflict_exception::ReplicatedWriteConflictException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_in_use_exception::BackupInUseException;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub use crate::types::error::_continuous_backups_unavailable_exception::ContinuousBackupsUnavailableException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_in_use_exception::TableInUseException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::error::_table_not_found_exception::TableNotFoundException;

+#[cfg(feature = "op_create_global_table")]
 pub use crate::types::error::_global_table_already_exists_exception::GlobalTableAlreadyExistsException;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_in_use_exception::ResourceInUseException;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_not_found_exception::BackupNotFoundException;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_conditional_check_failed_exception::ConditionalCheckFailedException;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_transaction_conflict_exception::TransactionConflictException;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub use crate::types::error::_policy_not_found_exception::PolicyNotFoundException;

+#[cfg(feature = "op_describe_export")]
 pub use crate::types::error::_export_not_found_exception::ExportNotFoundException;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::error::_global_table_not_found_exception::GlobalTableNotFoundException;

+#[cfg(feature = "op_describe_import")]
 pub use crate::types::error::_import_not_found_exception::ImportNotFoundException;

+#[cfg(feature = "op_execute_statement")]
 pub use crate::types::error::_duplicate_item_exception::DuplicateItemException;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_idempotent_parameter_mismatch_exception::IdempotentParameterMismatchException;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::error::_transaction_canceled_exception::TransactionCanceledException;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_transaction_in_progress_exception::TransactionInProgressException;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_export_conflict_exception::ExportConflictException;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_invalid_export_time_exception::InvalidExportTimeException;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_point_in_time_recovery_unavailable_exception::PointInTimeRecoveryUnavailableException;

+#[cfg(feature = "op_import_table")]
 pub use crate::types::error::_import_conflict_exception::ImportConflictException;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_already_exists_exception::TableAlreadyExistsException;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub use crate::types::error::_invalid_restore_time_exception::InvalidRestoreTimeException;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::error::_replica_already_exists_exception::ReplicaAlreadyExistsException;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub use crate::types::error::_replica_not_found_exception::ReplicaNotFoundException;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::error::_index_not_found_exception::IndexNotFoundException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 mod _backup_in_use_exception;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 mod _backup_not_found_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _conditional_check_failed_exception;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_unavailable_exception;

+#[cfg(feature = "op_execute_statement")]
 mod _duplicate_item_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod _export_conflict_exception;

+#[cfg(feature = "op_describe_export")]
 mod _export_not_found_exception;

+#[cfg(feature = "op_create_global_table")]
 mod _global_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 mod _global_table_not_found_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 mod _idempotent_parameter_mismatch_exception;

+#[cfg(feature = "op_import_table")]
 mod _import_conflict_exception;

+#[cfg(feature = "op_describe_import")]
 mod _import_not_found_exception;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _index_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _internal_server_error;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 mod _invalid_endpoint_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod _invalid_export_time_exception;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 mod _invalid_restore_time_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _item_collection_size_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _point_in_time_recovery_unavailable_exception;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 mod _policy_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _provisioned_throughput_exceeded_exception;

+#[cfg(feature = "op_update_global_table")]
 mod _replica_already_exists_exception;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 mod _replica_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _replicated_write_conflict_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _request_limit_exceeded;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _resource_in_use_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _table_already_exists_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _table_in_use_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 mod _table_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _throttling_exception;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 mod _transaction_canceled_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _transaction_conflict_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 mod _transaction_in_progress_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,70 +1,379 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_internal_server_error::InternalServerErrorBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_request_limit_exceeded::RequestLimitExceededBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_invalid_endpoint_exception::InvalidEndpointExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_provisioned_throughput_exceeded_exception::ProvisionedThroughputExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_item_collection_size_limit_exceeded_exception::ItemCollectionSizeLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_replicated_write_conflict_exception::ReplicatedWriteConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_in_use_exception::BackupInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub use crate::types::error::_continuous_backups_unavailable_exception::ContinuousBackupsUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_in_use_exception::TableInUseExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::error::_table_not_found_exception::TableNotFoundExceptionBuilder;

+#[cfg(feature = "op_create_global_table")]
 pub use crate::types::error::_global_table_already_exists_exception::GlobalTableAlreadyExistsExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_in_use_exception::ResourceInUseExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_not_found_exception::BackupNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_conditional_check_failed_exception::ConditionalCheckFailedExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_transaction_conflict_exception::TransactionConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub use crate::types::error::_policy_not_found_exception::PolicyNotFoundExceptionBuilder;

+#[cfg(feature = "op_describe_export")]
 pub use crate::types::error::_export_not_found_exception::ExportNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::error::_global_table_not_found_exception::GlobalTableNotFoundExceptionBuilder;

+#[cfg(feature = "op_describe_import")]
 pub use crate::types::error::_import_not_found_exception::ImportNotFoundExceptionBuilder;

+#[cfg(feature = "op_execute_statement")]
 pub use crate::types::error::_duplicate_item_exception::DuplicateItemExceptionBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_idempotent_parameter_mismatch_exception::IdempotentParameterMismatchExceptionBuilder;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::error::_transaction_canceled_exception::TransactionCanceledExceptionBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_transaction_in_progress_exception::TransactionInProgressExceptionBuilder;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_export_conflict_exception::ExportConflictExceptionBuilder;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_invalid_export_time_exception::InvalidExportTimeExceptionBuilder;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_point_in_time_recovery_unavailable_exception::PointInTimeRecoveryUnavailableExceptionBuilder;

+#[cfg(feature = "op_import_table")]
 pub use crate::types::error::_import_conflict_exception::ImportConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_already_exists_exception::TableAlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub use crate::types::error::_invalid_restore_time_exception::InvalidRestoreTimeExceptionBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::error::_replica_already_exists_exception::ReplicaAlreadyExistsExceptionBuilder;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub use crate::types::error::_replica_not_found_exception::ReplicaNotFoundExceptionBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::error::_index_not_found_exception::IndexNotFoundExceptionBuilder;
```

### `src/waiters.rs`

```diff
diff --git a/src/waiters.rs b/src/waiters.rs
--- a/src/waiters.rs
+++ b/src/waiters.rs
@@ -1,23 +1,36 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Supporting types for the `contributor_insights_enabled` waiter.
 pub mod contributor_insights_enabled;

+#[cfg(feature = "op_describe_export")]
 /// Supporting types for the `export_completed` waiter.
 pub mod export_completed;

+#[cfg(feature = "op_describe_import")]
 /// Supporting types for the `import_completed` waiter.
 pub mod import_completed;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Supporting types for the `kinesis_streaming_destination_active` waiter.
 pub mod kinesis_streaming_destination_active;

+#[cfg(feature = "op_describe_table")]
 /// Supporting types for the `table_exists` waiter.
 pub mod table_exists;

+#[cfg(feature = "op_describe_table")]
 /// Supporting types for the `table_not_exists` waiter.
 pub mod table_not_exists;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table"
+))]
 #[allow(clippy::needless_lifetimes)]
 #[allow(clippy::let_and_return)]
 pub(crate) mod matchers;
```

### `src/waiters/matchers.rs`

```diff
diff --git a/src/waiters/matchers.rs b/src/waiters/matchers.rs
--- a/src/waiters/matchers.rs
+++ b/src/waiters/matchers.rs
@@ -1,5 +1,6 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Matcher union: {"output":{"path":"ContributorInsightsStatus","expected":"ENABLED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_contributor_insights_57787899eaa02d958(
     _result: ::std::result::Result<
@@ -26,6 +27,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Matcher union: {"output":{"path":"ContributorInsightsStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_contributor_insights_5ba948784ca4cb322(
     _result: ::std::result::Result<
@@ -52,6 +54,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_export")]
 /// Matcher union: {"output":{"path":"ExportDescription.ExportStatus","expected":"COMPLETED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_export_a4219f96bc64309c4(
     _result: ::std::result::Result<
@@ -79,6 +82,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_export")]
 /// Matcher union: {"output":{"path":"ExportDescription.ExportStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_export_8d899fd0681b891e9(
     _result: ::std::result::Result<
@@ -106,6 +110,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"COMPLETED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_6175a829c57972dc3(
     _result: ::std::result::Result<
@@ -133,6 +138,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_ba4301a7fe05a6956(
     _result: ::std::result::Result<
@@ -160,6 +166,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"CANCELLED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_b4c5c86bd60d42041(
     _result: ::std::result::Result<
@@ -187,6 +194,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Matcher union: {"output":{"path":"KinesisDataStreamDestinations[].DestinationStatus","expected":"ACTIVE","comparator":"anyStringEquals"}}
 pub(crate) fn match_describe_kinesis_streaming_destination_56e18114fb2c2cf5a(
     _result: ::std::result::Result<
@@ -228,6 +236,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Matcher union: {"output":{"path":"length(KinesisDataStreamDestinations) > `0`  && length(KinesisDataStreamDestinations[?DestinationStatus == 'DISABLED' || DestinationStatus == 'ENABLE_FAILED']) ==  length(KinesisDataStreamDestinations)","expected":"true","comparator":"booleanEquals"}}
 pub(crate) fn match_describe_kinesis_streaming_destination_ce975c8fb2b65f98f(
     _result: ::std::result::Result<
@@ -282,6 +291,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_table")]
 /// Matcher union: {"output":{"path":"Table.TableStatus","expected":"ACTIVE","comparator":"stringEquals"}}
 pub(crate) fn match_describe_table_0429b99996ae6dab6(
     _result: ::std::result::Result<
@@ -309,6 +319,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_table")]
 /// Matcher union: {"errorType":"ResourceNotFoundException"}
 pub(crate) fn match_describe_table_1cce2c05524fb92d4(
     _result: ::std::result::Result<
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
@@ -90,51 +79,41 @@
 version = "0.5.1"

 [dev-dependencies.aws-config]
-path = "../aws-config"
 features = ["test-util"]
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

 [dev-dependencies.aws-smithy-xml]
-path = "../aws-smithy-xml"
 version = "0.62.0"

 [dev-dependencies.criterion]
@@ -167,6 +146,64 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_batch_execute_statement = []
+op_batch_get_item = []
+op_batch_write_item = []
+op_create_backup = []
+op_create_global_table = []
+op_create_table = []
+op_delete_backup = []
+op_delete_item = []
+op_delete_resource_policy = []
+op_delete_table = []
+op_describe_backup = []
+op_describe_continuous_backups = []
+op_describe_contributor_insights = []
+op_describe_endpoints = []
+op_describe_export = []
+op_describe_global_table = []
+op_describe_global_table_settings = []
+op_describe_import = []
+op_describe_kinesis_streaming_destination = []
+op_describe_limits = []
+op_describe_table = []
+op_describe_table_replica_auto_scaling = []
+op_describe_time_to_live = []
+op_disable_kinesis_streaming_destination = []
+op_enable_kinesis_streaming_destination = []
+op_execute_statement = []
+op_execute_transaction = []
+op_export_table_to_point_in_time = []
+op_get_item = []
+op_get_resource_policy = []
+op_import_table = []
+op_list_backups = []
+op_list_contributor_insights = []
+op_list_exports = []
+op_list_global_tables = []
+op_list_imports = []
+op_list_tables = []
+op_list_tags_of_resource = []
+op_put_item = []
+op_put_resource_policy = []
+op_query = []
+op_restore_table_from_backup = []
+op_restore_table_to_point_in_time = []
+op_scan = []
+op_search_vectors = []
+op_tag_resource = []
+op_transact_get_items = []
+op_transact_write_items = []
+op_untag_resource = []
+op_update_continuous_backups = []
+op_update_contributor_insights = []
+op_update_global_table = []
+op_update_global_table_settings = []
+op_update_item = []
+op_update_kinesis_streaming_destination = []
+op_update_table = []
+op_update_table_replica_auto_scaling = []
+op_update_time_to_live = []

 [hints]
 mostly-unused = true
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -140,35 +140,45 @@
 /// Import this trait to get `wait_until` methods on the client.
 ///
 pub trait Waiters {
+    #[cfg(feature = "op_describe_contributor_insights")]
     /// Wait for `contributor_insights_enabled`
     fn wait_until_contributor_insights_enabled(
         &self,
     ) -> crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder;
+    #[cfg(feature = "op_describe_export")]
     /// Wait for `export_completed`
     fn wait_until_export_completed(&self) -> crate::waiters::export_completed::ExportCompletedFluentBuilder;
+    #[cfg(feature = "op_describe_import")]
     /// Wait for `import_completed`
     fn wait_until_import_completed(&self) -> crate::waiters::import_completed::ImportCompletedFluentBuilder;
+    #[cfg(feature = "op_describe_kinesis_streaming_destination")]
     /// Wait for `kinesis_streaming_destination_active`
     fn wait_until_kinesis_streaming_destination_active(
         &self,
     ) -> crate::waiters::kinesis_streaming_destination_active::KinesisStreamingDestinationActiveFluentBuilder;
+    #[cfg(feature = "op_describe_table")]
     /// Wait for `table_exists`
     fn wait_until_table_exists(&self) -> crate::waiters::table_exists::TableExistsFluentBuilder;
+    #[cfg(feature = "op_describe_table")]
     /// Wait for `table_not_exists`
     fn wait_until_table_not_exists(&self) -> crate::waiters::table_not_exists::TableNotExistsFluentBuilder;
 }
 impl Waiters for Client {
+    #[cfg(feature = "op_describe_contributor_insights")]
     fn wait_until_contributor_insights_enabled(
         &self,
     ) -> crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder {
         crate::waiters::contributor_insights_enabled::ContributorInsightsEnabledFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_export")]
     fn wait_until_export_completed(&self) -> crate::waiters::export_completed::ExportCompletedFluentBuilder {
         crate::waiters::export_completed::ExportCompletedFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_import")]
     fn wait_until_import_completed(&self) -> crate::waiters::import_completed::ImportCompletedFluentBuilder {
         crate::waiters::import_completed::ImportCompletedFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_kinesis_streaming_destination")]
     fn wait_until_kinesis_streaming_destination_active(
         &self,
     ) -> crate::waiters::kinesis_streaming_destination_active::KinesisStreamingDestinationActiveFluentBuilder {
@@ -176,9 +186,11 @@
             self.handle.clone(),
         )
     }
+    #[cfg(feature = "op_describe_table")]
     fn wait_until_table_exists(&self) -> crate::waiters::table_exists::TableExistsFluentBuilder {
         crate::waiters::table_exists::TableExistsFluentBuilder::new(self.handle.clone())
     }
+    #[cfg(feature = "op_describe_table")]
     fn wait_until_table_not_exists(&self) -> crate::waiters::table_not_exists::TableNotExistsFluentBuilder {
         crate::waiters::table_not_exists::TableNotExistsFluentBuilder::new(self.handle.clone())
     }
@@ -200,16 +212,22 @@
     }
 }

+#[cfg(feature = "op_batch_execute_statement")]
 mod batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 mod batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 mod batch_write_item;

+#[cfg(feature = "op_create_backup")]
 mod create_backup;

+#[cfg(feature = "op_create_global_table")]
 mod create_global_table;

+#[cfg(feature = "op_create_table")]
 mod create_table;

 /// Operation customization and supporting types.
@@ -239,106 +257,158 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_backup")]
 mod delete_backup;

+#[cfg(feature = "op_delete_item")]
 mod delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 mod delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 mod delete_table;

+#[cfg(feature = "op_describe_backup")]
 mod describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 mod describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 mod describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 mod describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 mod describe_export;

+#[cfg(feature = "op_describe_global_table")]
 mod describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 mod describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 mod describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 mod describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 mod describe_limits;

+#[cfg(feature = "op_describe_table")]
 mod describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 mod describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 mod describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 mod disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 mod enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 mod execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 mod execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 mod get_item;

+#[cfg(feature = "op_get_resource_policy")]
 mod get_resource_policy;

+#[cfg(feature = "op_import_table")]
 mod import_table;

+#[cfg(feature = "op_list_backups")]
 mod list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 mod list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 mod list_exports;

+#[cfg(feature = "op_list_global_tables")]
 mod list_global_tables;

+#[cfg(feature = "op_list_imports")]
 mod list_imports;

+#[cfg(feature = "op_list_tables")]
 mod list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 mod list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 mod put_item;

+#[cfg(feature = "op_put_resource_policy")]
 mod put_resource_policy;

+#[cfg(feature = "op_query")]
 mod query;

+#[cfg(feature = "op_restore_table_from_backup")]
 mod restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 mod restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 mod scan;

+#[cfg(feature = "op_search_vectors")]
 mod search_vectors;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 mod transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 mod transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 mod update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 mod update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 mod update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 mod update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 mod update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 mod update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 mod update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 mod update_time_to_live;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,42 +3,207 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_delete_backup",
+        feature = "op_restore_table_from_backup"
+    ))]
     /// <p>There is another ongoing conflicting backup control plane operation on the table. The backup is either being created, deleted or restored to a table.</p>
     BackupInUseException(crate::types::error::BackupInUseException),
+    #[cfg(any(
+        feature = "op_delete_backup",
+        feature = "op_describe_backup",
+        feature = "op_restore_table_from_backup"
+    ))]
     /// <p>Backup not found for the given BackupARN.</p>
     BackupNotFoundException(crate::types::error::BackupNotFoundException),
+    #[cfg(any(
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>A condition specified in the operation failed to be evaluated.</p>
     ConditionalCheckFailedException(crate::types::error::ConditionalCheckFailedException),
+    #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
     /// <p>Backups have not yet been enabled for this table.</p>
     ContinuousBackupsUnavailableException(crate::types::error::ContinuousBackupsUnavailableException),
+    #[cfg(feature = "op_execute_statement")]
     /// <p>There was an attempt to insert an item with the same primary key as an item that already exists in the DynamoDB table.</p>
     DuplicateItemException(crate::types::error::DuplicateItemException),
+    #[cfg(feature = "op_export_table_to_point_in_time")]
     /// <p>There was a conflict when writing to the specified S3 bucket.</p>
     ExportConflictException(crate::types::error::ExportConflictException),
+    #[cfg(feature = "op_describe_export")]
     /// <p>The specified export was not found.</p>
     ExportNotFoundException(crate::types::error::ExportNotFoundException),
+    #[cfg(feature = "op_create_global_table")]
     /// <p>The specified global table already exists.</p>
     GlobalTableAlreadyExistsException(crate::types::error::GlobalTableAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings"
+    ))]
     /// <p>The specified global table does not exist.</p>
     GlobalTableNotFoundException(crate::types::error::GlobalTableNotFoundException),
+    #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
     /// <p>DynamoDB rejected the request because you retried a request with a different payload but with an idempotent token that was already used.</p>
     IdempotentParameterMismatchException(crate::types::error::IdempotentParameterMismatchException),
+    #[cfg(feature = "op_import_table")]
     /// <p>There was a conflict when importing from the specified S3 source. This can occur when the current import conflicts with a previous import request that had the same client token.</p>
     ImportConflictException(crate::types::error::ImportConflictException),
+    #[cfg(feature = "op_describe_import")]
     /// <p>The specified import was not found.</p>
     ImportNotFoundException(crate::types::error::ImportNotFoundException),
+    #[cfg(feature = "op_update_global_table_settings")]
     /// <p>The operation tried to access a nonexistent index.</p>
     IndexNotFoundException(crate::types::error::IndexNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_backup",
+        feature = "op_describe_continuous_backups",
+        feature = "op_describe_contributor_insights",
+        feature = "op_describe_export",
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_limits",
+        feature = "op_describe_table",
+        feature = "op_describe_table_replica_auto_scaling",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_backups",
+        feature = "op_list_contributor_insights",
+        feature = "op_list_exports",
+        feature = "op_list_global_tables",
+        feature = "op_list_tables",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_contributor_insights",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>An error occurred on the server side.</p>
     InternalServerError(crate::types::error::InternalServerError),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_backup",
+        feature = "op_describe_continuous_backups",
+        feature = "op_describe_global_table",
+        feature = "op_describe_global_table_settings",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_limits",
+        feature = "op_describe_table",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_backups",
+        feature = "op_list_global_tables",
+        feature = "op_list_tables",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_scan",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_global_table",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_time_to_live"
+    ))]
     #[allow(missing_docs)] // documentation missing in model
     InvalidEndpointException(crate::types::error::InvalidEndpointException),
+    #[cfg(feature = "op_export_table_to_point_in_time")]
     /// <p>The specified <code>ExportTime</code> is outside of the point in time recovery window.</p>
     InvalidExportTimeException(crate::types::error::InvalidExportTimeException),
+    #[cfg(feature = "op_restore_table_to_point_in_time")]
     /// <p>An invalid restore time was specified. RestoreDateTime must be between EarliestRestorableDateTime and LatestRestorableDateTime.</p>
     InvalidRestoreTimeException(crate::types::error::InvalidRestoreTimeException),
+    #[cfg(any(
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>An item collection is too large. This exception is only returned for tables that have one or more local secondary indexes.</p>
     ItemCollectionSizeLimitExceededException(crate::types::error::ItemCollectionSizeLimitExceededException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_create_table",
+        feature = "op_delete_backup",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_export",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_import_table",
+        feature = "op_list_exports",
+        feature = "op_list_imports",
+        feature = "op_put_resource_policy",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>There is no limit to the number of daily on-demand backups that can be taken.</p>
     /// <p>For most purposes, up to 500 simultaneous table operations are allowed per account. These operations include <code>CreateTable</code>, <code>UpdateTable</code>, <code>DeleteTable</code>,<code>UpdateTimeToLive</code>, <code>RestoreTableFromBackup</code>, and <code>RestoreTableToPointInTime</code>.</p>
     /// <p>When you are creating a table with one or more secondary indexes, you can have up to 250 such requests running at a time. However, if the table or index specifications are complex, then DynamoDB might temporarily reduce the number of concurrent operations.</p>
@@ -47,21 +212,84 @@
     /// <p>GetRecords was called with a value of more than 1000 for the limit request parameter.</p>
     /// <p>More than 2 processes are reading from the same streams shard at the same time. Exceeding this limit may result in request throttling.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>Point in time recovery has not yet been enabled for this source table.</p>
     PointInTimeRecoveryUnavailableException(crate::types::error::PointInTimeRecoveryUnavailableException),
+    #[cfg(any(
+        feature = "op_delete_resource_policy",
+        feature = "op_get_resource_policy",
+        feature = "op_put_resource_policy"
+    ))]
     /// <p>The operation tried to access a nonexistent resource-based policy.</p>
     /// <p>If you specified an <code>ExpectedRevisionId</code>, it's possible that a policy is present for the resource but its revision ID didn't match the expected value.</p>
     PolicyNotFoundException(crate::types::error::PolicyNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was denied due to request throttling. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception. The Amazon Web Services SDKs for DynamoDB automatically retry requests that receive this exception. Your request is eventually successful, unless your retry queue is too large to finish. Reduce the frequency of requests and use exponential backoff. For more information, go to <a href="https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Programming.Errors.html#Programming.Errors.RetryAndBackoff">Error Retries and Exponential Backoff</a> in the <i>Amazon DynamoDB Developer Guide</i>.</p>
     ProvisionedThroughputExceededException(crate::types::error::ProvisionedThroughputExceededException),
+    #[cfg(feature = "op_update_global_table")]
     /// <p>The specified replica is already part of the global table.</p>
     ReplicaAlreadyExistsException(crate::types::error::ReplicaAlreadyExistsException),
+    #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
     /// <p>The specified replica is no longer part of the global table.</p>
     ReplicaNotFoundException(crate::types::error::ReplicaNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was rejected because one or more items in the request are being modified by a request in another Region.</p>
     ReplicatedWriteConflictException(crate::types::error::ReplicatedWriteConflictException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>Throughput exceeds the current throughput quota for your account. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception. Contact <a href="https://aws.amazon.com/support">Amazon Web Services Support</a> to request a quota increase.</p>
     RequestLimitExceeded(crate::types::error::RequestLimitExceeded),
+    #[cfg(any(
+        feature = "op_create_table",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_import_table",
+        feature = "op_put_resource_policy",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_global_table_settings",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>The operation conflicts with the resource's availability. For example:</p>
     /// <ul>
     /// <li>
@@ -73,16 +301,90 @@
     /// </ul>
     /// <p>When appropriate, wait for the ongoing update to complete and attempt the request again.</p>
     ResourceInUseException(crate::types::error::ResourceInUseException),
+    #[cfg(any(
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_table",
+        feature = "op_describe_contributor_insights",
+        feature = "op_describe_kinesis_streaming_destination",
+        feature = "op_describe_table",
+        feature = "op_describe_table_replica_auto_scaling",
+        feature = "op_describe_time_to_live",
+        feature = "op_disable_kinesis_streaming_destination",
+        feature = "op_enable_kinesis_streaming_destination",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_get_resource_policy",
+        feature = "op_list_contributor_insights",
+        feature = "op_list_tags_of_resource",
+        feature = "op_put_item",
+        feature = "op_put_resource_policy",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_tag_resource",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_untag_resource",
+        feature = "op_update_contributor_insights",
+        feature = "op_update_item",
+        feature = "op_update_kinesis_streaming_destination",
+        feature = "op_update_table",
+        feature = "op_update_table_replica_auto_scaling",
+        feature = "op_update_time_to_live"
+    ))]
     /// <p>The operation tried to access a nonexistent table or index. The resource might not be specified correctly, or its status might not be <code>ACTIVE</code>.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>A target table with the specified name already exists.</p>
     TableAlreadyExistsException(crate::types::error::TableAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_restore_table_from_backup",
+        feature = "op_restore_table_to_point_in_time"
+    ))]
     /// <p>A target table with the specified name is either being created or deleted.</p>
     TableInUseException(crate::types::error::TableInUseException),
+    #[cfg(any(
+        feature = "op_create_backup",
+        feature = "op_create_global_table",
+        feature = "op_describe_continuous_backups",
+        feature = "op_export_table_to_point_in_time",
+        feature = "op_restore_table_to_point_in_time",
+        feature = "op_update_continuous_backups",
+        feature = "op_update_global_table"
+    ))]
     /// <p>A source table with the name <code>TableName</code> does not currently exist within the subscriber's account or the subscriber is operating in the wrong Amazon Web Services Region.</p>
     TableNotFoundException(crate::types::error::TableNotFoundException),
+    #[cfg(any(
+        feature = "op_batch_execute_statement",
+        feature = "op_batch_get_item",
+        feature = "op_batch_write_item",
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_execute_transaction",
+        feature = "op_get_item",
+        feature = "op_put_item",
+        feature = "op_query",
+        feature = "op_scan",
+        feature = "op_search_vectors",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items",
+        feature = "op_update_item"
+    ))]
     /// <p>The request was denied due to request throttling. For detailed information about why the request was throttled and the ARN of the impacted resource, find the <a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_ThrottlingReason.html">ThrottlingReason</a> field in the returned exception.</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(any(
+        feature = "op_execute_transaction",
+        feature = "op_transact_get_items",
+        feature = "op_transact_write_items"
+    ))]
     /// <p>The entire transaction request was canceled.</p>
     /// <p>DynamoDB cancels a <code>TransactWriteItems</code> request under the following circumstances:</p>
     /// <ul>
@@ -216,8 +518,15 @@
     /// </ul></li>
     /// </ul>
     TransactionCanceledException(crate::types::error::TransactionCanceledException),
+    #[cfg(any(
+        feature = "op_delete_item",
+        feature = "op_execute_statement",
+        feature = "op_put_item",
+        feature = "op_update_item"
+    ))]
     /// <p>Operation was rejected because there is an ongoing transaction for the item.</p>
     TransactionConflictException(crate::types::error::TransactionConflictException),
+    #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
     /// <p>The transaction with the given request token is already in progress.</p>
     /// <p>Recommended Settings</p><note>
     /// <p>This is a general recommendation for handling the <code>TransactionInProgressException</code>. These settings help ensure that the client retries will trigger completion of the ongoing <code>TransactWriteItems</code> request.</p>
@@ -265,40 +574,349 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ConditionalCheckFailedException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Error::ContinuousBackupsUnavailableException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_execute_statement")]
             Error::DuplicateItemException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::ExportConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_describe_export")]
             Error::ExportNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_create_global_table")]
             Error::GlobalTableAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Error::GlobalTableNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::IdempotentParameterMismatchException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_import_table")]
             Error::ImportConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_describe_import")]
             Error::ImportNotFoundException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_global_table_settings")]
             Error::IndexNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InternalServerError(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InvalidEndpointException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::InvalidExportTimeException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Error::InvalidRestoreTimeException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ItemCollectionSizeLimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::PointInTimeRecoveryUnavailableException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Error::PolicyNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ProvisionedThroughputExceededException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_update_global_table")]
             Error::ReplicaAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Error::ReplicaNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ReplicatedWriteConflictException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::RequestLimitExceeded(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableInUseException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Error::TableNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Error::TransactionCanceledException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::TransactionConflictException(inner) => inner.fmt(f),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::TransactionInProgressException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -323,45 +941,355 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ConditionalCheckFailedException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Self::ContinuousBackupsUnavailableException(inner) => inner.meta(),
+            #[cfg(feature = "op_execute_statement")]
             Self::DuplicateItemException(inner) => inner.meta(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::ExportConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_describe_export")]
             Self::ExportNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_create_global_table")]
             Self::GlobalTableAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Self::GlobalTableNotFoundException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::IdempotentParameterMismatchException(inner) => inner.meta(),
+            #[cfg(feature = "op_import_table")]
             Self::ImportConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_describe_import")]
             Self::ImportNotFoundException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Self::IndexNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InternalServerError(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InvalidEndpointException(inner) => inner.meta(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::InvalidExportTimeException(inner) => inner.meta(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Self::InvalidRestoreTimeException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ItemCollectionSizeLimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::PointInTimeRecoveryUnavailableException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Self::PolicyNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ProvisionedThroughputExceededException(inner) => inner.meta(),
+            #[cfg(feature = "op_update_global_table")]
             Self::ReplicaAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Self::ReplicaNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ReplicatedWriteConflictException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::RequestLimitExceeded(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableInUseException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Self::TableNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Self::TransactionCanceledException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::TransactionConflictException(inner) => inner.meta(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::TransactionInProgressException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_batch_execute_statement")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -387,6 +1315,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_execute_statement")]
 impl From<crate::operation::batch_execute_statement::BatchExecuteStatementError> for Error {
     fn from(err: crate::operation::batch_execute_statement::BatchExecuteStatementError) -> Self {
         match err {
@@ -405,6 +1334,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::batch_get_item::BatchGetItemError, R>>
     for Error
 where
@@ -422,6 +1352,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_item")]
 impl From<crate::operation::batch_get_item::BatchGetItemError> for Error {
     fn from(err: crate::operation::batch_get_item::BatchGetItemError) -> Self {
         match err {
@@ -447,6 +1378,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_write_item")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::batch_write_item::BatchWriteItemError, R>>
     for Error
@@ -468,6 +1400,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_write_item")]
 impl From<crate::operation::batch_write_item::BatchWriteItemError> for Error {
     fn from(err: crate::operation::batch_write_item::BatchWriteItemError) -> Self {
         match err {
@@ -499,6 +1432,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_backup")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_backup::CreateBackupError, R>>
     for Error
 where
@@ -516,6 +1450,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_backup")]
 impl From<crate::operation::create_backup::CreateBackupError> for Error {
     fn from(err: crate::operation::create_backup::CreateBackupError) -> Self {
         match err {
@@ -544,6 +1479,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -569,6 +1505,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_global_table")]
 impl From<crate::operation::create_global_table::CreateGlobalTableError> for Error {
     fn from(err: crate::operation::create_global_table::CreateGlobalTableError) -> Self {
         match err {
@@ -591,6 +1528,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_table::CreateTableError, R>>
     for Error
 where
@@ -608,6 +1546,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_table")]
 impl From<crate::operation::create_table::CreateTableError> for Error {
     fn from(err: crate::operation::create_table::CreateTableError) -> Self {
         match err {
@@ -627,6 +1566,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_backup")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_backup::DeleteBackupError, R>>
     for Error
 where
@@ -644,6 +1584,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_backup")]
 impl From<crate::operation::delete_backup::DeleteBackupError> for Error {
     fn from(err: crate::operation::delete_backup::DeleteBackupError) -> Self {
         match err {
@@ -666,6 +1607,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_item::DeleteItemError, R>>
     for Error
 where
@@ -683,6 +1625,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_item")]
 impl From<crate::operation::delete_item::DeleteItemError> for Error {
     fn from(err: crate::operation::delete_item::DeleteItemError) -> Self {
         match err {
@@ -720,6 +1663,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -745,6 +1689,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl From<crate::operation::delete_resource_policy::DeleteResourcePolicyError> for Error {
     fn from(err: crate::operation::delete_resource_policy::DeleteResourcePolicyError) -> Self {
         match err {
@@ -772,6 +1717,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_table::DeleteTableError, R>>
     for Error
 where
@@ -789,6 +1735,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_table")]
 impl From<crate::operation::delete_table::DeleteTableError> for Error {
     fn from(err: crate::operation::delete_table::DeleteTableError) -> Self {
         match err {
@@ -811,6 +1758,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_backup")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_backup::DescribeBackupError, R>>
     for Error
@@ -832,6 +1780,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_backup")]
 impl From<crate::operation::describe_backup::DescribeBackupError> for Error {
     fn from(err: crate::operation::describe_backup::DescribeBackupError) -> Self {
         match err {
@@ -848,6 +1797,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_continuous_backups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -873,6 +1823,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_continuous_backups")]
 impl From<crate::operation::describe_continuous_backups::DescribeContinuousBackupsError> for Error {
     fn from(err: crate::operation::describe_continuous_backups::DescribeContinuousBackupsError) -> Self {
         match err {
@@ -891,6 +1842,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -916,6 +1868,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_contributor_insights")]
 impl From<crate::operation::describe_contributor_insights::DescribeContributorInsightsError> for Error {
     fn from(err: crate::operation::describe_contributor_insights::DescribeContributorInsightsError) -> Self {
         match err {
@@ -929,6 +1882,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_endpoints")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -954,6 +1908,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_endpoints")]
 impl From<crate::operation::describe_endpoints::DescribeEndpointsError> for Error {
     fn from(err: crate::operation::describe_endpoints::DescribeEndpointsError) -> Self {
         match err {
@@ -961,6 +1916,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_export::DescribeExportError, R>>
     for Error
@@ -982,6 +1938,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export")]
 impl From<crate::operation::describe_export::DescribeExportError> for Error {
     fn from(err: crate::operation::describe_export::DescribeExportError) -> Self {
         match err {
@@ -998,6 +1955,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1023,6 +1981,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table")]
 impl From<crate::operation::describe_global_table::DescribeGlobalTableError> for Error {
     fn from(err: crate::operation::describe_global_table::DescribeGlobalTableError) -> Self {
         match err {
@@ -1041,6 +2000,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table_settings")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1066,6 +2026,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_global_table_settings")]
 impl From<crate::operation::describe_global_table_settings::DescribeGlobalTableSettingsError> for Error {
     fn from(err: crate::operation::describe_global_table_settings::DescribeGlobalTableSettingsError) -> Self {
         match err {
@@ -1082,6 +2043,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_import::DescribeImportError, R>>
     for Error
@@ -1103,6 +2065,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import")]
 impl From<crate::operation::describe_import::DescribeImportError> for Error {
     fn from(err: crate::operation::describe_import::DescribeImportError) -> Self {
         match err {
@@ -1113,6 +2076,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1138,6 +2102,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 impl From<crate::operation::describe_kinesis_streaming_destination::DescribeKinesisStreamingDestinationError>
     for Error
 {
@@ -1160,6 +2125,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_limits")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_limits::DescribeLimitsError, R>>
     for Error
@@ -1181,6 +2147,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_limits")]
 impl From<crate::operation::describe_limits::DescribeLimitsError> for Error {
     fn from(err: crate::operation::describe_limits::DescribeLimitsError) -> Self {
         match err {
@@ -1194,6 +2161,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_table::DescribeTableError, R>>
     for Error
@@ -1215,6 +2183,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table")]
 impl From<crate::operation::describe_table::DescribeTableError> for Error {
     fn from(err: crate::operation::describe_table::DescribeTableError) -> Self {
         match err {
@@ -1231,6 +2200,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1256,6 +2226,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 impl From<crate::operation::describe_table_replica_auto_scaling::DescribeTableReplicaAutoScalingError> for Error {
     fn from(err: crate::operation::describe_table_replica_auto_scaling::DescribeTableReplicaAutoScalingError) -> Self {
         match err {
@@ -1269,6 +2240,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_time_to_live")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1294,6 +2266,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_time_to_live")]
 impl From<crate::operation::describe_time_to_live::DescribeTimeToLiveError> for Error {
     fn from(err: crate::operation::describe_time_to_live::DescribeTimeToLiveError) -> Self {
         match err {
@@ -1312,6 +2285,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1337,6 +2311,7 @@
         }
     }
 }
+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 impl From<crate::operation::disable_kinesis_streaming_destination::DisableKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::disable_kinesis_streaming_destination::DisableKinesisStreamingDestinationError,
@@ -1363,6 +2338,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1388,6 +2364,7 @@
         }
     }
 }
+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 impl From<crate::operation::enable_kinesis_streaming_destination::EnableKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::enable_kinesis_streaming_destination::EnableKinesisStreamingDestinationError,
@@ -1414,6 +2391,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_statement")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1439,6 +2417,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_statement")]
 impl From<crate::operation::execute_statement::ExecuteStatementError> for Error {
     fn from(err: crate::operation::execute_statement::ExecuteStatementError) -> Self {
         match err {
@@ -1473,6 +2452,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_transaction")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1498,6 +2478,7 @@
         }
     }
 }
+#[cfg(feature = "op_execute_transaction")]
 impl From<crate::operation::execute_transaction::ExecuteTransactionError> for Error {
     fn from(err: crate::operation::execute_transaction::ExecuteTransactionError) -> Self {
         match err {
@@ -1529,6 +2510,7 @@
         }
     }
 }
+#[cfg(feature = "op_export_table_to_point_in_time")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1554,6 +2536,7 @@
         }
     }
 }
+#[cfg(feature = "op_export_table_to_point_in_time")]
 impl From<crate::operation::export_table_to_point_in_time::ExportTableToPointInTimeError> for Error {
     fn from(err: crate::operation::export_table_to_point_in_time::ExportTableToPointInTimeError) -> Self {
         match err {
@@ -1579,6 +2562,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_item::GetItemError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1595,6 +2579,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_item")]
 impl From<crate::operation::get_item::GetItemError> for Error {
     fn from(err: crate::operation::get_item::GetItemError) -> Self {
         match err {
@@ -1614,6 +2599,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1639,6 +2625,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_resource_policy")]
 impl From<crate::operation::get_resource_policy::GetResourcePolicyError> for Error {
     fn from(err: crate::operation::get_resource_policy::GetResourcePolicyError) -> Self {
         match err {
@@ -1658,6 +2645,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::import_table::ImportTableError, R>>
     for Error
 where
@@ -1675,6 +2663,7 @@
         }
     }
 }
+#[cfg(feature = "op_import_table")]
 impl From<crate::operation::import_table::ImportTableError> for Error {
     fn from(err: crate::operation::import_table::ImportTableError) -> Self {
         match err {
@@ -1691,6 +2680,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_backups")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_backups::ListBackupsError, R>>
     for Error
 where
@@ -1708,6 +2698,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_backups")]
 impl From<crate::operation::list_backups::ListBackupsError> for Error {
     fn from(err: crate::operation::list_backups::ListBackupsError) -> Self {
         match err {
@@ -1721,6 +2712,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1746,6 +2738,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contributor_insights")]
 impl From<crate::operation::list_contributor_insights::ListContributorInsightsError> for Error {
     fn from(err: crate::operation::list_contributor_insights::ListContributorInsightsError) -> Self {
         match err {
@@ -1761,6 +2754,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_exports")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_exports::ListExportsError, R>>
     for Error
 where
@@ -1778,6 +2772,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_exports")]
 impl From<crate::operation::list_exports::ListExportsError> for Error {
     fn from(err: crate::operation::list_exports::ListExportsError) -> Self {
         match err {
@@ -1791,6 +2786,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_global_tables")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1816,6 +2812,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_global_tables")]
 impl From<crate::operation::list_global_tables::ListGlobalTablesError> for Error {
     fn from(err: crate::operation::list_global_tables::ListGlobalTablesError) -> Self {
         match err {
@@ -1829,6 +2826,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_imports")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_imports::ListImportsError, R>>
     for Error
 where
@@ -1846,6 +2844,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_imports")]
 impl From<crate::operation::list_imports::ListImportsError> for Error {
     fn from(err: crate::operation::list_imports::ListImportsError) -> Self {
         match err {
@@ -1856,6 +2855,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tables")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_tables::ListTablesError, R>>
     for Error
 where
@@ -1873,6 +2873,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tables")]
 impl From<crate::operation::list_tables::ListTablesError> for Error {
     fn from(err: crate::operation::list_tables::ListTablesError) -> Self {
         match err {
@@ -1886,6 +2887,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_of_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1911,6 +2913,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_of_resource")]
 impl From<crate::operation::list_tags_of_resource::ListTagsOfResourceError> for Error {
     fn from(err: crate::operation::list_tags_of_resource::ListTagsOfResourceError) -> Self {
         match err {
@@ -1929,6 +2932,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_item::PutItemError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -1945,6 +2949,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_item")]
 impl From<crate::operation::put_item::PutItemError> for Error {
     fn from(err: crate::operation::put_item::PutItemError) -> Self {
         match err {
@@ -1976,6 +2981,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2001,6 +3007,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl From<crate::operation::put_resource_policy::PutResourcePolicyError> for Error {
     fn from(err: crate::operation::put_resource_policy::PutResourcePolicyError) -> Self {
         match err {
@@ -2026,6 +3033,7 @@
         }
     }
 }
+#[cfg(feature = "op_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::query::QueryError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2040,6 +3048,7 @@
         }
     }
 }
+#[cfg(feature = "op_query")]
 impl From<crate::operation::query::QueryError> for Error {
     fn from(err: crate::operation::query::QueryError) -> Self {
         match err {
@@ -2059,6 +3068,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_from_backup")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2084,6 +3094,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_from_backup")]
 impl From<crate::operation::restore_table_from_backup::RestoreTableFromBackupError> for Error {
     fn from(err: crate::operation::restore_table_from_backup::RestoreTableFromBackupError) -> Self {
         match err {
@@ -2114,6 +3125,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_to_point_in_time")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2139,6 +3151,7 @@
         }
     }
 }
+#[cfg(feature = "op_restore_table_to_point_in_time")]
 impl From<crate::operation::restore_table_to_point_in_time::RestoreTableToPointInTimeError> for Error {
     fn from(err: crate::operation::restore_table_to_point_in_time::RestoreTableToPointInTimeError) -> Self {
         match err {
@@ -2170,6 +3183,7 @@
         }
     }
 }
+#[cfg(feature = "op_scan")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::scan::ScanError, R>> for Error
 where
     R: Send + Sync + std::fmt::Debug + 'static,
@@ -2184,6 +3198,7 @@
         }
     }
 }
+#[cfg(feature = "op_scan")]
 impl From<crate::operation::scan::ScanError> for Error {
     fn from(err: crate::operation::scan::ScanError) -> Self {
         match err {
@@ -2203,6 +3218,7 @@
         }
     }
 }
+#[cfg(feature = "op_search_vectors")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::search_vectors::SearchVectorsError, R>>
     for Error
@@ -2224,6 +3240,7 @@
         }
     }
 }
+#[cfg(feature = "op_search_vectors")]
 impl From<crate::operation::search_vectors::SearchVectorsError> for Error {
     fn from(err: crate::operation::search_vectors::SearchVectorsError) -> Self {
         match err {
@@ -2243,6 +3260,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -2260,6 +3278,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -2282,6 +3301,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_get_items")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2307,6 +3327,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_get_items")]
 impl From<crate::operation::transact_get_items::TransactGetItemsError> for Error {
     fn from(err: crate::operation::transact_get_items::TransactGetItemsError) -> Self {
         match err {
@@ -2335,6 +3356,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_write_items")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2360,6 +3382,7 @@
         }
     }
 }
+#[cfg(feature = "op_transact_write_items")]
 impl From<crate::operation::transact_write_items::TransactWriteItemsError> for Error {
     fn from(err: crate::operation::transact_write_items::TransactWriteItemsError) -> Self {
         match err {
@@ -2396,6 +3419,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -2417,6 +3441,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -2439,6 +3464,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_continuous_backups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2464,6 +3490,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_continuous_backups")]
 impl From<crate::operation::update_continuous_backups::UpdateContinuousBackupsError> for Error {
     fn from(err: crate::operation::update_continuous_backups::UpdateContinuousBackupsError) -> Self {
         match err {
@@ -2483,6 +3510,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contributor_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2508,6 +3536,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contributor_insights")]
 impl From<crate::operation::update_contributor_insights::UpdateContributorInsightsError> for Error {
     fn from(err: crate::operation::update_contributor_insights::UpdateContributorInsightsError) -> Self {
         match err {
@@ -2521,6 +3550,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2546,6 +3576,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table")]
 impl From<crate::operation::update_global_table::UpdateGlobalTableError> for Error {
     fn from(err: crate::operation::update_global_table::UpdateGlobalTableError) -> Self {
         match err {
@@ -2571,6 +3602,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table_settings")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2596,6 +3628,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_global_table_settings")]
 impl From<crate::operation::update_global_table_settings::UpdateGlobalTableSettingsError> for Error {
     fn from(err: crate::operation::update_global_table_settings::UpdateGlobalTableSettingsError) -> Self {
         match err {
@@ -2624,6 +3657,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_item")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_item::UpdateItemError, R>>
     for Error
 where
@@ -2641,6 +3675,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_item")]
 impl From<crate::operation::update_item::UpdateItemError> for Error {
     fn from(err: crate::operation::update_item::UpdateItemError) -> Self {
         match err {
@@ -2678,6 +3713,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2703,6 +3739,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 impl From<crate::operation::update_kinesis_streaming_destination::UpdateKinesisStreamingDestinationError> for Error {
     fn from(
         err: crate::operation::update_kinesis_streaming_destination::UpdateKinesisStreamingDestinationError,
@@ -2729,6 +3766,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_table::UpdateTableError, R>>
     for Error
 where
@@ -2746,6 +3784,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table")]
 impl From<crate::operation::update_table::UpdateTableError> for Error {
     fn from(err: crate::operation::update_table::UpdateTableError) -> Self {
         match err {
@@ -2768,6 +3807,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2793,6 +3833,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 impl From<crate::operation::update_table_replica_auto_scaling::UpdateTableReplicaAutoScalingError> for Error {
     fn from(err: crate::operation::update_table_replica_auto_scaling::UpdateTableReplicaAutoScalingError) -> Self {
         match err {
@@ -2812,6 +3853,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_time_to_live")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2837,6 +3879,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_time_to_live")]
 impl From<crate::operation::update_time_to_live::UpdateTimeToLiveError> for Error {
     fn from(err: crate::operation::update_time_to_live::UpdateTimeToLiveError) -> Self {
         match err {
@@ -2874,40 +3917,349 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Error::BackupNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ConditionalCheckFailedException(inner) => inner.source(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Error::ContinuousBackupsUnavailableException(inner) => inner.source(),
+            #[cfg(feature = "op_execute_statement")]
             Error::DuplicateItemException(inner) => inner.source(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::ExportConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_describe_export")]
             Error::ExportNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_create_global_table")]
             Error::GlobalTableAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Error::GlobalTableNotFoundException(inner) => inner.source(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::IdempotentParameterMismatchException(inner) => inner.source(),
+            #[cfg(feature = "op_import_table")]
             Error::ImportConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_describe_import")]
             Error::ImportNotFoundException(inner) => inner.source(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Error::IndexNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InternalServerError(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Error::InvalidEndpointException(inner) => inner.source(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Error::InvalidExportTimeException(inner) => inner.source(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Error::InvalidRestoreTimeException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ItemCollectionSizeLimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::PointInTimeRecoveryUnavailableException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Error::PolicyNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ProvisionedThroughputExceededException(inner) => inner.source(),
+            #[cfg(feature = "op_update_global_table")]
             Error::ReplicaAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Error::ReplicaNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::ReplicatedWriteConflictException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::RequestLimitExceeded(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Error::TableInUseException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Error::TableNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Error::TransactionCanceledException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Error::TransactionConflictException(inner) => inner.source(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Error::TransactionInProgressException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -2916,40 +4268,349 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_delete_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_backup",
+                feature = "op_describe_backup",
+                feature = "op_restore_table_from_backup"
+            ))]
             Self::BackupNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ConditionalCheckFailedException(e) => e.request_id(),
+            #[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
             Self::ContinuousBackupsUnavailableException(e) => e.request_id(),
+            #[cfg(feature = "op_execute_statement")]
             Self::DuplicateItemException(e) => e.request_id(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::ExportConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_describe_export")]
             Self::ExportNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_create_global_table")]
             Self::GlobalTableAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings"
+            ))]
             Self::GlobalTableNotFoundException(e) => e.request_id(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::IdempotentParameterMismatchException(e) => e.request_id(),
+            #[cfg(feature = "op_import_table")]
             Self::ImportConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_describe_import")]
             Self::ImportNotFoundException(e) => e.request_id(),
+            #[cfg(feature = "op_update_global_table_settings")]
             Self::IndexNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_export",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_exports",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InternalServerError(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_backup",
+                feature = "op_describe_continuous_backups",
+                feature = "op_describe_global_table",
+                feature = "op_describe_global_table_settings",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_limits",
+                feature = "op_describe_table",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_backups",
+                feature = "op_list_global_tables",
+                feature = "op_list_tables",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_scan",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_time_to_live"
+            ))]
             Self::InvalidEndpointException(e) => e.request_id(),
+            #[cfg(feature = "op_export_table_to_point_in_time")]
             Self::InvalidExportTimeException(e) => e.request_id(),
+            #[cfg(feature = "op_restore_table_to_point_in_time")]
             Self::InvalidRestoreTimeException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ItemCollectionSizeLimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_create_table",
+                feature = "op_delete_backup",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_export",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_import_table",
+                feature = "op_list_exports",
+                feature = "op_list_imports",
+                feature = "op_put_resource_policy",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::PointInTimeRecoveryUnavailableException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_resource_policy",
+                feature = "op_get_resource_policy",
+                feature = "op_put_resource_policy"
+            ))]
             Self::PolicyNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ProvisionedThroughputExceededException(e) => e.request_id(),
+            #[cfg(feature = "op_update_global_table")]
             Self::ReplicaAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
             Self::ReplicaNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::ReplicatedWriteConflictException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::RequestLimitExceeded(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_table",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_import_table",
+                feature = "op_put_resource_policy",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_global_table_settings",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_table",
+                feature = "op_describe_contributor_insights",
+                feature = "op_describe_kinesis_streaming_destination",
+                feature = "op_describe_table",
+                feature = "op_describe_table_replica_auto_scaling",
+                feature = "op_describe_time_to_live",
+                feature = "op_disable_kinesis_streaming_destination",
+                feature = "op_enable_kinesis_streaming_destination",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_get_resource_policy",
+                feature = "op_list_contributor_insights",
+                feature = "op_list_tags_of_resource",
+                feature = "op_put_item",
+                feature = "op_put_resource_policy",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_tag_resource",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_untag_resource",
+                feature = "op_update_contributor_insights",
+                feature = "op_update_item",
+                feature = "op_update_kinesis_streaming_destination",
+                feature = "op_update_table",
+                feature = "op_update_table_replica_auto_scaling",
+                feature = "op_update_time_to_live"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_restore_table_from_backup",
+                feature = "op_restore_table_to_point_in_time"
+            ))]
             Self::TableInUseException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_backup",
+                feature = "op_create_global_table",
+                feature = "op_describe_continuous_backups",
+                feature = "op_export_table_to_point_in_time",
+                feature = "op_restore_table_to_point_in_time",
+                feature = "op_update_continuous_backups",
+                feature = "op_update_global_table"
+            ))]
             Self::TableNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_batch_execute_statement",
+                feature = "op_batch_get_item",
+                feature = "op_batch_write_item",
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_execute_transaction",
+                feature = "op_get_item",
+                feature = "op_put_item",
+                feature = "op_query",
+                feature = "op_scan",
+                feature = "op_search_vectors",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items",
+                feature = "op_update_item"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_execute_transaction",
+                feature = "op_transact_get_items",
+                feature = "op_transact_write_items"
+            ))]
             Self::TransactionCanceledException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_delete_item",
+                feature = "op_execute_statement",
+                feature = "op_put_item",
+                feature = "op_update_item"
+            ))]
             Self::TransactionConflictException(e) => e.request_id(),
+            #[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
             Self::TransactionInProgressException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) fn reflens_list_contributor_insights_output_output_next_token(
     input: &crate::operation::list_contributor_insights::ListContributorInsightsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_exports")]
 pub(crate) fn reflens_list_exports_output_output_next_token(
     input: &crate::operation::list_exports::ListExportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_imports")]
 pub(crate) fn reflens_list_imports_output_output_next_token(
     input: &crate::operation::list_imports::ListImportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tables")]
 pub(crate) fn reflens_list_tables_output_output_last_evaluated_table_name(
     input: &crate::operation::list_tables::ListTablesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_query")]
 pub(crate) fn reflens_query_output_output_last_evaluated_key(
     input: &crate::operation::query::QueryOutput,
 ) -> ::std::option::Option<&::std::collections::HashMap<::std::string::String, crate::types::AttributeValue>> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_scan")]
 pub(crate) fn reflens_scan_output_output_last_evaluated_key(
     input: &crate::operation::scan::ScanOutput,
 ) -> ::std::option::Option<&::std::collections::HashMap<::std::string::String, crate::types::AttributeValue>> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tables")]
 pub(crate) fn lens_list_tables_output_output_table_names(
     input: crate::operation::list_tables::ListTablesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -66,6 +73,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_query")]
 pub(crate) fn lens_query_output_output_items(
     input: crate::operation::query::QueryOutput,
 ) -> ::std::option::Option<
@@ -75,6 +83,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_scan")]
 pub(crate) fn lens_scan_output_output_items(
     input: crate::operation::scan::ScanOutput,
 ) -> ::std::option::Option<
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,176 +1,234 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_batch_execute_statement")]
 /// Types for the `BatchExecuteStatement` operation.
 pub mod batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 /// Types for the `BatchGetItem` operation.
 pub mod batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 /// Types for the `BatchWriteItem` operation.
 pub mod batch_write_item;

+#[cfg(feature = "op_create_backup")]
 /// Types for the `CreateBackup` operation.
 pub mod create_backup;

+#[cfg(feature = "op_create_global_table")]
 /// Types for the `CreateGlobalTable` operation.
 pub mod create_global_table;

+#[cfg(feature = "op_create_table")]
 /// Types for the `CreateTable` operation.
 pub mod create_table;

+#[cfg(feature = "op_delete_backup")]
 /// Types for the `DeleteBackup` operation.
 pub mod delete_backup;

+#[cfg(feature = "op_delete_item")]
 /// Types for the `DeleteItem` operation.
 pub mod delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 /// Types for the `DeleteResourcePolicy` operation.
 pub mod delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 /// Types for the `DeleteTable` operation.
 pub mod delete_table;

+#[cfg(feature = "op_describe_backup")]
 /// Types for the `DescribeBackup` operation.
 pub mod describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 /// Types for the `DescribeContinuousBackups` operation.
 pub mod describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Types for the `DescribeContributorInsights` operation.
 pub mod describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 /// Types for the `DescribeEndpoints` operation.
 pub mod describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 /// Types for the `DescribeExport` operation.
 pub mod describe_export;

+#[cfg(feature = "op_describe_global_table")]
 /// Types for the `DescribeGlobalTable` operation.
 pub mod describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 /// Types for the `DescribeGlobalTableSettings` operation.
 pub mod describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 /// Types for the `DescribeImport` operation.
 pub mod describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Types for the `DescribeKinesisStreamingDestination` operation.
 pub mod describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 /// Types for the `DescribeLimits` operation.
 pub mod describe_limits;

+#[cfg(feature = "op_describe_table")]
 /// Types for the `DescribeTable` operation.
 pub mod describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 /// Types for the `DescribeTableReplicaAutoScaling` operation.
 pub mod describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 /// Types for the `DescribeTimeToLive` operation.
 pub mod describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 /// Types for the `DisableKinesisStreamingDestination` operation.
 pub mod disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 /// Types for the `EnableKinesisStreamingDestination` operation.
 pub mod enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 /// Types for the `ExecuteStatement` operation.
 pub mod execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 /// Types for the `ExecuteTransaction` operation.
 pub mod execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 /// Types for the `ExportTableToPointInTime` operation.
 pub mod export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 /// Types for the `GetItem` operation.
 pub mod get_item;

+#[cfg(feature = "op_get_resource_policy")]
 /// Types for the `GetResourcePolicy` operation.
 pub mod get_resource_policy;

+#[cfg(feature = "op_import_table")]
 /// Types for the `ImportTable` operation.
 pub mod import_table;

+#[cfg(feature = "op_list_backups")]
 /// Types for the `ListBackups` operation.
 pub mod list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 /// Types for the `ListContributorInsights` operation.
 pub mod list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 /// Types for the `ListExports` operation.
 pub mod list_exports;

+#[cfg(feature = "op_list_global_tables")]
 /// Types for the `ListGlobalTables` operation.
 pub mod list_global_tables;

+#[cfg(feature = "op_list_imports")]
 /// Types for the `ListImports` operation.
 pub mod list_imports;

+#[cfg(feature = "op_list_tables")]
 /// Types for the `ListTables` operation.
 pub mod list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 /// Types for the `ListTagsOfResource` operation.
 pub mod list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 /// Types for the `PutItem` operation.
 pub mod put_item;

+#[cfg(feature = "op_put_resource_policy")]
 /// Types for the `PutResourcePolicy` operation.
 pub mod put_resource_policy;

+#[cfg(feature = "op_query")]
 /// Types for the `Query` operation.
 pub mod query;

+#[cfg(feature = "op_restore_table_from_backup")]
 /// Types for the `RestoreTableFromBackup` operation.
 pub mod restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 /// Types for the `RestoreTableToPointInTime` operation.
 pub mod restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 /// Types for the `Scan` operation.
 pub mod scan;

+#[cfg(feature = "op_search_vectors")]
 /// Types for the `SearchVectors` operation.
 pub mod search_vectors;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 /// Types for the `TransactGetItems` operation.
 pub mod transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 /// Types for the `TransactWriteItems` operation.
 pub mod transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 /// Types for the `UpdateContinuousBackups` operation.
 pub mod update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 /// Types for the `UpdateContributorInsights` operation.
 pub mod update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 /// Types for the `UpdateGlobalTable` operation.
 pub mod update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 /// Types for the `UpdateGlobalTableSettings` operation.
 pub mod update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 /// Types for the `UpdateItem` operation.
 pub mod update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 /// Types for the `UpdateKinesisStreamingDestination` operation.
 pub mod update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 /// Types for the `UpdateTable` operation.
 pub mod update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 /// Types for the `UpdateTableReplicaAutoScaling` operation.
 pub mod update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 /// Types for the `UpdateTimeToLive` operation.
 pub mod update_time_to_live;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,64 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +77,66 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,122 +148,240 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_execute_statement;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_item;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item;

+#[cfg(feature = "op_create_backup")]
 pub(crate) mod shape_create_backup;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_create_global_table;

+#[cfg(feature = "op_create_table")]
 pub(crate) mod shape_create_table;

+#[cfg(feature = "op_delete_backup")]
 pub(crate) mod shape_delete_backup;

+#[cfg(feature = "op_delete_item")]
 pub(crate) mod shape_delete_item;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy;

+#[cfg(feature = "op_delete_table")]
 pub(crate) mod shape_delete_table;

+#[cfg(feature = "op_describe_backup")]
 pub(crate) mod shape_describe_backup;

+#[cfg(feature = "op_describe_continuous_backups")]
 pub(crate) mod shape_describe_continuous_backups;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_describe_contributor_insights;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_describe_endpoints;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_describe_export;

+#[cfg(feature = "op_describe_global_table")]
 pub(crate) mod shape_describe_global_table;

+#[cfg(feature = "op_describe_global_table_settings")]
 pub(crate) mod shape_describe_global_table_settings;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_describe_import;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_describe_kinesis_streaming_destination;

+#[cfg(feature = "op_describe_limits")]
 pub(crate) mod shape_describe_limits;

+#[cfg(feature = "op_describe_table")]
 pub(crate) mod shape_describe_table;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 pub(crate) mod shape_describe_table_replica_auto_scaling;

+#[cfg(feature = "op_describe_time_to_live")]
 pub(crate) mod shape_describe_time_to_live;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 pub(crate) mod shape_disable_kinesis_streaming_destination;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 pub(crate) mod shape_enable_kinesis_streaming_destination;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_execute_statement;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_execute_transaction;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_table_to_point_in_time;

+#[cfg(feature = "op_get_item")]
 pub(crate) mod shape_get_item;

+#[cfg(feature = "op_get_resource_policy")]
 pub(crate) mod shape_get_resource_policy;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_table;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_list_backups;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_list_contributor_insights;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_list_exports;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_list_global_tables;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_list_imports;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_list_tables;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_list_tags_of_resource;

+#[cfg(feature = "op_put_item")]
 pub(crate) mod shape_put_item;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy;

+#[cfg(feature = "op_query")]
 pub(crate) mod shape_query;

+#[cfg(feature = "op_restore_table_from_backup")]
 pub(crate) mod shape_restore_table_from_backup;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_restore_table_to_point_in_time;

+#[cfg(feature = "op_scan")]
 pub(crate) mod shape_scan;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_vectors;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_items;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_items;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_update_continuous_backups;

+#[cfg(feature = "op_update_contributor_insights")]
 pub(crate) mod shape_update_contributor_insights;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_update_global_table;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_update_global_table_settings;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_update_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_destination;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_table;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_update_table_replica_auto_scaling;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_update_time_to_live;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_endpoints",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_import_table",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_imports",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -152,552 +390,1803 @@
     }
 }

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub(crate) mod shape_backup_in_use_exception;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub(crate) mod shape_backup_not_found_exception;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_execute_statement_input;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_item_input;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item_input;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_conditional_check_failed_exception;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_continuous_backups_unavailable_exception;

+#[cfg(feature = "op_create_backup")]
 pub(crate) mod shape_create_backup_input;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_create_global_table_input;

+#[cfg(feature = "op_create_table")]
 pub(crate) mod shape_create_table_input;

+#[cfg(feature = "op_delete_backup")]
 pub(crate) mod shape_delete_backup_input;

+#[cfg(feature = "op_delete_item")]
 pub(crate) mod shape_delete_item_input;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy_input;

+#[cfg(feature = "op_delete_table")]
 pub(crate) mod shape_delete_table_input;

+#[cfg(feature = "op_describe_backup")]
 pub(crate) mod shape_describe_backup_input;

+#[cfg(feature = "op_describe_continuous_backups")]
 pub(crate) mod shape_describe_continuous_backups_input;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_describe_contributor_insights_input;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_describe_export_input;

+#[cfg(feature = "op_describe_global_table")]
 pub(crate) mod shape_describe_global_table_input;

+#[cfg(feature = "op_describe_global_table_settings")]
 pub(crate) mod shape_describe_global_table_settings_input;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_describe_import_input;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_describe_kinesis_streaming_destination_input;

+#[cfg(feature = "op_describe_table")]
 pub(crate) mod shape_describe_table_input;

+#[cfg(feature = "op_describe_table_replica_auto_scaling")]
 pub(crate) mod shape_describe_table_replica_auto_scaling_input;

+#[cfg(feature = "op_describe_time_to_live")]
 pub(crate) mod shape_describe_time_to_live_input;

+#[cfg(feature = "op_disable_kinesis_streaming_destination")]
 pub(crate) mod shape_disable_kinesis_streaming_destination_input;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_duplicate_item_exception;

+#[cfg(feature = "op_enable_kinesis_streaming_destination")]
 pub(crate) mod shape_enable_kinesis_streaming_destination_input;

+#[cfg(feature = "op_execute_statement")]
 pub(crate) mod shape_execute_statement_input;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_execute_transaction_input;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_conflict_exception;

+#[cfg(feature = "op_describe_export")]
 pub(crate) mod shape_export_not_found_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_export_table_to_point_in_time_input;

+#[cfg(feature = "op_get_item")]
 pub(crate) mod shape_get_item_input;

+#[cfg(feature = "op_get_resource_policy")]
 pub(crate) mod shape_get_resource_policy_input;

+#[cfg(feature = "op_create_global_table")]
 pub(crate) mod shape_global_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_global_table_not_found_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub(crate) mod shape_idempotent_parameter_mismatch_exception;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_conflict_exception;

+#[cfg(feature = "op_describe_import")]
 pub(crate) mod shape_import_not_found_exception;

+#[cfg(feature = "op_import_table")]
 pub(crate) mod shape_import_table_input;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_index_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_internal_server_error;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_invalid_endpoint_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub(crate) mod shape_invalid_export_time_exception;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_invalid_restore_time_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_size_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_list_backups_input;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_list_contributor_insights_input;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_list_exports_input;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_list_global_tables_input;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_list_imports_input;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_list_tables_input;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_list_tags_of_resource_input;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_point_in_time_recovery_unavailable_exception;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub(crate) mod shape_policy_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_provisioned_throughput_exceeded_exception;

+#[cfg(feature = "op_put_item")]
 pub(crate) mod shape_put_item_input;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy_input;

+#[cfg(feature = "op_query")]
 pub(crate) mod shape_query_input;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_replica_already_exists_exception;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub(crate) mod shape_replica_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_replicated_write_conflict_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_request_limit_exceeded;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_resource_in_use_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(feature = "op_restore_table_from_backup")]
 pub(crate) mod shape_restore_table_from_backup_input;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub(crate) mod shape_restore_table_to_point_in_time_input;

+#[cfg(feature = "op_scan")]
 pub(crate) mod shape_scan_input;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_vectors_input;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_table_in_use_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub(crate) mod shape_table_not_found_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_items_input;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_items_input;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_transaction_canceled_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_transaction_conflict_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub(crate) mod shape_transaction_in_progress_exception;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_update_continuous_backups_input;

+#[cfg(feature = "op_update_contributor_insights")]
 pub(crate) mod shape_update_contributor_insights_input;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_update_global_table_input;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_update_global_table_settings_input;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_update_item_input;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_destination_input;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_table_input;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_update_table_replica_auto_scaling_input;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_update_time_to_live_input;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_attribute_map;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_attribute_value;

+#[cfg(feature = "op_update_item")]
 pub(crate) mod shape_attribute_value_update;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_settings_update;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_backup_description;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub(crate) mod shape_backup_details;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_backup_summaries;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_request_map;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_batch_get_response_map;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_request;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_batch_write_item_request_map;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_cancellation_reason_list;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub(crate) mod shape_condition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_consumed_capacity;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_consumed_capacity_multiple;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_continuous_backups_description;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_contributor_insights_rule_list;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_contributor_insights_summaries;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub(crate) mod shape_enable_kinesis_streaming_configuration;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_endpoints;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub(crate) mod shape_expected_attribute_value;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub(crate) mod shape_export_description;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_export_summaries;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub(crate) mod shape_failure_exception;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_global_secondary_index;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_global_secondary_index_auto_scaling_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_global_secondary_index_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub(crate) mod shape_global_table_description;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_global_table_global_secondary_index_settings_update;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_global_table_list;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_global_table_witness_group_update;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_import_summary_list;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_import_table_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub(crate) mod shape_incremental_export_specification;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_input_format_options;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_metrics;

+#[cfg(any(feature = "op_batch_write_item", feature = "op_transact_write_items"))]
 pub(crate) mod shape_item_collection_metrics_per_table;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_list;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub(crate) mod shape_item_response_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_key;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_key_schema_element;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_keys_and_attributes;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_kinesis_data_stream_destinations;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_local_secondary_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_on_demand_throughput;

+#[cfg(feature = "op_execute_transaction")]
 pub(crate) mod shape_parameterized_statement;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_parti_ql_batch_response;

+#[cfg(feature = "op_update_continuous_backups")]
 pub(crate) mod shape_point_in_time_recovery_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub(crate) mod shape_replica;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_replica_auto_scaling_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_settings_description_list;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_replica_settings_update;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_replica_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_replication_group_update;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub(crate) mod shape_s3_bucket_source;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_result_list;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_sse_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_stream_specification;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_table_auto_scaling_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_table_creation_parameters;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_description;

+#[cfg(feature = "op_list_tables")]
 pub(crate) mod shape_table_name_list;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(feature = "op_list_tags_of_resource")]
 pub(crate) mod shape_tag_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_reason_list;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub(crate) mod shape_time_to_live_description;

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) mod shape_time_to_live_specification;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_transact_get_item;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_transact_write_item;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub(crate) mod shape_update_kinesis_streaming_configuration;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_vector_capacity;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) mod shape_vector_index;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_vector_index_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_warm_throughput;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_write_request;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_archival_summary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_attribute_definitions;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_update;

+#[cfg(feature = "op_list_backups")]
 pub(crate) mod shape_backup_summary;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_billing_mode_summary;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub(crate) mod shape_cancellation_reason;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_capacity;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_condition_check;

+#[cfg(feature = "op_list_contributor_insights")]
 pub(crate) mod shape_contributor_insights_summary;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_create_replica_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_replication_group_member_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_create_vector_index_action;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_csv_options;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_delete;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 pub(crate) mod shape_delete_replica_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_replication_group_member_action;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_delete_request;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_delete_vector_index_action;

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) mod shape_endpoint;

+#[cfg(feature = "op_list_exports")]
 pub(crate) mod shape_export_summary;

+#[cfg(feature = "op_transact_get_items")]
 pub(crate) mod shape_get;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_description_list;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_global_table;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_table_witness_description_list;

+#[cfg(feature = "op_list_imports")]
 pub(crate) mod shape_import_summary;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_key_attribute_map;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_metrics_multiple;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_item_collection_size_estimate_range;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub(crate) mod shape_item_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_key_schema;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub(crate) mod shape_kinesis_data_stream_destination;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_local_secondary_index_description_list;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) mod shape_point_in_time_recovery_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput_description;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_put;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_put_request;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_auto_scaling_description_list;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_description_list;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_update;

+#[cfg(feature = "op_update_global_table_settings")]
 pub(crate) mod shape_replica_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_settings_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_restore_summary;

+#[cfg(feature = "op_search_vectors")]
 pub(crate) mod shape_search_result_item;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_search_schema_element;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_secondary_indexes_capacity_map;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_source_table_details;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_source_table_feature_details;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_sse_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_class_summary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_table_warm_throughput_description;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_throttling_reason;

+#[cfg(feature = "op_transact_write_items")]
 pub(crate) mod shape_update;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_update_replication_group_member_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_attribute_definition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_index_description_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_vector_indexes_capacity_map;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_write_requests;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_attribute_name_list;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_settings_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_target_tracking_scaling_policy_configuration_update;

+#[cfg(feature = "op_batch_execute_statement")]
 pub(crate) mod shape_batch_statement_error;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_binary_set_attribute_value;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_expression_attribute_name_map;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_global_secondary_index_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_global_secondary_indexes;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_table_witness_description;

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) mod shape_key_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_list_attribute_value;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_local_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_local_secondary_indexes;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_map_attribute_value;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_number_set_attribute_value;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_on_demand_throughput_override;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_provisioned_throughput_override;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_description;

+#[cfg(feature = "op_update_table")]
 pub(crate) mod shape_replica_global_secondary_index;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_global_secondary_index_settings_description_list;

+#[cfg(feature = "op_list_global_tables")]
 pub(crate) mod shape_replica_list;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub(crate) mod shape_string_set_attribute_value;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_vector_index_description;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_vector_index_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_vector_indexes;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_description_list;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) mod shape_csv_header_list;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_global_secondary_index_info;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_global_secondary_index_warm_throughput_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_local_secondary_index_info;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_description_list;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_global_secondary_index_description_list;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) mod shape_replica_global_secondary_index_settings_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_search_schema;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) mod shape_vector_index_info;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_policy_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_non_key_attribute_name_list;

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) mod shape_put_item_input_attribute_map;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_replica_global_secondary_index_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub(crate) mod shape_replica_global_secondary_index_description;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) mod shape_auto_scaling_target_tracking_scaling_policy_configuration_description;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) fn describe_endpoints_output_output_correct_errors(
     mut builder: crate::operation::describe_endpoints::builders::DescribeEndpointsOutputBuilder,
 ) -> crate::operation::describe_endpoints::builders::DescribeEndpointsOutputBuilder {
@@ -8,6 +9,7 @@
     builder
 }

+#[cfg(feature = "op_describe_import")]
 pub(crate) fn describe_import_output_output_correct_errors(
     mut builder: crate::operation::describe_import::builders::DescribeImportOutputBuilder,
 ) -> crate::operation::describe_import::builders::DescribeImportOutputBuilder {
@@ -20,6 +22,7 @@
     builder
 }

+#[cfg(feature = "op_import_table")]
 pub(crate) fn import_table_output_output_correct_errors(
     mut builder: crate::operation::import_table::builders::ImportTableOutputBuilder,
 ) -> crate::operation::import_table::builders::ImportTableOutputBuilder {
@@ -32,6 +35,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub(crate) fn backup_details_correct_errors(
     mut builder: crate::types::builders::BackupDetailsBuilder,
 ) -> crate::types::builders::BackupDetailsBuilder {
@@ -53,6 +61,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub(crate) fn continuous_backups_description_correct_errors(
     mut builder: crate::types::builders::ContinuousBackupsDescriptionBuilder,
 ) -> crate::types::builders::ContinuousBackupsDescriptionBuilder {
@@ -62,6 +71,7 @@
     builder
 }

+#[cfg(feature = "op_update_time_to_live")]
 pub(crate) fn time_to_live_specification_correct_errors(
     mut builder: crate::types::builders::TimeToLiveSpecificationBuilder,
 ) -> crate::types::builders::TimeToLiveSpecificationBuilder {
@@ -74,6 +84,7 @@
     builder
 }

+#[cfg(feature = "op_describe_endpoints")]
 pub(crate) fn endpoint_correct_errors(
     mut builder: crate::types::builders::EndpointBuilder,
 ) -> crate::types::builders::EndpointBuilder {
@@ -86,6 +97,7 @@
     builder
 }

+#[cfg(feature = "op_batch_get_item")]
 pub(crate) fn keys_and_attributes_correct_errors(
     mut builder: crate::types::builders::KeysAndAttributesBuilder,
 ) -> crate::types::builders::KeysAndAttributesBuilder {
@@ -95,6 +107,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) fn replica_settings_description_correct_errors(
     mut builder: crate::types::builders::ReplicaSettingsDescriptionBuilder,
 ) -> crate::types::builders::ReplicaSettingsDescriptionBuilder {
@@ -104,6 +120,14 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn restore_summary_correct_errors(
     mut builder: crate::types::builders::RestoreSummaryBuilder,
 ) -> crate::types::builders::RestoreSummaryBuilder {
@@ -116,6 +140,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub(crate) fn s3_bucket_source_correct_errors(
     mut builder: crate::types::builders::S3BucketSourceBuilder,
 ) -> crate::types::builders::S3BucketSourceBuilder {
@@ -125,6 +154,7 @@
     builder
 }

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub(crate) fn source_table_details_correct_errors(
     mut builder: crate::types::builders::SourceTableDetailsBuilder,
 ) -> crate::types::builders::SourceTableDetailsBuilder {
@@ -151,6 +181,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn stream_specification_correct_errors(
     mut builder: crate::types::builders::StreamSpecificationBuilder,
 ) -> crate::types::builders::StreamSpecificationBuilder {
@@ -160,6 +200,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub(crate) fn table_creation_parameters_correct_errors(
     mut builder: crate::types::builders::TableCreationParametersBuilder,
 ) -> crate::types::builders::TableCreationParametersBuilder {
@@ -175,6 +216,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
@@ -187,6 +233,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn attribute_definition_correct_errors(
     mut builder: crate::types::builders::AttributeDefinitionBuilder,
 ) -> crate::types::builders::AttributeDefinitionBuilder {
@@ -199,6 +255,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn key_schema_element_correct_errors(
     mut builder: crate::types::builders::KeySchemaElementBuilder,
 ) -> crate::types::builders::KeySchemaElementBuilder {
@@ -211,6 +279,16 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn provisioned_throughput_correct_errors(
     mut builder: crate::types::builders::ProvisionedThroughputBuilder,
 ) -> crate::types::builders::ProvisionedThroughputBuilder {
@@ -223,6 +301,7 @@
     builder
 }

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) fn delete_request_correct_errors(
     mut builder: crate::types::builders::DeleteRequestBuilder,
 ) -> crate::types::builders::DeleteRequestBuilder {
@@ -232,6 +311,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) fn global_secondary_index_correct_errors(
     mut builder: crate::types::builders::GlobalSecondaryIndexBuilder,
 ) -> crate::types::builders::GlobalSecondaryIndexBuilder {
@@ -250,6 +336,7 @@
     builder
 }

+#[cfg(feature = "op_batch_write_item")]
 pub(crate) fn put_request_correct_errors(
     mut builder: crate::types::builders::PutRequestBuilder,
 ) -> crate::types::builders::PutRequestBuilder {
@@ -259,6 +346,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub(crate) fn replica_global_secondary_index_settings_description_correct_errors(
     mut builder: crate::types::builders::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder,
 ) -> crate::types::builders::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder {
@@ -268,6 +359,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn vector_attribute_definition_correct_errors(
     mut builder: crate::types::builders::VectorAttributeDefinitionBuilder,
 ) -> crate::types::builders::VectorAttributeDefinitionBuilder {
@@ -277,6 +380,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub(crate) fn vector_index_correct_errors(
     mut builder: crate::types::builders::VectorIndexBuilder,
 ) -> crate::types::builders::VectorIndexBuilder {
@@ -306,6 +416,18 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub(crate) fn search_schema_element_correct_errors(
     mut builder: crate::types::builders::SearchSchemaElementBuilder,
 ) -> crate::types::builders::SearchSchemaElementBuilder {
@@ -318,6 +440,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub(crate) fn auto_scaling_target_tracking_scaling_policy_configuration_description_correct_errors(
     mut builder: crate::types::builders::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder,
 ) -> crate::types::builders::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,678 +1,2350 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_consumed_capacity::ReturnConsumedCapacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_item_collection_metrics::ReturnItemCollectionMetrics;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub use crate::types::_backup_details::BackupDetails;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_description::GlobalTableDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode::BillingMode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput::ProvisionedThroughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_specification::StreamSpecification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_specification::SseSpecification;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class::TableClass;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_warm_throughput::WarmThroughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput::OnDemandThroughput;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_settings_replication_mode::GlobalTableSettingsReplicationMode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_description::TableDescription;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_backup_description::BackupDescription;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 pub use crate::types::_conditional_operator::ConditionalOperator;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_return_value::ReturnValue;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_return_values_on_condition_check_failure::ReturnValuesOnConditionCheckFailure;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_consumed_capacity::ConsumedCapacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_item_collection_metrics::ItemCollectionMetrics;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_description::ContinuousBackupsDescription;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 pub use crate::types::_contributor_insights_status::ContributorInsightsStatus;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub use crate::types::_failure_exception::FailureException;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 pub use crate::types::_contributor_insights_mode::ContributorInsightsMode;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_description::ExportDescription;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_import_table_description::ImportTableDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_auto_scaling_description::TableAutoScalingDescription;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_description::TimeToLiveDescription;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub use crate::types::_enable_kinesis_streaming_configuration::EnableKinesisStreamingConfiguration;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 pub use crate::types::_destination_status::DestinationStatus;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_s3_sse_algorithm::S3SseAlgorithm;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_format::ExportFormat;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 pub use crate::types::_export_type::ExportType;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_incremental_export_specification::IncrementalExportSpecification;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_s3_bucket_source::S3BucketSource;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_input_format::InputFormat;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_format_options::InputFormatOptions;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_compression_type::InputCompressionType;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_table_creation_parameters::TableCreationParameters;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_type_filter::BackupTypeFilter;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_select::Select;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_vector_capacity::VectorCapacity;

+#[cfg(feature = "op_update_continuous_backups")]
 pub use crate::types::_point_in_time_recovery_specification::PointInTimeRecoverySpecification;

+#[cfg(feature = "op_update_contributor_insights")]
 pub use crate::types::_contributor_insights_action::ContributorInsightsAction;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_update::AutoScalingSettingsUpdate;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub use crate::types::_update_kinesis_streaming_configuration::UpdateKinesisStreamingConfiguration;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_multi_region_consistency::MultiRegionConsistency;

+#[cfg(feature = "op_update_time_to_live")]
 pub use crate::types::_time_to_live_specification::TimeToLiveSpecification;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_request::BatchStatementRequest;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_response::BatchStatementResponse;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_throttling_reason::ThrottlingReason;

+#[cfg(feature = "op_batch_get_item")]
 pub use crate::types::_keys_and_attributes::KeysAndAttributes;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 pub use crate::types::_backup_status::BackupStatus;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 pub use crate::types::_backup_type::BackupType;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub use crate::types::_replica::Replica;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_status::GlobalTableStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_attribute_definition::AttributeDefinition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_schema_element::KeySchemaElement;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_local_secondary_index::LocalSecondaryIndex;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_global_secondary_index::GlobalSecondaryIndex;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_view_type::StreamViewType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_type::SseType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_vector_index::VectorIndex;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_status::TableStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_description::ProvisionedThroughputDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode_summary::BillingModeSummary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_restore_summary::RestoreSummary;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_description::SseDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_archival_summary::ArchivalSummary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class_summary::TableClassSummary;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_warm_throughput_description::TableWarmThroughputDescription;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_details::SourceTableDetails;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_feature_details::SourceTableFeatureDetails;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_attribute_value::AttributeValue;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_expected_attribute_value::ExpectedAttributeValue;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_capacity::Capacity;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_status::ContinuousBackupsStatus;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_description::PointInTimeRecoveryDescription;

+#[cfg(feature = "op_describe_endpoints")]
 pub use crate::types::_endpoint::Endpoint;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 pub use crate::types::_export_status::ExportStatus;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_settings_description::ReplicaSettingsDescription;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_import_status::ImportStatus;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub use crate::types::_kinesis_data_stream_destination::KinesisDataStreamDestination;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_status::TimeToLiveStatus;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 pub use crate::types::_approximate_creation_date_time_precision::ApproximateCreationDateTimePrecision;

+#[cfg(feature = "op_execute_transaction")]
 pub use crate::types::_parameterized_statement::ParameterizedStatement;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub use crate::types::_item_response::ItemResponse;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::_cancellation_reason::CancellationReason;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_view_type::ExportViewType;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_csv_options::CsvOptions;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_summary::BackupSummary;

+#[cfg(feature = "op_list_contributor_insights")]
 pub use crate::types::_contributor_insights_summary::ContributorInsightsSummary;

+#[cfg(feature = "op_list_exports")]
 pub use crate::types::_export_summary::ExportSummary;

+#[cfg(feature = "op_list_global_tables")]
 pub use crate::types::_global_table::GlobalTable;

+#[cfg(feature = "op_list_imports")]
 pub use crate::types::_import_summary::ImportSummary;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_condition::Condition;

+#[cfg(feature = "op_search_vectors")]
 pub use crate::types::_search_result_item::SearchResultItem;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_transact_get_item::TransactGetItem;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_transact_write_item::TransactWriteItem;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_replica_update::ReplicaUpdate;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_update::AutoScalingPolicyUpdate;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_global_table_global_secondary_index_settings_update::GlobalTableGlobalSecondaryIndexSettingsUpdate;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_settings_update::ReplicaSettingsUpdate;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_value_update::AttributeValueUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_secondary_index_update::GlobalSecondaryIndexUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replication_group_update::ReplicationGroupUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_table_witness_group_update::GlobalTableWitnessGroupUpdate;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_vector_index_update::VectorIndexUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_global_secondary_index_auto_scaling_update::GlobalSecondaryIndexAutoScalingUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_auto_scaling_update::ReplicaAutoScalingUpdate;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error::BatchStatementError;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_write_request::WriteRequest;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_description::ReplicaDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_scalar_attribute_type::ScalarAttributeType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_type::KeyType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection::Projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_attribute_definition::VectorAttributeDefinition;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_distance_function::VectorDistanceFunction;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_local_secondary_index_description::LocalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_description::GlobalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_witness_description::GlobalTableWitnessDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_status::SseStatus;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_index_description::VectorIndexDescription;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 pub use crate::types::_comparison_operator::ComparisonOperator;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_status::PointInTimeRecoveryStatus;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_status::ReplicaStatus;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_description::AutoScalingSettingsDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_auto_scaling_description::ReplicaAutoScalingDescription;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_get::Get;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_condition_check::ConditionCheck;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_put::Put;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_delete::Delete;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_update::Update;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_create_replica_action::CreateReplicaAction;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_delete_replica_action::DeleteReplicaAction;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_update::AutoScalingTargetTrackingScalingPolicyConfigurationUpdate;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_action::AttributeAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_global_secondary_index_action::UpdateGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_secondary_index_action::CreateGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_secondary_index_action::DeleteGlobalSecondaryIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_replication_group_member_action::CreateReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_replication_group_member_action::UpdateReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_replication_group_member_action::DeleteReplicationGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_table_witness_group_member_action::CreateGlobalTableWitnessGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_table_witness_group_member_action::DeleteGlobalTableWitnessGroupMemberAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_vector_index_action::CreateVectorIndexAction;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_vector_index_action::DeleteVectorIndexAction;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error_code_enum::BatchStatementErrorCodeEnum;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_put_request::PutRequest;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_delete_request::DeleteRequest;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_override::ProvisionedThroughputOverride;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput_override::OnDemandThroughputOverride;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection_type::ProjectionType;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element::SearchSchemaElement;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_index_status::IndexStatus;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_warm_throughput_description::GlobalSecondaryIndexWarmThroughputDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_witness_status::WitnessStatus;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_local_secondary_index_info::LocalSecondaryIndexInfo;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_global_secondary_index_info::GlobalSecondaryIndexInfo;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_vector_index_info::VectorIndexInfo;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_global_secondary_index_settings_description::ReplicaGlobalSecondaryIndexSettingsDescription;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_global_secondary_index_settings_update::ReplicaGlobalSecondaryIndexSettingsUpdate;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_update::ReplicaGlobalSecondaryIndexAutoScalingUpdate;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_global_secondary_index_description::ReplicaGlobalSecondaryIndexDescription;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element_type::SearchSchemaElementType;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_description::AutoScalingPolicyDescription;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_description::ReplicaGlobalSecondaryIndexAutoScalingDescription;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replica_global_secondary_index::ReplicaGlobalSecondaryIndex;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_description::AutoScalingTargetTrackingScalingPolicyConfigurationDescription;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 mod _approximate_creation_date_time_precision;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _archival_summary;

+#[cfg(feature = "op_update_item")]
 mod _attribute_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _attribute_value;

+#[cfg(feature = "op_update_item")]
 mod _attribute_value_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_policy_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_policy_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_settings_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_target_tracking_scaling_policy_configuration_description;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _auto_scaling_target_tracking_scaling_policy_configuration_update;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _backup_description;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 mod _backup_details;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 mod _backup_status;

+#[cfg(feature = "op_list_backups")]
 mod _backup_summary;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_list_backups"
+))]
 mod _backup_type;

+#[cfg(feature = "op_list_backups")]
 mod _backup_type_filter;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_error;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_error_code_enum;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_request;

+#[cfg(feature = "op_batch_execute_statement")]
 mod _batch_statement_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _billing_mode;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _billing_mode_summary;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 mod _cancellation_reason;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _capacity;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 mod _comparison_operator;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 mod _condition;

+#[cfg(feature = "op_transact_write_items")]
 mod _condition_check;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_update_item"
+))]
 mod _conditional_operator;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _consumed_capacity;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_description;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_status;

+#[cfg(feature = "op_update_contributor_insights")]
 mod _contributor_insights_action;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 mod _contributor_insights_mode;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_list_contributor_insights",
+    feature = "op_update_contributor_insights"
+))]
 mod _contributor_insights_status;

+#[cfg(feature = "op_list_contributor_insights")]
 mod _contributor_insights_summary;

+#[cfg(feature = "op_update_table")]
 mod _create_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 mod _create_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 mod _create_replica_action;

+#[cfg(feature = "op_update_table")]
 mod _create_replication_group_member_action;

+#[cfg(feature = "op_update_table")]
 mod _create_vector_index_action;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _csv_options;

+#[cfg(feature = "op_transact_write_items")]
 mod _delete;

+#[cfg(feature = "op_update_table")]
 mod _delete_global_secondary_index_action;

+#[cfg(feature = "op_update_table")]
 mod _delete_global_table_witness_group_member_action;

+#[cfg(feature = "op_update_global_table")]
 mod _delete_replica_action;

+#[cfg(feature = "op_update_table")]
 mod _delete_replication_group_member_action;

+#[cfg(feature = "op_batch_write_item")]
 mod _delete_request;

+#[cfg(feature = "op_update_table")]
 mod _delete_vector_index_action;

+#[cfg(any(
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_update_kinesis_streaming_destination"
+))]
 mod _destination_status;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 mod _enable_kinesis_streaming_configuration;

+#[cfg(feature = "op_describe_endpoints")]
 mod _endpoint;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 mod _expected_attribute_value;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_format;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 mod _export_status;

+#[cfg(feature = "op_list_exports")]
 mod _export_summary;

+#[cfg(any(
+    feature = "op_describe_export",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_list_exports"
+))]
 mod _export_type;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _export_view_type;

+#[cfg(feature = "op_describe_contributor_insights")]
 mod _failure_exception;

+#[cfg(feature = "op_transact_get_items")]
 mod _get;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _global_secondary_index;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _global_secondary_index_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _global_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _global_secondary_index_info;

+#[cfg(feature = "op_update_table")]
 mod _global_secondary_index_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _global_secondary_index_warm_throughput_description;

+#[cfg(feature = "op_list_global_tables")]
 mod _global_table;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 mod _global_table_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _global_table_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _global_table_settings_replication_mode;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 mod _global_table_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _global_table_witness_description;

+#[cfg(feature = "op_update_table")]
 mod _global_table_witness_group_update;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _import_status;

+#[cfg(feature = "op_list_imports")]
 mod _import_summary;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _import_table_description;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _incremental_export_specification;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _index_status;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _input_compression_type;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _input_format;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _input_format_options;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _item_collection_metrics;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 mod _item_response;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _key_schema_element;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _key_type;

+#[cfg(feature = "op_batch_get_item")]
 mod _keys_and_attributes;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 mod _kinesis_data_stream_destination;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _local_secondary_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _local_secondary_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _local_secondary_index_info;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _multi_region_consistency;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _on_demand_throughput;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _on_demand_throughput_override;

+#[cfg(feature = "op_execute_transaction")]
 mod _parameterized_statement;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _point_in_time_recovery_description;

+#[cfg(feature = "op_update_continuous_backups")]
 mod _point_in_time_recovery_specification;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 mod _point_in_time_recovery_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _projection;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _projection_type;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _provisioned_throughput_override;

+#[cfg(feature = "op_transact_write_items")]
 mod _put;

+#[cfg(feature = "op_batch_write_item")]
 mod _put_request;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 mod _replica;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_auto_scaling_description;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _replica_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _replica_description;

+#[cfg(feature = "op_update_table")]
 mod _replica_global_secondary_index;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_global_secondary_index_auto_scaling_description;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 mod _replica_global_secondary_index_auto_scaling_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _replica_global_secondary_index_description;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 mod _replica_global_secondary_index_settings_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _replica_global_secondary_index_settings_update;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 mod _replica_settings_description;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _replica_settings_update;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _replica_status;

+#[cfg(feature = "op_update_global_table")]
 mod _replica_update;

+#[cfg(feature = "op_update_table")]
 mod _replication_group_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _restore_summary;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_consumed_capacity;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_item_collection_metrics;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 mod _return_value;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _return_values_on_condition_check_failure;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 mod _s3_bucket_source;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 mod _s3_sse_algorithm;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _scalar_attribute_type;

+#[cfg(feature = "op_search_vectors")]
 mod _search_result_item;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _search_schema_element;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _search_schema_element_type;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 mod _select;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _source_table_details;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _source_table_feature_details;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_status;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _sse_type;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _stream_specification;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _stream_view_type;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _table_auto_scaling_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _table_class;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 mod _table_class_summary;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 mod _table_creation_parameters;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _table_description;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 mod _table_status;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 mod _table_warm_throughput_description;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _throttling_reason;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 mod _time_to_live_description;

+#[cfg(feature = "op_update_time_to_live")]
 mod _time_to_live_specification;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 mod _time_to_live_status;

+#[cfg(feature = "op_transact_get_items")]
 mod _transact_get_item;

+#[cfg(feature = "op_transact_write_items")]
 mod _transact_write_item;

+#[cfg(feature = "op_transact_write_items")]
 mod _update;

+#[cfg(feature = "op_update_table")]
 mod _update_global_secondary_index_action;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 mod _update_kinesis_streaming_configuration;

+#[cfg(feature = "op_update_table")]
 mod _update_replication_group_member_action;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_attribute_definition;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _vector_capacity;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_distance_function;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _vector_index;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _vector_index_description;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 mod _vector_index_info;

+#[cfg(feature = "op_update_table")]
 mod _vector_index_update;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _warm_throughput;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 mod _witness_status;

+#[cfg(feature = "op_batch_write_item")]
 mod _write_request;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,246 +1,757 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup"
+))]
 pub use crate::types::_backup_details::BackupDetailsBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_describe_global_table",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::_global_table_description::GlobalTableDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput::ProvisionedThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_stream_specification::StreamSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_specification::SseSpecificationBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_warm_throughput::WarmThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput::OnDemandThroughputBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_description::TableDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_backup_description::BackupDescriptionBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_consumed_capacity::ConsumedCapacityBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_item_collection_metrics::ItemCollectionMetricsBuilder;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_continuous_backups_description::ContinuousBackupsDescriptionBuilder;

+#[cfg(feature = "op_describe_contributor_insights")]
 pub use crate::types::_failure_exception::FailureExceptionBuilder;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_export_description::ExportDescriptionBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_import_table_description::ImportTableDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_table_auto_scaling_description::TableAutoScalingDescriptionBuilder;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_describe_time_to_live"
+))]
 pub use crate::types::_time_to_live_description::TimeToLiveDescriptionBuilder;

+#[cfg(any(
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination"
+))]
 pub use crate::types::_enable_kinesis_streaming_configuration::EnableKinesisStreamingConfigurationBuilder;

+#[cfg(any(feature = "op_describe_export", feature = "op_export_table_to_point_in_time"))]
 pub use crate::types::_incremental_export_specification::IncrementalExportSpecificationBuilder;

+#[cfg(any(
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_list_imports"
+))]
 pub use crate::types::_s3_bucket_source::S3BucketSourceBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_input_format_options::InputFormatOptionsBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_table_creation_parameters::TableCreationParametersBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_vector_capacity::VectorCapacityBuilder;

+#[cfg(feature = "op_update_continuous_backups")]
 pub use crate::types::_point_in_time_recovery_specification::PointInTimeRecoverySpecificationBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_update::AutoScalingSettingsUpdateBuilder;

+#[cfg(feature = "op_update_kinesis_streaming_destination")]
 pub use crate::types::_update_kinesis_streaming_configuration::UpdateKinesisStreamingConfigurationBuilder;

+#[cfg(feature = "op_update_time_to_live")]
 pub use crate::types::_time_to_live_specification::TimeToLiveSpecificationBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_request::BatchStatementRequestBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_response::BatchStatementResponseBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_throttling_reason::ThrottlingReasonBuilder;

+#[cfg(feature = "op_batch_get_item")]
 pub use crate::types::_keys_and_attributes::KeysAndAttributesBuilder;

+#[cfg(any(feature = "op_create_global_table", feature = "op_list_global_tables"))]
 pub use crate::types::_replica::ReplicaBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_attribute_definition::AttributeDefinitionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_key_schema_element::KeySchemaElementBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_local_secondary_index::LocalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_global_secondary_index::GlobalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_list_tags_of_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_describe_import",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::_vector_index::VectorIndexBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_description::ProvisionedThroughputDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_billing_mode_summary::BillingModeSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_restore_summary::RestoreSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_sse_description::SseDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_archival_summary::ArchivalSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_class_summary::TableClassSummaryBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_table_warm_throughput_description::TableWarmThroughputDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_details::SourceTableDetailsBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_source_table_feature_details::SourceTableFeatureDetailsBuilder;

+#[cfg(any(feature = "op_delete_item", feature = "op_put_item", feature = "op_update_item"))]
 pub use crate::types::_expected_attribute_value::ExpectedAttributeValueBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::_capacity::CapacityBuilder;

+#[cfg(any(feature = "op_describe_continuous_backups", feature = "op_update_continuous_backups"))]
 pub use crate::types::_point_in_time_recovery_description::PointInTimeRecoveryDescriptionBuilder;

+#[cfg(feature = "op_describe_endpoints")]
 pub use crate::types::_endpoint::EndpointBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_settings_description::ReplicaSettingsDescriptionBuilder;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 pub use crate::types::_kinesis_data_stream_destination::KinesisDataStreamDestinationBuilder;

+#[cfg(feature = "op_execute_transaction")]
 pub use crate::types::_parameterized_statement::ParameterizedStatementBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_get_items"))]
 pub use crate::types::_item_response::ItemResponseBuilder;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::_cancellation_reason::CancellationReasonBuilder;

+#[cfg(any(feature = "op_describe_import", feature = "op_import_table"))]
 pub use crate::types::_csv_options::CsvOptionsBuilder;

+#[cfg(feature = "op_list_backups")]
 pub use crate::types::_backup_summary::BackupSummaryBuilder;

+#[cfg(feature = "op_list_contributor_insights")]
 pub use crate::types::_contributor_insights_summary::ContributorInsightsSummaryBuilder;

+#[cfg(feature = "op_list_exports")]
 pub use crate::types::_export_summary::ExportSummaryBuilder;

+#[cfg(feature = "op_list_global_tables")]
 pub use crate::types::_global_table::GlobalTableBuilder;

+#[cfg(feature = "op_list_imports")]
 pub use crate::types::_import_summary::ImportSummaryBuilder;

+#[cfg(any(feature = "op_query", feature = "op_scan"))]
 pub use crate::types::_condition::ConditionBuilder;

+#[cfg(feature = "op_search_vectors")]
 pub use crate::types::_search_result_item::SearchResultItemBuilder;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_transact_get_item::TransactGetItemBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_transact_write_item::TransactWriteItemBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_replica_update::ReplicaUpdateBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_update::AutoScalingPolicyUpdateBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_global_table_global_secondary_index_settings_update::GlobalTableGlobalSecondaryIndexSettingsUpdateBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_settings_update::ReplicaSettingsUpdateBuilder;

+#[cfg(feature = "op_update_item")]
 pub use crate::types::_attribute_value_update::AttributeValueUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_secondary_index_update::GlobalSecondaryIndexUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replication_group_update::ReplicationGroupUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_global_table_witness_group_update::GlobalTableWitnessGroupUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_vector_index_update::VectorIndexUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_global_secondary_index_auto_scaling_update::GlobalSecondaryIndexAutoScalingUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_auto_scaling_update::ReplicaAutoScalingUpdateBuilder;

+#[cfg(feature = "op_batch_execute_statement")]
 pub use crate::types::_batch_statement_error::BatchStatementErrorBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_write_request::WriteRequestBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_description::ReplicaDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_projection::ProjectionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_attribute_definition::VectorAttributeDefinitionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_local_secondary_index_description::LocalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_description::GlobalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_table_witness_description::GlobalTableWitnessDescriptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_vector_index_description::VectorIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_settings_description::AutoScalingSettingsDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_auto_scaling_description::ReplicaAutoScalingDescriptionBuilder;

+#[cfg(feature = "op_transact_get_items")]
 pub use crate::types::_get::GetBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_condition_check::ConditionCheckBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_put::PutBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_delete::DeleteBuilder;

+#[cfg(feature = "op_transact_write_items")]
 pub use crate::types::_update::UpdateBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_create_replica_action::CreateReplicaActionBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::_delete_replica_action::DeleteReplicaActionBuilder;

+#[cfg(any(
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_update::AutoScalingTargetTrackingScalingPolicyConfigurationUpdateBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_global_secondary_index_action::UpdateGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_secondary_index_action::CreateGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_secondary_index_action::DeleteGlobalSecondaryIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_replication_group_member_action::CreateReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_update_replication_group_member_action::UpdateReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_replication_group_member_action::DeleteReplicationGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_global_table_witness_group_member_action::CreateGlobalTableWitnessGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_global_table_witness_group_member_action::DeleteGlobalTableWitnessGroupMemberActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_create_vector_index_action::CreateVectorIndexActionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_delete_vector_index_action::DeleteVectorIndexActionBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_put_request::PutRequestBuilder;

+#[cfg(feature = "op_batch_write_item")]
 pub use crate::types::_delete_request::DeleteRequestBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_provisioned_throughput_override::ProvisionedThroughputOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_on_demand_throughput_override::OnDemandThroughputOverrideBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_import",
+    feature = "op_describe_table",
+    feature = "op_import_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_table"
+))]
 pub use crate::types::_search_schema_element::SearchSchemaElementBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_global_secondary_index_warm_throughput_description::GlobalSecondaryIndexWarmThroughputDescriptionBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_local_secondary_index_info::LocalSecondaryIndexInfoBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_global_secondary_index_info::GlobalSecondaryIndexInfoBuilder;

+#[cfg(any(feature = "op_delete_backup", feature = "op_describe_backup"))]
 pub use crate::types::_vector_index_info::VectorIndexInfoBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::_replica_global_secondary_index_settings_description::ReplicaGlobalSecondaryIndexSettingsDescriptionBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::_replica_global_secondary_index_settings_update::ReplicaGlobalSecondaryIndexSettingsUpdateBuilder;

+#[cfg(feature = "op_update_table_replica_auto_scaling")]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_update::ReplicaGlobalSecondaryIndexAutoScalingUpdateBuilder;

+#[cfg(any(
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_table",
+    feature = "op_describe_global_table",
+    feature = "op_describe_table",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_global_table",
+    feature = "op_update_table"
+))]
 pub use crate::types::_replica_global_secondary_index_description::ReplicaGlobalSecondaryIndexDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_policy_description::AutoScalingPolicyDescriptionBuilder;

+#[cfg(any(
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_replica_global_secondary_index_auto_scaling_description::ReplicaGlobalSecondaryIndexAutoScalingDescriptionBuilder;

+#[cfg(feature = "op_update_table")]
 pub use crate::types::_replica_global_secondary_index::ReplicaGlobalSecondaryIndexBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_table_replica_auto_scaling"
+))]
 pub use crate::types::_auto_scaling_target_tracking_scaling_policy_configuration_description::AutoScalingTargetTrackingScalingPolicyConfigurationDescriptionBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,142 +1,760 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_internal_server_error::InternalServerError;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_request_limit_exceeded::RequestLimitExceeded;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_invalid_endpoint_exception::InvalidEndpointException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_provisioned_throughput_exceeded_exception::ProvisionedThroughputExceededException;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_item_collection_size_limit_exceeded_exception::ItemCollectionSizeLimitExceededException;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_replicated_write_conflict_exception::ReplicatedWriteConflictException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_in_use_exception::BackupInUseException;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub use crate::types::error::_continuous_backups_unavailable_exception::ContinuousBackupsUnavailableException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_in_use_exception::TableInUseException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::error::_table_not_found_exception::TableNotFoundException;

+#[cfg(feature = "op_create_global_table")]
 pub use crate::types::error::_global_table_already_exists_exception::GlobalTableAlreadyExistsException;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_in_use_exception::ResourceInUseException;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_not_found_exception::BackupNotFoundException;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_conditional_check_failed_exception::ConditionalCheckFailedException;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_transaction_conflict_exception::TransactionConflictException;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub use crate::types::error::_policy_not_found_exception::PolicyNotFoundException;

+#[cfg(feature = "op_describe_export")]
 pub use crate::types::error::_export_not_found_exception::ExportNotFoundException;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::error::_global_table_not_found_exception::GlobalTableNotFoundException;

+#[cfg(feature = "op_describe_import")]
 pub use crate::types::error::_import_not_found_exception::ImportNotFoundException;

+#[cfg(feature = "op_execute_statement")]
 pub use crate::types::error::_duplicate_item_exception::DuplicateItemException;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_idempotent_parameter_mismatch_exception::IdempotentParameterMismatchException;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::error::_transaction_canceled_exception::TransactionCanceledException;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_transaction_in_progress_exception::TransactionInProgressException;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_export_conflict_exception::ExportConflictException;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_invalid_export_time_exception::InvalidExportTimeException;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_point_in_time_recovery_unavailable_exception::PointInTimeRecoveryUnavailableException;

+#[cfg(feature = "op_import_table")]
 pub use crate::types::error::_import_conflict_exception::ImportConflictException;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_already_exists_exception::TableAlreadyExistsException;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub use crate::types::error::_invalid_restore_time_exception::InvalidRestoreTimeException;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::error::_replica_already_exists_exception::ReplicaAlreadyExistsException;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub use crate::types::error::_replica_not_found_exception::ReplicaNotFoundException;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::error::_index_not_found_exception::IndexNotFoundException;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 mod _backup_in_use_exception;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 mod _backup_not_found_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _conditional_check_failed_exception;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 mod _continuous_backups_unavailable_exception;

+#[cfg(feature = "op_execute_statement")]
 mod _duplicate_item_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod _export_conflict_exception;

+#[cfg(feature = "op_describe_export")]
 mod _export_not_found_exception;

+#[cfg(feature = "op_create_global_table")]
 mod _global_table_already_exists_exception;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 mod _global_table_not_found_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 mod _idempotent_parameter_mismatch_exception;

+#[cfg(feature = "op_import_table")]
 mod _import_conflict_exception;

+#[cfg(feature = "op_describe_import")]
 mod _import_not_found_exception;

+#[cfg(feature = "op_update_global_table_settings")]
 mod _index_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _internal_server_error;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 mod _invalid_endpoint_exception;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 mod _invalid_export_time_exception;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 mod _invalid_restore_time_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _item_collection_size_limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _point_in_time_recovery_unavailable_exception;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 mod _policy_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _provisioned_throughput_exceeded_exception;

+#[cfg(feature = "op_update_global_table")]
 mod _replica_already_exists_exception;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 mod _replica_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _replicated_write_conflict_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _request_limit_exceeded;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _resource_in_use_exception;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _table_already_exists_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 mod _table_in_use_exception;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 mod _table_not_found_exception;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 mod _throttling_exception;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 mod _transaction_canceled_exception;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 mod _transaction_conflict_exception;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 mod _transaction_in_progress_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,70 +1,379 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_exports",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_internal_server_error::InternalServerErrorBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_request_limit_exceeded::RequestLimitExceededBuilder;

+#[cfg(any(
+    feature = "op_batch_execute_statement",
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_backup",
+    feature = "op_describe_continuous_backups",
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_limits",
+    feature = "op_describe_table",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_backups",
+    feature = "op_list_global_tables",
+    feature = "op_list_tables",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_scan",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_invalid_endpoint_exception::InvalidEndpointExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_put_item",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_provisioned_throughput_exceeded_exception::ProvisionedThroughputExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_get_item",
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table",
+    feature = "op_describe_table_replica_auto_scaling",
+    feature = "op_describe_time_to_live",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_execute_statement",
+    feature = "op_execute_transaction",
+    feature = "op_get_item",
+    feature = "op_get_resource_policy",
+    feature = "op_list_contributor_insights",
+    feature = "op_list_tags_of_resource",
+    feature = "op_put_item",
+    feature = "op_put_resource_policy",
+    feature = "op_query",
+    feature = "op_scan",
+    feature = "op_search_vectors",
+    feature = "op_tag_resource",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items",
+    feature = "op_untag_resource",
+    feature = "op_update_contributor_insights",
+    feature = "op_update_item",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_item_collection_size_limit_exceeded_exception::ItemCollectionSizeLimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_batch_write_item",
+    feature = "op_delete_item",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_replicated_write_conflict_exception::ReplicatedWriteConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_delete_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_in_use_exception::BackupInUseExceptionBuilder;

+#[cfg(any(feature = "op_create_backup", feature = "op_update_continuous_backups"))]
 pub use crate::types::error::_continuous_backups_unavailable_exception::ContinuousBackupsUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_create_table",
+    feature = "op_delete_backup",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_describe_export",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_import_table",
+    feature = "op_list_exports",
+    feature = "op_list_imports",
+    feature = "op_put_resource_policy",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_in_use_exception::TableInUseExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_backup",
+    feature = "op_create_global_table",
+    feature = "op_describe_continuous_backups",
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time",
+    feature = "op_update_continuous_backups",
+    feature = "op_update_global_table"
+))]
 pub use crate::types::error::_table_not_found_exception::TableNotFoundExceptionBuilder;

+#[cfg(feature = "op_create_global_table")]
 pub use crate::types::error::_global_table_already_exists_exception::GlobalTableAlreadyExistsExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_table",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_table",
+    feature = "op_disable_kinesis_streaming_destination",
+    feature = "op_enable_kinesis_streaming_destination",
+    feature = "op_import_table",
+    feature = "op_put_resource_policy",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_global_table_settings",
+    feature = "op_update_kinesis_streaming_destination",
+    feature = "op_update_table",
+    feature = "op_update_table_replica_auto_scaling",
+    feature = "op_update_time_to_live"
+))]
 pub use crate::types::error::_resource_in_use_exception::ResourceInUseExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_backup",
+    feature = "op_describe_backup",
+    feature = "op_restore_table_from_backup"
+))]
 pub use crate::types::error::_backup_not_found_exception::BackupNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_conditional_check_failed_exception::ConditionalCheckFailedExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_item",
+    feature = "op_execute_statement",
+    feature = "op_put_item",
+    feature = "op_update_item"
+))]
 pub use crate::types::error::_transaction_conflict_exception::TransactionConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_delete_resource_policy",
+    feature = "op_get_resource_policy",
+    feature = "op_put_resource_policy"
+))]
 pub use crate::types::error::_policy_not_found_exception::PolicyNotFoundExceptionBuilder;

+#[cfg(feature = "op_describe_export")]
 pub use crate::types::error::_export_not_found_exception::ExportNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_describe_global_table",
+    feature = "op_describe_global_table_settings",
+    feature = "op_update_global_table",
+    feature = "op_update_global_table_settings"
+))]
 pub use crate::types::error::_global_table_not_found_exception::GlobalTableNotFoundExceptionBuilder;

+#[cfg(feature = "op_describe_import")]
 pub use crate::types::error::_import_not_found_exception::ImportNotFoundExceptionBuilder;

+#[cfg(feature = "op_execute_statement")]
 pub use crate::types::error::_duplicate_item_exception::DuplicateItemExceptionBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_idempotent_parameter_mismatch_exception::IdempotentParameterMismatchExceptionBuilder;

+#[cfg(any(
+    feature = "op_execute_transaction",
+    feature = "op_transact_get_items",
+    feature = "op_transact_write_items"
+))]
 pub use crate::types::error::_transaction_canceled_exception::TransactionCanceledExceptionBuilder;

+#[cfg(any(feature = "op_execute_transaction", feature = "op_transact_write_items"))]
 pub use crate::types::error::_transaction_in_progress_exception::TransactionInProgressExceptionBuilder;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_export_conflict_exception::ExportConflictExceptionBuilder;

+#[cfg(feature = "op_export_table_to_point_in_time")]
 pub use crate::types::error::_invalid_export_time_exception::InvalidExportTimeExceptionBuilder;

+#[cfg(any(
+    feature = "op_export_table_to_point_in_time",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_point_in_time_recovery_unavailable_exception::PointInTimeRecoveryUnavailableExceptionBuilder;

+#[cfg(feature = "op_import_table")]
 pub use crate::types::error::_import_conflict_exception::ImportConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_restore_table_from_backup",
+    feature = "op_restore_table_to_point_in_time"
+))]
 pub use crate::types::error::_table_already_exists_exception::TableAlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_restore_table_to_point_in_time")]
 pub use crate::types::error::_invalid_restore_time_exception::InvalidRestoreTimeExceptionBuilder;

+#[cfg(feature = "op_update_global_table")]
 pub use crate::types::error::_replica_already_exists_exception::ReplicaAlreadyExistsExceptionBuilder;

+#[cfg(any(feature = "op_update_global_table", feature = "op_update_global_table_settings"))]
 pub use crate::types::error::_replica_not_found_exception::ReplicaNotFoundExceptionBuilder;

+#[cfg(feature = "op_update_global_table_settings")]
 pub use crate::types::error::_index_not_found_exception::IndexNotFoundExceptionBuilder;
diff --git a/src/waiters.rs b/src/waiters.rs
--- a/src/waiters.rs
+++ b/src/waiters.rs
@@ -1,23 +1,36 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Supporting types for the `contributor_insights_enabled` waiter.
 pub mod contributor_insights_enabled;

+#[cfg(feature = "op_describe_export")]
 /// Supporting types for the `export_completed` waiter.
 pub mod export_completed;

+#[cfg(feature = "op_describe_import")]
 /// Supporting types for the `import_completed` waiter.
 pub mod import_completed;

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Supporting types for the `kinesis_streaming_destination_active` waiter.
 pub mod kinesis_streaming_destination_active;

+#[cfg(feature = "op_describe_table")]
 /// Supporting types for the `table_exists` waiter.
 pub mod table_exists;

+#[cfg(feature = "op_describe_table")]
 /// Supporting types for the `table_not_exists` waiter.
 pub mod table_not_exists;

+#[cfg(any(
+    feature = "op_describe_contributor_insights",
+    feature = "op_describe_export",
+    feature = "op_describe_import",
+    feature = "op_describe_kinesis_streaming_destination",
+    feature = "op_describe_table"
+))]
 #[allow(clippy::needless_lifetimes)]
 #[allow(clippy::let_and_return)]
 pub(crate) mod matchers;
diff --git a/src/waiters/matchers.rs b/src/waiters/matchers.rs
--- a/src/waiters/matchers.rs
+++ b/src/waiters/matchers.rs
@@ -1,5 +1,6 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Matcher union: {"output":{"path":"ContributorInsightsStatus","expected":"ENABLED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_contributor_insights_57787899eaa02d958(
     _result: ::std::result::Result<
@@ -26,6 +27,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_contributor_insights")]
 /// Matcher union: {"output":{"path":"ContributorInsightsStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_contributor_insights_5ba948784ca4cb322(
     _result: ::std::result::Result<
@@ -52,6 +54,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_export")]
 /// Matcher union: {"output":{"path":"ExportDescription.ExportStatus","expected":"COMPLETED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_export_a4219f96bc64309c4(
     _result: ::std::result::Result<
@@ -79,6 +82,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_export")]
 /// Matcher union: {"output":{"path":"ExportDescription.ExportStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_export_8d899fd0681b891e9(
     _result: ::std::result::Result<
@@ -106,6 +110,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"COMPLETED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_6175a829c57972dc3(
     _result: ::std::result::Result<
@@ -133,6 +138,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"FAILED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_ba4301a7fe05a6956(
     _result: ::std::result::Result<
@@ -160,6 +166,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_import")]
 /// Matcher union: {"output":{"path":"ImportTableDescription.ImportStatus","expected":"CANCELLED","comparator":"stringEquals"}}
 pub(crate) fn match_describe_import_b4c5c86bd60d42041(
     _result: ::std::result::Result<
@@ -187,6 +194,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Matcher union: {"output":{"path":"KinesisDataStreamDestinations[].DestinationStatus","expected":"ACTIVE","comparator":"anyStringEquals"}}
 pub(crate) fn match_describe_kinesis_streaming_destination_56e18114fb2c2cf5a(
     _result: ::std::result::Result<
@@ -228,6 +236,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_kinesis_streaming_destination")]
 /// Matcher union: {"output":{"path":"length(KinesisDataStreamDestinations) > `0`  && length(KinesisDataStreamDestinations[?DestinationStatus == 'DISABLED' || DestinationStatus == 'ENABLE_FAILED']) ==  length(KinesisDataStreamDestinations)","expected":"true","comparator":"booleanEquals"}}
 pub(crate) fn match_describe_kinesis_streaming_destination_ce975c8fb2b65f98f(
     _result: ::std::result::Result<
@@ -282,6 +291,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_table")]
 /// Matcher union: {"output":{"path":"Table.TableStatus","expected":"ACTIVE","comparator":"stringEquals"}}
 pub(crate) fn match_describe_table_0429b99996ae6dab6(
     _result: ::std::result::Result<
@@ -309,6 +319,7 @@
         .unwrap_or_default()
 }

+#[cfg(feature = "op_describe_table")]
 /// Matcher union: {"errorType":"ResourceNotFoundException"}
 pub(crate) fn match_describe_table_1cce2c05524fb92d4(
     _result: ::std::result::Result<
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
