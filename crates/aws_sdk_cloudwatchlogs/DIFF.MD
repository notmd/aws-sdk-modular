# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/cloudwatchlogs`
- model: `aws-models/cloudwatch-logs.json`
- package: `aws-sdk-cloudwatchlogs`
- library: `aws_sdk_cloudwatchlogs`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_associate_kms_key`: `AssociateKmsKey`
- `op_associate_source_to_s3_table_integration`: `AssociateSourceToS3TableIntegration`
- `op_cancel_export_task`: `CancelExportTask`
- `op_cancel_import_task`: `CancelImportTask`
- `op_create_delivery`: `CreateDelivery`
- `op_create_export_task`: `CreateExportTask`
- `op_create_import_task`: `CreateImportTask`
- `op_create_log_anomaly_detector`: `CreateLogAnomalyDetector`
- `op_create_log_group`: `CreateLogGroup`
- `op_create_log_stream`: `CreateLogStream`
- `op_create_lookup_table`: `CreateLookupTable`
- `op_create_scheduled_query`: `CreateScheduledQuery`
- `op_delete_account_policy`: `DeleteAccountPolicy`
- `op_delete_data_protection_policy`: `DeleteDataProtectionPolicy`
- `op_delete_delivery`: `DeleteDelivery`
- `op_delete_delivery_destination`: `DeleteDeliveryDestination`
- `op_delete_delivery_destination_policy`: `DeleteDeliveryDestinationPolicy`
- `op_delete_delivery_source`: `DeleteDeliverySource`
- `op_delete_destination`: `DeleteDestination`
- `op_delete_index_policy`: `DeleteIndexPolicy`
- `op_delete_integration`: `DeleteIntegration`
- `op_delete_log_anomaly_detector`: `DeleteLogAnomalyDetector`
- `op_delete_log_group`: `DeleteLogGroup`
- `op_delete_log_stream`: `DeleteLogStream`
- `op_delete_lookup_table`: `DeleteLookupTable`
- `op_delete_metric_filter`: `DeleteMetricFilter`
- `op_delete_query_definition`: `DeleteQueryDefinition`
- `op_delete_resource_policy`: `DeleteResourcePolicy`
- `op_delete_retention_policy`: `DeleteRetentionPolicy`
- `op_delete_scheduled_query`: `DeleteScheduledQuery`
- `op_delete_subscription_filter`: `DeleteSubscriptionFilter`
- `op_delete_syslog_configuration`: `DeleteSyslogConfiguration`
- `op_delete_transformer`: `DeleteTransformer`
- `op_describe_account_policies`: `DescribeAccountPolicies`
- `op_describe_configuration_templates`: `DescribeConfigurationTemplates`
- `op_describe_deliveries`: `DescribeDeliveries`
- `op_describe_delivery_destinations`: `DescribeDeliveryDestinations`
- `op_describe_delivery_sources`: `DescribeDeliverySources`
- `op_describe_destinations`: `DescribeDestinations`
- `op_describe_export_tasks`: `DescribeExportTasks`
- `op_describe_field_indexes`: `DescribeFieldIndexes`
- `op_describe_import_task_batches`: `DescribeImportTaskBatches`
- `op_describe_import_tasks`: `DescribeImportTasks`
- `op_describe_index_policies`: `DescribeIndexPolicies`
- `op_describe_log_groups`: `DescribeLogGroups`
- `op_describe_log_streams`: `DescribeLogStreams`
- `op_describe_lookup_tables`: `DescribeLookupTables`
- `op_describe_metric_filters`: `DescribeMetricFilters`
- `op_describe_queries`: `DescribeQueries`
- `op_describe_query_definitions`: `DescribeQueryDefinitions`
- `op_describe_resource_policies`: `DescribeResourcePolicies`
- `op_describe_subscription_filters`: `DescribeSubscriptionFilters`
- `op_disassociate_kms_key`: `DisassociateKmsKey`
- `op_disassociate_source_from_s3_table_integration`: `DisassociateSourceFromS3TableIntegration`
- `op_filter_log_events`: `FilterLogEvents`
- `op_get_data_protection_policy`: `GetDataProtectionPolicy`
- `op_get_delivery`: `GetDelivery`
- `op_get_delivery_destination`: `GetDeliveryDestination`
- `op_get_delivery_destination_policy`: `GetDeliveryDestinationPolicy`
- `op_get_delivery_source`: `GetDeliverySource`
- `op_get_integration`: `GetIntegration`
- `op_get_log_anomaly_detector`: `GetLogAnomalyDetector`
- `op_get_log_events`: `GetLogEvents`
- `op_get_log_fields`: `GetLogFields`
- `op_get_log_group_fields`: `GetLogGroupFields`
- `op_get_log_object`: `GetLogObject`
- `op_get_log_record`: `GetLogRecord`
- `op_get_lookup_table`: `GetLookupTable`
- `op_get_query_results`: `GetQueryResults`
- `op_get_scheduled_query`: `GetScheduledQuery`
- `op_get_scheduled_query_history`: `GetScheduledQueryHistory`
- `op_get_storage_tier_policy`: `GetStorageTierPolicy`
- `op_get_transformer`: `GetTransformer`
- `op_list_aggregate_log_group_summaries`: `ListAggregateLogGroupSummaries`
- `op_list_anomalies`: `ListAnomalies`
- `op_list_integrations`: `ListIntegrations`
- `op_list_log_anomaly_detectors`: `ListLogAnomalyDetectors`
- `op_list_log_groups`: `ListLogGroups`
- `op_list_log_groups_for_query`: `ListLogGroupsForQuery`
- `op_list_scheduled_queries`: `ListScheduledQueries`
- `op_list_sources_for_s3_table_integration`: `ListSourcesForS3TableIntegration`
- `op_list_syslog_configurations`: `ListSyslogConfigurations`
- `op_list_tags_for_resource`: `ListTagsForResource`
- `op_list_tags_log_group`: `ListTagsLogGroup`
- `op_put_account_policy`: `PutAccountPolicy`
- `op_put_bearer_token_authentication`: `PutBearerTokenAuthentication`
- `op_put_data_protection_policy`: `PutDataProtectionPolicy`
- `op_put_delivery_destination`: `PutDeliveryDestination`
- `op_put_delivery_destination_policy`: `PutDeliveryDestinationPolicy`
- `op_put_delivery_source`: `PutDeliverySource`
- `op_put_destination`: `PutDestination`
- `op_put_destination_policy`: `PutDestinationPolicy`
- `op_put_index_policy`: `PutIndexPolicy`
- `op_put_integration`: `PutIntegration`
- `op_put_log_events`: `PutLogEvents`
- `op_put_log_group_deletion_protection`: `PutLogGroupDeletionProtection`
- `op_put_metric_filter`: `PutMetricFilter`
- `op_put_query_definition`: `PutQueryDefinition`
- `op_put_resource_policy`: `PutResourcePolicy`
- `op_put_retention_policy`: `PutRetentionPolicy`
- `op_put_storage_tier_policy`: `PutStorageTierPolicy`
- `op_put_subscription_filter`: `PutSubscriptionFilter`
- `op_put_syslog_configuration`: `PutSyslogConfiguration`
- `op_put_transformer`: `PutTransformer`
- `op_start_live_tail`: `StartLiveTail`
- `op_start_query`: `StartQuery`
- `op_stop_query`: `StopQuery`
- `op_tag_log_group`: `TagLogGroup`
- `op_tag_resource`: `TagResource`
- `op_test_metric_filter`: `TestMetricFilter`
- `op_test_transformer`: `TestTransformer`
- `op_untag_log_group`: `UntagLogGroup`
- `op_untag_resource`: `UntagResource`
- `op_update_anomaly`: `UpdateAnomaly`
- `op_update_delivery_configuration`: `UpdateDeliveryConfiguration`
- `op_update_log_anomaly_detector`: `UpdateLogAnomalyDetector`
- `op_update_lookup_table`: `UpdateLookupTable`
- `op_update_scheduled_query`: `UpdateScheduledQuery`

## Changed files

- `Cargo.toml`
- `src/client.rs`
- `src/error_meta.rs`
- `src/event_stream_serde.rs`
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
@@ -19,56 +19,44 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["event-stream"]
 version = "1.9.2"

 [dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 version = "1.3.0"

 [dependencies.aws-smithy-eventstream]
-path = "../aws-smithy-eventstream"
 version = "0.61.2"

 [dependencies.aws-smithy-http]
-path = "../aws-smithy-http"
 features = ["event-stream"]
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
@@ -90,50 +78,40 @@
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

 [dev-dependencies.aws-smithy-eventstream]
-path = "../aws-smithy-eventstream"
 features = ["test-util"]
 version = "0.61.2"

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

@@ -164,3 +142,121 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_associate_kms_key = []
+op_associate_source_to_s3_table_integration = []
+op_cancel_export_task = []
+op_cancel_import_task = []
+op_create_delivery = []
+op_create_export_task = []
+op_create_import_task = []
+op_create_log_anomaly_detector = []
+op_create_log_group = []
+op_create_log_stream = []
+op_create_lookup_table = []
+op_create_scheduled_query = []
+op_delete_account_policy = []
+op_delete_data_protection_policy = []
+op_delete_delivery = []
+op_delete_delivery_destination = []
+op_delete_delivery_destination_policy = []
+op_delete_delivery_source = []
+op_delete_destination = []
+op_delete_index_policy = []
+op_delete_integration = []
+op_delete_log_anomaly_detector = []
+op_delete_log_group = []
+op_delete_log_stream = []
+op_delete_lookup_table = []
+op_delete_metric_filter = []
+op_delete_query_definition = []
+op_delete_resource_policy = []
+op_delete_retention_policy = []
+op_delete_scheduled_query = []
+op_delete_subscription_filter = []
+op_delete_syslog_configuration = []
+op_delete_transformer = []
+op_describe_account_policies = []
+op_describe_configuration_templates = []
+op_describe_deliveries = []
+op_describe_delivery_destinations = []
+op_describe_delivery_sources = []
+op_describe_destinations = []
+op_describe_export_tasks = []
+op_describe_field_indexes = []
+op_describe_import_task_batches = []
+op_describe_import_tasks = []
+op_describe_index_policies = []
+op_describe_log_groups = []
+op_describe_log_streams = []
+op_describe_lookup_tables = []
+op_describe_metric_filters = []
+op_describe_queries = []
+op_describe_query_definitions = []
+op_describe_resource_policies = []
+op_describe_subscription_filters = []
+op_disassociate_kms_key = []
+op_disassociate_source_from_s3_table_integration = []
+op_filter_log_events = []
+op_get_data_protection_policy = []
+op_get_delivery = []
+op_get_delivery_destination = []
+op_get_delivery_destination_policy = []
+op_get_delivery_source = []
+op_get_integration = []
+op_get_log_anomaly_detector = []
+op_get_log_events = []
+op_get_log_fields = []
+op_get_log_group_fields = []
+op_get_log_object = []
+op_get_log_record = []
+op_get_lookup_table = []
+op_get_query_results = []
+op_get_scheduled_query = []
+op_get_scheduled_query_history = []
+op_get_storage_tier_policy = []
+op_get_transformer = []
+op_list_aggregate_log_group_summaries = []
+op_list_anomalies = []
+op_list_integrations = []
+op_list_log_anomaly_detectors = []
+op_list_log_groups = []
+op_list_log_groups_for_query = []
+op_list_scheduled_queries = []
+op_list_sources_for_s3_table_integration = []
+op_list_syslog_configurations = []
+op_list_tags_for_resource = []
+op_list_tags_log_group = []
+op_put_account_policy = []
+op_put_bearer_token_authentication = []
+op_put_data_protection_policy = []
+op_put_delivery_destination = []
+op_put_delivery_destination_policy = []
+op_put_delivery_source = []
+op_put_destination = []
+op_put_destination_policy = []
+op_put_index_policy = []
+op_put_integration = []
+op_put_log_events = []
+op_put_log_group_deletion_protection = []
+op_put_metric_filter = []
+op_put_query_definition = []
+op_put_resource_policy = []
+op_put_retention_policy = []
+op_put_storage_tier_policy = []
+op_put_subscription_filter = []
+op_put_syslog_configuration = []
+op_put_transformer = []
+op_start_live_tail = []
+op_start_query = []
+op_stop_query = []
+op_tag_log_group = []
+op_tag_resource = []
+op_test_metric_filter = []
+op_test_transformer = []
+op_untag_log_group = []
+op_untag_resource = []
+op_update_anomaly = []
+op_update_delivery_configuration = []
+op_update_log_anomaly_detector = []
+op_update_lookup_table = []
+op_update_scheduled_query = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,28 +136,40 @@
     }
 }

+#[cfg(feature = "op_associate_kms_key")]
 mod associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 mod associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 mod cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 mod cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 mod create_delivery;

+#[cfg(feature = "op_create_export_task")]
 mod create_export_task;

+#[cfg(feature = "op_create_import_task")]
 mod create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 mod create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 mod create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 mod create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 mod create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 mod create_scheduled_query;

 /// Operation customization and supporting types.
@@ -187,214 +199,320 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_account_policy")]
 mod delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 mod delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 mod delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 mod delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 mod delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 mod delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 mod delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 mod delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 mod delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 mod delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 mod delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 mod delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 mod delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 mod delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 mod delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 mod delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 mod delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 mod delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 mod delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 mod delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 mod delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 mod describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 mod describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 mod describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 mod describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 mod describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 mod describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 mod describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 mod describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 mod describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 mod describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 mod describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 mod describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 mod describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 mod describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 mod describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 mod describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 mod describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 mod describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 mod disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 mod disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 mod filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 mod get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 mod get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 mod get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 mod get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 mod get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 mod get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 mod get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 mod get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 mod get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 mod get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 mod get_log_object;

+#[cfg(feature = "op_get_log_record")]
 mod get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 mod get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 mod get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 mod get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 mod get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 mod get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 mod list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 mod list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 mod list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 mod list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 mod list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 mod list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 mod list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 mod put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 mod put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 mod put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 mod put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 mod put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 mod put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 mod put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 mod put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 mod put_index_policy;

+#[cfg(feature = "op_put_integration")]
 mod put_integration;

+#[cfg(feature = "op_put_log_events")]
 mod put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 mod put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 mod put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 mod put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 mod put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 mod put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 mod put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 mod put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 mod put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 mod put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 mod start_live_tail;

+#[cfg(feature = "op_start_query")]
 mod start_query;

+#[cfg(feature = "op_stop_query")]
 mod stop_query;

+#[cfg(feature = "op_tag_log_group")]
 mod tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 mod test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 mod test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 mod untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 mod update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 mod update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 mod update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 mod update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 mod update_scheduled_query;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,51 +3,588 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_lookup_table",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_lookup_tables",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_log_object",
+        feature = "op_get_lookup_table",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_syslog_configuration",
+        feature = "op_start_live_tail",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>You don't have sufficient permissions to perform this action.</p>
     AccessDeniedException(crate::types::error::AccessDeniedException),
+    #[cfg(any(
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>This operation attempted to create a resource that already exists.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The event was already logged.</p><important>
     /// <p><code>PutLogEvents</code> actions are now always accepted and never return <code>DataAlreadyAcceptedException</code> regardless of whether a given batch of log events has already been accepted.</p>
     /// </important>
     DataAlreadyAcceptedException(crate::types::error::DataAlreadyAcceptedException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_scheduled_query",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>An internal server error occurred while processing the request. This exception is returned when the service encounters an unexpected condition that prevents it from fulfilling the request.</p>
     InternalServerException(crate::types::error::InternalServerException),
+    #[cfg(feature = "op_get_log_object")]
     /// <p>An internal error occurred during the streaming of log data. This exception is thrown when there's an issue with the internal streaming mechanism used by the GetLogObject operation.</p>
     InternalStreamingException(crate::types::error::InternalStreamingException),
+    #[cfg(any(
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_import_task",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_get_log_object",
+        feature = "op_get_transformer",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_test_transformer"
+    ))]
     /// <p>The operation is not valid on the specified resource.</p>
     InvalidOperationException(crate::types::error::InvalidOperationException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_export_task",
+        feature = "op_create_import_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_destinations",
+        feature = "op_describe_export_tasks",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_groups",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_query_definitions",
+        feature = "op_describe_resource_policies",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_anomalies",
+        feature = "op_list_integrations",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_log_group",
+        feature = "op_tag_resource",
+        feature = "op_test_metric_filter",
+        feature = "op_test_transformer",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table"
+    ))]
     /// <p>A parameter is specified incorrectly.</p>
     InvalidParameterException(crate::types::error::InvalidParameterException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The sequence token is not valid. You can get the correct sequence token in the <code>expectedSequenceToken</code> field in the <code>InvalidSequenceTokenException</code> message.</p><important>
     /// <p><code>PutLogEvents</code> actions are now always accepted and never return <code>InvalidSequenceTokenException</code> regardless of receiving an invalid sequence token.</p>
     /// </important>
     InvalidSequenceTokenException(crate::types::error::InvalidSequenceTokenException),
+    #[cfg(any(
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_index_policy",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_put_account_policy",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query"
+    ))]
     /// <p>You have reached the maximum number of resources that can be created.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(feature = "op_start_query")]
     /// <p>The query string is not valid. Details about this error are displayed in a <code>QueryCompileError</code> object. For more information, see <a href="https://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_QueryCompileError.html">QueryCompileError</a>.</p>
     /// <p>For more information about valid query syntax, see <a href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html">CloudWatch Logs Insights Query Syntax</a>.</p>
     MalformedQueryException(crate::types::error::MalformedQueryException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_disassociate_kms_key",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_fields",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_list_anomalies",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_update_anomaly",
+        feature = "op_update_log_anomaly_detector"
+    ))]
     /// <p>Multiple concurrent requests to update the same resource were in conflict.</p>
     OperationAbortedException(crate::types::error::OperationAbortedException),
+    #[cfg(any(
+        feature = "op_create_export_task",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table"
+    ))]
     /// <p>The specified resource already exists.</p>
     ResourceAlreadyExistsException(crate::types::error::ResourceAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_export_task",
+        feature = "op_create_import_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_stream",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_anomalies",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tags_log_group",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_index_policy",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_log_group",
+        feature = "op_tag_resource",
+        feature = "op_untag_log_group",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>The specified resource does not exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_create_delivery",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_source",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_source",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_source"
+    ))]
     /// <p>This request exceeds a service quota.</p>
     ServiceQuotaExceededException(crate::types::error::ServiceQuotaExceededException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_cancel_export_task",
+        feature = "op_create_delivery",
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_describe_destinations",
+        feature = "op_describe_export_tasks",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_groups",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_query_definitions",
+        feature = "op_describe_resource_policies",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_anomalies",
+        feature = "op_list_integrations",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tags_log_group",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_resource",
+        feature = "op_test_metric_filter",
+        feature = "op_test_transformer",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table"
+    ))]
     /// <p>The service cannot complete the request.</p>
     ServiceUnavailableException(crate::types::error::ServiceUnavailableException),
+    #[cfg(feature = "op_start_live_tail")]
     /// <p>This exception is returned if an unknown error occurs during a Live Tail session.</p>
     SessionStreamingException(crate::types::error::SessionStreamingException),
+    #[cfg(feature = "op_start_live_tail")]
     /// <p>This exception is returned in a Live Tail stream when the Live Tail session times out. Live Tail sessions time out after three hours.</p>
     SessionTimeoutException(crate::types::error::SessionTimeoutException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_source",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_source",
+        feature = "op_put_syslog_configuration",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>The request was throttled because of quota limits.</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(feature = "op_tag_resource")]
     /// <p>A resource can have no more than 50 tags.</p>
     TooManyTagsException(crate::types::error::TooManyTagsException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The most likely cause is an Amazon Web Services access key ID or secret key that's not valid.</p>
     UnrecognizedClientException(crate::types::error::UnrecognizedClientException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_lookup_table",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_scheduled_query",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_integration",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>One of the parameters for the request is not valid.</p>
     ValidationException(crate::types::error::ValidationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -64,26 +601,563 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::AccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::DataAlreadyAcceptedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::InternalServerException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_log_object")]
             Error::InternalStreamingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Error::InvalidOperationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::InvalidParameterException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::InvalidSequenceTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_query")]
             Error::MalformedQueryException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Error::OperationAbortedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Error::ResourceAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionStreamingException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_tag_resource")]
             Error::TooManyTagsException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::UnrecognizedClientException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -108,31 +1182,569 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::AccessDeniedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::DataAlreadyAcceptedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::InternalServerException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_log_object")]
             Self::InternalStreamingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Self::InvalidOperationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::InvalidParameterException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::InvalidSequenceTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_query")]
             Self::MalformedQueryException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Self::OperationAbortedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Self::ResourceAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Self::ServiceQuotaExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::ServiceUnavailableException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionStreamingException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(feature = "op_tag_resource")]
             Self::TooManyTagsException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::UnrecognizedClientException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_associate_kms_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -158,6 +1770,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_kms_key")]
 impl From<crate::operation::associate_kms_key::AssociateKmsKeyError> for Error {
     fn from(err: crate::operation::associate_kms_key::AssociateKmsKeyError) -> Self {
         match err {
@@ -177,6 +1790,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -202,6 +1816,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 impl From<crate::operation::associate_source_to_s3_table_integration::AssociateSourceToS3TableIntegrationError>
     for Error
 {
@@ -230,6 +1845,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -255,6 +1871,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_task")]
 impl From<crate::operation::cancel_export_task::CancelExportTaskError> for Error {
     fn from(err: crate::operation::cancel_export_task::CancelExportTaskError) -> Self {
         match err {
@@ -274,6 +1891,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_import_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -299,6 +1917,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_import_task")]
 impl From<crate::operation::cancel_import_task::CancelImportTaskError> for Error {
     fn from(err: crate::operation::cancel_import_task::CancelImportTaskError) -> Self {
         match err {
@@ -321,6 +1940,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_delivery")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_delivery::CreateDeliveryError, R>>
     for Error
@@ -342,6 +1962,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_delivery")]
 impl From<crate::operation::create_delivery::CreateDeliveryError> for Error {
     fn from(err: crate::operation::create_delivery::CreateDeliveryError) -> Self {
         match err {
@@ -370,6 +1991,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -395,6 +2017,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_task")]
 impl From<crate::operation::create_export_task::CreateExportTaskError> for Error {
     fn from(err: crate::operation::create_export_task::CreateExportTaskError) -> Self {
         match err {
@@ -420,6 +2043,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -445,6 +2069,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_task")]
 impl From<crate::operation::create_import_task::CreateImportTaskError> for Error {
     fn from(err: crate::operation::create_import_task::CreateImportTaskError) -> Self {
         match err {
@@ -473,6 +2098,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -498,6 +2124,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_anomaly_detector")]
 impl From<crate::operation::create_log_anomaly_detector::CreateLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::create_log_anomaly_detector::CreateLogAnomalyDetectorError) -> Self {
         match err {
@@ -520,6 +2147,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_log_group::CreateLogGroupError, R>>
     for Error
@@ -541,6 +2169,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_group")]
 impl From<crate::operation::create_log_group::CreateLogGroupError> for Error {
     fn from(err: crate::operation::create_log_group::CreateLogGroupError) -> Self {
         match err {
@@ -563,6 +2192,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -588,6 +2218,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_stream")]
 impl From<crate::operation::create_log_stream::CreateLogStreamError> for Error {
     fn from(err: crate::operation::create_log_stream::CreateLogStreamError) -> Self {
         match err {
@@ -607,6 +2238,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -632,6 +2264,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_lookup_table")]
 impl From<crate::operation::create_lookup_table::CreateLookupTableError> for Error {
     fn from(err: crate::operation::create_lookup_table::CreateLookupTableError) -> Self {
         match err {
@@ -657,6 +2290,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -682,6 +2316,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduled_query")]
 impl From<crate::operation::create_scheduled_query::CreateScheduledQueryError> for Error {
     fn from(err: crate::operation::create_scheduled_query::CreateScheduledQueryError) -> Self {
         match err {
@@ -712,6 +2347,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_account_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -737,6 +2373,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_account_policy")]
 impl From<crate::operation::delete_account_policy::DeleteAccountPolicyError> for Error {
     fn from(err: crate::operation::delete_account_policy::DeleteAccountPolicyError) -> Self {
         match err {
@@ -758,6 +2395,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -783,6 +2421,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_data_protection_policy")]
 impl From<crate::operation::delete_data_protection_policy::DeleteDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::delete_data_protection_policy::DeleteDataProtectionPolicyError) -> Self {
         match err {
@@ -802,6 +2441,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_delivery::DeleteDeliveryError, R>>
     for Error
@@ -823,6 +2463,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery")]
 impl From<crate::operation::delete_delivery::DeleteDeliveryError> for Error {
     fn from(err: crate::operation::delete_delivery::DeleteDeliveryError) -> Self {
         match err {
@@ -848,6 +2489,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -873,6 +2515,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination")]
 impl From<crate::operation::delete_delivery_destination::DeleteDeliveryDestinationError> for Error {
     fn from(err: crate::operation::delete_delivery_destination::DeleteDeliveryDestinationError) -> Self {
         match err {
@@ -898,6 +2541,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -923,6 +2567,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination_policy")]
 impl From<crate::operation::delete_delivery_destination_policy::DeleteDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::delete_delivery_destination_policy::DeleteDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -942,6 +2587,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -967,6 +2613,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_source")]
 impl From<crate::operation::delete_delivery_source::DeleteDeliverySourceError> for Error {
     fn from(err: crate::operation::delete_delivery_source::DeleteDeliverySourceError) -> Self {
         match err {
@@ -994,6 +2641,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1019,6 +2667,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_destination")]
 impl From<crate::operation::delete_destination::DeleteDestinationError> for Error {
     fn from(err: crate::operation::delete_destination::DeleteDestinationError) -> Self {
         match err {
@@ -1038,6 +2687,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_index_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1063,6 +2713,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_index_policy")]
 impl From<crate::operation::delete_index_policy::DeleteIndexPolicyError> for Error {
     fn from(err: crate::operation::delete_index_policy::DeleteIndexPolicyError) -> Self {
         match err {
@@ -1085,6 +2736,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1110,6 +2762,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_integration")]
 impl From<crate::operation::delete_integration::DeleteIntegrationError> for Error {
     fn from(err: crate::operation::delete_integration::DeleteIntegrationError) -> Self {
         match err {
@@ -1129,6 +2782,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1154,6 +2808,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_anomaly_detector")]
 impl From<crate::operation::delete_log_anomaly_detector::DeleteLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::delete_log_anomaly_detector::DeleteLogAnomalyDetectorError) -> Self {
         match err {
@@ -1173,6 +2828,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_log_group::DeleteLogGroupError, R>>
     for Error
@@ -1194,6 +2850,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_group")]
 impl From<crate::operation::delete_log_group::DeleteLogGroupError> for Error {
     fn from(err: crate::operation::delete_log_group::DeleteLogGroupError) -> Self {
         match err {
@@ -1216,6 +2873,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1241,6 +2899,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_stream")]
 impl From<crate::operation::delete_log_stream::DeleteLogStreamError> for Error {
     fn from(err: crate::operation::delete_log_stream::DeleteLogStreamError) -> Self {
         match err {
@@ -1263,6 +2922,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1288,6 +2948,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_lookup_table")]
 impl From<crate::operation::delete_lookup_table::DeleteLookupTableError> for Error {
     fn from(err: crate::operation::delete_lookup_table::DeleteLookupTableError) -> Self {
         match err {
@@ -1307,6 +2968,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1332,6 +2994,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_metric_filter")]
 impl From<crate::operation::delete_metric_filter::DeleteMetricFilterError> for Error {
     fn from(err: crate::operation::delete_metric_filter::DeleteMetricFilterError) -> Self {
         match err {
@@ -1353,6 +3016,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_query_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1378,6 +3042,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_query_definition")]
 impl From<crate::operation::delete_query_definition::DeleteQueryDefinitionError> for Error {
     fn from(err: crate::operation::delete_query_definition::DeleteQueryDefinitionError) -> Self {
         match err {
@@ -1396,6 +3061,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1421,6 +3087,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl From<crate::operation::delete_resource_policy::DeleteResourcePolicyError> for Error {
     fn from(err: crate::operation::delete_resource_policy::DeleteResourcePolicyError) -> Self {
         match err {
@@ -1442,6 +3109,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_retention_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1467,6 +3135,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_retention_policy")]
 impl From<crate::operation::delete_retention_policy::DeleteRetentionPolicyError> for Error {
     fn from(err: crate::operation::delete_retention_policy::DeleteRetentionPolicyError) -> Self {
         match err {
@@ -1488,6 +3157,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1513,6 +3183,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduled_query")]
 impl From<crate::operation::delete_scheduled_query::DeleteScheduledQueryError> for Error {
     fn from(err: crate::operation::delete_scheduled_query::DeleteScheduledQueryError) -> Self {
         match err {
@@ -1537,6 +3208,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_subscription_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1562,6 +3234,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_subscription_filter")]
 impl From<crate::operation::delete_subscription_filter::DeleteSubscriptionFilterError> for Error {
     fn from(err: crate::operation::delete_subscription_filter::DeleteSubscriptionFilterError) -> Self {
         match err {
@@ -1581,6 +3254,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_syslog_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1606,6 +3280,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_syslog_configuration")]
 impl From<crate::operation::delete_syslog_configuration::DeleteSyslogConfigurationError> for Error {
     fn from(err: crate::operation::delete_syslog_configuration::DeleteSyslogConfigurationError) -> Self {
         match err {
@@ -1634,6 +3309,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_transformer")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1659,6 +3335,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_transformer")]
 impl From<crate::operation::delete_transformer::DeleteTransformerError> for Error {
     fn from(err: crate::operation::delete_transformer::DeleteTransformerError) -> Self {
         match err {
@@ -1681,6 +3358,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_account_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1706,6 +3384,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_account_policies")]
 impl From<crate::operation::describe_account_policies::DescribeAccountPoliciesError> for Error {
     fn from(err: crate::operation::describe_account_policies::DescribeAccountPoliciesError) -> Self {
         match err {
@@ -1727,6 +3406,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_configuration_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1752,6 +3432,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_configuration_templates")]
 impl From<crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesError> for Error {
     fn from(err: crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesError) -> Self {
         match err {
@@ -1771,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_deliveries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1796,6 +3478,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_deliveries")]
 impl From<crate::operation::describe_deliveries::DescribeDeliveriesError> for Error {
     fn from(err: crate::operation::describe_deliveries::DescribeDeliveriesError) -> Self {
         match err {
@@ -1815,6 +3498,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1840,6 +3524,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_destinations")]
 impl From<crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsError> for Error {
     fn from(err: crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsError) -> Self {
         match err {
@@ -1859,6 +3544,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_sources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1884,6 +3570,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_sources")]
 impl From<crate::operation::describe_delivery_sources::DescribeDeliverySourcesError> for Error {
     fn from(err: crate::operation::describe_delivery_sources::DescribeDeliverySourcesError) -> Self {
         match err {
@@ -1903,6 +3590,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1928,6 +3616,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_destinations")]
 impl From<crate::operation::describe_destinations::DescribeDestinationsError> for Error {
     fn from(err: crate::operation::describe_destinations::DescribeDestinationsError) -> Self {
         match err {
@@ -1943,6 +3632,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1968,6 +3658,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export_tasks")]
 impl From<crate::operation::describe_export_tasks::DescribeExportTasksError> for Error {
     fn from(err: crate::operation::describe_export_tasks::DescribeExportTasksError) -> Self {
         match err {
@@ -1983,6 +3674,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_field_indexes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2008,6 +3700,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_field_indexes")]
 impl From<crate::operation::describe_field_indexes::DescribeFieldIndexesError> for Error {
     fn from(err: crate::operation::describe_field_indexes::DescribeFieldIndexesError) -> Self {
         match err {
@@ -2032,6 +3725,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_task_batches")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2057,6 +3751,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_task_batches")]
 impl From<crate::operation::describe_import_task_batches::DescribeImportTaskBatchesError> for Error {
     fn from(err: crate::operation::describe_import_task_batches::DescribeImportTaskBatchesError) -> Self {
         match err {
@@ -2079,6 +3774,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2104,6 +3800,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_tasks")]
 impl From<crate::operation::describe_import_tasks::DescribeImportTasksError> for Error {
     fn from(err: crate::operation::describe_import_tasks::DescribeImportTasksError) -> Self {
         match err {
@@ -2128,6 +3825,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_index_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2153,6 +3851,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_index_policies")]
 impl From<crate::operation::describe_index_policies::DescribeIndexPoliciesError> for Error {
     fn from(err: crate::operation::describe_index_policies::DescribeIndexPoliciesError) -> Self {
         match err {
@@ -2177,6 +3876,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_groups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2202,6 +3902,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_groups")]
 impl From<crate::operation::describe_log_groups::DescribeLogGroupsError> for Error {
     fn from(err: crate::operation::describe_log_groups::DescribeLogGroupsError) -> Self {
         match err {
@@ -2215,6 +3916,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_streams")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2240,6 +3942,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_streams")]
 impl From<crate::operation::describe_log_streams::DescribeLogStreamsError> for Error {
     fn from(err: crate::operation::describe_log_streams::DescribeLogStreamsError) -> Self {
         match err {
@@ -2258,6 +3961,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_lookup_tables")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2283,6 +3987,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_lookup_tables")]
 impl From<crate::operation::describe_lookup_tables::DescribeLookupTablesError> for Error {
     fn from(err: crate::operation::describe_lookup_tables::DescribeLookupTablesError) -> Self {
         match err {
@@ -2304,6 +4009,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_metric_filters")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2329,6 +4035,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_metric_filters")]
 impl From<crate::operation::describe_metric_filters::DescribeMetricFiltersError> for Error {
     fn from(err: crate::operation::describe_metric_filters::DescribeMetricFiltersError) -> Self {
         match err {
@@ -2347,6 +4054,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_queries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_queries::DescribeQueriesError, R>,
@@ -2369,6 +4077,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_queries")]
 impl From<crate::operation::describe_queries::DescribeQueriesError> for Error {
     fn from(err: crate::operation::describe_queries::DescribeQueriesError) -> Self {
         match err {
@@ -2385,6 +4094,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_query_definitions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2410,6 +4120,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_query_definitions")]
 impl From<crate::operation::describe_query_definitions::DescribeQueryDefinitionsError> for Error {
     fn from(err: crate::operation::describe_query_definitions::DescribeQueryDefinitionsError) -> Self {
         match err {
@@ -2423,6 +4134,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_resource_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2448,6 +4160,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_resource_policies")]
 impl From<crate::operation::describe_resource_policies::DescribeResourcePoliciesError> for Error {
     fn from(err: crate::operation::describe_resource_policies::DescribeResourcePoliciesError) -> Self {
         match err {
@@ -2461,6 +4174,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_subscription_filters")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2486,6 +4200,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_subscription_filters")]
 impl From<crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersError> for Error {
     fn from(err: crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersError) -> Self {
         match err {
@@ -2502,6 +4217,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_kms_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2527,6 +4243,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_kms_key")]
 impl From<crate::operation::disassociate_kms_key::DisassociateKmsKeyError> for Error {
     fn from(err: crate::operation::disassociate_kms_key::DisassociateKmsKeyError) -> Self {
         match err {
@@ -2548,6 +4265,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2573,6 +4291,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 impl
     From<crate::operation::disassociate_source_from_s3_table_integration::DisassociateSourceFromS3TableIntegrationError>
     for Error
@@ -2590,6 +4309,7 @@
         }
     }
 }
+#[cfg(feature = "op_filter_log_events")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2615,6 +4335,7 @@
         }
     }
 }
+#[cfg(feature = "op_filter_log_events")]
 impl From<crate::operation::filter_log_events::FilterLogEventsError> for Error {
     fn from(err: crate::operation::filter_log_events::FilterLogEventsError) -> Self {
         match err {
@@ -2631,6 +4352,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2656,6 +4378,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl From<crate::operation::get_data_protection_policy::GetDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::get_data_protection_policy::GetDataProtectionPolicyError) -> Self {
         match err {
@@ -2677,6 +4400,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_delivery::GetDeliveryError, R>>
     for Error
 where
@@ -2694,6 +4418,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery")]
 impl From<crate::operation::get_delivery::GetDeliveryError> for Error {
     fn from(err: crate::operation::get_delivery::GetDeliveryError) -> Self {
         match err {
@@ -2716,6 +4441,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2741,6 +4467,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination")]
 impl From<crate::operation::get_delivery_destination::GetDeliveryDestinationError> for Error {
     fn from(err: crate::operation::get_delivery_destination::GetDeliveryDestinationError) -> Self {
         match err {
@@ -2765,6 +4492,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2790,6 +4518,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination_policy")]
 impl From<crate::operation::get_delivery_destination_policy::GetDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::get_delivery_destination_policy::GetDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -2806,6 +4535,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2831,6 +4561,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_source")]
 impl From<crate::operation::get_delivery_source::GetDeliverySourceError> for Error {
     fn from(err: crate::operation::get_delivery_source::GetDeliverySourceError) -> Self {
         match err {
@@ -2853,6 +4584,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_integration")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_integration::GetIntegrationError, R>>
     for Error
@@ -2874,6 +4606,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_integration")]
 impl From<crate::operation::get_integration::GetIntegrationError> for Error {
     fn from(err: crate::operation::get_integration::GetIntegrationError) -> Self {
         match err {
@@ -2890,6 +4623,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2915,6 +4649,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_anomaly_detector")]
 impl From<crate::operation::get_log_anomaly_detector::GetLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::get_log_anomaly_detector::GetLogAnomalyDetectorError) -> Self {
         match err {
@@ -2936,6 +4671,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_events")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_events::GetLogEventsError, R>>
     for Error
 where
@@ -2953,6 +4689,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_events")]
 impl From<crate::operation::get_log_events::GetLogEventsError> for Error {
     fn from(err: crate::operation::get_log_events::GetLogEventsError) -> Self {
         match err {
@@ -2969,6 +4706,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_fields")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_fields::GetLogFieldsError, R>>
     for Error
 where
@@ -2986,6 +4724,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_fields")]
 impl From<crate::operation::get_log_fields::GetLogFieldsError> for Error {
     fn from(err: crate::operation::get_log_fields::GetLogFieldsError) -> Self {
         match err {
@@ -3005,6 +4744,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_group_fields")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3030,6 +4770,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_group_fields")]
 impl From<crate::operation::get_log_group_fields::GetLogGroupFieldsError> for Error {
     fn from(err: crate::operation::get_log_group_fields::GetLogGroupFieldsError) -> Self {
         match err {
@@ -3049,6 +4790,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_object::GetLogObjectError, R>>
     for Error
 where
@@ -3066,6 +4808,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl From<crate::operation::get_log_object::GetLogObjectError> for Error {
     fn from(err: crate::operation::get_log_object::GetLogObjectError) -> Self {
         match err {
@@ -3091,6 +4834,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_record")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_record::GetLogRecordError, R>>
     for Error
 where
@@ -3108,6 +4852,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_record")]
 impl From<crate::operation::get_log_record::GetLogRecordError> for Error {
     fn from(err: crate::operation::get_log_record::GetLogRecordError) -> Self {
         match err {
@@ -3127,6 +4872,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_lookup_table")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_lookup_table::GetLookupTableError, R>>
     for Error
@@ -3148,6 +4894,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_lookup_table")]
 impl From<crate::operation::get_lookup_table::GetLookupTableError> for Error {
     fn from(err: crate::operation::get_lookup_table::GetLookupTableError) -> Self {
         match err {
@@ -3167,6 +4914,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_query_results")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3192,6 +4940,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_query_results")]
 impl From<crate::operation::get_query_results::GetQueryResultsError> for Error {
     fn from(err: crate::operation::get_query_results::GetQueryResultsError) -> Self {
         match err {
@@ -3208,6 +4957,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3233,6 +4983,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query")]
 impl From<crate::operation::get_scheduled_query::GetScheduledQueryError> for Error {
     fn from(err: crate::operation::get_scheduled_query::GetScheduledQueryError) -> Self {
         match err {
@@ -3255,6 +5006,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query_history")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3280,6 +5032,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query_history")]
 impl From<crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryError> for Error {
     fn from(err: crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryError) -> Self {
         match err {
@@ -3304,6 +5057,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_storage_tier_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3329,6 +5083,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_storage_tier_policy")]
 impl From<crate::operation::get_storage_tier_policy::GetStorageTierPolicyError> for Error {
     fn from(err: crate::operation::get_storage_tier_policy::GetStorageTierPolicyError) -> Self {
         match err {
@@ -3353,6 +5108,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_transformer")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_transformer::GetTransformerError, R>>
     for Error
@@ -3374,6 +5130,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_transformer")]
 impl From<crate::operation::get_transformer::GetTransformerError> for Error {
     fn from(err: crate::operation::get_transformer::GetTransformerError) -> Self {
         match err {
@@ -3393,6 +5150,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3418,6 +5176,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 impl From<crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesError> for Error {
     fn from(err: crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesError) -> Self {
         match err {
@@ -3434,6 +5193,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_anomalies")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_anomalies::ListAnomaliesError, R>>
     for Error
@@ -3455,6 +5215,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_anomalies")]
 impl From<crate::operation::list_anomalies::ListAnomaliesError> for Error {
     fn from(err: crate::operation::list_anomalies::ListAnomaliesError) -> Self {
         match err {
@@ -3474,6 +5235,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_integrations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3499,6 +5261,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_integrations")]
 impl From<crate::operation::list_integrations::ListIntegrationsError> for Error {
     fn from(err: crate::operation::list_integrations::ListIntegrationsError) -> Self {
         match err {
@@ -3512,6 +5275,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_anomaly_detectors")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3537,6 +5301,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_anomaly_detectors")]
 impl From<crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsError> for Error {
     fn from(err: crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsError) -> Self {
         match err {
@@ -3558,6 +5323,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_log_groups::ListLogGroupsError, R>>
     for Error
@@ -3579,6 +5345,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups")]
 impl From<crate::operation::list_log_groups::ListLogGroupsError> for Error {
     fn from(err: crate::operation::list_log_groups::ListLogGroupsError) -> Self {
         match err {
@@ -3592,6 +5359,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups_for_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3617,6 +5385,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups_for_query")]
 impl From<crate::operation::list_log_groups_for_query::ListLogGroupsForQueryError> for Error {
     fn from(err: crate::operation::list_log_groups_for_query::ListLogGroupsForQueryError) -> Self {
         match err {
@@ -3638,6 +5407,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduled_queries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3663,6 +5433,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduled_queries")]
 impl From<crate::operation::list_scheduled_queries::ListScheduledQueriesError> for Error {
     fn from(err: crate::operation::list_scheduled_queries::ListScheduledQueriesError) -> Self {
         match err {
@@ -3684,6 +5455,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3709,6 +5481,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 impl From<crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationError> for Error {
     fn from(
         err: crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationError,
@@ -3735,6 +5508,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_syslog_configurations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3760,6 +5534,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_syslog_configurations")]
 impl From<crate::operation::list_syslog_configurations::ListSyslogConfigurationsError> for Error {
     fn from(err: crate::operation::list_syslog_configurations::ListSyslogConfigurationsError) -> Self {
         match err {
@@ -3785,6 +5560,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3810,6 +5586,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -3828,6 +5605,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_log_group")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3853,6 +5631,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_log_group")]
 impl From<crate::operation::list_tags_log_group::ListTagsLogGroupError> for Error {
     fn from(err: crate::operation::list_tags_log_group::ListTagsLogGroupError) -> Self {
         match err {
@@ -3866,6 +5645,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3891,6 +5671,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_policy")]
 impl From<crate::operation::put_account_policy::PutAccountPolicyError> for Error {
     fn from(err: crate::operation::put_account_policy::PutAccountPolicyError) -> Self {
         match err {
@@ -3910,6 +5691,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_bearer_token_authentication")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3935,6 +5717,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_bearer_token_authentication")]
 impl From<crate::operation::put_bearer_token_authentication::PutBearerTokenAuthenticationError> for Error {
     fn from(err: crate::operation::put_bearer_token_authentication::PutBearerTokenAuthenticationError) -> Self {
         match err {
@@ -3960,6 +5743,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3985,6 +5769,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl From<crate::operation::put_data_protection_policy::PutDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::put_data_protection_policy::PutDataProtectionPolicyError) -> Self {
         match err {
@@ -4009,6 +5794,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4034,6 +5820,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination")]
 impl From<crate::operation::put_delivery_destination::PutDeliveryDestinationError> for Error {
     fn from(err: crate::operation::put_delivery_destination::PutDeliveryDestinationError) -> Self {
         match err {
@@ -4061,6 +5848,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4086,6 +5874,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination_policy")]
 impl From<crate::operation::put_delivery_destination_policy::PutDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::put_delivery_destination_policy::PutDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -4105,6 +5894,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4130,6 +5920,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_source")]
 impl From<crate::operation::put_delivery_source::PutDeliverySourceError> for Error {
     fn from(err: crate::operation::put_delivery_source::PutDeliverySourceError) -> Self {
         match err {
@@ -4155,6 +5946,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_destination::PutDestinationError, R>>
     for Error
@@ -4176,6 +5968,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination")]
 impl From<crate::operation::put_destination::PutDestinationError> for Error {
     fn from(err: crate::operation::put_destination::PutDestinationError) -> Self {
         match err {
@@ -4192,6 +5985,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4217,6 +6011,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination_policy")]
 impl From<crate::operation::put_destination_policy::PutDestinationPolicyError> for Error {
     fn from(err: crate::operation::put_destination_policy::PutDestinationPolicyError) -> Self {
         match err {
@@ -4235,6 +6030,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_index_policy")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_index_policy::PutIndexPolicyError, R>>
     for Error
@@ -4256,6 +6052,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_index_policy")]
 impl From<crate::operation::put_index_policy::PutIndexPolicyError> for Error {
     fn from(err: crate::operation::put_index_policy::PutIndexPolicyError) -> Self {
         match err {
@@ -4278,6 +6075,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_integration")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_integration::PutIntegrationError, R>>
     for Error
@@ -4299,6 +6097,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_integration")]
 impl From<crate::operation::put_integration::PutIntegrationError> for Error {
     fn from(err: crate::operation::put_integration::PutIntegrationError) -> Self {
         match err {
@@ -4318,6 +6117,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_events")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_log_events::PutLogEventsError, R>>
     for Error
 where
@@ -4335,6 +6135,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_events")]
 impl From<crate::operation::put_log_events::PutLogEventsError> for Error {
     fn from(err: crate::operation::put_log_events::PutLogEventsError) -> Self {
         match err {
@@ -4360,6 +6161,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_group_deletion_protection")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4385,6 +6187,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_group_deletion_protection")]
 impl From<crate::operation::put_log_group_deletion_protection::PutLogGroupDeletionProtectionError> for Error {
     fn from(err: crate::operation::put_log_group_deletion_protection::PutLogGroupDeletionProtectionError) -> Self {
         match err {
@@ -4410,6 +6213,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4435,6 +6239,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_metric_filter")]
 impl From<crate::operation::put_metric_filter::PutMetricFilterError> for Error {
     fn from(err: crate::operation::put_metric_filter::PutMetricFilterError) -> Self {
         match err {
@@ -4460,6 +6265,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_query_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4485,6 +6291,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_query_definition")]
 impl From<crate::operation::put_query_definition::PutQueryDefinitionError> for Error {
     fn from(err: crate::operation::put_query_definition::PutQueryDefinitionError) -> Self {
         match err {
@@ -4506,6 +6313,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4531,6 +6339,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl From<crate::operation::put_resource_policy::PutResourcePolicyError> for Error {
     fn from(err: crate::operation::put_resource_policy::PutResourcePolicyError) -> Self {
         match err {
@@ -4553,6 +6362,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_retention_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4578,6 +6388,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_retention_policy")]
 impl From<crate::operation::put_retention_policy::PutRetentionPolicyError> for Error {
     fn from(err: crate::operation::put_retention_policy::PutRetentionPolicyError) -> Self {
         match err {
@@ -4599,6 +6410,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_storage_tier_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4624,6 +6436,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_storage_tier_policy")]
 impl From<crate::operation::put_storage_tier_policy::PutStorageTierPolicyError> for Error {
     fn from(err: crate::operation::put_storage_tier_policy::PutStorageTierPolicyError) -> Self {
         match err {
@@ -4648,6 +6461,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_subscription_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4673,6 +6487,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_subscription_filter")]
 impl From<crate::operation::put_subscription_filter::PutSubscriptionFilterError> for Error {
     fn from(err: crate::operation::put_subscription_filter::PutSubscriptionFilterError) -> Self {
         match err {
@@ -4700,6 +6515,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_syslog_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4725,6 +6541,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_syslog_configuration")]
 impl From<crate::operation::put_syslog_configuration::PutSyslogConfigurationError> for Error {
     fn from(err: crate::operation::put_syslog_configuration::PutSyslogConfigurationError) -> Self {
         match err {
@@ -4755,6 +6572,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_transformer")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_transformer::PutTransformerError, R>>
     for Error
@@ -4776,6 +6594,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_transformer")]
 impl From<crate::operation::put_transformer::PutTransformerError> for Error {
     fn from(err: crate::operation::put_transformer::PutTransformerError) -> Self {
         match err {
@@ -4801,6 +6620,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::start_live_tail::StartLiveTailError, R>>
     for Error
@@ -4822,6 +6642,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl From<crate::operation::start_live_tail::StartLiveTailError> for Error {
     fn from(err: crate::operation::start_live_tail::StartLiveTailError) -> Self {
         match err {
@@ -4850,6 +6671,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::start_query::StartQueryError, R>>
     for Error
 where
@@ -4867,6 +6689,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_query")]
 impl From<crate::operation::start_query::StartQueryError> for Error {
     fn from(err: crate::operation::start_query::StartQueryError) -> Self {
         match err {
@@ -4889,6 +6712,7 @@
         }
     }
 }
+#[cfg(feature = "op_stop_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::stop_query::StopQueryError, R>>
     for Error
 where
@@ -4906,6 +6730,7 @@
         }
     }
 }
+#[cfg(feature = "op_stop_query")]
 impl From<crate::operation::stop_query::StopQueryError> for Error {
     fn from(err: crate::operation::stop_query::StopQueryError) -> Self {
         match err {
@@ -4922,6 +6747,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_log_group")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_log_group::TagLogGroupError, R>>
     for Error
 where
@@ -4939,6 +6765,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_log_group")]
 impl From<crate::operation::tag_log_group::TagLogGroupError> for Error {
     fn from(err: crate::operation::tag_log_group::TagLogGroupError) -> Self {
         match err {
@@ -4952,6 +6779,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -4969,6 +6797,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -4988,6 +6817,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5013,6 +6843,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_metric_filter")]
 impl From<crate::operation::test_metric_filter::TestMetricFilterError> for Error {
     fn from(err: crate::operation::test_metric_filter::TestMetricFilterError) -> Self {
         match err {
@@ -5026,6 +6857,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_transformer")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<crate::operation::test_transformer::TestTransformerError, R>,
@@ -5048,6 +6880,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_transformer")]
 impl From<crate::operation::test_transformer::TestTransformerError> for Error {
     fn from(err: crate::operation::test_transformer::TestTransformerError) -> Self {
         match err {
@@ -5064,6 +6897,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_log_group::UntagLogGroupError, R>>
     for Error
@@ -5085,6 +6919,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_log_group")]
 impl From<crate::operation::untag_log_group::UntagLogGroupError> for Error {
     fn from(err: crate::operation::untag_log_group::UntagLogGroupError) -> Self {
         match err {
@@ -5095,6 +6930,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -5116,6 +6952,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -5132,6 +6969,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_anomaly")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_anomaly::UpdateAnomalyError, R>>
     for Error
@@ -5153,6 +6991,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_anomaly")]
 impl From<crate::operation::update_anomaly::UpdateAnomalyError> for Error {
     fn from(err: crate::operation::update_anomaly::UpdateAnomalyError) -> Self {
         match err {
@@ -5172,6 +7011,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_delivery_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5197,6 +7037,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_delivery_configuration")]
 impl From<crate::operation::update_delivery_configuration::UpdateDeliveryConfigurationError> for Error {
     fn from(err: crate::operation::update_delivery_configuration::UpdateDeliveryConfigurationError) -> Self {
         match err {
@@ -5222,6 +7063,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5247,6 +7089,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_log_anomaly_detector")]
 impl From<crate::operation::update_log_anomaly_detector::UpdateLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::update_log_anomaly_detector::UpdateLogAnomalyDetectorError) -> Self {
         match err {
@@ -5266,6 +7109,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5291,6 +7135,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_lookup_table")]
 impl From<crate::operation::update_lookup_table::UpdateLookupTableError> for Error {
     fn from(err: crate::operation::update_lookup_table::UpdateLookupTableError) -> Self {
         match err {
@@ -5313,6 +7158,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5338,6 +7184,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduled_query")]
 impl From<crate::operation::update_scheduled_query::UpdateScheduledQueryError> for Error {
     fn from(err: crate::operation::update_scheduled_query::UpdateScheduledQueryError) -> Self {
         match err {
@@ -5365,6 +7212,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::GetLogObjectResponseStreamError, R>>
     for Error
@@ -5386,6 +7234,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl From<crate::types::error::GetLogObjectResponseStreamError> for Error {
     fn from(err: crate::types::error::GetLogObjectResponseStreamError) -> Self {
         match err {
@@ -5396,6 +7245,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::StartLiveTailResponseStreamError, R>>
     for Error
@@ -5417,6 +7267,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl From<crate::types::error::StartLiveTailResponseStreamError> for Error {
     fn from(err: crate::types::error::StartLiveTailResponseStreamError) -> Self {
         match err {
@@ -5433,26 +7284,563 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::AccessDeniedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::DataAlreadyAcceptedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::InternalServerException(inner) => inner.source(),
+            #[cfg(feature = "op_get_log_object")]
             Error::InternalStreamingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Error::InvalidOperationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::InvalidParameterException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::InvalidSequenceTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(feature = "op_start_query")]
             Error::MalformedQueryException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Error::OperationAbortedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Error::ResourceAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.source(),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionStreamingException(inner) => inner.source(),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(feature = "op_tag_resource")]
             Error::TooManyTagsException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::UnrecognizedClientException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ValidationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -5461,26 +7849,563 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::AccessDeniedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::DataAlreadyAcceptedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::InternalServerException(e) => e.request_id(),
+            #[cfg(feature = "op_get_log_object")]
             Self::InternalStreamingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Self::InvalidOperationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::InvalidParameterException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::InvalidSequenceTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(feature = "op_start_query")]
             Self::MalformedQueryException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Self::OperationAbortedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Self::ResourceAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Self::ServiceQuotaExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::ServiceUnavailableException(e) => e.request_id(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionStreamingException(e) => e.request_id(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(feature = "op_tag_resource")]
             Self::TooManyTagsException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::UnrecognizedClientException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ValidationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
```

### `src/event_stream_serde.rs`

```diff
diff --git a/src/event_stream_serde.rs b/src/event_stream_serde.rs
--- a/src/event_stream_serde.rs
+++ b/src/event_stream_serde.rs
@@ -8,6 +8,7 @@
         GetLogObjectResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for GetLogObjectResponseStreamUnmarshaller {
     type Output = crate::types::GetLogObjectResponseStream;
     type Error = crate::types::error::GetLogObjectResponseStreamError;
@@ -84,6 +85,7 @@
         StartLiveTailResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for StartLiveTailResponseStreamUnmarshaller {
     type Output = crate::types::StartLiveTailResponseStream;
     type Error = crate::types::error::StartLiveTailResponseStreamError;
```

### `src/lens.rs`

```diff
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn reflens_describe_configuration_templates_output_output_next_token(
     input: &crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) fn reflens_describe_deliveries_output_output_next_token(
     input: &crate::operation::describe_deliveries::DescribeDeliveriesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) fn reflens_describe_delivery_destinations_output_output_next_token(
     input: &crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) fn reflens_describe_delivery_sources_output_output_next_token(
     input: &crate::operation::describe_delivery_sources::DescribeDeliverySourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) fn reflens_describe_destinations_output_output_next_token(
     input: &crate::operation::describe_destinations::DescribeDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) fn reflens_describe_log_groups_output_output_next_token(
     input: &crate::operation::describe_log_groups::DescribeLogGroupsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) fn reflens_describe_log_streams_output_output_next_token(
     input: &crate::operation::describe_log_streams::DescribeLogStreamsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) fn reflens_describe_metric_filters_output_output_next_token(
     input: &crate::operation::describe_metric_filters::DescribeMetricFiltersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) fn reflens_describe_subscription_filters_output_output_next_token(
     input: &crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) fn reflens_filter_log_events_output_output_next_token(
     input: &crate::operation::filter_log_events::FilterLogEventsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_log_events")]
 pub(crate) fn reflens_get_log_events_output_output_next_forward_token(
     input: &crate::operation::get_log_events::GetLogEventsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -109,6 +120,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) fn reflens_get_scheduled_query_history_output_output_next_token(
     input: &crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -119,6 +131,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) fn reflens_list_aggregate_log_group_summaries_output_output_next_token(
     input: &crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -129,6 +142,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn reflens_list_anomalies_output_output_next_token(
     input: &crate::operation::list_anomalies::ListAnomaliesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -139,6 +153,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) fn reflens_list_log_anomaly_detectors_output_output_next_token(
     input: &crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -149,6 +164,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) fn reflens_list_log_groups_for_query_output_output_next_token(
     input: &crate::operation::list_log_groups_for_query::ListLogGroupsForQueryOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -159,6 +175,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) fn reflens_list_scheduled_queries_output_output_next_token(
     input: &crate::operation::list_scheduled_queries::ListScheduledQueriesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -169,6 +186,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) fn reflens_list_sources_for_s3_table_integration_output_output_next_token(
     input: &crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -179,6 +197,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn lens_describe_configuration_templates_output_output_configuration_templates(
     input: crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ConfigurationTemplate>> {
@@ -186,6 +205,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) fn lens_describe_deliveries_output_output_deliveries(
     input: crate::operation::describe_deliveries::DescribeDeliveriesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Delivery>> {
@@ -193,6 +213,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) fn lens_describe_delivery_destinations_output_output_delivery_destinations(
     input: crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::DeliveryDestination>> {
@@ -200,6 +221,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) fn lens_describe_delivery_sources_output_output_delivery_sources(
     input: crate::operation::describe_delivery_sources::DescribeDeliverySourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::DeliverySource>> {
@@ -207,6 +229,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) fn lens_describe_destinations_output_output_destinations(
     input: crate::operation::describe_destinations::DescribeDestinationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Destination>> {
@@ -214,6 +237,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) fn lens_describe_log_groups_output_output_log_groups(
     input: crate::operation::describe_log_groups::DescribeLogGroupsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::LogGroup>> {
@@ -221,6 +245,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) fn lens_describe_log_streams_output_output_log_streams(
     input: crate::operation::describe_log_streams::DescribeLogStreamsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::LogStream>> {
@@ -228,6 +253,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) fn lens_describe_metric_filters_output_output_metric_filters(
     input: crate::operation::describe_metric_filters::DescribeMetricFiltersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::MetricFilter>> {
@@ -235,6 +261,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) fn lens_describe_subscription_filters_output_output_subscription_filters(
     input: crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SubscriptionFilter>> {
@@ -242,6 +269,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_log_events")]
 pub(crate) fn lens_get_log_events_output_output_events(
     input: crate::operation::get_log_events::GetLogEventsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::OutputLogEvent>> {
@@ -249,6 +277,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) fn lens_get_scheduled_query_history_output_output_trigger_history(
     input: crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TriggerHistoryRecord>> {
@@ -256,6 +285,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) fn lens_list_aggregate_log_group_summaries_output_output_aggregate_log_group_summaries(
     input: crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AggregateLogGroupSummary>> {
@@ -263,6 +293,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn lens_list_anomalies_output_output_anomalies(
     input: crate::operation::list_anomalies::ListAnomaliesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Anomaly>> {
@@ -270,6 +301,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) fn lens_list_log_anomaly_detectors_output_output_anomaly_detectors(
     input: crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AnomalyDetector>> {
@@ -277,6 +309,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) fn lens_list_log_groups_for_query_output_output_log_group_identifiers(
     input: crate::operation::list_log_groups_for_query::ListLogGroupsForQueryOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -284,6 +317,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) fn lens_list_scheduled_queries_output_output_scheduled_queries(
     input: crate::operation::list_scheduled_queries::ListScheduledQueriesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ScheduledQuerySummary>> {
@@ -291,6 +325,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) fn lens_list_sources_for_s3_table_integration_output_output_sources(
     input: crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::S3TableIntegrationSource>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,356 +1,474 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_associate_kms_key")]
 /// Types for the `AssociateKmsKey` operation.
 pub mod associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 /// Types for the `AssociateSourceToS3TableIntegration` operation.
 pub mod associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 /// Types for the `CancelExportTask` operation.
 pub mod cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 /// Types for the `CancelImportTask` operation.
 pub mod cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 /// Types for the `CreateDelivery` operation.
 pub mod create_delivery;

+#[cfg(feature = "op_create_export_task")]
 /// Types for the `CreateExportTask` operation.
 pub mod create_export_task;

+#[cfg(feature = "op_create_import_task")]
 /// Types for the `CreateImportTask` operation.
 pub mod create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 /// Types for the `CreateLogAnomalyDetector` operation.
 pub mod create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 /// Types for the `CreateLogGroup` operation.
 pub mod create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 /// Types for the `CreateLogStream` operation.
 pub mod create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 /// Types for the `CreateLookupTable` operation.
 pub mod create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 /// Types for the `CreateScheduledQuery` operation.
 pub mod create_scheduled_query;

+#[cfg(feature = "op_delete_account_policy")]
 /// Types for the `DeleteAccountPolicy` operation.
 pub mod delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 /// Types for the `DeleteDataProtectionPolicy` operation.
 pub mod delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 /// Types for the `DeleteDelivery` operation.
 pub mod delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 /// Types for the `DeleteDeliveryDestination` operation.
 pub mod delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 /// Types for the `DeleteDeliveryDestinationPolicy` operation.
 pub mod delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 /// Types for the `DeleteDeliverySource` operation.
 pub mod delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 /// Types for the `DeleteDestination` operation.
 pub mod delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 /// Types for the `DeleteIndexPolicy` operation.
 pub mod delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 /// Types for the `DeleteIntegration` operation.
 pub mod delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 /// Types for the `DeleteLogAnomalyDetector` operation.
 pub mod delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 /// Types for the `DeleteLogGroup` operation.
 pub mod delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 /// Types for the `DeleteLogStream` operation.
 pub mod delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 /// Types for the `DeleteLookupTable` operation.
 pub mod delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 /// Types for the `DeleteMetricFilter` operation.
 pub mod delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 /// Types for the `DeleteQueryDefinition` operation.
 pub mod delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 /// Types for the `DeleteResourcePolicy` operation.
 pub mod delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 /// Types for the `DeleteRetentionPolicy` operation.
 pub mod delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 /// Types for the `DeleteScheduledQuery` operation.
 pub mod delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 /// Types for the `DeleteSubscriptionFilter` operation.
 pub mod delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 /// Types for the `DeleteSyslogConfiguration` operation.
 pub mod delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 /// Types for the `DeleteTransformer` operation.
 pub mod delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 /// Types for the `DescribeAccountPolicies` operation.
 pub mod describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 /// Types for the `DescribeConfigurationTemplates` operation.
 pub mod describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 /// Types for the `DescribeDeliveries` operation.
 pub mod describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 /// Types for the `DescribeDeliveryDestinations` operation.
 pub mod describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 /// Types for the `DescribeDeliverySources` operation.
 pub mod describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 /// Types for the `DescribeDestinations` operation.
 pub mod describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 /// Types for the `DescribeExportTasks` operation.
 pub mod describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 /// Types for the `DescribeFieldIndexes` operation.
 pub mod describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 /// Types for the `DescribeImportTaskBatches` operation.
 pub mod describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 /// Types for the `DescribeImportTasks` operation.
 pub mod describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 /// Types for the `DescribeIndexPolicies` operation.
 pub mod describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 /// Types for the `DescribeLogGroups` operation.
 pub mod describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 /// Types for the `DescribeLogStreams` operation.
 pub mod describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 /// Types for the `DescribeLookupTables` operation.
 pub mod describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 /// Types for the `DescribeMetricFilters` operation.
 pub mod describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 /// Types for the `DescribeQueries` operation.
 pub mod describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 /// Types for the `DescribeQueryDefinitions` operation.
 pub mod describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 /// Types for the `DescribeResourcePolicies` operation.
 pub mod describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 /// Types for the `DescribeSubscriptionFilters` operation.
 pub mod describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 /// Types for the `DisassociateKmsKey` operation.
 pub mod disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 /// Types for the `DisassociateSourceFromS3TableIntegration` operation.
 pub mod disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 /// Types for the `FilterLogEvents` operation.
 pub mod filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 /// Types for the `GetDataProtectionPolicy` operation.
 pub mod get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 /// Types for the `GetDelivery` operation.
 pub mod get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 /// Types for the `GetDeliveryDestination` operation.
 pub mod get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 /// Types for the `GetDeliveryDestinationPolicy` operation.
 pub mod get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 /// Types for the `GetDeliverySource` operation.
 pub mod get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 /// Types for the `GetIntegration` operation.
 pub mod get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 /// Types for the `GetLogAnomalyDetector` operation.
 pub mod get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 /// Types for the `GetLogEvents` operation.
 pub mod get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 /// Types for the `GetLogFields` operation.
 pub mod get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 /// Types for the `GetLogGroupFields` operation.
 pub mod get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 /// Types for the `GetLogObject` operation.
 pub mod get_log_object;

+#[cfg(feature = "op_get_log_record")]
 /// Types for the `GetLogRecord` operation.
 pub mod get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 /// Types for the `GetLookupTable` operation.
 pub mod get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 /// Types for the `GetQueryResults` operation.
 pub mod get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 /// Types for the `GetScheduledQuery` operation.
 pub mod get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 /// Types for the `GetScheduledQueryHistory` operation.
 pub mod get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 /// Types for the `GetStorageTierPolicy` operation.
 pub mod get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 /// Types for the `GetTransformer` operation.
 pub mod get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 /// Types for the `ListAggregateLogGroupSummaries` operation.
 pub mod list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 /// Types for the `ListAnomalies` operation.
 pub mod list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 /// Types for the `ListIntegrations` operation.
 pub mod list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 /// Types for the `ListLogAnomalyDetectors` operation.
 pub mod list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 /// Types for the `ListLogGroups` operation.
 pub mod list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 /// Types for the `ListLogGroupsForQuery` operation.
 pub mod list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 /// Types for the `ListScheduledQueries` operation.
 pub mod list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 /// Types for the `ListSourcesForS3TableIntegration` operation.
 pub mod list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 /// Types for the `ListSyslogConfigurations` operation.
 pub mod list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 /// Types for the `ListTagsLogGroup` operation.
 pub mod list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 /// Types for the `PutAccountPolicy` operation.
 pub mod put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 /// Types for the `PutBearerTokenAuthentication` operation.
 pub mod put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 /// Types for the `PutDataProtectionPolicy` operation.
 pub mod put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 /// Types for the `PutDeliveryDestination` operation.
 pub mod put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 /// Types for the `PutDeliveryDestinationPolicy` operation.
 pub mod put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 /// Types for the `PutDeliverySource` operation.
 pub mod put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 /// Types for the `PutDestination` operation.
 pub mod put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 /// Types for the `PutDestinationPolicy` operation.
 pub mod put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 /// Types for the `PutIndexPolicy` operation.
 pub mod put_index_policy;

+#[cfg(feature = "op_put_integration")]
 /// Types for the `PutIntegration` operation.
 pub mod put_integration;

+#[cfg(feature = "op_put_log_events")]
 /// Types for the `PutLogEvents` operation.
 pub mod put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 /// Types for the `PutLogGroupDeletionProtection` operation.
 pub mod put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 /// Types for the `PutMetricFilter` operation.
 pub mod put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 /// Types for the `PutQueryDefinition` operation.
 pub mod put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 /// Types for the `PutResourcePolicy` operation.
 pub mod put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 /// Types for the `PutRetentionPolicy` operation.
 pub mod put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 /// Types for the `PutStorageTierPolicy` operation.
 pub mod put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 /// Types for the `PutSubscriptionFilter` operation.
 pub mod put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 /// Types for the `PutSyslogConfiguration` operation.
 pub mod put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 /// Types for the `PutTransformer` operation.
 pub mod put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 /// Types for the `StartLiveTail` operation.
 pub mod start_live_tail;

+#[cfg(feature = "op_start_query")]
 /// Types for the `StartQuery` operation.
 pub mod start_query;

+#[cfg(feature = "op_stop_query")]
 /// Types for the `StopQuery` operation.
 pub mod stop_query;

+#[cfg(feature = "op_tag_log_group")]
 /// Types for the `TagLogGroup` operation.
 pub mod tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 /// Types for the `TestMetricFilter` operation.
 pub mod test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 /// Types for the `TestTransformer` operation.
 pub mod test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 /// Types for the `UntagLogGroup` operation.
 pub mod untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 /// Types for the `UpdateAnomaly` operation.
 pub mod update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 /// Types for the `UpdateDeliveryConfiguration` operation.
 pub mod update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 /// Types for the `UpdateLogAnomalyDetector` operation.
 pub mod update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 /// Types for the `UpdateLookupTable` operation.
 pub mod update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 /// Types for the `UpdateScheduledQuery` operation.
 pub mod update_scheduled_query;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,124 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +137,126 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,242 +268,480 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_associate_kms_key")]
 pub(crate) mod shape_associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 pub(crate) mod shape_associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 pub(crate) mod shape_cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 pub(crate) mod shape_cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 pub(crate) mod shape_create_delivery;

+#[cfg(feature = "op_create_export_task")]
 pub(crate) mod shape_create_export_task;

+#[cfg(feature = "op_create_import_task")]
 pub(crate) mod shape_create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 pub(crate) mod shape_create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 pub(crate) mod shape_create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 pub(crate) mod shape_create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 pub(crate) mod shape_create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 pub(crate) mod shape_create_scheduled_query;

+#[cfg(feature = "op_delete_account_policy")]
 pub(crate) mod shape_delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 pub(crate) mod shape_delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 pub(crate) mod shape_delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 pub(crate) mod shape_delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 pub(crate) mod shape_delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 pub(crate) mod shape_delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 pub(crate) mod shape_delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 pub(crate) mod shape_delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 pub(crate) mod shape_delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 pub(crate) mod shape_delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 pub(crate) mod shape_delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 pub(crate) mod shape_delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 pub(crate) mod shape_delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 pub(crate) mod shape_delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 pub(crate) mod shape_delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 pub(crate) mod shape_delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 pub(crate) mod shape_delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 pub(crate) mod shape_delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 pub(crate) mod shape_delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 pub(crate) mod shape_delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 pub(crate) mod shape_disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 pub(crate) mod shape_disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 pub(crate) mod shape_get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 pub(crate) mod shape_get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 pub(crate) mod shape_get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 pub(crate) mod shape_get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 pub(crate) mod shape_get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 pub(crate) mod shape_get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 pub(crate) mod shape_get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 pub(crate) mod shape_get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 pub(crate) mod shape_list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 pub(crate) mod shape_put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 pub(crate) mod shape_put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 pub(crate) mod shape_put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 pub(crate) mod shape_put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 pub(crate) mod shape_put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 pub(crate) mod shape_put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 pub(crate) mod shape_put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 pub(crate) mod shape_put_index_policy;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_put_integration;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 pub(crate) mod shape_put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 pub(crate) mod shape_put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 pub(crate) mod shape_put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 pub(crate) mod shape_put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 pub(crate) mod shape_put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 pub(crate) mod shape_put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 pub(crate) mod shape_put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 pub(crate) mod shape_put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_start_query;

+#[cfg(feature = "op_stop_query")]
 pub(crate) mod shape_stop_query;

+#[cfg(feature = "op_tag_log_group")]
 pub(crate) mod shape_tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 pub(crate) mod shape_untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 pub(crate) mod shape_update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 pub(crate) mod shape_update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 pub(crate) mod shape_update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 pub(crate) mod shape_update_scheduled_query;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -272,286 +750,943 @@
     }
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_access_denied_exception;

+#[cfg(feature = "op_associate_kms_key")]
 pub(crate) mod shape_associate_kms_key_input;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 pub(crate) mod shape_associate_source_to_s3_table_integration_input;

+#[cfg(feature = "op_cancel_export_task")]
 pub(crate) mod shape_cancel_export_task_input;

+#[cfg(feature = "op_cancel_import_task")]
 pub(crate) mod shape_cancel_import_task_input;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_create_delivery")]
 pub(crate) mod shape_create_delivery_input;

+#[cfg(feature = "op_create_export_task")]
 pub(crate) mod shape_create_export_task_input;

+#[cfg(feature = "op_create_import_task")]
 pub(crate) mod shape_create_import_task_input;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 pub(crate) mod shape_create_log_anomaly_detector_input;

+#[cfg(feature = "op_create_log_group")]
 pub(crate) mod shape_create_log_group_input;

+#[cfg(feature = "op_create_log_stream")]
 pub(crate) mod shape_create_log_stream_input;

+#[cfg(feature = "op_create_lookup_table")]
 pub(crate) mod shape_create_lookup_table_input;

+#[cfg(feature = "op_create_scheduled_query")]
 pub(crate) mod shape_create_scheduled_query_input;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_data_already_accepted_exception;

+#[cfg(feature = "op_delete_account_policy")]
 pub(crate) mod shape_delete_account_policy_input;

+#[cfg(feature = "op_delete_data_protection_policy")]
 pub(crate) mod shape_delete_data_protection_policy_input;

+#[cfg(feature = "op_delete_delivery_destination")]
 pub(crate) mod shape_delete_delivery_destination_input;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 pub(crate) mod shape_delete_delivery_destination_policy_input;

+#[cfg(feature = "op_delete_delivery")]
 pub(crate) mod shape_delete_delivery_input;

+#[cfg(feature = "op_delete_delivery_source")]
 pub(crate) mod shape_delete_delivery_source_input;

+#[cfg(feature = "op_delete_destination")]
 pub(crate) mod shape_delete_destination_input;

+#[cfg(feature = "op_delete_index_policy")]
 pub(crate) mod shape_delete_index_policy_input;

+#[cfg(feature = "op_delete_integration")]
 pub(crate) mod shape_delete_integration_input;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 pub(crate) mod shape_delete_log_anomaly_detector_input;

+#[cfg(feature = "op_delete_log_group")]
 pub(crate) mod shape_delete_log_group_input;

+#[cfg(feature = "op_delete_log_stream")]
 pub(crate) mod shape_delete_log_stream_input;

+#[cfg(feature = "op_delete_lookup_table")]
 pub(crate) mod shape_delete_lookup_table_input;

+#[cfg(feature = "op_delete_metric_filter")]
 pub(crate) mod shape_delete_metric_filter_input;

+#[cfg(feature = "op_delete_query_definition")]
 pub(crate) mod shape_delete_query_definition_input;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy_input;

+#[cfg(feature = "op_delete_retention_policy")]
 pub(crate) mod shape_delete_retention_policy_input;

+#[cfg(feature = "op_delete_scheduled_query")]
 pub(crate) mod shape_delete_scheduled_query_input;

+#[cfg(feature = "op_delete_subscription_filter")]
 pub(crate) mod shape_delete_subscription_filter_input;

+#[cfg(feature = "op_delete_syslog_configuration")]
 pub(crate) mod shape_delete_syslog_configuration_input;

+#[cfg(feature = "op_delete_transformer")]
 pub(crate) mod shape_delete_transformer_input;

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_describe_account_policies_input;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_describe_configuration_templates_input;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_describe_deliveries_input;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_describe_delivery_destinations_input;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_describe_delivery_sources_input;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_describe_destinations_input;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_describe_export_tasks_input;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_describe_field_indexes_input;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_describe_import_task_batches_input;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_describe_import_tasks_input;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_describe_index_policies_input;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_describe_log_groups_input;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_describe_log_streams_input;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_describe_lookup_tables_input;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_describe_metric_filters_input;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_describe_queries_input;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_describe_query_definitions_input;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_describe_resource_policies_input;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_describe_subscription_filters_input;

+#[cfg(feature = "op_disassociate_kms_key")]
 pub(crate) mod shape_disassociate_kms_key_input;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 pub(crate) mod shape_disassociate_source_from_s3_table_integration_input;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filter_log_events_input;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy_input;

+#[cfg(feature = "op_get_delivery_destination")]
 pub(crate) mod shape_get_delivery_destination_input;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 pub(crate) mod shape_get_delivery_destination_policy_input;

+#[cfg(feature = "op_get_delivery")]
 pub(crate) mod shape_get_delivery_input;

+#[cfg(feature = "op_get_delivery_source")]
 pub(crate) mod shape_get_delivery_source_input;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_get_integration_input;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 pub(crate) mod shape_get_log_anomaly_detector_input;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_get_log_events_input;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_get_log_fields_input;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_get_log_group_fields_input;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object_input;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object_output;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_get_log_record_input;

+#[cfg(feature = "op_get_lookup_table")]
 pub(crate) mod shape_get_lookup_table_input;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_get_query_results_input;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_get_scheduled_query_history_input;

+#[cfg(feature = "op_get_scheduled_query")]
 pub(crate) mod shape_get_scheduled_query_input;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_get_transformer_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_internal_server_exception;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_internal_streaming_exception;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_invalid_operation_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub(crate) mod shape_invalid_parameter_exception;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_invalid_sequence_token_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_list_aggregate_log_group_summaries_input;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_list_anomalies_input;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_list_integrations_input;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_list_log_anomaly_detectors_input;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_list_log_groups_for_query_input;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_list_log_groups_input;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_list_scheduled_queries_input;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_list_sources_for_s3_table_integration_input;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_list_syslog_configurations_input;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource_input;

+#[cfg(feature = "op_list_tags_log_group")]
 pub(crate) mod shape_list_tags_log_group_input;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_malformed_query_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub(crate) mod shape_operation_aborted_exception;

+#[cfg(feature = "op_put_account_policy")]
 pub(crate) mod shape_put_account_policy_input;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 pub(crate) mod shape_put_bearer_token_authentication_input;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy_input;

+#[cfg(feature = "op_put_delivery_destination")]
 pub(crate) mod shape_put_delivery_destination_input;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 pub(crate) mod shape_put_delivery_destination_policy_input;

+#[cfg(feature = "op_put_delivery_source")]
 pub(crate) mod shape_put_delivery_source_input;

+#[cfg(feature = "op_put_destination")]
 pub(crate) mod shape_put_destination_input;

+#[cfg(feature = "op_put_destination_policy")]
 pub(crate) mod shape_put_destination_policy_input;

+#[cfg(feature = "op_put_index_policy")]
 pub(crate) mod shape_put_index_policy_input;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_put_integration_input;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_put_log_events_input;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 pub(crate) mod shape_put_log_group_deletion_protection_input;

+#[cfg(feature = "op_put_metric_filter")]
 pub(crate) mod shape_put_metric_filter_input;

+#[cfg(feature = "op_put_query_definition")]
 pub(crate) mod shape_put_query_definition_input;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy_input;

+#[cfg(feature = "op_put_retention_policy")]
 pub(crate) mod shape_put_retention_policy_input;

+#[cfg(feature = "op_put_storage_tier_policy")]
 pub(crate) mod shape_put_storage_tier_policy_input;

+#[cfg(feature = "op_put_subscription_filter")]
 pub(crate) mod shape_put_subscription_filter_input;

+#[cfg(feature = "op_put_syslog_configuration")]
 pub(crate) mod shape_put_syslog_configuration_input;

+#[cfg(feature = "op_put_transformer")]
 pub(crate) mod shape_put_transformer_input;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub(crate) mod shape_resource_already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub(crate) mod shape_service_unavailable_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_session_streaming_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_session_timeout_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_input;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_output;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_start_query_input;

+#[cfg(feature = "op_stop_query")]
 pub(crate) mod shape_stop_query_input;

+#[cfg(feature = "op_tag_log_group")]
 pub(crate) mod shape_tag_log_group_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_test_metric_filter_input;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_test_transformer_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_too_many_tags_exception;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_unrecognized_client_exception;

+#[cfg(feature = "op_untag_log_group")]
 pub(crate) mod shape_untag_log_group_input;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_update_anomaly_input;

+#[cfg(feature = "op_update_delivery_configuration")]
 pub(crate) mod shape_update_delivery_configuration_input;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 pub(crate) mod shape_update_log_anomaly_detector_input;

+#[cfg(feature = "op_update_lookup_table")]
 pub(crate) mod shape_update_lookup_table_input;

+#[cfg(feature = "op_update_scheduled_query")]
 pub(crate) mod shape_update_scheduled_query_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(any(feature = "op_get_log_object", feature = "op_start_live_tail"))]
 pub fn parse_event_stream_error_metadata(
     payload: &::bytes::Bytes,
 ) -> ::std::result::Result<
@@ -561,398 +1696,848 @@
     crate::json_errors::parse_error_metadata(payload, &::aws_smithy_runtime_api::http::Headers::new())
 }

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_account_policies;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub(crate) mod shape_account_policy;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_anomalies;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_anomaly_detectors;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_templates;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub(crate) mod shape_data_source;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub(crate) mod shape_data_source_filter;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_deliveries;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub(crate) mod shape_delivery;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) mod shape_delivery_destination;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) mod shape_delivery_destination_configuration;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_delivery_destinations;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_delivery_source;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_delivery_sources;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub(crate) mod shape_destination;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_destination_configuration;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_destinations;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_entity;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_field_indexes;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filtered_log_events;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_import_batch_list;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub(crate) mod shape_import_filter;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_import_list;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub(crate) mod shape_import_statistics;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_index_policies;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub(crate) mod shape_index_policy;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_input_log_event;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_integration_details;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_integration_summaries;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_fields_list;

+#[cfg(any(
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors"
+))]
 pub(crate) mod shape_log_group_arn_list;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_log_group_field_list;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_log_group_identifiers;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_log_group_summaries;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_log_groups;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_log_record;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_lookup_tables;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_metric_filter_matches;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_filters;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) mod shape_metric_transformation;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_output_log_events;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub(crate) mod shape_policy;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_processor;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_processors;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_query_compile_error;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_definition_list;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_query_info_list;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub(crate) mod shape_query_parameter;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_query_results;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_query_statistics;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_rejected_entity_info;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_rejected_log_events_info;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_resource_config;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_resource_policies;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub(crate) mod shape_resource_policy;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub(crate) mod shape_s3_delivery_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_s3_table_integration_sources;

+#[cfg(any(feature = "op_get_scheduled_query", feature = "op_update_scheduled_query"))]
 pub(crate) mod shape_scheduled_query_log_group_identifiers;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_scheduled_query_summary_list;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_searched_log_streams;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_subscription_filters;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_suppression_period;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_syslog_configurations;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_tag_filter;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_tags;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_transformed_logs;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_trigger_history_record_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_keys;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_aggregate_log_group_summary;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_anomaly;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_anomaly_detector;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_template;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_csv;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_date_time_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_delete_keys;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_delivery_source_configuration;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_field_index;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_fields_data;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filtered_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_grok;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_import;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_import_batch;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_integration_summary;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_list_to_map;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_start;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_update;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_fields_list_item;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_log_group;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_log_group_field;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_log_group_summary;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_log_stream;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_lookup_table;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_lookup_table_configuration;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_lower_case_string;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_filter;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_metric_filter_match_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_keys;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_integration_details;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_open_search_resource_config;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_output_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_cloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_json;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_key_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_postgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_route53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_to_ocsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_vpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_waf;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_query_compile_error_location;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_definition;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_query_info;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub(crate) mod shape_record_fields;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_keys;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_resource_arns;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_result_rows;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_s3_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_s3_table_integration_source;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_scheduled_query_summary;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_searched_log_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_subscription_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_syslog_configuration;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_transformed_log_record;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_trigger_history_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_trim_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_upper_case_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_key_entry;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_allowed_field_delimiters;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_allowed_fields;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_template_delivery_config_values;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value_entry;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_schemas;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_describe_subscription_filters"))]
 pub(crate) mod shape_emit_system_fields;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task_execution_info;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task_status;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_extracted_values;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_grouping_identifiers;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_histogram;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_inherited_properties;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_field_type;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_log_group_names;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_log_samples;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_transformations;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_key_entry;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_application;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_collection;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_data_access_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_data_source;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_encryption_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_lifecycle_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_network_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_workspace;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_output_formats;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_pattern_tokens;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_parameter_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_key_entry;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_result_field;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_s3_tables_integration;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_scheduled_query_destination_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string_entry;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_table_fields;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_key_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_columns;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_delete_with_keys;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_schema;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_grouping_identifier;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_input_log_stream_names;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_metadata;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_results;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_lower_case_string_with_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_match_patterns;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_key_entries;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_resource_status;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_pattern_token;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_record_field;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_key_entries;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_scheduled_query_destination;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string_entries;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_log_group_identifiers;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_trim_string_with_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_upper_case_string_with_keys;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_supported_values;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) mod shape_dimensions;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_enumerations;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_log_event;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_put_log_events")]
 pub(crate) fn rejected_entity_info_correct_errors(
     mut builder: crate::types::builders::RejectedEntityInfoBuilder,
 ) -> crate::types::builders::RejectedEntityInfoBuilder {
@@ -10,6 +11,7 @@
     builder
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn anomaly_correct_errors(
     mut builder: crate::types::builders::AnomalyBuilder,
 ) -> crate::types::builders::AnomalyBuilder {
@@ -55,6 +57,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) fn delivery_destination_configuration_correct_errors(
     mut builder: crate::types::builders::DeliveryDestinationConfigurationBuilder,
 ) -> crate::types::builders::DeliveryDestinationConfigurationBuilder {
@@ -64,6 +71,7 @@
     builder
 }

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) fn import_batch_correct_errors(
     mut builder: crate::types::builders::ImportBatchBuilder,
 ) -> crate::types::builders::ImportBatchBuilder {
@@ -76,6 +84,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn lookup_table_configuration_correct_errors(
     mut builder: crate::types::builders::LookupTableConfigurationBuilder,
 ) -> crate::types::builders::LookupTableConfigurationBuilder {
@@ -88,6 +102,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn s3_configuration_correct_errors(
     mut builder: crate::types::builders::S3ConfigurationBuilder,
 ) -> crate::types::builders::S3ConfigurationBuilder {
@@ -100,6 +120,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn add_keys_correct_errors(
     mut builder: crate::types::builders::AddKeysBuilder,
 ) -> crate::types::builders::AddKeysBuilder {
@@ -109,6 +134,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn copy_value_correct_errors(
     mut builder: crate::types::builders::CopyValueBuilder,
 ) -> crate::types::builders::CopyValueBuilder {
@@ -118,6 +148,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub(crate) fn data_source_correct_errors(
     mut builder: crate::types::builders::DataSourceBuilder,
 ) -> crate::types::builders::DataSourceBuilder {
@@ -127,6 +161,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn date_time_converter_correct_errors(
     mut builder: crate::types::builders::DateTimeConverterBuilder,
 ) -> crate::types::builders::DateTimeConverterBuilder {
@@ -142,6 +181,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn delete_keys_correct_errors(
     mut builder: crate::types::builders::DeleteKeysBuilder,
 ) -> crate::types::builders::DeleteKeysBuilder {
@@ -151,6 +195,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn grok_correct_errors(
     mut builder: crate::types::builders::GrokBuilder,
 ) -> crate::types::builders::GrokBuilder {
@@ -160,6 +209,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn list_to_map_correct_errors(
     mut builder: crate::types::builders::ListToMapBuilder,
 ) -> crate::types::builders::ListToMapBuilder {
@@ -172,6 +226,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn lower_case_string_correct_errors(
     mut builder: crate::types::builders::LowerCaseStringBuilder,
 ) -> crate::types::builders::LowerCaseStringBuilder {
@@ -181,6 +240,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn move_keys_correct_errors(
     mut builder: crate::types::builders::MoveKeysBuilder,
 ) -> crate::types::builders::MoveKeysBuilder {
@@ -190,6 +254,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn parse_to_ocsf_correct_errors(
     mut builder: crate::types::builders::ParseToOcsfBuilder,
 ) -> crate::types::builders::ParseToOcsfBuilder {
@@ -202,6 +271,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn rename_keys_correct_errors(
     mut builder: crate::types::builders::RenameKeysBuilder,
 ) -> crate::types::builders::RenameKeysBuilder {
@@ -211,6 +285,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn split_string_correct_errors(
     mut builder: crate::types::builders::SplitStringBuilder,
 ) -> crate::types::builders::SplitStringBuilder {
@@ -220,6 +299,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn substitute_string_correct_errors(
     mut builder: crate::types::builders::SubstituteStringBuilder,
 ) -> crate::types::builders::SubstituteStringBuilder {
@@ -229,6 +313,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn trim_string_correct_errors(
     mut builder: crate::types::builders::TrimStringBuilder,
 ) -> crate::types::builders::TrimStringBuilder {
@@ -238,6 +327,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn type_converter_correct_errors(
     mut builder: crate::types::builders::TypeConverterBuilder,
 ) -> crate::types::builders::TypeConverterBuilder {
@@ -247,6 +341,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn upper_case_string_correct_errors(
     mut builder: crate::types::builders::UpperCaseStringBuilder,
 ) -> crate::types::builders::UpperCaseStringBuilder {
@@ -256,6 +355,7 @@
     builder
 }

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn delivery_source_configuration_schema_correct_errors(
     mut builder: crate::types::builders::DeliverySourceConfigurationSchemaBuilder,
 ) -> crate::types::builders::DeliverySourceConfigurationSchemaBuilder {
@@ -273,6 +373,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) fn metric_transformation_correct_errors(
     mut builder: crate::types::builders::MetricTransformationBuilder,
 ) -> crate::types::builders::MetricTransformationBuilder {
@@ -288,6 +389,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub(crate) fn query_parameter_correct_errors(
     mut builder: crate::types::builders::QueryParameterBuilder,
 ) -> crate::types::builders::QueryParameterBuilder {
@@ -297,6 +399,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn add_key_entry_correct_errors(
     mut builder: crate::types::builders::AddKeyEntryBuilder,
 ) -> crate::types::builders::AddKeyEntryBuilder {
@@ -309,6 +416,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn copy_value_entry_correct_errors(
     mut builder: crate::types::builders::CopyValueEntryBuilder,
 ) -> crate::types::builders::CopyValueEntryBuilder {
@@ -321,6 +433,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn move_key_entry_correct_errors(
     mut builder: crate::types::builders::MoveKeyEntryBuilder,
 ) -> crate::types::builders::MoveKeyEntryBuilder {
@@ -333,6 +450,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn rename_key_entry_correct_errors(
     mut builder: crate::types::builders::RenameKeyEntryBuilder,
 ) -> crate::types::builders::RenameKeyEntryBuilder {
@@ -345,6 +467,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn split_string_entry_correct_errors(
     mut builder: crate::types::builders::SplitStringEntryBuilder,
 ) -> crate::types::builders::SplitStringEntryBuilder {
@@ -357,6 +484,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn substitute_string_entry_correct_errors(
     mut builder: crate::types::builders::SubstituteStringEntryBuilder,
 ) -> crate::types::builders::SubstituteStringEntryBuilder {
@@ -372,6 +504,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn type_converter_entry_correct_errors(
     mut builder: crate::types::builders::TypeConverterEntryBuilder,
 ) -> crate::types::builders::TypeConverterEntryBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,654 +1,1486 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub use crate::types::_data_source::DataSource;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_statistics::ImportStatistics;

+#[cfg(any(
+    feature = "op_cancel_import_task",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks"
+))]
 pub use crate::types::_import_status::ImportStatus;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub use crate::types::_s3_delivery_configuration::S3DeliveryConfiguration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub use crate::types::_delivery::Delivery;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_filter::ImportFilter;

+#[cfg(any(
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::_evaluation_frequency::EvaluationFrequency;

+#[cfg(any(
+    feature = "op_create_log_group",
+    feature = "op_describe_log_groups",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_log_groups"
+))]
 pub use crate::types::_log_group_class::LogGroupClass;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_put_query_definition",
+    feature = "op_start_query",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_query_language::QueryLanguage;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_destination_configuration::DestinationConfiguration;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_scheduled_query_state::ScheduledQueryState;

+#[cfg(any(
+    feature = "op_delete_account_policy",
+    feature = "op_describe_account_policies",
+    feature = "op_put_account_policy"
+))]
 pub use crate::types::_policy_type::PolicyType;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status_code::ExportTaskStatusCode;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_order_by::OrderBy;

+#[cfg(any(feature = "op_describe_queries", feature = "op_get_query_results"))]
 pub use crate::types::_query_status::QueryStatus;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_policy_scope::PolicyScope;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination::DeliveryDestination;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub use crate::types::_policy::Policy;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source::DeliverySource;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 pub use crate::types::_integration_type::IntegrationType;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 pub use crate::types::_integration_status::IntegrationStatus;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_integration_details::IntegrationDetails;

+#[cfg(any(feature = "op_get_log_anomaly_detector", feature = "op_list_log_anomaly_detectors"))]
 pub use crate::types::_anomaly_detector_status::AnomalyDetectorStatus;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_get_log_object_response_stream::GetLogObjectResponseStream;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_query_statistics::QueryStatistics;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_schedule_type::ScheduleType;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_execution_status::ExecutionStatus;

+#[cfg(any(feature = "op_get_storage_tier_policy", feature = "op_put_storage_tier_policy"))]
 pub use crate::types::_storage_tier::StorageTier;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_list_aggregate_log_group_summaries_group_by::ListAggregateLogGroupSummariesGroupBy;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_suppression_state::SuppressionState;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_scope::Scope;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_account_policy::AccountPolicy;

+#[cfg(any(
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_output_format::OutputFormat;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_configuration::DeliveryDestinationConfiguration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_type::DeliveryDestinationType;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub use crate::types::_destination::Destination;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_policy::IndexPolicy;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_resource_config::ResourceConfig;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity::Entity;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_log_events_info::RejectedLogEventsInfo;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_entity_info::RejectedEntityInfo;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_resource_policy::ResourcePolicy;

+#[cfg(any(feature = "op_describe_subscription_filters", feature = "op_put_subscription_filter"))]
 pub use crate::types::_distribution::Distribution;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_start_live_tail_response_stream::StartLiveTailResponseStream;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error::QueryCompileError;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_type::SuppressionType;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_period::SuppressionPeriod;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_s3_configuration::S3Configuration;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_lookup_table_configuration::LookupTableConfiguration;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template::ConfigurationTemplate;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task::ExportTask;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_index_category::IndexCategory;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_field_index::FieldIndex;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub use crate::types::_import_batch::ImportBatch;

+#[cfg(feature = "op_describe_import_tasks")]
 pub use crate::types::_import::Import;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_log_group::LogGroup;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_log_stream::LogStream;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub use crate::types::_lookup_table::LookupTable;

+#[cfg(feature = "op_describe_metric_filters")]
 pub use crate::types::_metric_filter::MetricFilter;

+#[cfg(feature = "op_describe_queries")]
 pub use crate::types::_query_info::QueryInfo;

+#[cfg(feature = "op_describe_query_definitions")]
 pub use crate::types::_query_definition::QueryDefinition;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub use crate::types::_subscription_filter::SubscriptionFilter;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_filtered_log_event::FilteredLogEvent;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_searched_log_stream::SearchedLogStream;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source_status::DeliverySourceStatus;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source_status_reason::DeliverySourceStatusReason;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_integration_details::OpenSearchIntegrationDetails;

+#[cfg(feature = "op_get_log_events")]
 pub use crate::types::_output_log_event::OutputLogEvent;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_fields_list_item::LogFieldsListItem;

+#[cfg(feature = "op_get_log_group_fields")]
 pub use crate::types::_log_group_field::LogGroupField;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_fields_data::FieldsData;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_trigger_history_record::TriggerHistoryRecord;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_processor::Processor;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub use crate::types::_data_source_filter::DataSourceFilter;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_aggregate_log_group_summary::AggregateLogGroupSummary;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_anomaly::Anomaly;

+#[cfg(feature = "op_list_integrations")]
 pub use crate::types::_integration_summary::IntegrationSummary;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub use crate::types::_anomaly_detector::AnomalyDetector;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_tag_filter::TagFilter;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_log_group_summary::LogGroupSummary;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub use crate::types::_scheduled_query_summary::ScheduledQuerySummary;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source::S3TableIntegrationSource;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_configuration::SyslogConfiguration;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_source::IndexSource;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_open_search_resource_config::OpenSearchResourceConfig;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_input_log_event::InputLogEvent;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity_rejection_error_type::EntityRejectionErrorType;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_metric_transformation::MetricTransformation;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub use crate::types::_query_parameter::QueryParameter;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_start::LiveTailSessionStart;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_update::LiveTailSessionUpdate;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error_location::QueryCompileErrorLocation;

+#[cfg(feature = "op_test_metric_filter")]
 pub use crate::types::_metric_filter_match_record::MetricFilterMatchRecord;

+#[cfg(feature = "op_test_transformer")]
 pub use crate::types::_transformed_log_record::TransformedLogRecord;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_unit::SuppressionUnit;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template_delivery_config_values::ConfigurationTemplateDeliveryConfigValues;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_s3_tables_integration::S3TablesIntegration;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status::ExportTaskStatus;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_execution_info::ExportTaskExecutionInfo;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_index_type::IndexType;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_data_protection_status::DataProtectionStatus;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_source::OpenSearchDataSource;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_application::OpenSearchApplication;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_collection::OpenSearchCollection;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_workspace::OpenSearchWorkspace;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_encryption_policy::OpenSearchEncryptionPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_network_policy::OpenSearchNetworkPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_access_policy::OpenSearchDataAccessPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_lifecycle_policy::OpenSearchLifecyclePolicy;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_field_type::LogFieldType;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_result_field::ResultField;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_keys::AddKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value::CopyValue;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_csv::Csv;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_date_time_converter::DateTimeConverter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_delete_keys::DeleteKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_grok::Grok;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_list_to_map::ListToMap;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_lower_case_string::LowerCaseString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_keys::MoveKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_cloudfront::ParseCloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_json::ParseJson;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_key_value::ParseKeyValue;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_route53::ParseRoute53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_to_ocsf::ParseToOcsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_postgres::ParsePostgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_vpc::ParseVpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_waf::ParseWaf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_keys::RenameKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string::SplitString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string::SubstituteString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_trim_string::TrimString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter::TypeConverter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_upper_case_string::UpperCaseString;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_state::State;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source_status::S3TableIntegrationSourceStatus;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_source_type::SyslogSourceType;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_standard_unit::StandardUnit;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_metadata::LiveTailSessionMetadata;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_record_field::RecordField;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema::DeliverySourceConfigurationSchema;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_inherited_property::InheritedProperty;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status::OpenSearchResourceStatus;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination::ScheduledQueryDestination;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_flattened_element::FlattenedElement;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_event_source::EventSource;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_ocsf_version::OcsfVersion;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_grouping_identifier::GroupingIdentifier;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_log_event::LogEvent;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_pattern_token::PatternToken;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_log_event::LiveTailSessionLogEvent;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema_value_type::DeliverySourceConfigurationSchemaValueType;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status_type::OpenSearchResourceStatusType;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination_type::ScheduledQueryDestinationType;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_action_status::ActionStatus;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_key_entry::AddKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value_entry::CopyValueEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_key_entry::MoveKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_key_entry::RenameKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string_entry::SplitStringEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string_entry::SubstituteStringEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter_entry::TypeConverterEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_::Type;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 mod _account_policy;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _action_status;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _add_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _add_keys;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _aggregate_log_group_summary;

+#[cfg(feature = "op_list_anomalies")]
 mod _anomaly;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 mod _anomaly_detector;

+#[cfg(any(feature = "op_get_log_anomaly_detector", feature = "op_list_log_anomaly_detectors"))]
 mod _anomaly_detector_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _configuration_template;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _configuration_template_delivery_config_values;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _copy_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _copy_value_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _csv;

+#[cfg(feature = "op_describe_log_groups")]
 mod _data_protection_status;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 mod _data_source;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 mod _data_source_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _date_time_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _delete_keys;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 mod _delivery;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination_configuration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination_type;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _delivery_source_configuration_schema;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _delivery_source_configuration_schema_value_type;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source_status;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source_status_reason;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 mod _destination;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _destination_configuration;

+#[cfg(any(feature = "op_describe_subscription_filters", feature = "op_put_subscription_filter"))]
 mod _distribution;

+#[cfg(feature = "op_put_log_events")]
 mod _entity;

+#[cfg(feature = "op_put_log_events")]
 mod _entity_rejection_error_type;

+#[cfg(any(
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_update_log_anomaly_detector"
+))]
 mod _evaluation_frequency;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _event_source;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _execution_status;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_execution_info;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_status;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_status_code;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _field_index;

+#[cfg(feature = "op_get_log_object")]
 mod _fields_data;

+#[cfg(feature = "op_filter_log_events")]
 mod _filtered_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _flattened_element;

+#[cfg(feature = "op_get_log_object")]
 mod _get_log_object_response_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _grok;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _grouping_identifier;

+#[cfg(feature = "op_describe_import_tasks")]
 mod _import;

+#[cfg(feature = "op_describe_import_task_batches")]
 mod _import_batch;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 mod _import_filter;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 mod _import_statistics;

+#[cfg(any(
+    feature = "op_cancel_import_task",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks"
+))]
 mod _import_status;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _index_category;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 mod _index_policy;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 mod _index_source;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _index_type;

+#[cfg(feature = "op_describe_log_groups")]
 mod _inherited_property;

+#[cfg(feature = "op_put_log_events")]
 mod _input_log_event;

+#[cfg(feature = "op_get_integration")]
 mod _integration_details;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 mod _integration_status;

+#[cfg(feature = "op_list_integrations")]
 mod _integration_summary;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 mod _integration_type;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _list_aggregate_log_group_summaries_group_by;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _list_to_map;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_log_event;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_metadata;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_start;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_update;

+#[cfg(feature = "op_list_anomalies")]
 mod _log_event;

+#[cfg(feature = "op_get_log_fields")]
 mod _log_field_type;

+#[cfg(feature = "op_get_log_fields")]
 mod _log_fields_list_item;

+#[cfg(feature = "op_describe_log_groups")]
 mod _log_group;

+#[cfg(any(
+    feature = "op_create_log_group",
+    feature = "op_describe_log_groups",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_log_groups"
+))]
 mod _log_group_class;

+#[cfg(feature = "op_get_log_group_fields")]
 mod _log_group_field;

+#[cfg(feature = "op_list_log_groups")]
 mod _log_group_summary;

+#[cfg(feature = "op_describe_log_streams")]
 mod _log_stream;

+#[cfg(feature = "op_describe_lookup_tables")]
 mod _lookup_table;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _lookup_table_configuration;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _lower_case_string;

+#[cfg(feature = "op_describe_metric_filters")]
 mod _metric_filter;

+#[cfg(feature = "op_test_metric_filter")]
 mod _metric_filter_match_record;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 mod _metric_transformation;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _move_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _move_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _ocsf_version;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_application;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_collection;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_data_access_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_data_source;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_encryption_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_integration_details;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_lifecycle_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_network_policy;

+#[cfg(feature = "op_put_integration")]
 mod _open_search_resource_config;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_resource_status;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_resource_status_type;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_workspace;

+#[cfg(feature = "op_describe_log_streams")]
 mod _order_by;

+#[cfg(any(
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _output_format;

+#[cfg(feature = "op_get_log_events")]
 mod _output_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_cloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_json;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_key_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_postgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_route53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_to_ocsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_vpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_waf;

+#[cfg(feature = "op_list_anomalies")]
 mod _pattern_token;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 mod _policy;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 mod _policy_scope;

+#[cfg(any(
+    feature = "op_delete_account_policy",
+    feature = "op_describe_account_policies",
+    feature = "op_put_account_policy"
+))]
 mod _policy_type;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _processor;

+#[cfg(feature = "op_start_query")]
 mod _query_compile_error;

+#[cfg(feature = "op_start_query")]
 mod _query_compile_error_location;

+#[cfg(feature = "op_describe_query_definitions")]
 mod _query_definition;

+#[cfg(feature = "op_describe_queries")]
 mod _query_info;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_put_query_definition",
+    feature = "op_start_query",
+    feature = "op_update_scheduled_query"
+))]
 mod _query_language;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 mod _query_parameter;

+#[cfg(feature = "op_get_query_results")]
 mod _query_statistics;

+#[cfg(any(feature = "op_describe_queries", feature = "op_get_query_results"))]
 mod _query_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _record_field;

+#[cfg(feature = "op_put_log_events")]
 mod _rejected_entity_info;

+#[cfg(feature = "op_put_log_events")]
 mod _rejected_log_events_info;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _rename_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _rename_keys;

+#[cfg(feature = "op_put_integration")]
 mod _resource_config;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 mod _resource_policy;

+#[cfg(feature = "op_get_query_results")]
 mod _result_field;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _s3_configuration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 mod _s3_delivery_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod _s3_table_integration_source;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod _s3_table_integration_source_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _s3_tables_integration;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _schedule_type;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _scheduled_query_destination;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _scheduled_query_destination_type;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _scheduled_query_state;

+#[cfg(feature = "op_list_scheduled_queries")]
 mod _scheduled_query_summary;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 mod _scope;

+#[cfg(feature = "op_filter_log_events")]
 mod _searched_log_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _split_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _split_string_entry;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 mod _standard_unit;

+#[cfg(feature = "op_start_live_tail")]
 mod _start_live_tail_response_stream;

+#[cfg(feature = "op_list_anomalies")]
 mod _state;

+#[cfg(any(feature = "op_get_storage_tier_policy", feature = "op_put_storage_tier_policy"))]
 mod _storage_tier;

+#[cfg(feature = "op_describe_subscription_filters")]
 mod _subscription_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _substitute_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _substitute_string_entry;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_period;

+#[cfg(feature = "op_list_anomalies")]
 mod _suppression_state;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_type;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_unit;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod _syslog_configuration;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod _syslog_source_type;

+#[cfg(feature = "op_list_log_groups")]
 mod _tag_filter;

+#[cfg(feature = "op_test_transformer")]
 mod _transformed_log_record;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _trigger_history_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _trim_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_converter_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _upper_case_string;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,230 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub use crate::types::_data_source::DataSourceBuilder;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_statistics::ImportStatisticsBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub use crate::types::_s3_delivery_configuration::S3DeliveryConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub use crate::types::_delivery::DeliveryBuilder;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_filter::ImportFilterBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_destination_configuration::DestinationConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination::DeliveryDestinationBuilder;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub use crate::types::_policy::PolicyBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source::DeliverySourceBuilder;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_query_statistics::QueryStatisticsBuilder;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_account_policy::AccountPolicyBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_configuration::DeliveryDestinationConfigurationBuilder;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub use crate::types::_destination::DestinationBuilder;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_policy::IndexPolicyBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity::EntityBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_log_events_info::RejectedLogEventsInfoBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_entity_info::RejectedEntityInfoBuilder;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_resource_policy::ResourcePolicyBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error::QueryCompileErrorBuilder;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_period::SuppressionPeriodBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_s3_configuration::S3ConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_lookup_table_configuration::LookupTableConfigurationBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template::ConfigurationTemplateBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task::ExportTaskBuilder;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_field_index::FieldIndexBuilder;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub use crate::types::_import_batch::ImportBatchBuilder;

+#[cfg(feature = "op_describe_import_tasks")]
 pub use crate::types::_import::ImportBuilder;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_log_group::LogGroupBuilder;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_log_stream::LogStreamBuilder;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub use crate::types::_lookup_table::LookupTableBuilder;

+#[cfg(feature = "op_describe_metric_filters")]
 pub use crate::types::_metric_filter::MetricFilterBuilder;

+#[cfg(feature = "op_describe_queries")]
 pub use crate::types::_query_info::QueryInfoBuilder;

+#[cfg(feature = "op_describe_query_definitions")]
 pub use crate::types::_query_definition::QueryDefinitionBuilder;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub use crate::types::_subscription_filter::SubscriptionFilterBuilder;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_filtered_log_event::FilteredLogEventBuilder;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_searched_log_stream::SearchedLogStreamBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_integration_details::OpenSearchIntegrationDetailsBuilder;

+#[cfg(feature = "op_get_log_events")]
 pub use crate::types::_output_log_event::OutputLogEventBuilder;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_fields_list_item::LogFieldsListItemBuilder;

+#[cfg(feature = "op_get_log_group_fields")]
 pub use crate::types::_log_group_field::LogGroupFieldBuilder;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_fields_data::FieldsDataBuilder;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_trigger_history_record::TriggerHistoryRecordBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_processor::ProcessorBuilder;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub use crate::types::_data_source_filter::DataSourceFilterBuilder;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_aggregate_log_group_summary::AggregateLogGroupSummaryBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_anomaly::AnomalyBuilder;

+#[cfg(feature = "op_list_integrations")]
 pub use crate::types::_integration_summary::IntegrationSummaryBuilder;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub use crate::types::_anomaly_detector::AnomalyDetectorBuilder;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_tag_filter::TagFilterBuilder;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_log_group_summary::LogGroupSummaryBuilder;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub use crate::types::_scheduled_query_summary::ScheduledQuerySummaryBuilder;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source::S3TableIntegrationSourceBuilder;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_configuration::SyslogConfigurationBuilder;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_open_search_resource_config::OpenSearchResourceConfigBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_input_log_event::InputLogEventBuilder;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_metric_transformation::MetricTransformationBuilder;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub use crate::types::_query_parameter::QueryParameterBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_start::LiveTailSessionStartBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_update::LiveTailSessionUpdateBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error_location::QueryCompileErrorLocationBuilder;

+#[cfg(feature = "op_test_metric_filter")]
 pub use crate::types::_metric_filter_match_record::MetricFilterMatchRecordBuilder;

+#[cfg(feature = "op_test_transformer")]
 pub use crate::types::_transformed_log_record::TransformedLogRecordBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template_delivery_config_values::ConfigurationTemplateDeliveryConfigValuesBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_s3_tables_integration::S3TablesIntegrationBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status::ExportTaskStatusBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_execution_info::ExportTaskExecutionInfoBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_source::OpenSearchDataSourceBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_application::OpenSearchApplicationBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_collection::OpenSearchCollectionBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_workspace::OpenSearchWorkspaceBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_encryption_policy::OpenSearchEncryptionPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_network_policy::OpenSearchNetworkPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_access_policy::OpenSearchDataAccessPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_lifecycle_policy::OpenSearchLifecyclePolicyBuilder;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_field_type::LogFieldTypeBuilder;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_result_field::ResultFieldBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_keys::AddKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value::CopyValueBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_csv::CsvBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_date_time_converter::DateTimeConverterBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_delete_keys::DeleteKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_grok::GrokBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_list_to_map::ListToMapBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_lower_case_string::LowerCaseStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_keys::MoveKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_cloudfront::ParseCloudfrontBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_json::ParseJsonBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_key_value::ParseKeyValueBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_route53::ParseRoute53Builder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_to_ocsf::ParseToOcsfBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_postgres::ParsePostgresBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_vpc::ParseVpcBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_waf::ParseWafBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_keys::RenameKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string::SplitStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string::SubstituteStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_trim_string::TrimStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter::TypeConverterBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_upper_case_string::UpperCaseStringBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_metadata::LiveTailSessionMetadataBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_record_field::RecordFieldBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema::DeliverySourceConfigurationSchemaBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status::OpenSearchResourceStatusBuilder;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination::ScheduledQueryDestinationBuilder;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_grouping_identifier::GroupingIdentifierBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_log_event::LogEventBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_pattern_token::PatternTokenBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_log_event::LiveTailSessionLogEventBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_key_entry::AddKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value_entry::CopyValueEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_key_entry::MoveKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_key_entry::RenameKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string_entry::SplitStringEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string_entry::SubstituteStringEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter_entry::TypeConverterEntryBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,46 +1,584 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::error::_operation_aborted_exception::OperationAbortedException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::error::_invalid_operation_exception::InvalidOperationException;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededException;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub use crate::types::error::_resource_already_exists_exception::ResourceAlreadyExistsException;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::error::_internal_streaming_exception::InternalStreamingException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_data_already_accepted_exception::DataAlreadyAcceptedException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_invalid_sequence_token_exception::InvalidSequenceTokenException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_unrecognized_client_exception::UnrecognizedClientException;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_timeout_exception::SessionTimeoutException;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_streaming_exception::SessionStreamingException;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::error::_malformed_query_exception::MalformedQueryException;

+#[cfg(feature = "op_tag_resource")]
 pub use crate::types::error::_too_many_tags_exception::TooManyTagsException;

+#[cfg(feature = "op_get_log_object")]
 /// Error type for the `GetLogObjectResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -58,6 +596,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_get_log_object")]
 impl GetLogObjectResponseStreamError {
     /// Creates the `GetLogObjectResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -93,6 +632,7 @@
         matches!(self, Self::InternalStreamingException(_))
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::std::error::Error for GetLogObjectResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -101,6 +641,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::std::fmt::Display for GetLogObjectResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -117,6 +658,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for GetLogObjectResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -125,6 +667,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for GetLogObjectResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -135,6 +678,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for GetLogObjectResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -146,6 +690,7 @@
         })
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_types::request_id::RequestId for crate::types::error::GetLogObjectResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -152,6 +697,7 @@
     }
 }

+#[cfg(feature = "op_start_live_tail")]
 /// Error type for the `StartLiveTailResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -171,6 +717,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_start_live_tail")]
 impl StartLiveTailResponseStreamError {
     /// Creates the `StartLiveTailResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -211,6 +758,7 @@
         matches!(self, Self::SessionStreamingException(_))
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::std::error::Error for StartLiveTailResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -220,6 +768,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::std::fmt::Display for StartLiveTailResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -237,6 +786,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for StartLiveTailResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -245,6 +795,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for StartLiveTailResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -258,6 +809,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for StartLiveTailResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -269,6 +821,7 @@
         })
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_types::request_id::RequestId for crate::types::error::StartLiveTailResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -275,46 +828,583 @@
     }
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _access_denied_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 mod _conflict_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _data_already_accepted_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 mod _internal_server_exception;

+#[cfg(feature = "op_get_log_object")]
 mod _internal_streaming_exception;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 mod _invalid_operation_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 mod _invalid_parameter_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _invalid_sequence_token_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 mod _limit_exceeded_exception;

+#[cfg(feature = "op_start_query")]
 mod _malformed_query_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 mod _operation_aborted_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 mod _resource_already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 mod _service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 mod _service_unavailable_exception;

+#[cfg(feature = "op_start_live_tail")]
 mod _session_streaming_exception;

+#[cfg(feature = "op_start_live_tail")]
 mod _session_timeout_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 mod _throttling_exception;

+#[cfg(feature = "op_tag_resource")]
 mod _too_many_tags_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _unrecognized_client_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _validation_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,42 +1,579 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::error::_operation_aborted_exception::OperationAbortedExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::error::_invalid_operation_exception::InvalidOperationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub use crate::types::error::_resource_already_exists_exception::ResourceAlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::error::_internal_streaming_exception::InternalStreamingExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_data_already_accepted_exception::DataAlreadyAcceptedExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_invalid_sequence_token_exception::InvalidSequenceTokenExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_unrecognized_client_exception::UnrecognizedClientExceptionBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_timeout_exception::SessionTimeoutExceptionBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_streaming_exception::SessionStreamingExceptionBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::error::_malformed_query_exception::MalformedQueryExceptionBuilder;

+#[cfg(feature = "op_tag_resource")]
 pub use crate::types::error::_too_many_tags_exception::TooManyTagsExceptionBuilder;
```

## Unified diff

```diff
diff --git a/Cargo.toml b/Cargo.toml
--- a/Cargo.toml
+++ b/Cargo.toml
@@ -19,56 +19,44 @@
 version = "1"

 [dependencies.aws-credential-types]
-path = "../aws-credential-types"
 version = "1.3.0"

 [dependencies.aws-runtime]
-path = "../aws-runtime"
 features = ["event-stream"]
 version = "1.9.2"

 [dependencies.aws-smithy-async]
-path = "../aws-smithy-async"
 version = "1.3.0"

 [dependencies.aws-smithy-eventstream]
-path = "../aws-smithy-eventstream"
 version = "0.61.2"

 [dependencies.aws-smithy-http]
-path = "../aws-smithy-http"
 features = ["event-stream"]
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
@@ -90,50 +78,40 @@
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

 [dev-dependencies.aws-smithy-eventstream]
-path = "../aws-smithy-eventstream"
 features = ["test-util"]
 version = "0.61.2"

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

@@ -164,3 +142,121 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["rustls", "default-https-client", "rt-tokio"]
+op_associate_kms_key = []
+op_associate_source_to_s3_table_integration = []
+op_cancel_export_task = []
+op_cancel_import_task = []
+op_create_delivery = []
+op_create_export_task = []
+op_create_import_task = []
+op_create_log_anomaly_detector = []
+op_create_log_group = []
+op_create_log_stream = []
+op_create_lookup_table = []
+op_create_scheduled_query = []
+op_delete_account_policy = []
+op_delete_data_protection_policy = []
+op_delete_delivery = []
+op_delete_delivery_destination = []
+op_delete_delivery_destination_policy = []
+op_delete_delivery_source = []
+op_delete_destination = []
+op_delete_index_policy = []
+op_delete_integration = []
+op_delete_log_anomaly_detector = []
+op_delete_log_group = []
+op_delete_log_stream = []
+op_delete_lookup_table = []
+op_delete_metric_filter = []
+op_delete_query_definition = []
+op_delete_resource_policy = []
+op_delete_retention_policy = []
+op_delete_scheduled_query = []
+op_delete_subscription_filter = []
+op_delete_syslog_configuration = []
+op_delete_transformer = []
+op_describe_account_policies = []
+op_describe_configuration_templates = []
+op_describe_deliveries = []
+op_describe_delivery_destinations = []
+op_describe_delivery_sources = []
+op_describe_destinations = []
+op_describe_export_tasks = []
+op_describe_field_indexes = []
+op_describe_import_task_batches = []
+op_describe_import_tasks = []
+op_describe_index_policies = []
+op_describe_log_groups = []
+op_describe_log_streams = []
+op_describe_lookup_tables = []
+op_describe_metric_filters = []
+op_describe_queries = []
+op_describe_query_definitions = []
+op_describe_resource_policies = []
+op_describe_subscription_filters = []
+op_disassociate_kms_key = []
+op_disassociate_source_from_s3_table_integration = []
+op_filter_log_events = []
+op_get_data_protection_policy = []
+op_get_delivery = []
+op_get_delivery_destination = []
+op_get_delivery_destination_policy = []
+op_get_delivery_source = []
+op_get_integration = []
+op_get_log_anomaly_detector = []
+op_get_log_events = []
+op_get_log_fields = []
+op_get_log_group_fields = []
+op_get_log_object = []
+op_get_log_record = []
+op_get_lookup_table = []
+op_get_query_results = []
+op_get_scheduled_query = []
+op_get_scheduled_query_history = []
+op_get_storage_tier_policy = []
+op_get_transformer = []
+op_list_aggregate_log_group_summaries = []
+op_list_anomalies = []
+op_list_integrations = []
+op_list_log_anomaly_detectors = []
+op_list_log_groups = []
+op_list_log_groups_for_query = []
+op_list_scheduled_queries = []
+op_list_sources_for_s3_table_integration = []
+op_list_syslog_configurations = []
+op_list_tags_for_resource = []
+op_list_tags_log_group = []
+op_put_account_policy = []
+op_put_bearer_token_authentication = []
+op_put_data_protection_policy = []
+op_put_delivery_destination = []
+op_put_delivery_destination_policy = []
+op_put_delivery_source = []
+op_put_destination = []
+op_put_destination_policy = []
+op_put_index_policy = []
+op_put_integration = []
+op_put_log_events = []
+op_put_log_group_deletion_protection = []
+op_put_metric_filter = []
+op_put_query_definition = []
+op_put_resource_policy = []
+op_put_retention_policy = []
+op_put_storage_tier_policy = []
+op_put_subscription_filter = []
+op_put_syslog_configuration = []
+op_put_transformer = []
+op_start_live_tail = []
+op_start_query = []
+op_stop_query = []
+op_tag_log_group = []
+op_tag_resource = []
+op_test_metric_filter = []
+op_test_transformer = []
+op_untag_log_group = []
+op_untag_resource = []
+op_update_anomaly = []
+op_update_delivery_configuration = []
+op_update_log_anomaly_detector = []
+op_update_lookup_table = []
+op_update_scheduled_query = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,28 +136,40 @@
     }
 }

+#[cfg(feature = "op_associate_kms_key")]
 mod associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 mod associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 mod cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 mod cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 mod create_delivery;

+#[cfg(feature = "op_create_export_task")]
 mod create_export_task;

+#[cfg(feature = "op_create_import_task")]
 mod create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 mod create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 mod create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 mod create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 mod create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 mod create_scheduled_query;

 /// Operation customization and supporting types.
@@ -187,214 +199,320 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_account_policy")]
 mod delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 mod delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 mod delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 mod delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 mod delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 mod delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 mod delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 mod delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 mod delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 mod delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 mod delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 mod delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 mod delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 mod delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 mod delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 mod delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 mod delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 mod delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 mod delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 mod delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 mod delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 mod describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 mod describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 mod describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 mod describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 mod describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 mod describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 mod describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 mod describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 mod describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 mod describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 mod describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 mod describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 mod describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 mod describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 mod describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 mod describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 mod describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 mod describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 mod disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 mod disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 mod filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 mod get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 mod get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 mod get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 mod get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 mod get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 mod get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 mod get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 mod get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 mod get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 mod get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 mod get_log_object;

+#[cfg(feature = "op_get_log_record")]
 mod get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 mod get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 mod get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 mod get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 mod get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 mod get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 mod list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 mod list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 mod list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 mod list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 mod list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 mod list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 mod list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 mod put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 mod put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 mod put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 mod put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 mod put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 mod put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 mod put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 mod put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 mod put_index_policy;

+#[cfg(feature = "op_put_integration")]
 mod put_integration;

+#[cfg(feature = "op_put_log_events")]
 mod put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 mod put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 mod put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 mod put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 mod put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 mod put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 mod put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 mod put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 mod put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 mod put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 mod start_live_tail;

+#[cfg(feature = "op_start_query")]
 mod start_query;

+#[cfg(feature = "op_stop_query")]
 mod stop_query;

+#[cfg(feature = "op_tag_log_group")]
 mod tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 mod test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 mod test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 mod untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 mod update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 mod update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 mod update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 mod update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 mod update_scheduled_query;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,51 +3,588 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_lookup_table",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_lookup_tables",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_log_object",
+        feature = "op_get_lookup_table",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_syslog_configuration",
+        feature = "op_start_live_tail",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>You don't have sufficient permissions to perform this action.</p>
     AccessDeniedException(crate::types::error::AccessDeniedException),
+    #[cfg(any(
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>This operation attempted to create a resource that already exists.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The event was already logged.</p><important>
     /// <p><code>PutLogEvents</code> actions are now always accepted and never return <code>DataAlreadyAcceptedException</code> regardless of whether a given batch of log events has already been accepted.</p>
     /// </important>
     DataAlreadyAcceptedException(crate::types::error::DataAlreadyAcceptedException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_scheduled_query",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>An internal server error occurred while processing the request. This exception is returned when the service encounters an unexpected condition that prevents it from fulfilling the request.</p>
     InternalServerException(crate::types::error::InternalServerException),
+    #[cfg(feature = "op_get_log_object")]
     /// <p>An internal error occurred during the streaming of log data. This exception is thrown when there's an issue with the internal streaming mechanism used by the GetLogObject operation.</p>
     InternalStreamingException(crate::types::error::InternalStreamingException),
+    #[cfg(any(
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_import_task",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_get_log_object",
+        feature = "op_get_transformer",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_test_transformer"
+    ))]
     /// <p>The operation is not valid on the specified resource.</p>
     InvalidOperationException(crate::types::error::InvalidOperationException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_export_task",
+        feature = "op_create_import_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_destinations",
+        feature = "op_describe_export_tasks",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_groups",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_query_definitions",
+        feature = "op_describe_resource_policies",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_anomalies",
+        feature = "op_list_integrations",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_log_group",
+        feature = "op_tag_resource",
+        feature = "op_test_metric_filter",
+        feature = "op_test_transformer",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table"
+    ))]
     /// <p>A parameter is specified incorrectly.</p>
     InvalidParameterException(crate::types::error::InvalidParameterException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The sequence token is not valid. You can get the correct sequence token in the <code>expectedSequenceToken</code> field in the <code>InvalidSequenceTokenException</code> message.</p><important>
     /// <p><code>PutLogEvents</code> actions are now always accepted and never return <code>InvalidSequenceTokenException</code> regardless of receiving an invalid sequence token.</p>
     /// </important>
     InvalidSequenceTokenException(crate::types::error::InvalidSequenceTokenException),
+    #[cfg(any(
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_index_policy",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_put_account_policy",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query"
+    ))]
     /// <p>You have reached the maximum number of resources that can be created.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(feature = "op_start_query")]
     /// <p>The query string is not valid. Details about this error are displayed in a <code>QueryCompileError</code> object. For more information, see <a href="https://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_QueryCompileError.html">QueryCompileError</a>.</p>
     /// <p>For more information about valid query syntax, see <a href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html">CloudWatch Logs Insights Query Syntax</a>.</p>
     MalformedQueryException(crate::types::error::MalformedQueryException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_disassociate_kms_key",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_fields",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_list_anomalies",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_update_anomaly",
+        feature = "op_update_log_anomaly_detector"
+    ))]
     /// <p>Multiple concurrent requests to update the same resource were in conflict.</p>
     OperationAbortedException(crate::types::error::OperationAbortedException),
+    #[cfg(any(
+        feature = "op_create_export_task",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table"
+    ))]
     /// <p>The specified resource already exists.</p>
     ResourceAlreadyExistsException(crate::types::error::ResourceAlreadyExistsException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_export_task",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_export_task",
+        feature = "op_create_import_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_stream",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_object",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_anomalies",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tags_log_group",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_index_policy",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_live_tail",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_log_group",
+        feature = "op_tag_resource",
+        feature = "op_untag_log_group",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>The specified resource does not exist.</p>
     ResourceNotFoundException(crate::types::error::ResourceNotFoundException),
+    #[cfg(any(
+        feature = "op_create_delivery",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_source",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_source",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_source"
+    ))]
     /// <p>This request exceeds a service quota.</p>
     ServiceQuotaExceededException(crate::types::error::ServiceQuotaExceededException),
+    #[cfg(any(
+        feature = "op_associate_kms_key",
+        feature = "op_cancel_export_task",
+        feature = "op_create_delivery",
+        feature = "op_create_export_task",
+        feature = "op_create_log_anomaly_detector",
+        feature = "op_create_log_group",
+        feature = "op_create_log_stream",
+        feature = "op_create_lookup_table",
+        feature = "op_delete_account_policy",
+        feature = "op_delete_data_protection_policy",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_destination",
+        feature = "op_delete_index_policy",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_anomaly_detector",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_lookup_table",
+        feature = "op_delete_metric_filter",
+        feature = "op_delete_query_definition",
+        feature = "op_delete_resource_policy",
+        feature = "op_delete_retention_policy",
+        feature = "op_delete_subscription_filter",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_delete_transformer",
+        feature = "op_describe_account_policies",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_describe_destinations",
+        feature = "op_describe_export_tasks",
+        feature = "op_describe_field_indexes",
+        feature = "op_describe_index_policies",
+        feature = "op_describe_log_groups",
+        feature = "op_describe_log_streams",
+        feature = "op_describe_lookup_tables",
+        feature = "op_describe_metric_filters",
+        feature = "op_describe_queries",
+        feature = "op_describe_query_definitions",
+        feature = "op_describe_resource_policies",
+        feature = "op_describe_subscription_filters",
+        feature = "op_disassociate_kms_key",
+        feature = "op_filter_log_events",
+        feature = "op_get_data_protection_policy",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_integration",
+        feature = "op_get_log_anomaly_detector",
+        feature = "op_get_log_events",
+        feature = "op_get_log_fields",
+        feature = "op_get_log_group_fields",
+        feature = "op_get_log_record",
+        feature = "op_get_lookup_table",
+        feature = "op_get_query_results",
+        feature = "op_get_storage_tier_policy",
+        feature = "op_get_transformer",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_anomalies",
+        feature = "op_list_integrations",
+        feature = "op_list_log_anomaly_detectors",
+        feature = "op_list_log_groups",
+        feature = "op_list_log_groups_for_query",
+        feature = "op_list_syslog_configurations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tags_log_group",
+        feature = "op_put_account_policy",
+        feature = "op_put_bearer_token_authentication",
+        feature = "op_put_data_protection_policy",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_destination",
+        feature = "op_put_destination_policy",
+        feature = "op_put_index_policy",
+        feature = "op_put_integration",
+        feature = "op_put_log_events",
+        feature = "op_put_log_group_deletion_protection",
+        feature = "op_put_metric_filter",
+        feature = "op_put_query_definition",
+        feature = "op_put_resource_policy",
+        feature = "op_put_retention_policy",
+        feature = "op_put_storage_tier_policy",
+        feature = "op_put_subscription_filter",
+        feature = "op_put_syslog_configuration",
+        feature = "op_put_transformer",
+        feature = "op_start_query",
+        feature = "op_stop_query",
+        feature = "op_tag_resource",
+        feature = "op_test_metric_filter",
+        feature = "op_test_transformer",
+        feature = "op_untag_resource",
+        feature = "op_update_anomaly",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_log_anomaly_detector",
+        feature = "op_update_lookup_table"
+    ))]
     /// <p>The service cannot complete the request.</p>
     ServiceUnavailableException(crate::types::error::ServiceUnavailableException),
+    #[cfg(feature = "op_start_live_tail")]
     /// <p>This exception is returned if an unknown error occurs during a Live Tail session.</p>
     SessionStreamingException(crate::types::error::SessionStreamingException),
+    #[cfg(feature = "op_start_live_tail")]
     /// <p>This exception is returned in a Live Tail stream when the Live Tail session times out. Live Tail sessions time out after three hours.</p>
     SessionTimeoutException(crate::types::error::SessionTimeoutException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_cancel_import_task",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_scheduled_query",
+        feature = "op_delete_syslog_configuration",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_describe_import_task_batches",
+        feature = "op_describe_import_tasks",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_source",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_list_syslog_configurations",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_source",
+        feature = "op_put_syslog_configuration",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>The request was throttled because of quota limits.</p>
     ThrottlingException(crate::types::error::ThrottlingException),
+    #[cfg(feature = "op_tag_resource")]
     /// <p>A resource can have no more than 50 tags.</p>
     TooManyTagsException(crate::types::error::TooManyTagsException),
+    #[cfg(feature = "op_put_log_events")]
     /// <p>The most likely cause is an Amazon Web Services access key ID or secret key that's not valid.</p>
     UnrecognizedClientException(crate::types::error::UnrecognizedClientException),
+    #[cfg(any(
+        feature = "op_associate_source_to_s3_table_integration",
+        feature = "op_create_delivery",
+        feature = "op_create_import_task",
+        feature = "op_create_lookup_table",
+        feature = "op_create_scheduled_query",
+        feature = "op_delete_delivery",
+        feature = "op_delete_delivery_destination",
+        feature = "op_delete_delivery_destination_policy",
+        feature = "op_delete_delivery_source",
+        feature = "op_delete_integration",
+        feature = "op_delete_log_group",
+        feature = "op_delete_log_stream",
+        feature = "op_delete_scheduled_query",
+        feature = "op_describe_configuration_templates",
+        feature = "op_describe_deliveries",
+        feature = "op_describe_delivery_destinations",
+        feature = "op_describe_delivery_sources",
+        feature = "op_disassociate_source_from_s3_table_integration",
+        feature = "op_get_delivery",
+        feature = "op_get_delivery_destination",
+        feature = "op_get_delivery_destination_policy",
+        feature = "op_get_delivery_source",
+        feature = "op_get_scheduled_query",
+        feature = "op_get_scheduled_query_history",
+        feature = "op_list_aggregate_log_group_summaries",
+        feature = "op_list_scheduled_queries",
+        feature = "op_list_sources_for_s3_table_integration",
+        feature = "op_put_delivery_destination",
+        feature = "op_put_delivery_destination_policy",
+        feature = "op_put_delivery_source",
+        feature = "op_put_integration",
+        feature = "op_update_delivery_configuration",
+        feature = "op_update_lookup_table",
+        feature = "op_update_scheduled_query"
+    ))]
     /// <p>One of the parameters for the request is not valid.</p>
     ValidationException(crate::types::error::ValidationException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -64,26 +601,563 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::AccessDeniedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::DataAlreadyAcceptedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::InternalServerException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_get_log_object")]
             Error::InternalStreamingException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Error::InvalidOperationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::InvalidParameterException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::InvalidSequenceTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_query")]
             Error::MalformedQueryException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Error::OperationAbortedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Error::ResourceAlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionStreamingException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionTimeoutException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ThrottlingException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_tag_resource")]
             Error::TooManyTagsException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_put_log_events")]
             Error::UnrecognizedClientException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ValidationException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -108,31 +1182,569 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::AccessDeniedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::DataAlreadyAcceptedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::InternalServerException(inner) => inner.meta(),
+            #[cfg(feature = "op_get_log_object")]
             Self::InternalStreamingException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Self::InvalidOperationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::InvalidParameterException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::InvalidSequenceTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_query")]
             Self::MalformedQueryException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Self::OperationAbortedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Self::ResourceAlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ResourceNotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Self::ServiceQuotaExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::ServiceUnavailableException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionStreamingException(inner) => inner.meta(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionTimeoutException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ThrottlingException(inner) => inner.meta(),
+            #[cfg(feature = "op_tag_resource")]
             Self::TooManyTagsException(inner) => inner.meta(),
+            #[cfg(feature = "op_put_log_events")]
             Self::UnrecognizedClientException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ValidationException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_associate_kms_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -158,6 +1770,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_kms_key")]
 impl From<crate::operation::associate_kms_key::AssociateKmsKeyError> for Error {
     fn from(err: crate::operation::associate_kms_key::AssociateKmsKeyError) -> Self {
         match err {
@@ -177,6 +1790,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -202,6 +1816,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 impl From<crate::operation::associate_source_to_s3_table_integration::AssociateSourceToS3TableIntegrationError>
     for Error
 {
@@ -230,6 +1845,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -255,6 +1871,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_task")]
 impl From<crate::operation::cancel_export_task::CancelExportTaskError> for Error {
     fn from(err: crate::operation::cancel_export_task::CancelExportTaskError) -> Self {
         match err {
@@ -274,6 +1891,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_import_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -299,6 +1917,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_import_task")]
 impl From<crate::operation::cancel_import_task::CancelImportTaskError> for Error {
     fn from(err: crate::operation::cancel_import_task::CancelImportTaskError) -> Self {
         match err {
@@ -321,6 +1940,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_delivery")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_delivery::CreateDeliveryError, R>>
     for Error
@@ -342,6 +1962,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_delivery")]
 impl From<crate::operation::create_delivery::CreateDeliveryError> for Error {
     fn from(err: crate::operation::create_delivery::CreateDeliveryError) -> Self {
         match err {
@@ -370,6 +1991,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -395,6 +2017,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_task")]
 impl From<crate::operation::create_export_task::CreateExportTaskError> for Error {
     fn from(err: crate::operation::create_export_task::CreateExportTaskError) -> Self {
         match err {
@@ -420,6 +2043,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_task")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -445,6 +2069,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_task")]
 impl From<crate::operation::create_import_task::CreateImportTaskError> for Error {
     fn from(err: crate::operation::create_import_task::CreateImportTaskError) -> Self {
         match err {
@@ -473,6 +2098,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -498,6 +2124,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_anomaly_detector")]
 impl From<crate::operation::create_log_anomaly_detector::CreateLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::create_log_anomaly_detector::CreateLogAnomalyDetectorError) -> Self {
         match err {
@@ -520,6 +2147,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_log_group::CreateLogGroupError, R>>
     for Error
@@ -541,6 +2169,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_group")]
 impl From<crate::operation::create_log_group::CreateLogGroupError> for Error {
     fn from(err: crate::operation::create_log_group::CreateLogGroupError) -> Self {
         match err {
@@ -563,6 +2192,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -588,6 +2218,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_log_stream")]
 impl From<crate::operation::create_log_stream::CreateLogStreamError> for Error {
     fn from(err: crate::operation::create_log_stream::CreateLogStreamError) -> Self {
         match err {
@@ -607,6 +2238,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -632,6 +2264,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_lookup_table")]
 impl From<crate::operation::create_lookup_table::CreateLookupTableError> for Error {
     fn from(err: crate::operation::create_lookup_table::CreateLookupTableError) -> Self {
         match err {
@@ -657,6 +2290,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -682,6 +2316,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_scheduled_query")]
 impl From<crate::operation::create_scheduled_query::CreateScheduledQueryError> for Error {
     fn from(err: crate::operation::create_scheduled_query::CreateScheduledQueryError) -> Self {
         match err {
@@ -712,6 +2347,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_account_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -737,6 +2373,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_account_policy")]
 impl From<crate::operation::delete_account_policy::DeleteAccountPolicyError> for Error {
     fn from(err: crate::operation::delete_account_policy::DeleteAccountPolicyError) -> Self {
         match err {
@@ -758,6 +2395,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -783,6 +2421,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_data_protection_policy")]
 impl From<crate::operation::delete_data_protection_policy::DeleteDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::delete_data_protection_policy::DeleteDataProtectionPolicyError) -> Self {
         match err {
@@ -802,6 +2441,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_delivery::DeleteDeliveryError, R>>
     for Error
@@ -823,6 +2463,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery")]
 impl From<crate::operation::delete_delivery::DeleteDeliveryError> for Error {
     fn from(err: crate::operation::delete_delivery::DeleteDeliveryError) -> Self {
         match err {
@@ -848,6 +2489,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -873,6 +2515,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination")]
 impl From<crate::operation::delete_delivery_destination::DeleteDeliveryDestinationError> for Error {
     fn from(err: crate::operation::delete_delivery_destination::DeleteDeliveryDestinationError) -> Self {
         match err {
@@ -898,6 +2541,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -923,6 +2567,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_destination_policy")]
 impl From<crate::operation::delete_delivery_destination_policy::DeleteDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::delete_delivery_destination_policy::DeleteDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -942,6 +2587,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -967,6 +2613,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_delivery_source")]
 impl From<crate::operation::delete_delivery_source::DeleteDeliverySourceError> for Error {
     fn from(err: crate::operation::delete_delivery_source::DeleteDeliverySourceError) -> Self {
         match err {
@@ -994,6 +2641,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1019,6 +2667,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_destination")]
 impl From<crate::operation::delete_destination::DeleteDestinationError> for Error {
     fn from(err: crate::operation::delete_destination::DeleteDestinationError) -> Self {
         match err {
@@ -1038,6 +2687,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_index_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1063,6 +2713,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_index_policy")]
 impl From<crate::operation::delete_index_policy::DeleteIndexPolicyError> for Error {
     fn from(err: crate::operation::delete_index_policy::DeleteIndexPolicyError) -> Self {
         match err {
@@ -1085,6 +2736,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1110,6 +2762,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_integration")]
 impl From<crate::operation::delete_integration::DeleteIntegrationError> for Error {
     fn from(err: crate::operation::delete_integration::DeleteIntegrationError) -> Self {
         match err {
@@ -1129,6 +2782,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1154,6 +2808,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_anomaly_detector")]
 impl From<crate::operation::delete_log_anomaly_detector::DeleteLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::delete_log_anomaly_detector::DeleteLogAnomalyDetectorError) -> Self {
         match err {
@@ -1173,6 +2828,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_log_group::DeleteLogGroupError, R>>
     for Error
@@ -1194,6 +2850,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_group")]
 impl From<crate::operation::delete_log_group::DeleteLogGroupError> for Error {
     fn from(err: crate::operation::delete_log_group::DeleteLogGroupError) -> Self {
         match err {
@@ -1216,6 +2873,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_stream")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1241,6 +2899,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_log_stream")]
 impl From<crate::operation::delete_log_stream::DeleteLogStreamError> for Error {
     fn from(err: crate::operation::delete_log_stream::DeleteLogStreamError) -> Self {
         match err {
@@ -1263,6 +2922,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1288,6 +2948,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_lookup_table")]
 impl From<crate::operation::delete_lookup_table::DeleteLookupTableError> for Error {
     fn from(err: crate::operation::delete_lookup_table::DeleteLookupTableError) -> Self {
         match err {
@@ -1307,6 +2968,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1332,6 +2994,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_metric_filter")]
 impl From<crate::operation::delete_metric_filter::DeleteMetricFilterError> for Error {
     fn from(err: crate::operation::delete_metric_filter::DeleteMetricFilterError) -> Self {
         match err {
@@ -1353,6 +3016,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_query_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1378,6 +3042,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_query_definition")]
 impl From<crate::operation::delete_query_definition::DeleteQueryDefinitionError> for Error {
     fn from(err: crate::operation::delete_query_definition::DeleteQueryDefinitionError) -> Self {
         match err {
@@ -1396,6 +3061,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1421,6 +3087,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_resource_policy")]
 impl From<crate::operation::delete_resource_policy::DeleteResourcePolicyError> for Error {
     fn from(err: crate::operation::delete_resource_policy::DeleteResourcePolicyError) -> Self {
         match err {
@@ -1442,6 +3109,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_retention_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1467,6 +3135,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_retention_policy")]
 impl From<crate::operation::delete_retention_policy::DeleteRetentionPolicyError> for Error {
     fn from(err: crate::operation::delete_retention_policy::DeleteRetentionPolicyError) -> Self {
         match err {
@@ -1488,6 +3157,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1513,6 +3183,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_scheduled_query")]
 impl From<crate::operation::delete_scheduled_query::DeleteScheduledQueryError> for Error {
     fn from(err: crate::operation::delete_scheduled_query::DeleteScheduledQueryError) -> Self {
         match err {
@@ -1537,6 +3208,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_subscription_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1562,6 +3234,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_subscription_filter")]
 impl From<crate::operation::delete_subscription_filter::DeleteSubscriptionFilterError> for Error {
     fn from(err: crate::operation::delete_subscription_filter::DeleteSubscriptionFilterError) -> Self {
         match err {
@@ -1581,6 +3254,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_syslog_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1606,6 +3280,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_syslog_configuration")]
 impl From<crate::operation::delete_syslog_configuration::DeleteSyslogConfigurationError> for Error {
     fn from(err: crate::operation::delete_syslog_configuration::DeleteSyslogConfigurationError) -> Self {
         match err {
@@ -1634,6 +3309,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_transformer")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1659,6 +3335,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_transformer")]
 impl From<crate::operation::delete_transformer::DeleteTransformerError> for Error {
     fn from(err: crate::operation::delete_transformer::DeleteTransformerError) -> Self {
         match err {
@@ -1681,6 +3358,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_account_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1706,6 +3384,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_account_policies")]
 impl From<crate::operation::describe_account_policies::DescribeAccountPoliciesError> for Error {
     fn from(err: crate::operation::describe_account_policies::DescribeAccountPoliciesError) -> Self {
         match err {
@@ -1727,6 +3406,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_configuration_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1752,6 +3432,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_configuration_templates")]
 impl From<crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesError> for Error {
     fn from(err: crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesError) -> Self {
         match err {
@@ -1771,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_deliveries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1796,6 +3478,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_deliveries")]
 impl From<crate::operation::describe_deliveries::DescribeDeliveriesError> for Error {
     fn from(err: crate::operation::describe_deliveries::DescribeDeliveriesError) -> Self {
         match err {
@@ -1815,6 +3498,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1840,6 +3524,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_destinations")]
 impl From<crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsError> for Error {
     fn from(err: crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsError) -> Self {
         match err {
@@ -1859,6 +3544,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_sources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1884,6 +3570,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_delivery_sources")]
 impl From<crate::operation::describe_delivery_sources::DescribeDeliverySourcesError> for Error {
     fn from(err: crate::operation::describe_delivery_sources::DescribeDeliverySourcesError) -> Self {
         match err {
@@ -1903,6 +3590,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1928,6 +3616,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_destinations")]
 impl From<crate::operation::describe_destinations::DescribeDestinationsError> for Error {
     fn from(err: crate::operation::describe_destinations::DescribeDestinationsError) -> Self {
         match err {
@@ -1943,6 +3632,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1968,6 +3658,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_export_tasks")]
 impl From<crate::operation::describe_export_tasks::DescribeExportTasksError> for Error {
     fn from(err: crate::operation::describe_export_tasks::DescribeExportTasksError) -> Self {
         match err {
@@ -1983,6 +3674,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_field_indexes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2008,6 +3700,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_field_indexes")]
 impl From<crate::operation::describe_field_indexes::DescribeFieldIndexesError> for Error {
     fn from(err: crate::operation::describe_field_indexes::DescribeFieldIndexesError) -> Self {
         match err {
@@ -2032,6 +3725,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_task_batches")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2057,6 +3751,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_task_batches")]
 impl From<crate::operation::describe_import_task_batches::DescribeImportTaskBatchesError> for Error {
     fn from(err: crate::operation::describe_import_task_batches::DescribeImportTaskBatchesError) -> Self {
         match err {
@@ -2079,6 +3774,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_tasks")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2104,6 +3800,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_import_tasks")]
 impl From<crate::operation::describe_import_tasks::DescribeImportTasksError> for Error {
     fn from(err: crate::operation::describe_import_tasks::DescribeImportTasksError) -> Self {
         match err {
@@ -2128,6 +3825,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_index_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2153,6 +3851,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_index_policies")]
 impl From<crate::operation::describe_index_policies::DescribeIndexPoliciesError> for Error {
     fn from(err: crate::operation::describe_index_policies::DescribeIndexPoliciesError) -> Self {
         match err {
@@ -2177,6 +3876,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_groups")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2202,6 +3902,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_groups")]
 impl From<crate::operation::describe_log_groups::DescribeLogGroupsError> for Error {
     fn from(err: crate::operation::describe_log_groups::DescribeLogGroupsError) -> Self {
         match err {
@@ -2215,6 +3916,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_streams")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2240,6 +3942,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_log_streams")]
 impl From<crate::operation::describe_log_streams::DescribeLogStreamsError> for Error {
     fn from(err: crate::operation::describe_log_streams::DescribeLogStreamsError) -> Self {
         match err {
@@ -2258,6 +3961,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_lookup_tables")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2283,6 +3987,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_lookup_tables")]
 impl From<crate::operation::describe_lookup_tables::DescribeLookupTablesError> for Error {
     fn from(err: crate::operation::describe_lookup_tables::DescribeLookupTablesError) -> Self {
         match err {
@@ -2304,6 +4009,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_metric_filters")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2329,6 +4035,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_metric_filters")]
 impl From<crate::operation::describe_metric_filters::DescribeMetricFiltersError> for Error {
     fn from(err: crate::operation::describe_metric_filters::DescribeMetricFiltersError) -> Self {
         match err {
@@ -2347,6 +4054,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_queries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<crate::operation::describe_queries::DescribeQueriesError, R>,
@@ -2369,6 +4077,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_queries")]
 impl From<crate::operation::describe_queries::DescribeQueriesError> for Error {
     fn from(err: crate::operation::describe_queries::DescribeQueriesError) -> Self {
         match err {
@@ -2385,6 +4094,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_query_definitions")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2410,6 +4120,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_query_definitions")]
 impl From<crate::operation::describe_query_definitions::DescribeQueryDefinitionsError> for Error {
     fn from(err: crate::operation::describe_query_definitions::DescribeQueryDefinitionsError) -> Self {
         match err {
@@ -2423,6 +4134,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_resource_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2448,6 +4160,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_resource_policies")]
 impl From<crate::operation::describe_resource_policies::DescribeResourcePoliciesError> for Error {
     fn from(err: crate::operation::describe_resource_policies::DescribeResourcePoliciesError) -> Self {
         match err {
@@ -2461,6 +4174,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_subscription_filters")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2486,6 +4200,7 @@
         }
     }
 }
+#[cfg(feature = "op_describe_subscription_filters")]
 impl From<crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersError> for Error {
     fn from(err: crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersError) -> Self {
         match err {
@@ -2502,6 +4217,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_kms_key")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2527,6 +4243,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_kms_key")]
 impl From<crate::operation::disassociate_kms_key::DisassociateKmsKeyError> for Error {
     fn from(err: crate::operation::disassociate_kms_key::DisassociateKmsKeyError) -> Self {
         match err {
@@ -2548,6 +4265,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2573,6 +4291,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 impl
     From<crate::operation::disassociate_source_from_s3_table_integration::DisassociateSourceFromS3TableIntegrationError>
     for Error
@@ -2590,6 +4309,7 @@
         }
     }
 }
+#[cfg(feature = "op_filter_log_events")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2615,6 +4335,7 @@
         }
     }
 }
+#[cfg(feature = "op_filter_log_events")]
 impl From<crate::operation::filter_log_events::FilterLogEventsError> for Error {
     fn from(err: crate::operation::filter_log_events::FilterLogEventsError) -> Self {
         match err {
@@ -2631,6 +4352,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2656,6 +4378,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_data_protection_policy")]
 impl From<crate::operation::get_data_protection_policy::GetDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::get_data_protection_policy::GetDataProtectionPolicyError) -> Self {
         match err {
@@ -2677,6 +4400,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_delivery::GetDeliveryError, R>>
     for Error
 where
@@ -2694,6 +4418,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery")]
 impl From<crate::operation::get_delivery::GetDeliveryError> for Error {
     fn from(err: crate::operation::get_delivery::GetDeliveryError) -> Self {
         match err {
@@ -2716,6 +4441,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2741,6 +4467,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination")]
 impl From<crate::operation::get_delivery_destination::GetDeliveryDestinationError> for Error {
     fn from(err: crate::operation::get_delivery_destination::GetDeliveryDestinationError) -> Self {
         match err {
@@ -2765,6 +4492,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2790,6 +4518,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_destination_policy")]
 impl From<crate::operation::get_delivery_destination_policy::GetDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::get_delivery_destination_policy::GetDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -2806,6 +4535,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2831,6 +4561,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_delivery_source")]
 impl From<crate::operation::get_delivery_source::GetDeliverySourceError> for Error {
     fn from(err: crate::operation::get_delivery_source::GetDeliverySourceError) -> Self {
         match err {
@@ -2853,6 +4584,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_integration")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_integration::GetIntegrationError, R>>
     for Error
@@ -2874,6 +4606,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_integration")]
 impl From<crate::operation::get_integration::GetIntegrationError> for Error {
     fn from(err: crate::operation::get_integration::GetIntegrationError) -> Self {
         match err {
@@ -2890,6 +4623,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2915,6 +4649,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_anomaly_detector")]
 impl From<crate::operation::get_log_anomaly_detector::GetLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::get_log_anomaly_detector::GetLogAnomalyDetectorError) -> Self {
         match err {
@@ -2936,6 +4671,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_events")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_events::GetLogEventsError, R>>
     for Error
 where
@@ -2953,6 +4689,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_events")]
 impl From<crate::operation::get_log_events::GetLogEventsError> for Error {
     fn from(err: crate::operation::get_log_events::GetLogEventsError) -> Self {
         match err {
@@ -2969,6 +4706,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_fields")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_fields::GetLogFieldsError, R>>
     for Error
 where
@@ -2986,6 +4724,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_fields")]
 impl From<crate::operation::get_log_fields::GetLogFieldsError> for Error {
     fn from(err: crate::operation::get_log_fields::GetLogFieldsError) -> Self {
         match err {
@@ -3005,6 +4744,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_group_fields")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3030,6 +4770,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_group_fields")]
 impl From<crate::operation::get_log_group_fields::GetLogGroupFieldsError> for Error {
     fn from(err: crate::operation::get_log_group_fields::GetLogGroupFieldsError) -> Self {
         match err {
@@ -3049,6 +4790,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_object::GetLogObjectError, R>>
     for Error
 where
@@ -3066,6 +4808,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl From<crate::operation::get_log_object::GetLogObjectError> for Error {
     fn from(err: crate::operation::get_log_object::GetLogObjectError) -> Self {
         match err {
@@ -3091,6 +4834,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_record")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_log_record::GetLogRecordError, R>>
     for Error
 where
@@ -3108,6 +4852,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_record")]
 impl From<crate::operation::get_log_record::GetLogRecordError> for Error {
     fn from(err: crate::operation::get_log_record::GetLogRecordError) -> Self {
         match err {
@@ -3127,6 +4872,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_lookup_table")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_lookup_table::GetLookupTableError, R>>
     for Error
@@ -3148,6 +4894,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_lookup_table")]
 impl From<crate::operation::get_lookup_table::GetLookupTableError> for Error {
     fn from(err: crate::operation::get_lookup_table::GetLookupTableError) -> Self {
         match err {
@@ -3167,6 +4914,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_query_results")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3192,6 +4940,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_query_results")]
 impl From<crate::operation::get_query_results::GetQueryResultsError> for Error {
     fn from(err: crate::operation::get_query_results::GetQueryResultsError) -> Self {
         match err {
@@ -3208,6 +4957,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3233,6 +4983,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query")]
 impl From<crate::operation::get_scheduled_query::GetScheduledQueryError> for Error {
     fn from(err: crate::operation::get_scheduled_query::GetScheduledQueryError) -> Self {
         match err {
@@ -3255,6 +5006,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query_history")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3280,6 +5032,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_scheduled_query_history")]
 impl From<crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryError> for Error {
     fn from(err: crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryError) -> Self {
         match err {
@@ -3304,6 +5057,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_storage_tier_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3329,6 +5083,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_storage_tier_policy")]
 impl From<crate::operation::get_storage_tier_policy::GetStorageTierPolicyError> for Error {
     fn from(err: crate::operation::get_storage_tier_policy::GetStorageTierPolicyError) -> Self {
         match err {
@@ -3353,6 +5108,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_transformer")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_transformer::GetTransformerError, R>>
     for Error
@@ -3374,6 +5130,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_transformer")]
 impl From<crate::operation::get_transformer::GetTransformerError> for Error {
     fn from(err: crate::operation::get_transformer::GetTransformerError) -> Self {
         match err {
@@ -3393,6 +5150,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3418,6 +5176,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 impl From<crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesError> for Error {
     fn from(err: crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesError) -> Self {
         match err {
@@ -3434,6 +5193,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_anomalies")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_anomalies::ListAnomaliesError, R>>
     for Error
@@ -3455,6 +5215,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_anomalies")]
 impl From<crate::operation::list_anomalies::ListAnomaliesError> for Error {
     fn from(err: crate::operation::list_anomalies::ListAnomaliesError) -> Self {
         match err {
@@ -3474,6 +5235,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_integrations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3499,6 +5261,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_integrations")]
 impl From<crate::operation::list_integrations::ListIntegrationsError> for Error {
     fn from(err: crate::operation::list_integrations::ListIntegrationsError) -> Self {
         match err {
@@ -3512,6 +5275,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_anomaly_detectors")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3537,6 +5301,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_anomaly_detectors")]
 impl From<crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsError> for Error {
     fn from(err: crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsError) -> Self {
         match err {
@@ -3558,6 +5323,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_log_groups::ListLogGroupsError, R>>
     for Error
@@ -3579,6 +5345,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups")]
 impl From<crate::operation::list_log_groups::ListLogGroupsError> for Error {
     fn from(err: crate::operation::list_log_groups::ListLogGroupsError) -> Self {
         match err {
@@ -3592,6 +5359,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups_for_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3617,6 +5385,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_log_groups_for_query")]
 impl From<crate::operation::list_log_groups_for_query::ListLogGroupsForQueryError> for Error {
     fn from(err: crate::operation::list_log_groups_for_query::ListLogGroupsForQueryError) -> Self {
         match err {
@@ -3638,6 +5407,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduled_queries")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3663,6 +5433,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_scheduled_queries")]
 impl From<crate::operation::list_scheduled_queries::ListScheduledQueriesError> for Error {
     fn from(err: crate::operation::list_scheduled_queries::ListScheduledQueriesError) -> Self {
         match err {
@@ -3684,6 +5455,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3709,6 +5481,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 impl From<crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationError> for Error {
     fn from(
         err: crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationError,
@@ -3735,6 +5508,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_syslog_configurations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3760,6 +5534,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_syslog_configurations")]
 impl From<crate::operation::list_syslog_configurations::ListSyslogConfigurationsError> for Error {
     fn from(err: crate::operation::list_syslog_configurations::ListSyslogConfigurationsError) -> Self {
         match err {
@@ -3785,6 +5560,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3810,6 +5586,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -3828,6 +5605,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_log_group")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3853,6 +5631,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_log_group")]
 impl From<crate::operation::list_tags_log_group::ListTagsLogGroupError> for Error {
     fn from(err: crate::operation::list_tags_log_group::ListTagsLogGroupError) -> Self {
         match err {
@@ -3866,6 +5645,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3891,6 +5671,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_policy")]
 impl From<crate::operation::put_account_policy::PutAccountPolicyError> for Error {
     fn from(err: crate::operation::put_account_policy::PutAccountPolicyError) -> Self {
         match err {
@@ -3910,6 +5691,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_bearer_token_authentication")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3935,6 +5717,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_bearer_token_authentication")]
 impl From<crate::operation::put_bearer_token_authentication::PutBearerTokenAuthenticationError> for Error {
     fn from(err: crate::operation::put_bearer_token_authentication::PutBearerTokenAuthenticationError) -> Self {
         match err {
@@ -3960,6 +5743,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3985,6 +5769,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_data_protection_policy")]
 impl From<crate::operation::put_data_protection_policy::PutDataProtectionPolicyError> for Error {
     fn from(err: crate::operation::put_data_protection_policy::PutDataProtectionPolicyError) -> Self {
         match err {
@@ -4009,6 +5794,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4034,6 +5820,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination")]
 impl From<crate::operation::put_delivery_destination::PutDeliveryDestinationError> for Error {
     fn from(err: crate::operation::put_delivery_destination::PutDeliveryDestinationError) -> Self {
         match err {
@@ -4061,6 +5848,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4086,6 +5874,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_destination_policy")]
 impl From<crate::operation::put_delivery_destination_policy::PutDeliveryDestinationPolicyError> for Error {
     fn from(err: crate::operation::put_delivery_destination_policy::PutDeliveryDestinationPolicyError) -> Self {
         match err {
@@ -4105,6 +5894,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_source")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4130,6 +5920,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_delivery_source")]
 impl From<crate::operation::put_delivery_source::PutDeliverySourceError> for Error {
     fn from(err: crate::operation::put_delivery_source::PutDeliverySourceError) -> Self {
         match err {
@@ -4155,6 +5946,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_destination::PutDestinationError, R>>
     for Error
@@ -4176,6 +5968,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination")]
 impl From<crate::operation::put_destination::PutDestinationError> for Error {
     fn from(err: crate::operation::put_destination::PutDestinationError) -> Self {
         match err {
@@ -4192,6 +5985,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4217,6 +6011,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_destination_policy")]
 impl From<crate::operation::put_destination_policy::PutDestinationPolicyError> for Error {
     fn from(err: crate::operation::put_destination_policy::PutDestinationPolicyError) -> Self {
         match err {
@@ -4235,6 +6030,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_index_policy")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_index_policy::PutIndexPolicyError, R>>
     for Error
@@ -4256,6 +6052,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_index_policy")]
 impl From<crate::operation::put_index_policy::PutIndexPolicyError> for Error {
     fn from(err: crate::operation::put_index_policy::PutIndexPolicyError) -> Self {
         match err {
@@ -4278,6 +6075,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_integration")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_integration::PutIntegrationError, R>>
     for Error
@@ -4299,6 +6097,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_integration")]
 impl From<crate::operation::put_integration::PutIntegrationError> for Error {
     fn from(err: crate::operation::put_integration::PutIntegrationError) -> Self {
         match err {
@@ -4318,6 +6117,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_events")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_log_events::PutLogEventsError, R>>
     for Error
 where
@@ -4335,6 +6135,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_events")]
 impl From<crate::operation::put_log_events::PutLogEventsError> for Error {
     fn from(err: crate::operation::put_log_events::PutLogEventsError) -> Self {
         match err {
@@ -4360,6 +6161,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_group_deletion_protection")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4385,6 +6187,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_log_group_deletion_protection")]
 impl From<crate::operation::put_log_group_deletion_protection::PutLogGroupDeletionProtectionError> for Error {
     fn from(err: crate::operation::put_log_group_deletion_protection::PutLogGroupDeletionProtectionError) -> Self {
         match err {
@@ -4410,6 +6213,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4435,6 +6239,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_metric_filter")]
 impl From<crate::operation::put_metric_filter::PutMetricFilterError> for Error {
     fn from(err: crate::operation::put_metric_filter::PutMetricFilterError) -> Self {
         match err {
@@ -4460,6 +6265,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_query_definition")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4485,6 +6291,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_query_definition")]
 impl From<crate::operation::put_query_definition::PutQueryDefinitionError> for Error {
     fn from(err: crate::operation::put_query_definition::PutQueryDefinitionError) -> Self {
         match err {
@@ -4506,6 +6313,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4531,6 +6339,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_resource_policy")]
 impl From<crate::operation::put_resource_policy::PutResourcePolicyError> for Error {
     fn from(err: crate::operation::put_resource_policy::PutResourcePolicyError) -> Self {
         match err {
@@ -4553,6 +6362,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_retention_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4578,6 +6388,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_retention_policy")]
 impl From<crate::operation::put_retention_policy::PutRetentionPolicyError> for Error {
     fn from(err: crate::operation::put_retention_policy::PutRetentionPolicyError) -> Self {
         match err {
@@ -4599,6 +6410,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_storage_tier_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4624,6 +6436,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_storage_tier_policy")]
 impl From<crate::operation::put_storage_tier_policy::PutStorageTierPolicyError> for Error {
     fn from(err: crate::operation::put_storage_tier_policy::PutStorageTierPolicyError) -> Self {
         match err {
@@ -4648,6 +6461,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_subscription_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4673,6 +6487,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_subscription_filter")]
 impl From<crate::operation::put_subscription_filter::PutSubscriptionFilterError> for Error {
     fn from(err: crate::operation::put_subscription_filter::PutSubscriptionFilterError) -> Self {
         match err {
@@ -4700,6 +6515,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_syslog_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4725,6 +6541,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_syslog_configuration")]
 impl From<crate::operation::put_syslog_configuration::PutSyslogConfigurationError> for Error {
     fn from(err: crate::operation::put_syslog_configuration::PutSyslogConfigurationError) -> Self {
         match err {
@@ -4755,6 +6572,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_transformer")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::put_transformer::PutTransformerError, R>>
     for Error
@@ -4776,6 +6594,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_transformer")]
 impl From<crate::operation::put_transformer::PutTransformerError> for Error {
     fn from(err: crate::operation::put_transformer::PutTransformerError) -> Self {
         match err {
@@ -4801,6 +6620,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::start_live_tail::StartLiveTailError, R>>
     for Error
@@ -4822,6 +6642,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl From<crate::operation::start_live_tail::StartLiveTailError> for Error {
     fn from(err: crate::operation::start_live_tail::StartLiveTailError) -> Self {
         match err {
@@ -4850,6 +6671,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::start_query::StartQueryError, R>>
     for Error
 where
@@ -4867,6 +6689,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_query")]
 impl From<crate::operation::start_query::StartQueryError> for Error {
     fn from(err: crate::operation::start_query::StartQueryError) -> Self {
         match err {
@@ -4889,6 +6712,7 @@
         }
     }
 }
+#[cfg(feature = "op_stop_query")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::stop_query::StopQueryError, R>>
     for Error
 where
@@ -4906,6 +6730,7 @@
         }
     }
 }
+#[cfg(feature = "op_stop_query")]
 impl From<crate::operation::stop_query::StopQueryError> for Error {
     fn from(err: crate::operation::stop_query::StopQueryError) -> Self {
         match err {
@@ -4922,6 +6747,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_log_group")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_log_group::TagLogGroupError, R>>
     for Error
 where
@@ -4939,6 +6765,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_log_group")]
 impl From<crate::operation::tag_log_group::TagLogGroupError> for Error {
     fn from(err: crate::operation::tag_log_group::TagLogGroupError) -> Self {
         match err {
@@ -4952,6 +6779,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -4969,6 +6797,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -4988,6 +6817,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_metric_filter")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5013,6 +6843,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_metric_filter")]
 impl From<crate::operation::test_metric_filter::TestMetricFilterError> for Error {
     fn from(err: crate::operation::test_metric_filter::TestMetricFilterError) -> Self {
         match err {
@@ -5026,6 +6857,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_transformer")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<crate::operation::test_transformer::TestTransformerError, R>,
@@ -5048,6 +6880,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_transformer")]
 impl From<crate::operation::test_transformer::TestTransformerError> for Error {
     fn from(err: crate::operation::test_transformer::TestTransformerError) -> Self {
         match err {
@@ -5064,6 +6897,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_log_group")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_log_group::UntagLogGroupError, R>>
     for Error
@@ -5085,6 +6919,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_log_group")]
 impl From<crate::operation::untag_log_group::UntagLogGroupError> for Error {
     fn from(err: crate::operation::untag_log_group::UntagLogGroupError) -> Self {
         match err {
@@ -5095,6 +6930,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -5116,6 +6952,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -5132,6 +6969,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_anomaly")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_anomaly::UpdateAnomalyError, R>>
     for Error
@@ -5153,6 +6991,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_anomaly")]
 impl From<crate::operation::update_anomaly::UpdateAnomalyError> for Error {
     fn from(err: crate::operation::update_anomaly::UpdateAnomalyError) -> Self {
         match err {
@@ -5172,6 +7011,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_delivery_configuration")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5197,6 +7037,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_delivery_configuration")]
 impl From<crate::operation::update_delivery_configuration::UpdateDeliveryConfigurationError> for Error {
     fn from(err: crate::operation::update_delivery_configuration::UpdateDeliveryConfigurationError) -> Self {
         match err {
@@ -5222,6 +7063,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_log_anomaly_detector")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5247,6 +7089,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_log_anomaly_detector")]
 impl From<crate::operation::update_log_anomaly_detector::UpdateLogAnomalyDetectorError> for Error {
     fn from(err: crate::operation::update_log_anomaly_detector::UpdateLogAnomalyDetectorError) -> Self {
         match err {
@@ -5266,6 +7109,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_lookup_table")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5291,6 +7135,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_lookup_table")]
 impl From<crate::operation::update_lookup_table::UpdateLookupTableError> for Error {
     fn from(err: crate::operation::update_lookup_table::UpdateLookupTableError) -> Self {
         match err {
@@ -5313,6 +7158,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduled_query")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -5338,6 +7184,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_scheduled_query")]
 impl From<crate::operation::update_scheduled_query::UpdateScheduledQueryError> for Error {
     fn from(err: crate::operation::update_scheduled_query::UpdateScheduledQueryError) -> Self {
         match err {
@@ -5365,6 +7212,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::GetLogObjectResponseStreamError, R>>
     for Error
@@ -5386,6 +7234,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl From<crate::types::error::GetLogObjectResponseStreamError> for Error {
     fn from(err: crate::types::error::GetLogObjectResponseStreamError) -> Self {
         match err {
@@ -5396,6 +7245,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::types::error::StartLiveTailResponseStreamError, R>>
     for Error
@@ -5417,6 +7267,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl From<crate::types::error::StartLiveTailResponseStreamError> for Error {
     fn from(err: crate::types::error::StartLiveTailResponseStreamError) -> Self {
         match err {
@@ -5433,26 +7284,563 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::AccessDeniedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::DataAlreadyAcceptedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::InternalServerException(inner) => inner.source(),
+            #[cfg(feature = "op_get_log_object")]
             Error::InternalStreamingException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Error::InvalidOperationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::InvalidParameterException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::InvalidSequenceTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(feature = "op_start_query")]
             Error::MalformedQueryException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Error::OperationAbortedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Error::ResourceAlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ResourceNotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Error::ServiceQuotaExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Error::ServiceUnavailableException(inner) => inner.source(),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionStreamingException(inner) => inner.source(),
+            #[cfg(feature = "op_start_live_tail")]
             Error::SessionTimeoutException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ThrottlingException(inner) => inner.source(),
+            #[cfg(feature = "op_tag_resource")]
             Error::TooManyTagsException(inner) => inner.source(),
+            #[cfg(feature = "op_put_log_events")]
             Error::UnrecognizedClientException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Error::ValidationException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -5461,26 +7849,563 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_lookup_tables",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_log_object",
+                feature = "op_get_lookup_table",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_syslog_configuration",
+                feature = "op_start_live_tail",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::AccessDeniedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::DataAlreadyAcceptedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_scheduled_query",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::InternalServerException(e) => e.request_id(),
+            #[cfg(feature = "op_get_log_object")]
             Self::InternalStreamingException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_import_task",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_get_log_object",
+                feature = "op_get_transformer",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_test_transformer"
+            ))]
             Self::InvalidOperationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::InvalidParameterException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::InvalidSequenceTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_index_policy",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_put_account_policy",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(feature = "op_start_query")]
             Self::MalformedQueryException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_disassociate_kms_key",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_fields",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_update_anomaly",
+                feature = "op_update_log_anomaly_detector"
+            ))]
             Self::OperationAbortedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_export_task",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table"
+            ))]
             Self::ResourceAlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_export_task",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_import_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_stream",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_object",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_anomalies",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_index_policy",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_live_tail",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_log_group",
+                feature = "op_tag_resource",
+                feature = "op_untag_log_group",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ResourceNotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_delivery",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source"
+            ))]
             Self::ServiceQuotaExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_kms_key",
+                feature = "op_cancel_export_task",
+                feature = "op_create_delivery",
+                feature = "op_create_export_task",
+                feature = "op_create_log_anomaly_detector",
+                feature = "op_create_log_group",
+                feature = "op_create_log_stream",
+                feature = "op_create_lookup_table",
+                feature = "op_delete_account_policy",
+                feature = "op_delete_data_protection_policy",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_destination",
+                feature = "op_delete_index_policy",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_anomaly_detector",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_lookup_table",
+                feature = "op_delete_metric_filter",
+                feature = "op_delete_query_definition",
+                feature = "op_delete_resource_policy",
+                feature = "op_delete_retention_policy",
+                feature = "op_delete_subscription_filter",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_delete_transformer",
+                feature = "op_describe_account_policies",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_destinations",
+                feature = "op_describe_export_tasks",
+                feature = "op_describe_field_indexes",
+                feature = "op_describe_index_policies",
+                feature = "op_describe_log_groups",
+                feature = "op_describe_log_streams",
+                feature = "op_describe_lookup_tables",
+                feature = "op_describe_metric_filters",
+                feature = "op_describe_queries",
+                feature = "op_describe_query_definitions",
+                feature = "op_describe_resource_policies",
+                feature = "op_describe_subscription_filters",
+                feature = "op_disassociate_kms_key",
+                feature = "op_filter_log_events",
+                feature = "op_get_data_protection_policy",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_integration",
+                feature = "op_get_log_anomaly_detector",
+                feature = "op_get_log_events",
+                feature = "op_get_log_fields",
+                feature = "op_get_log_group_fields",
+                feature = "op_get_log_record",
+                feature = "op_get_lookup_table",
+                feature = "op_get_query_results",
+                feature = "op_get_storage_tier_policy",
+                feature = "op_get_transformer",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_anomalies",
+                feature = "op_list_integrations",
+                feature = "op_list_log_anomaly_detectors",
+                feature = "op_list_log_groups",
+                feature = "op_list_log_groups_for_query",
+                feature = "op_list_syslog_configurations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tags_log_group",
+                feature = "op_put_account_policy",
+                feature = "op_put_bearer_token_authentication",
+                feature = "op_put_data_protection_policy",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_destination",
+                feature = "op_put_destination_policy",
+                feature = "op_put_index_policy",
+                feature = "op_put_integration",
+                feature = "op_put_log_events",
+                feature = "op_put_log_group_deletion_protection",
+                feature = "op_put_metric_filter",
+                feature = "op_put_query_definition",
+                feature = "op_put_resource_policy",
+                feature = "op_put_retention_policy",
+                feature = "op_put_storage_tier_policy",
+                feature = "op_put_subscription_filter",
+                feature = "op_put_syslog_configuration",
+                feature = "op_put_transformer",
+                feature = "op_start_query",
+                feature = "op_stop_query",
+                feature = "op_tag_resource",
+                feature = "op_test_metric_filter",
+                feature = "op_test_transformer",
+                feature = "op_untag_resource",
+                feature = "op_update_anomaly",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_log_anomaly_detector",
+                feature = "op_update_lookup_table"
+            ))]
             Self::ServiceUnavailableException(e) => e.request_id(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionStreamingException(e) => e.request_id(),
+            #[cfg(feature = "op_start_live_tail")]
             Self::SessionTimeoutException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_cancel_import_task",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_scheduled_query",
+                feature = "op_delete_syslog_configuration",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_describe_import_task_batches",
+                feature = "op_describe_import_tasks",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_list_syslog_configurations",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_source",
+                feature = "op_put_syslog_configuration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ThrottlingException(e) => e.request_id(),
+            #[cfg(feature = "op_tag_resource")]
             Self::TooManyTagsException(e) => e.request_id(),
+            #[cfg(feature = "op_put_log_events")]
             Self::UnrecognizedClientException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_source_to_s3_table_integration",
+                feature = "op_create_delivery",
+                feature = "op_create_import_task",
+                feature = "op_create_lookup_table",
+                feature = "op_create_scheduled_query",
+                feature = "op_delete_delivery",
+                feature = "op_delete_delivery_destination",
+                feature = "op_delete_delivery_destination_policy",
+                feature = "op_delete_delivery_source",
+                feature = "op_delete_integration",
+                feature = "op_delete_log_group",
+                feature = "op_delete_log_stream",
+                feature = "op_delete_scheduled_query",
+                feature = "op_describe_configuration_templates",
+                feature = "op_describe_deliveries",
+                feature = "op_describe_delivery_destinations",
+                feature = "op_describe_delivery_sources",
+                feature = "op_disassociate_source_from_s3_table_integration",
+                feature = "op_get_delivery",
+                feature = "op_get_delivery_destination",
+                feature = "op_get_delivery_destination_policy",
+                feature = "op_get_delivery_source",
+                feature = "op_get_scheduled_query",
+                feature = "op_get_scheduled_query_history",
+                feature = "op_list_aggregate_log_group_summaries",
+                feature = "op_list_scheduled_queries",
+                feature = "op_list_sources_for_s3_table_integration",
+                feature = "op_put_delivery_destination",
+                feature = "op_put_delivery_destination_policy",
+                feature = "op_put_delivery_source",
+                feature = "op_put_integration",
+                feature = "op_update_delivery_configuration",
+                feature = "op_update_lookup_table",
+                feature = "op_update_scheduled_query"
+            ))]
             Self::ValidationException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/event_stream_serde.rs b/src/event_stream_serde.rs
--- a/src/event_stream_serde.rs
+++ b/src/event_stream_serde.rs
@@ -8,6 +8,7 @@
         GetLogObjectResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for GetLogObjectResponseStreamUnmarshaller {
     type Output = crate::types::GetLogObjectResponseStream;
     type Error = crate::types::error::GetLogObjectResponseStreamError;
@@ -84,6 +85,7 @@
         StartLiveTailResponseStreamUnmarshaller
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_eventstream::frame::UnmarshallMessage for StartLiveTailResponseStreamUnmarshaller {
     type Output = crate::types::StartLiveTailResponseStream;
     type Error = crate::types::error::StartLiveTailResponseStreamError;
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn reflens_describe_configuration_templates_output_output_next_token(
     input: &crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) fn reflens_describe_deliveries_output_output_next_token(
     input: &crate::operation::describe_deliveries::DescribeDeliveriesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) fn reflens_describe_delivery_destinations_output_output_next_token(
     input: &crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) fn reflens_describe_delivery_sources_output_output_next_token(
     input: &crate::operation::describe_delivery_sources::DescribeDeliverySourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) fn reflens_describe_destinations_output_output_next_token(
     input: &crate::operation::describe_destinations::DescribeDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) fn reflens_describe_log_groups_output_output_next_token(
     input: &crate::operation::describe_log_groups::DescribeLogGroupsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) fn reflens_describe_log_streams_output_output_next_token(
     input: &crate::operation::describe_log_streams::DescribeLogStreamsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) fn reflens_describe_metric_filters_output_output_next_token(
     input: &crate::operation::describe_metric_filters::DescribeMetricFiltersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) fn reflens_describe_subscription_filters_output_output_next_token(
     input: &crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) fn reflens_filter_log_events_output_output_next_token(
     input: &crate::operation::filter_log_events::FilterLogEventsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_log_events")]
 pub(crate) fn reflens_get_log_events_output_output_next_forward_token(
     input: &crate::operation::get_log_events::GetLogEventsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -109,6 +120,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) fn reflens_get_scheduled_query_history_output_output_next_token(
     input: &crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -119,6 +131,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) fn reflens_list_aggregate_log_group_summaries_output_output_next_token(
     input: &crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -129,6 +142,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn reflens_list_anomalies_output_output_next_token(
     input: &crate::operation::list_anomalies::ListAnomaliesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -139,6 +153,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) fn reflens_list_log_anomaly_detectors_output_output_next_token(
     input: &crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -149,6 +164,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) fn reflens_list_log_groups_for_query_output_output_next_token(
     input: &crate::operation::list_log_groups_for_query::ListLogGroupsForQueryOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -159,6 +175,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) fn reflens_list_scheduled_queries_output_output_next_token(
     input: &crate::operation::list_scheduled_queries::ListScheduledQueriesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -169,6 +186,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) fn reflens_list_sources_for_s3_table_integration_output_output_next_token(
     input: &crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -179,6 +197,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn lens_describe_configuration_templates_output_output_configuration_templates(
     input: crate::operation::describe_configuration_templates::DescribeConfigurationTemplatesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ConfigurationTemplate>> {
@@ -186,6 +205,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) fn lens_describe_deliveries_output_output_deliveries(
     input: crate::operation::describe_deliveries::DescribeDeliveriesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Delivery>> {
@@ -193,6 +213,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) fn lens_describe_delivery_destinations_output_output_delivery_destinations(
     input: crate::operation::describe_delivery_destinations::DescribeDeliveryDestinationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::DeliveryDestination>> {
@@ -200,6 +221,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) fn lens_describe_delivery_sources_output_output_delivery_sources(
     input: crate::operation::describe_delivery_sources::DescribeDeliverySourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::DeliverySource>> {
@@ -207,6 +229,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) fn lens_describe_destinations_output_output_destinations(
     input: crate::operation::describe_destinations::DescribeDestinationsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Destination>> {
@@ -214,6 +237,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) fn lens_describe_log_groups_output_output_log_groups(
     input: crate::operation::describe_log_groups::DescribeLogGroupsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::LogGroup>> {
@@ -221,6 +245,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) fn lens_describe_log_streams_output_output_log_streams(
     input: crate::operation::describe_log_streams::DescribeLogStreamsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::LogStream>> {
@@ -228,6 +253,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) fn lens_describe_metric_filters_output_output_metric_filters(
     input: crate::operation::describe_metric_filters::DescribeMetricFiltersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::MetricFilter>> {
@@ -235,6 +261,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) fn lens_describe_subscription_filters_output_output_subscription_filters(
     input: crate::operation::describe_subscription_filters::DescribeSubscriptionFiltersOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::SubscriptionFilter>> {
@@ -242,6 +269,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_log_events")]
 pub(crate) fn lens_get_log_events_output_output_events(
     input: crate::operation::get_log_events::GetLogEventsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::OutputLogEvent>> {
@@ -249,6 +277,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) fn lens_get_scheduled_query_history_output_output_trigger_history(
     input: crate::operation::get_scheduled_query_history::GetScheduledQueryHistoryOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TriggerHistoryRecord>> {
@@ -256,6 +285,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) fn lens_list_aggregate_log_group_summaries_output_output_aggregate_log_group_summaries(
     input: crate::operation::list_aggregate_log_group_summaries::ListAggregateLogGroupSummariesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AggregateLogGroupSummary>> {
@@ -263,6 +293,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn lens_list_anomalies_output_output_anomalies(
     input: crate::operation::list_anomalies::ListAnomaliesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::Anomaly>> {
@@ -270,6 +301,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) fn lens_list_log_anomaly_detectors_output_output_anomaly_detectors(
     input: crate::operation::list_log_anomaly_detectors::ListLogAnomalyDetectorsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::AnomalyDetector>> {
@@ -277,6 +309,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) fn lens_list_log_groups_for_query_output_output_log_group_identifiers(
     input: crate::operation::list_log_groups_for_query::ListLogGroupsForQueryOutput,
 ) -> ::std::option::Option<::std::vec::Vec<::std::string::String>> {
@@ -284,6 +317,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) fn lens_list_scheduled_queries_output_output_scheduled_queries(
     input: crate::operation::list_scheduled_queries::ListScheduledQueriesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ScheduledQuerySummary>> {
@@ -291,6 +325,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) fn lens_list_sources_for_s3_table_integration_output_output_sources(
     input: crate::operation::list_sources_for_s3_table_integration::ListSourcesForS3TableIntegrationOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::S3TableIntegrationSource>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,356 +1,474 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_associate_kms_key")]
 /// Types for the `AssociateKmsKey` operation.
 pub mod associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 /// Types for the `AssociateSourceToS3TableIntegration` operation.
 pub mod associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 /// Types for the `CancelExportTask` operation.
 pub mod cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 /// Types for the `CancelImportTask` operation.
 pub mod cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 /// Types for the `CreateDelivery` operation.
 pub mod create_delivery;

+#[cfg(feature = "op_create_export_task")]
 /// Types for the `CreateExportTask` operation.
 pub mod create_export_task;

+#[cfg(feature = "op_create_import_task")]
 /// Types for the `CreateImportTask` operation.
 pub mod create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 /// Types for the `CreateLogAnomalyDetector` operation.
 pub mod create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 /// Types for the `CreateLogGroup` operation.
 pub mod create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 /// Types for the `CreateLogStream` operation.
 pub mod create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 /// Types for the `CreateLookupTable` operation.
 pub mod create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 /// Types for the `CreateScheduledQuery` operation.
 pub mod create_scheduled_query;

+#[cfg(feature = "op_delete_account_policy")]
 /// Types for the `DeleteAccountPolicy` operation.
 pub mod delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 /// Types for the `DeleteDataProtectionPolicy` operation.
 pub mod delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 /// Types for the `DeleteDelivery` operation.
 pub mod delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 /// Types for the `DeleteDeliveryDestination` operation.
 pub mod delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 /// Types for the `DeleteDeliveryDestinationPolicy` operation.
 pub mod delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 /// Types for the `DeleteDeliverySource` operation.
 pub mod delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 /// Types for the `DeleteDestination` operation.
 pub mod delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 /// Types for the `DeleteIndexPolicy` operation.
 pub mod delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 /// Types for the `DeleteIntegration` operation.
 pub mod delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 /// Types for the `DeleteLogAnomalyDetector` operation.
 pub mod delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 /// Types for the `DeleteLogGroup` operation.
 pub mod delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 /// Types for the `DeleteLogStream` operation.
 pub mod delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 /// Types for the `DeleteLookupTable` operation.
 pub mod delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 /// Types for the `DeleteMetricFilter` operation.
 pub mod delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 /// Types for the `DeleteQueryDefinition` operation.
 pub mod delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 /// Types for the `DeleteResourcePolicy` operation.
 pub mod delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 /// Types for the `DeleteRetentionPolicy` operation.
 pub mod delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 /// Types for the `DeleteScheduledQuery` operation.
 pub mod delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 /// Types for the `DeleteSubscriptionFilter` operation.
 pub mod delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 /// Types for the `DeleteSyslogConfiguration` operation.
 pub mod delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 /// Types for the `DeleteTransformer` operation.
 pub mod delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 /// Types for the `DescribeAccountPolicies` operation.
 pub mod describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 /// Types for the `DescribeConfigurationTemplates` operation.
 pub mod describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 /// Types for the `DescribeDeliveries` operation.
 pub mod describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 /// Types for the `DescribeDeliveryDestinations` operation.
 pub mod describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 /// Types for the `DescribeDeliverySources` operation.
 pub mod describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 /// Types for the `DescribeDestinations` operation.
 pub mod describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 /// Types for the `DescribeExportTasks` operation.
 pub mod describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 /// Types for the `DescribeFieldIndexes` operation.
 pub mod describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 /// Types for the `DescribeImportTaskBatches` operation.
 pub mod describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 /// Types for the `DescribeImportTasks` operation.
 pub mod describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 /// Types for the `DescribeIndexPolicies` operation.
 pub mod describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 /// Types for the `DescribeLogGroups` operation.
 pub mod describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 /// Types for the `DescribeLogStreams` operation.
 pub mod describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 /// Types for the `DescribeLookupTables` operation.
 pub mod describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 /// Types for the `DescribeMetricFilters` operation.
 pub mod describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 /// Types for the `DescribeQueries` operation.
 pub mod describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 /// Types for the `DescribeQueryDefinitions` operation.
 pub mod describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 /// Types for the `DescribeResourcePolicies` operation.
 pub mod describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 /// Types for the `DescribeSubscriptionFilters` operation.
 pub mod describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 /// Types for the `DisassociateKmsKey` operation.
 pub mod disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 /// Types for the `DisassociateSourceFromS3TableIntegration` operation.
 pub mod disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 /// Types for the `FilterLogEvents` operation.
 pub mod filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 /// Types for the `GetDataProtectionPolicy` operation.
 pub mod get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 /// Types for the `GetDelivery` operation.
 pub mod get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 /// Types for the `GetDeliveryDestination` operation.
 pub mod get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 /// Types for the `GetDeliveryDestinationPolicy` operation.
 pub mod get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 /// Types for the `GetDeliverySource` operation.
 pub mod get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 /// Types for the `GetIntegration` operation.
 pub mod get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 /// Types for the `GetLogAnomalyDetector` operation.
 pub mod get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 /// Types for the `GetLogEvents` operation.
 pub mod get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 /// Types for the `GetLogFields` operation.
 pub mod get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 /// Types for the `GetLogGroupFields` operation.
 pub mod get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 /// Types for the `GetLogObject` operation.
 pub mod get_log_object;

+#[cfg(feature = "op_get_log_record")]
 /// Types for the `GetLogRecord` operation.
 pub mod get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 /// Types for the `GetLookupTable` operation.
 pub mod get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 /// Types for the `GetQueryResults` operation.
 pub mod get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 /// Types for the `GetScheduledQuery` operation.
 pub mod get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 /// Types for the `GetScheduledQueryHistory` operation.
 pub mod get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 /// Types for the `GetStorageTierPolicy` operation.
 pub mod get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 /// Types for the `GetTransformer` operation.
 pub mod get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 /// Types for the `ListAggregateLogGroupSummaries` operation.
 pub mod list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 /// Types for the `ListAnomalies` operation.
 pub mod list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 /// Types for the `ListIntegrations` operation.
 pub mod list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 /// Types for the `ListLogAnomalyDetectors` operation.
 pub mod list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 /// Types for the `ListLogGroups` operation.
 pub mod list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 /// Types for the `ListLogGroupsForQuery` operation.
 pub mod list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 /// Types for the `ListScheduledQueries` operation.
 pub mod list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 /// Types for the `ListSourcesForS3TableIntegration` operation.
 pub mod list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 /// Types for the `ListSyslogConfigurations` operation.
 pub mod list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 /// Types for the `ListTagsLogGroup` operation.
 pub mod list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 /// Types for the `PutAccountPolicy` operation.
 pub mod put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 /// Types for the `PutBearerTokenAuthentication` operation.
 pub mod put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 /// Types for the `PutDataProtectionPolicy` operation.
 pub mod put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 /// Types for the `PutDeliveryDestination` operation.
 pub mod put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 /// Types for the `PutDeliveryDestinationPolicy` operation.
 pub mod put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 /// Types for the `PutDeliverySource` operation.
 pub mod put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 /// Types for the `PutDestination` operation.
 pub mod put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 /// Types for the `PutDestinationPolicy` operation.
 pub mod put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 /// Types for the `PutIndexPolicy` operation.
 pub mod put_index_policy;

+#[cfg(feature = "op_put_integration")]
 /// Types for the `PutIntegration` operation.
 pub mod put_integration;

+#[cfg(feature = "op_put_log_events")]
 /// Types for the `PutLogEvents` operation.
 pub mod put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 /// Types for the `PutLogGroupDeletionProtection` operation.
 pub mod put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 /// Types for the `PutMetricFilter` operation.
 pub mod put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 /// Types for the `PutQueryDefinition` operation.
 pub mod put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 /// Types for the `PutResourcePolicy` operation.
 pub mod put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 /// Types for the `PutRetentionPolicy` operation.
 pub mod put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 /// Types for the `PutStorageTierPolicy` operation.
 pub mod put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 /// Types for the `PutSubscriptionFilter` operation.
 pub mod put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 /// Types for the `PutSyslogConfiguration` operation.
 pub mod put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 /// Types for the `PutTransformer` operation.
 pub mod put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 /// Types for the `StartLiveTail` operation.
 pub mod start_live_tail;

+#[cfg(feature = "op_start_query")]
 /// Types for the `StartQuery` operation.
 pub mod start_query;

+#[cfg(feature = "op_stop_query")]
 /// Types for the `StopQuery` operation.
 pub mod stop_query;

+#[cfg(feature = "op_tag_log_group")]
 /// Types for the `TagLogGroup` operation.
 pub mod tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 /// Types for the `TestMetricFilter` operation.
 pub mod test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 /// Types for the `TestTransformer` operation.
 pub mod test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 /// Types for the `UntagLogGroup` operation.
 pub mod untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 /// Types for the `UpdateAnomaly` operation.
 pub mod update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 /// Types for the `UpdateDeliveryConfiguration` operation.
 pub mod update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 /// Types for the `UpdateLogAnomalyDetector` operation.
 pub mod update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 /// Types for the `UpdateLookupTable` operation.
 pub mod update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 /// Types for the `UpdateScheduledQuery` operation.
 pub mod update_scheduled_query;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,124 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +137,126 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,242 +268,480 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_associate_kms_key")]
 pub(crate) mod shape_associate_kms_key;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 pub(crate) mod shape_associate_source_to_s3_table_integration;

+#[cfg(feature = "op_cancel_export_task")]
 pub(crate) mod shape_cancel_export_task;

+#[cfg(feature = "op_cancel_import_task")]
 pub(crate) mod shape_cancel_import_task;

+#[cfg(feature = "op_create_delivery")]
 pub(crate) mod shape_create_delivery;

+#[cfg(feature = "op_create_export_task")]
 pub(crate) mod shape_create_export_task;

+#[cfg(feature = "op_create_import_task")]
 pub(crate) mod shape_create_import_task;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 pub(crate) mod shape_create_log_anomaly_detector;

+#[cfg(feature = "op_create_log_group")]
 pub(crate) mod shape_create_log_group;

+#[cfg(feature = "op_create_log_stream")]
 pub(crate) mod shape_create_log_stream;

+#[cfg(feature = "op_create_lookup_table")]
 pub(crate) mod shape_create_lookup_table;

+#[cfg(feature = "op_create_scheduled_query")]
 pub(crate) mod shape_create_scheduled_query;

+#[cfg(feature = "op_delete_account_policy")]
 pub(crate) mod shape_delete_account_policy;

+#[cfg(feature = "op_delete_data_protection_policy")]
 pub(crate) mod shape_delete_data_protection_policy;

+#[cfg(feature = "op_delete_delivery")]
 pub(crate) mod shape_delete_delivery;

+#[cfg(feature = "op_delete_delivery_destination")]
 pub(crate) mod shape_delete_delivery_destination;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 pub(crate) mod shape_delete_delivery_destination_policy;

+#[cfg(feature = "op_delete_delivery_source")]
 pub(crate) mod shape_delete_delivery_source;

+#[cfg(feature = "op_delete_destination")]
 pub(crate) mod shape_delete_destination;

+#[cfg(feature = "op_delete_index_policy")]
 pub(crate) mod shape_delete_index_policy;

+#[cfg(feature = "op_delete_integration")]
 pub(crate) mod shape_delete_integration;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 pub(crate) mod shape_delete_log_anomaly_detector;

+#[cfg(feature = "op_delete_log_group")]
 pub(crate) mod shape_delete_log_group;

+#[cfg(feature = "op_delete_log_stream")]
 pub(crate) mod shape_delete_log_stream;

+#[cfg(feature = "op_delete_lookup_table")]
 pub(crate) mod shape_delete_lookup_table;

+#[cfg(feature = "op_delete_metric_filter")]
 pub(crate) mod shape_delete_metric_filter;

+#[cfg(feature = "op_delete_query_definition")]
 pub(crate) mod shape_delete_query_definition;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy;

+#[cfg(feature = "op_delete_retention_policy")]
 pub(crate) mod shape_delete_retention_policy;

+#[cfg(feature = "op_delete_scheduled_query")]
 pub(crate) mod shape_delete_scheduled_query;

+#[cfg(feature = "op_delete_subscription_filter")]
 pub(crate) mod shape_delete_subscription_filter;

+#[cfg(feature = "op_delete_syslog_configuration")]
 pub(crate) mod shape_delete_syslog_configuration;

+#[cfg(feature = "op_delete_transformer")]
 pub(crate) mod shape_delete_transformer;

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_describe_account_policies;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_describe_configuration_templates;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_describe_deliveries;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_describe_delivery_destinations;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_describe_delivery_sources;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_describe_destinations;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_describe_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_describe_field_indexes;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_describe_import_task_batches;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_describe_import_tasks;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_describe_index_policies;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_describe_log_groups;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_describe_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_describe_lookup_tables;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_describe_metric_filters;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_describe_queries;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_describe_query_definitions;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_describe_resource_policies;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_describe_subscription_filters;

+#[cfg(feature = "op_disassociate_kms_key")]
 pub(crate) mod shape_disassociate_kms_key;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 pub(crate) mod shape_disassociate_source_from_s3_table_integration;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filter_log_events;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy;

+#[cfg(feature = "op_get_delivery")]
 pub(crate) mod shape_get_delivery;

+#[cfg(feature = "op_get_delivery_destination")]
 pub(crate) mod shape_get_delivery_destination;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 pub(crate) mod shape_get_delivery_destination_policy;

+#[cfg(feature = "op_get_delivery_source")]
 pub(crate) mod shape_get_delivery_source;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_get_integration;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 pub(crate) mod shape_get_log_anomaly_detector;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_get_log_events;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_get_log_fields;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_get_log_group_fields;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_get_log_record;

+#[cfg(feature = "op_get_lookup_table")]
 pub(crate) mod shape_get_lookup_table;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_get_query_results;

+#[cfg(feature = "op_get_scheduled_query")]
 pub(crate) mod shape_get_scheduled_query;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_get_scheduled_query_history;

+#[cfg(feature = "op_get_storage_tier_policy")]
 pub(crate) mod shape_get_storage_tier_policy;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_get_transformer;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_list_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_list_anomalies;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_list_integrations;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_list_log_anomaly_detectors;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_list_log_groups;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_list_log_groups_for_query;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_list_scheduled_queries;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_list_sources_for_s3_table_integration;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_list_syslog_configurations;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tags_log_group")]
 pub(crate) mod shape_list_tags_log_group;

+#[cfg(feature = "op_put_account_policy")]
 pub(crate) mod shape_put_account_policy;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 pub(crate) mod shape_put_bearer_token_authentication;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy;

+#[cfg(feature = "op_put_delivery_destination")]
 pub(crate) mod shape_put_delivery_destination;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 pub(crate) mod shape_put_delivery_destination_policy;

+#[cfg(feature = "op_put_delivery_source")]
 pub(crate) mod shape_put_delivery_source;

+#[cfg(feature = "op_put_destination")]
 pub(crate) mod shape_put_destination;

+#[cfg(feature = "op_put_destination_policy")]
 pub(crate) mod shape_put_destination_policy;

+#[cfg(feature = "op_put_index_policy")]
 pub(crate) mod shape_put_index_policy;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_put_integration;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_put_log_events;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 pub(crate) mod shape_put_log_group_deletion_protection;

+#[cfg(feature = "op_put_metric_filter")]
 pub(crate) mod shape_put_metric_filter;

+#[cfg(feature = "op_put_query_definition")]
 pub(crate) mod shape_put_query_definition;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy;

+#[cfg(feature = "op_put_retention_policy")]
 pub(crate) mod shape_put_retention_policy;

+#[cfg(feature = "op_put_storage_tier_policy")]
 pub(crate) mod shape_put_storage_tier_policy;

+#[cfg(feature = "op_put_subscription_filter")]
 pub(crate) mod shape_put_subscription_filter;

+#[cfg(feature = "op_put_syslog_configuration")]
 pub(crate) mod shape_put_syslog_configuration;

+#[cfg(feature = "op_put_transformer")]
 pub(crate) mod shape_put_transformer;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_start_query;

+#[cfg(feature = "op_stop_query")]
 pub(crate) mod shape_stop_query;

+#[cfg(feature = "op_tag_log_group")]
 pub(crate) mod shape_tag_log_group;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_test_metric_filter;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_test_transformer;

+#[cfg(feature = "op_untag_log_group")]
 pub(crate) mod shape_untag_log_group;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_update_anomaly;

+#[cfg(feature = "op_update_delivery_configuration")]
 pub(crate) mod shape_update_delivery_configuration;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 pub(crate) mod shape_update_log_anomaly_detector;

+#[cfg(feature = "op_update_lookup_table")]
 pub(crate) mod shape_update_lookup_table;

+#[cfg(feature = "op_update_scheduled_query")]
 pub(crate) mod shape_update_scheduled_query;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -272,286 +750,943 @@
     }
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_access_denied_exception;

+#[cfg(feature = "op_associate_kms_key")]
 pub(crate) mod shape_associate_kms_key_input;

+#[cfg(feature = "op_associate_source_to_s3_table_integration")]
 pub(crate) mod shape_associate_source_to_s3_table_integration_input;

+#[cfg(feature = "op_cancel_export_task")]
 pub(crate) mod shape_cancel_export_task_input;

+#[cfg(feature = "op_cancel_import_task")]
 pub(crate) mod shape_cancel_import_task_input;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_create_delivery")]
 pub(crate) mod shape_create_delivery_input;

+#[cfg(feature = "op_create_export_task")]
 pub(crate) mod shape_create_export_task_input;

+#[cfg(feature = "op_create_import_task")]
 pub(crate) mod shape_create_import_task_input;

+#[cfg(feature = "op_create_log_anomaly_detector")]
 pub(crate) mod shape_create_log_anomaly_detector_input;

+#[cfg(feature = "op_create_log_group")]
 pub(crate) mod shape_create_log_group_input;

+#[cfg(feature = "op_create_log_stream")]
 pub(crate) mod shape_create_log_stream_input;

+#[cfg(feature = "op_create_lookup_table")]
 pub(crate) mod shape_create_lookup_table_input;

+#[cfg(feature = "op_create_scheduled_query")]
 pub(crate) mod shape_create_scheduled_query_input;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_data_already_accepted_exception;

+#[cfg(feature = "op_delete_account_policy")]
 pub(crate) mod shape_delete_account_policy_input;

+#[cfg(feature = "op_delete_data_protection_policy")]
 pub(crate) mod shape_delete_data_protection_policy_input;

+#[cfg(feature = "op_delete_delivery_destination")]
 pub(crate) mod shape_delete_delivery_destination_input;

+#[cfg(feature = "op_delete_delivery_destination_policy")]
 pub(crate) mod shape_delete_delivery_destination_policy_input;

+#[cfg(feature = "op_delete_delivery")]
 pub(crate) mod shape_delete_delivery_input;

+#[cfg(feature = "op_delete_delivery_source")]
 pub(crate) mod shape_delete_delivery_source_input;

+#[cfg(feature = "op_delete_destination")]
 pub(crate) mod shape_delete_destination_input;

+#[cfg(feature = "op_delete_index_policy")]
 pub(crate) mod shape_delete_index_policy_input;

+#[cfg(feature = "op_delete_integration")]
 pub(crate) mod shape_delete_integration_input;

+#[cfg(feature = "op_delete_log_anomaly_detector")]
 pub(crate) mod shape_delete_log_anomaly_detector_input;

+#[cfg(feature = "op_delete_log_group")]
 pub(crate) mod shape_delete_log_group_input;

+#[cfg(feature = "op_delete_log_stream")]
 pub(crate) mod shape_delete_log_stream_input;

+#[cfg(feature = "op_delete_lookup_table")]
 pub(crate) mod shape_delete_lookup_table_input;

+#[cfg(feature = "op_delete_metric_filter")]
 pub(crate) mod shape_delete_metric_filter_input;

+#[cfg(feature = "op_delete_query_definition")]
 pub(crate) mod shape_delete_query_definition_input;

+#[cfg(feature = "op_delete_resource_policy")]
 pub(crate) mod shape_delete_resource_policy_input;

+#[cfg(feature = "op_delete_retention_policy")]
 pub(crate) mod shape_delete_retention_policy_input;

+#[cfg(feature = "op_delete_scheduled_query")]
 pub(crate) mod shape_delete_scheduled_query_input;

+#[cfg(feature = "op_delete_subscription_filter")]
 pub(crate) mod shape_delete_subscription_filter_input;

+#[cfg(feature = "op_delete_syslog_configuration")]
 pub(crate) mod shape_delete_syslog_configuration_input;

+#[cfg(feature = "op_delete_transformer")]
 pub(crate) mod shape_delete_transformer_input;

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_describe_account_policies_input;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_describe_configuration_templates_input;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_describe_deliveries_input;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_describe_delivery_destinations_input;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_describe_delivery_sources_input;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_describe_destinations_input;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_describe_export_tasks_input;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_describe_field_indexes_input;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_describe_import_task_batches_input;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_describe_import_tasks_input;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_describe_index_policies_input;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_describe_log_groups_input;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_describe_log_streams_input;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_describe_lookup_tables_input;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_describe_metric_filters_input;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_describe_queries_input;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_describe_query_definitions_input;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_describe_resource_policies_input;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_describe_subscription_filters_input;

+#[cfg(feature = "op_disassociate_kms_key")]
 pub(crate) mod shape_disassociate_kms_key_input;

+#[cfg(feature = "op_disassociate_source_from_s3_table_integration")]
 pub(crate) mod shape_disassociate_source_from_s3_table_integration_input;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filter_log_events_input;

+#[cfg(feature = "op_get_data_protection_policy")]
 pub(crate) mod shape_get_data_protection_policy_input;

+#[cfg(feature = "op_get_delivery_destination")]
 pub(crate) mod shape_get_delivery_destination_input;

+#[cfg(feature = "op_get_delivery_destination_policy")]
 pub(crate) mod shape_get_delivery_destination_policy_input;

+#[cfg(feature = "op_get_delivery")]
 pub(crate) mod shape_get_delivery_input;

+#[cfg(feature = "op_get_delivery_source")]
 pub(crate) mod shape_get_delivery_source_input;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_get_integration_input;

+#[cfg(feature = "op_get_log_anomaly_detector")]
 pub(crate) mod shape_get_log_anomaly_detector_input;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_get_log_events_input;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_get_log_fields_input;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_get_log_group_fields_input;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object_input;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_get_log_object_output;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_get_log_record_input;

+#[cfg(feature = "op_get_lookup_table")]
 pub(crate) mod shape_get_lookup_table_input;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_get_query_results_input;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_get_scheduled_query_history_input;

+#[cfg(feature = "op_get_scheduled_query")]
 pub(crate) mod shape_get_scheduled_query_input;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_get_transformer_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_internal_server_exception;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_internal_streaming_exception;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_invalid_operation_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub(crate) mod shape_invalid_parameter_exception;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_invalid_sequence_token_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_list_aggregate_log_group_summaries_input;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_list_anomalies_input;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_list_integrations_input;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_list_log_anomaly_detectors_input;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_list_log_groups_for_query_input;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_list_log_groups_input;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_list_scheduled_queries_input;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_list_sources_for_s3_table_integration_input;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_list_syslog_configurations_input;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource_input;

+#[cfg(feature = "op_list_tags_log_group")]
 pub(crate) mod shape_list_tags_log_group_input;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_malformed_query_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub(crate) mod shape_operation_aborted_exception;

+#[cfg(feature = "op_put_account_policy")]
 pub(crate) mod shape_put_account_policy_input;

+#[cfg(feature = "op_put_bearer_token_authentication")]
 pub(crate) mod shape_put_bearer_token_authentication_input;

+#[cfg(feature = "op_put_data_protection_policy")]
 pub(crate) mod shape_put_data_protection_policy_input;

+#[cfg(feature = "op_put_delivery_destination")]
 pub(crate) mod shape_put_delivery_destination_input;

+#[cfg(feature = "op_put_delivery_destination_policy")]
 pub(crate) mod shape_put_delivery_destination_policy_input;

+#[cfg(feature = "op_put_delivery_source")]
 pub(crate) mod shape_put_delivery_source_input;

+#[cfg(feature = "op_put_destination")]
 pub(crate) mod shape_put_destination_input;

+#[cfg(feature = "op_put_destination_policy")]
 pub(crate) mod shape_put_destination_policy_input;

+#[cfg(feature = "op_put_index_policy")]
 pub(crate) mod shape_put_index_policy_input;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_put_integration_input;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_put_log_events_input;

+#[cfg(feature = "op_put_log_group_deletion_protection")]
 pub(crate) mod shape_put_log_group_deletion_protection_input;

+#[cfg(feature = "op_put_metric_filter")]
 pub(crate) mod shape_put_metric_filter_input;

+#[cfg(feature = "op_put_query_definition")]
 pub(crate) mod shape_put_query_definition_input;

+#[cfg(feature = "op_put_resource_policy")]
 pub(crate) mod shape_put_resource_policy_input;

+#[cfg(feature = "op_put_retention_policy")]
 pub(crate) mod shape_put_retention_policy_input;

+#[cfg(feature = "op_put_storage_tier_policy")]
 pub(crate) mod shape_put_storage_tier_policy_input;

+#[cfg(feature = "op_put_subscription_filter")]
 pub(crate) mod shape_put_subscription_filter_input;

+#[cfg(feature = "op_put_syslog_configuration")]
 pub(crate) mod shape_put_syslog_configuration_input;

+#[cfg(feature = "op_put_transformer")]
 pub(crate) mod shape_put_transformer_input;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub(crate) mod shape_resource_already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub(crate) mod shape_service_unavailable_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_session_streaming_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_session_timeout_exception;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_input;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_output;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_start_query_input;

+#[cfg(feature = "op_stop_query")]
 pub(crate) mod shape_stop_query_input;

+#[cfg(feature = "op_tag_log_group")]
 pub(crate) mod shape_tag_log_group_input;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_test_metric_filter_input;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_test_transformer_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_throttling_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_too_many_tags_exception;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_unrecognized_client_exception;

+#[cfg(feature = "op_untag_log_group")]
 pub(crate) mod shape_untag_log_group_input;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource_input;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_update_anomaly_input;

+#[cfg(feature = "op_update_delivery_configuration")]
 pub(crate) mod shape_update_delivery_configuration_input;

+#[cfg(feature = "op_update_log_anomaly_detector")]
 pub(crate) mod shape_update_log_anomaly_detector_input;

+#[cfg(feature = "op_update_lookup_table")]
 pub(crate) mod shape_update_lookup_table_input;

+#[cfg(feature = "op_update_scheduled_query")]
 pub(crate) mod shape_update_scheduled_query_input;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_validation_exception;

+#[cfg(any(feature = "op_get_log_object", feature = "op_start_live_tail"))]
 pub fn parse_event_stream_error_metadata(
     payload: &::bytes::Bytes,
 ) -> ::std::result::Result<
@@ -561,398 +1696,848 @@
     crate::json_errors::parse_error_metadata(payload, &::aws_smithy_runtime_api::http::Headers::new())
 }

+#[cfg(feature = "op_describe_account_policies")]
 pub(crate) mod shape_account_policies;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub(crate) mod shape_account_policy;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_aggregate_log_group_summaries;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_anomalies;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_anomaly_detectors;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_templates;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub(crate) mod shape_data_source;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub(crate) mod shape_data_source_filter;

+#[cfg(feature = "op_describe_deliveries")]
 pub(crate) mod shape_deliveries;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub(crate) mod shape_delivery;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) mod shape_delivery_destination;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) mod shape_delivery_destination_configuration;

+#[cfg(feature = "op_describe_delivery_destinations")]
 pub(crate) mod shape_delivery_destinations;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_delivery_source;

+#[cfg(feature = "op_describe_delivery_sources")]
 pub(crate) mod shape_delivery_sources;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub(crate) mod shape_destination;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_destination_configuration;

+#[cfg(feature = "op_describe_destinations")]
 pub(crate) mod shape_destinations;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_entity;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_tasks;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_field_indexes;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filtered_log_events;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_import_batch_list;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub(crate) mod shape_import_filter;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_import_list;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub(crate) mod shape_import_statistics;

+#[cfg(feature = "op_describe_index_policies")]
 pub(crate) mod shape_index_policies;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub(crate) mod shape_index_policy;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_input_log_event;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_integration_details;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_integration_summaries;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_fields_list;

+#[cfg(any(
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors"
+))]
 pub(crate) mod shape_log_group_arn_list;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_log_group_field_list;

+#[cfg(feature = "op_list_log_groups_for_query")]
 pub(crate) mod shape_log_group_identifiers;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_log_group_summaries;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_log_groups;

+#[cfg(feature = "op_get_log_record")]
 pub(crate) mod shape_log_record;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_log_streams;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_lookup_tables;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_metric_filter_matches;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_filters;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) mod shape_metric_transformation;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_output_log_events;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub(crate) mod shape_policy;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_processor;

+#[cfg(feature = "op_get_transformer")]
 pub(crate) mod shape_processors;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_query_compile_error;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_definition_list;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_query_info_list;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub(crate) mod shape_query_parameter;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_query_results;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_query_statistics;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_rejected_entity_info;

+#[cfg(feature = "op_put_log_events")]
 pub(crate) mod shape_rejected_log_events_info;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_resource_config;

+#[cfg(feature = "op_describe_resource_policies")]
 pub(crate) mod shape_resource_policies;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub(crate) mod shape_resource_policy;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub(crate) mod shape_s3_delivery_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_s3_table_integration_sources;

+#[cfg(any(feature = "op_get_scheduled_query", feature = "op_update_scheduled_query"))]
 pub(crate) mod shape_scheduled_query_log_group_identifiers;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_scheduled_query_summary_list;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_searched_log_streams;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_subscription_filters;

+#[cfg(feature = "op_update_anomaly")]
 pub(crate) mod shape_suppression_period;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_syslog_configurations;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_tag_filter;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_tags;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_transformed_logs;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_trigger_history_record_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_keys;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_aggregate_log_group_summary;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_anomaly;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub(crate) mod shape_anomaly_detector;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_template;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_csv;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_date_time_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_delete_keys;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_delivery_source_configuration;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task;

+#[cfg(feature = "op_describe_field_indexes")]
 pub(crate) mod shape_field_index;

+#[cfg(feature = "op_get_log_object")]
 pub(crate) mod shape_fields_data;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_filtered_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_grok;

+#[cfg(feature = "op_describe_import_tasks")]
 pub(crate) mod shape_import;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) mod shape_import_batch;

+#[cfg(feature = "op_list_integrations")]
 pub(crate) mod shape_integration_summary;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_list_to_map;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_start;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_update;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_fields_list_item;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_log_group;

+#[cfg(feature = "op_get_log_group_fields")]
 pub(crate) mod shape_log_group_field;

+#[cfg(feature = "op_list_log_groups")]
 pub(crate) mod shape_log_group_summary;

+#[cfg(feature = "op_describe_log_streams")]
 pub(crate) mod shape_log_stream;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_lookup_table;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_lookup_table_configuration;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_lower_case_string;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_filter;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_metric_filter_match_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_keys;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_integration_details;

+#[cfg(feature = "op_put_integration")]
 pub(crate) mod shape_open_search_resource_config;

+#[cfg(feature = "op_get_log_events")]
 pub(crate) mod shape_output_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_cloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_json;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_key_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_postgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_route53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_to_ocsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_vpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_parse_waf;

+#[cfg(feature = "op_start_query")]
 pub(crate) mod shape_query_compile_error_location;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_definition;

+#[cfg(feature = "op_describe_queries")]
 pub(crate) mod shape_query_info;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub(crate) mod shape_record_fields;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_keys;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub(crate) mod shape_resource_arns;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_result_rows;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) mod shape_s3_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub(crate) mod shape_s3_table_integration_source;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub(crate) mod shape_scheduled_query_summary;

+#[cfg(feature = "op_filter_log_events")]
 pub(crate) mod shape_searched_log_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub(crate) mod shape_subscription_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub(crate) mod shape_syslog_configuration;

+#[cfg(feature = "op_test_transformer")]
 pub(crate) mod shape_transformed_log_record;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_trigger_history_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_trim_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_upper_case_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_key_entry;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_allowed_field_delimiters;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_allowed_fields;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_configuration_template_delivery_config_values;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value_entry;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_schemas;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_describe_subscription_filters"))]
 pub(crate) mod shape_emit_system_fields;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task_execution_info;

+#[cfg(feature = "op_describe_export_tasks")]
 pub(crate) mod shape_export_task_status;

+#[cfg(feature = "op_test_metric_filter")]
 pub(crate) mod shape_extracted_values;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_grouping_identifiers;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_histogram;

+#[cfg(feature = "op_describe_log_groups")]
 pub(crate) mod shape_inherited_properties;

+#[cfg(feature = "op_get_log_fields")]
 pub(crate) mod shape_log_field_type;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_log_group_names;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_log_samples;

+#[cfg(feature = "op_describe_metric_filters")]
 pub(crate) mod shape_metric_transformations;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_key_entry;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_application;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_collection;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_data_access_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_data_source;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_encryption_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_lifecycle_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_network_policy;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_workspace;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_output_formats;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_pattern_tokens;

+#[cfg(feature = "op_describe_query_definitions")]
 pub(crate) mod shape_query_parameter_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_key_entry;

+#[cfg(feature = "op_get_query_results")]
 pub(crate) mod shape_result_field;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_s3_tables_integration;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_scheduled_query_destination_list;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string_entry;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub(crate) mod shape_table_fields;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_add_key_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_columns;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_copy_value_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_delete_with_keys;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_schema;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub(crate) mod shape_grouping_identifier;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_input_log_stream_names;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_metadata;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_results;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_lower_case_string_with_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_match_patterns;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_move_key_entries;

+#[cfg(feature = "op_get_integration")]
 pub(crate) mod shape_open_search_resource_status;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_pattern_token;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_record_field;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_rename_key_entries;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub(crate) mod shape_scheduled_query_destination;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_split_string_entries;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_start_live_tail_log_group_identifiers;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_substitute_string_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_trim_string_with_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_type_converter_entries;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) mod shape_upper_case_string_with_keys;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) mod shape_delivery_source_configuration_supported_values;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) mod shape_dimensions;

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) mod shape_enumerations;

+#[cfg(feature = "op_start_live_tail")]
 pub(crate) mod shape_live_tail_session_log_event;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_put_log_events")]
 pub(crate) fn rejected_entity_info_correct_errors(
     mut builder: crate::types::builders::RejectedEntityInfoBuilder,
 ) -> crate::types::builders::RejectedEntityInfoBuilder {
@@ -10,6 +11,7 @@
     builder
 }

+#[cfg(feature = "op_list_anomalies")]
 pub(crate) fn anomaly_correct_errors(
     mut builder: crate::types::builders::AnomalyBuilder,
 ) -> crate::types::builders::AnomalyBuilder {
@@ -55,6 +57,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub(crate) fn delivery_destination_configuration_correct_errors(
     mut builder: crate::types::builders::DeliveryDestinationConfigurationBuilder,
 ) -> crate::types::builders::DeliveryDestinationConfigurationBuilder {
@@ -64,6 +71,7 @@
     builder
 }

+#[cfg(feature = "op_describe_import_task_batches")]
 pub(crate) fn import_batch_correct_errors(
     mut builder: crate::types::builders::ImportBatchBuilder,
 ) -> crate::types::builders::ImportBatchBuilder {
@@ -76,6 +84,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn lookup_table_configuration_correct_errors(
     mut builder: crate::types::builders::LookupTableConfigurationBuilder,
 ) -> crate::types::builders::LookupTableConfigurationBuilder {
@@ -88,6 +102,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub(crate) fn s3_configuration_correct_errors(
     mut builder: crate::types::builders::S3ConfigurationBuilder,
 ) -> crate::types::builders::S3ConfigurationBuilder {
@@ -100,6 +120,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn add_keys_correct_errors(
     mut builder: crate::types::builders::AddKeysBuilder,
 ) -> crate::types::builders::AddKeysBuilder {
@@ -109,6 +134,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn copy_value_correct_errors(
     mut builder: crate::types::builders::CopyValueBuilder,
 ) -> crate::types::builders::CopyValueBuilder {
@@ -118,6 +148,10 @@
     builder
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub(crate) fn data_source_correct_errors(
     mut builder: crate::types::builders::DataSourceBuilder,
 ) -> crate::types::builders::DataSourceBuilder {
@@ -127,6 +161,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn date_time_converter_correct_errors(
     mut builder: crate::types::builders::DateTimeConverterBuilder,
 ) -> crate::types::builders::DateTimeConverterBuilder {
@@ -142,6 +181,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn delete_keys_correct_errors(
     mut builder: crate::types::builders::DeleteKeysBuilder,
 ) -> crate::types::builders::DeleteKeysBuilder {
@@ -151,6 +195,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn grok_correct_errors(
     mut builder: crate::types::builders::GrokBuilder,
 ) -> crate::types::builders::GrokBuilder {
@@ -160,6 +209,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn list_to_map_correct_errors(
     mut builder: crate::types::builders::ListToMapBuilder,
 ) -> crate::types::builders::ListToMapBuilder {
@@ -172,6 +226,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn lower_case_string_correct_errors(
     mut builder: crate::types::builders::LowerCaseStringBuilder,
 ) -> crate::types::builders::LowerCaseStringBuilder {
@@ -181,6 +240,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn move_keys_correct_errors(
     mut builder: crate::types::builders::MoveKeysBuilder,
 ) -> crate::types::builders::MoveKeysBuilder {
@@ -190,6 +254,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn parse_to_ocsf_correct_errors(
     mut builder: crate::types::builders::ParseToOcsfBuilder,
 ) -> crate::types::builders::ParseToOcsfBuilder {
@@ -202,6 +271,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn rename_keys_correct_errors(
     mut builder: crate::types::builders::RenameKeysBuilder,
 ) -> crate::types::builders::RenameKeysBuilder {
@@ -211,6 +285,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn split_string_correct_errors(
     mut builder: crate::types::builders::SplitStringBuilder,
 ) -> crate::types::builders::SplitStringBuilder {
@@ -220,6 +299,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn substitute_string_correct_errors(
     mut builder: crate::types::builders::SubstituteStringBuilder,
 ) -> crate::types::builders::SubstituteStringBuilder {
@@ -229,6 +313,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn trim_string_correct_errors(
     mut builder: crate::types::builders::TrimStringBuilder,
 ) -> crate::types::builders::TrimStringBuilder {
@@ -238,6 +327,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn type_converter_correct_errors(
     mut builder: crate::types::builders::TypeConverterBuilder,
 ) -> crate::types::builders::TypeConverterBuilder {
@@ -247,6 +341,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn upper_case_string_correct_errors(
     mut builder: crate::types::builders::UpperCaseStringBuilder,
 ) -> crate::types::builders::UpperCaseStringBuilder {
@@ -256,6 +355,7 @@
     builder
 }

+#[cfg(feature = "op_describe_configuration_templates")]
 pub(crate) fn delivery_source_configuration_schema_correct_errors(
     mut builder: crate::types::builders::DeliverySourceConfigurationSchemaBuilder,
 ) -> crate::types::builders::DeliverySourceConfigurationSchemaBuilder {
@@ -273,6 +373,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub(crate) fn metric_transformation_correct_errors(
     mut builder: crate::types::builders::MetricTransformationBuilder,
 ) -> crate::types::builders::MetricTransformationBuilder {
@@ -288,6 +389,7 @@
     builder
 }

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub(crate) fn query_parameter_correct_errors(
     mut builder: crate::types::builders::QueryParameterBuilder,
 ) -> crate::types::builders::QueryParameterBuilder {
@@ -297,6 +399,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn add_key_entry_correct_errors(
     mut builder: crate::types::builders::AddKeyEntryBuilder,
 ) -> crate::types::builders::AddKeyEntryBuilder {
@@ -309,6 +416,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn copy_value_entry_correct_errors(
     mut builder: crate::types::builders::CopyValueEntryBuilder,
 ) -> crate::types::builders::CopyValueEntryBuilder {
@@ -321,6 +433,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn move_key_entry_correct_errors(
     mut builder: crate::types::builders::MoveKeyEntryBuilder,
 ) -> crate::types::builders::MoveKeyEntryBuilder {
@@ -333,6 +450,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn rename_key_entry_correct_errors(
     mut builder: crate::types::builders::RenameKeyEntryBuilder,
 ) -> crate::types::builders::RenameKeyEntryBuilder {
@@ -345,6 +467,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn split_string_entry_correct_errors(
     mut builder: crate::types::builders::SplitStringEntryBuilder,
 ) -> crate::types::builders::SplitStringEntryBuilder {
@@ -357,6 +484,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn substitute_string_entry_correct_errors(
     mut builder: crate::types::builders::SubstituteStringEntryBuilder,
 ) -> crate::types::builders::SubstituteStringEntryBuilder {
@@ -372,6 +504,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub(crate) fn type_converter_entry_correct_errors(
     mut builder: crate::types::builders::TypeConverterEntryBuilder,
 ) -> crate::types::builders::TypeConverterEntryBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,654 +1,1486 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub use crate::types::_data_source::DataSource;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_statistics::ImportStatistics;

+#[cfg(any(
+    feature = "op_cancel_import_task",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks"
+))]
 pub use crate::types::_import_status::ImportStatus;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub use crate::types::_s3_delivery_configuration::S3DeliveryConfiguration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub use crate::types::_delivery::Delivery;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_filter::ImportFilter;

+#[cfg(any(
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::_evaluation_frequency::EvaluationFrequency;

+#[cfg(any(
+    feature = "op_create_log_group",
+    feature = "op_describe_log_groups",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_log_groups"
+))]
 pub use crate::types::_log_group_class::LogGroupClass;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_put_query_definition",
+    feature = "op_start_query",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_query_language::QueryLanguage;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_destination_configuration::DestinationConfiguration;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_scheduled_query_state::ScheduledQueryState;

+#[cfg(any(
+    feature = "op_delete_account_policy",
+    feature = "op_describe_account_policies",
+    feature = "op_put_account_policy"
+))]
 pub use crate::types::_policy_type::PolicyType;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status_code::ExportTaskStatusCode;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_order_by::OrderBy;

+#[cfg(any(feature = "op_describe_queries", feature = "op_get_query_results"))]
 pub use crate::types::_query_status::QueryStatus;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_policy_scope::PolicyScope;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination::DeliveryDestination;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub use crate::types::_policy::Policy;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source::DeliverySource;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 pub use crate::types::_integration_type::IntegrationType;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 pub use crate::types::_integration_status::IntegrationStatus;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_integration_details::IntegrationDetails;

+#[cfg(any(feature = "op_get_log_anomaly_detector", feature = "op_list_log_anomaly_detectors"))]
 pub use crate::types::_anomaly_detector_status::AnomalyDetectorStatus;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_get_log_object_response_stream::GetLogObjectResponseStream;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_query_statistics::QueryStatistics;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_schedule_type::ScheduleType;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_execution_status::ExecutionStatus;

+#[cfg(any(feature = "op_get_storage_tier_policy", feature = "op_put_storage_tier_policy"))]
 pub use crate::types::_storage_tier::StorageTier;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_list_aggregate_log_group_summaries_group_by::ListAggregateLogGroupSummariesGroupBy;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_suppression_state::SuppressionState;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_scope::Scope;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_account_policy::AccountPolicy;

+#[cfg(any(
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_output_format::OutputFormat;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_configuration::DeliveryDestinationConfiguration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_type::DeliveryDestinationType;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub use crate::types::_destination::Destination;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_policy::IndexPolicy;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_resource_config::ResourceConfig;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity::Entity;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_log_events_info::RejectedLogEventsInfo;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_entity_info::RejectedEntityInfo;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_resource_policy::ResourcePolicy;

+#[cfg(any(feature = "op_describe_subscription_filters", feature = "op_put_subscription_filter"))]
 pub use crate::types::_distribution::Distribution;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_start_live_tail_response_stream::StartLiveTailResponseStream;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error::QueryCompileError;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_type::SuppressionType;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_period::SuppressionPeriod;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_s3_configuration::S3Configuration;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_lookup_table_configuration::LookupTableConfiguration;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template::ConfigurationTemplate;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task::ExportTask;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_index_category::IndexCategory;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_field_index::FieldIndex;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub use crate::types::_import_batch::ImportBatch;

+#[cfg(feature = "op_describe_import_tasks")]
 pub use crate::types::_import::Import;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_log_group::LogGroup;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_log_stream::LogStream;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub use crate::types::_lookup_table::LookupTable;

+#[cfg(feature = "op_describe_metric_filters")]
 pub use crate::types::_metric_filter::MetricFilter;

+#[cfg(feature = "op_describe_queries")]
 pub use crate::types::_query_info::QueryInfo;

+#[cfg(feature = "op_describe_query_definitions")]
 pub use crate::types::_query_definition::QueryDefinition;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub use crate::types::_subscription_filter::SubscriptionFilter;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_filtered_log_event::FilteredLogEvent;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_searched_log_stream::SearchedLogStream;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source_status::DeliverySourceStatus;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source_status_reason::DeliverySourceStatusReason;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_integration_details::OpenSearchIntegrationDetails;

+#[cfg(feature = "op_get_log_events")]
 pub use crate::types::_output_log_event::OutputLogEvent;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_fields_list_item::LogFieldsListItem;

+#[cfg(feature = "op_get_log_group_fields")]
 pub use crate::types::_log_group_field::LogGroupField;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_fields_data::FieldsData;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_trigger_history_record::TriggerHistoryRecord;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_processor::Processor;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub use crate::types::_data_source_filter::DataSourceFilter;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_aggregate_log_group_summary::AggregateLogGroupSummary;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_anomaly::Anomaly;

+#[cfg(feature = "op_list_integrations")]
 pub use crate::types::_integration_summary::IntegrationSummary;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub use crate::types::_anomaly_detector::AnomalyDetector;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_tag_filter::TagFilter;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_log_group_summary::LogGroupSummary;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub use crate::types::_scheduled_query_summary::ScheduledQuerySummary;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source::S3TableIntegrationSource;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_configuration::SyslogConfiguration;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_source::IndexSource;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_open_search_resource_config::OpenSearchResourceConfig;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_input_log_event::InputLogEvent;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity_rejection_error_type::EntityRejectionErrorType;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_metric_transformation::MetricTransformation;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub use crate::types::_query_parameter::QueryParameter;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_start::LiveTailSessionStart;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_update::LiveTailSessionUpdate;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error_location::QueryCompileErrorLocation;

+#[cfg(feature = "op_test_metric_filter")]
 pub use crate::types::_metric_filter_match_record::MetricFilterMatchRecord;

+#[cfg(feature = "op_test_transformer")]
 pub use crate::types::_transformed_log_record::TransformedLogRecord;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_unit::SuppressionUnit;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template_delivery_config_values::ConfigurationTemplateDeliveryConfigValues;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_s3_tables_integration::S3TablesIntegration;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status::ExportTaskStatus;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_execution_info::ExportTaskExecutionInfo;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_index_type::IndexType;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_data_protection_status::DataProtectionStatus;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_source::OpenSearchDataSource;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_application::OpenSearchApplication;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_collection::OpenSearchCollection;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_workspace::OpenSearchWorkspace;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_encryption_policy::OpenSearchEncryptionPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_network_policy::OpenSearchNetworkPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_access_policy::OpenSearchDataAccessPolicy;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_lifecycle_policy::OpenSearchLifecyclePolicy;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_field_type::LogFieldType;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_result_field::ResultField;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_keys::AddKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value::CopyValue;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_csv::Csv;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_date_time_converter::DateTimeConverter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_delete_keys::DeleteKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_grok::Grok;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_list_to_map::ListToMap;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_lower_case_string::LowerCaseString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_keys::MoveKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_cloudfront::ParseCloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_json::ParseJson;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_key_value::ParseKeyValue;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_route53::ParseRoute53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_to_ocsf::ParseToOcsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_postgres::ParsePostgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_vpc::ParseVpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_waf::ParseWaf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_keys::RenameKeys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string::SplitString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string::SubstituteString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_trim_string::TrimString;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter::TypeConverter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_upper_case_string::UpperCaseString;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_state::State;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source_status::S3TableIntegrationSourceStatus;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_source_type::SyslogSourceType;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_standard_unit::StandardUnit;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_metadata::LiveTailSessionMetadata;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_record_field::RecordField;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema::DeliverySourceConfigurationSchema;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_inherited_property::InheritedProperty;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status::OpenSearchResourceStatus;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination::ScheduledQueryDestination;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_flattened_element::FlattenedElement;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_event_source::EventSource;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_ocsf_version::OcsfVersion;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_grouping_identifier::GroupingIdentifier;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_log_event::LogEvent;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_pattern_token::PatternToken;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_log_event::LiveTailSessionLogEvent;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema_value_type::DeliverySourceConfigurationSchemaValueType;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status_type::OpenSearchResourceStatusType;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination_type::ScheduledQueryDestinationType;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_action_status::ActionStatus;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_key_entry::AddKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value_entry::CopyValueEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_key_entry::MoveKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_key_entry::RenameKeyEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string_entry::SplitStringEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string_entry::SubstituteStringEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter_entry::TypeConverterEntry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_::Type;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 mod _account_policy;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _action_status;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _add_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _add_keys;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _aggregate_log_group_summary;

+#[cfg(feature = "op_list_anomalies")]
 mod _anomaly;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 mod _anomaly_detector;

+#[cfg(any(feature = "op_get_log_anomaly_detector", feature = "op_list_log_anomaly_detectors"))]
 mod _anomaly_detector_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _configuration_template;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _configuration_template_delivery_config_values;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _copy_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _copy_value_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _csv;

+#[cfg(feature = "op_describe_log_groups")]
 mod _data_protection_status;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 mod _data_source;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 mod _data_source_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _date_time_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _delete_keys;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 mod _delivery;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination_configuration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _delivery_destination_type;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _delivery_source_configuration_schema;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _delivery_source_configuration_schema_value_type;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source_status;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 mod _delivery_source_status_reason;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 mod _destination;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _destination_configuration;

+#[cfg(any(feature = "op_describe_subscription_filters", feature = "op_put_subscription_filter"))]
 mod _distribution;

+#[cfg(feature = "op_put_log_events")]
 mod _entity;

+#[cfg(feature = "op_put_log_events")]
 mod _entity_rejection_error_type;

+#[cfg(any(
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_update_log_anomaly_detector"
+))]
 mod _evaluation_frequency;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _event_source;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _execution_status;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_execution_info;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_status;

+#[cfg(feature = "op_describe_export_tasks")]
 mod _export_task_status_code;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _field_index;

+#[cfg(feature = "op_get_log_object")]
 mod _fields_data;

+#[cfg(feature = "op_filter_log_events")]
 mod _filtered_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _flattened_element;

+#[cfg(feature = "op_get_log_object")]
 mod _get_log_object_response_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _grok;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _grouping_identifier;

+#[cfg(feature = "op_describe_import_tasks")]
 mod _import;

+#[cfg(feature = "op_describe_import_task_batches")]
 mod _import_batch;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 mod _import_filter;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 mod _import_statistics;

+#[cfg(any(
+    feature = "op_cancel_import_task",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks"
+))]
 mod _import_status;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _index_category;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 mod _index_policy;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 mod _index_source;

+#[cfg(feature = "op_describe_field_indexes")]
 mod _index_type;

+#[cfg(feature = "op_describe_log_groups")]
 mod _inherited_property;

+#[cfg(feature = "op_put_log_events")]
 mod _input_log_event;

+#[cfg(feature = "op_get_integration")]
 mod _integration_details;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 mod _integration_status;

+#[cfg(feature = "op_list_integrations")]
 mod _integration_summary;

+#[cfg(any(
+    feature = "op_get_integration",
+    feature = "op_list_integrations",
+    feature = "op_put_integration"
+))]
 mod _integration_type;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 mod _list_aggregate_log_group_summaries_group_by;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _list_to_map;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_log_event;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_metadata;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_start;

+#[cfg(feature = "op_start_live_tail")]
 mod _live_tail_session_update;

+#[cfg(feature = "op_list_anomalies")]
 mod _log_event;

+#[cfg(feature = "op_get_log_fields")]
 mod _log_field_type;

+#[cfg(feature = "op_get_log_fields")]
 mod _log_fields_list_item;

+#[cfg(feature = "op_describe_log_groups")]
 mod _log_group;

+#[cfg(any(
+    feature = "op_create_log_group",
+    feature = "op_describe_log_groups",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_log_groups"
+))]
 mod _log_group_class;

+#[cfg(feature = "op_get_log_group_fields")]
 mod _log_group_field;

+#[cfg(feature = "op_list_log_groups")]
 mod _log_group_summary;

+#[cfg(feature = "op_describe_log_streams")]
 mod _log_stream;

+#[cfg(feature = "op_describe_lookup_tables")]
 mod _lookup_table;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _lookup_table_configuration;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _lower_case_string;

+#[cfg(feature = "op_describe_metric_filters")]
 mod _metric_filter;

+#[cfg(feature = "op_test_metric_filter")]
 mod _metric_filter_match_record;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 mod _metric_transformation;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _move_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _move_keys;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _ocsf_version;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_application;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_collection;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_data_access_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_data_source;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_encryption_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_integration_details;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_lifecycle_policy;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_network_policy;

+#[cfg(feature = "op_put_integration")]
 mod _open_search_resource_config;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_resource_status;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_resource_status_type;

+#[cfg(feature = "op_get_integration")]
 mod _open_search_workspace;

+#[cfg(feature = "op_describe_log_streams")]
 mod _order_by;

+#[cfg(any(
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 mod _output_format;

+#[cfg(feature = "op_get_log_events")]
 mod _output_log_event;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_cloudfront;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_json;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_key_value;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_postgres;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_route53;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_to_ocsf;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_vpc;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _parse_waf;

+#[cfg(feature = "op_list_anomalies")]
 mod _pattern_token;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 mod _policy;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 mod _policy_scope;

+#[cfg(any(
+    feature = "op_delete_account_policy",
+    feature = "op_describe_account_policies",
+    feature = "op_put_account_policy"
+))]
 mod _policy_type;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _processor;

+#[cfg(feature = "op_start_query")]
 mod _query_compile_error;

+#[cfg(feature = "op_start_query")]
 mod _query_compile_error_location;

+#[cfg(feature = "op_describe_query_definitions")]
 mod _query_definition;

+#[cfg(feature = "op_describe_queries")]
 mod _query_info;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_put_query_definition",
+    feature = "op_start_query",
+    feature = "op_update_scheduled_query"
+))]
 mod _query_language;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 mod _query_parameter;

+#[cfg(feature = "op_get_query_results")]
 mod _query_statistics;

+#[cfg(any(feature = "op_describe_queries", feature = "op_get_query_results"))]
 mod _query_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _record_field;

+#[cfg(feature = "op_put_log_events")]
 mod _rejected_entity_info;

+#[cfg(feature = "op_put_log_events")]
 mod _rejected_log_events_info;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _rename_key_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _rename_keys;

+#[cfg(feature = "op_put_integration")]
 mod _resource_config;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 mod _resource_policy;

+#[cfg(feature = "op_get_query_results")]
 mod _result_field;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _s3_configuration;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 mod _s3_delivery_configuration;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod _s3_table_integration_source;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 mod _s3_table_integration_source_status;

+#[cfg(feature = "op_describe_configuration_templates")]
 mod _s3_tables_integration;

+#[cfg(any(
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _schedule_type;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _scheduled_query_destination;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _scheduled_query_destination_type;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 mod _scheduled_query_state;

+#[cfg(feature = "op_list_scheduled_queries")]
 mod _scheduled_query_summary;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 mod _scope;

+#[cfg(feature = "op_filter_log_events")]
 mod _searched_log_stream;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _split_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _split_string_entry;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 mod _standard_unit;

+#[cfg(feature = "op_start_live_tail")]
 mod _start_live_tail_response_stream;

+#[cfg(feature = "op_list_anomalies")]
 mod _state;

+#[cfg(any(feature = "op_get_storage_tier_policy", feature = "op_put_storage_tier_policy"))]
 mod _storage_tier;

+#[cfg(feature = "op_describe_subscription_filters")]
 mod _subscription_filter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _substitute_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _substitute_string_entry;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_period;

+#[cfg(feature = "op_list_anomalies")]
 mod _suppression_state;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_type;

+#[cfg(feature = "op_update_anomaly")]
 mod _suppression_unit;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod _syslog_configuration;

+#[cfg(feature = "op_list_syslog_configurations")]
 mod _syslog_source_type;

+#[cfg(feature = "op_list_log_groups")]
 mod _tag_filter;

+#[cfg(feature = "op_test_transformer")]
 mod _transformed_log_record;

+#[cfg(feature = "op_get_scheduled_query_history")]
 mod _trigger_history_record;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _trim_string;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_converter;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _type_converter_entry;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 mod _upper_case_string;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,230 +1,512 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_list_sources_for_s3_table_integration"
+))]
 pub use crate::types::_data_source::DataSourceBuilder;

+#[cfg(any(feature = "op_cancel_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_statistics::ImportStatisticsBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery",
+    feature = "op_update_delivery_configuration"
+))]
 pub use crate::types::_s3_delivery_configuration::S3DeliveryConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_describe_deliveries",
+    feature = "op_get_delivery"
+))]
 pub use crate::types::_delivery::DeliveryBuilder;

+#[cfg(any(feature = "op_create_import_task", feature = "op_describe_import_tasks"))]
 pub use crate::types::_import_filter::ImportFilterBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_destination_configuration::DestinationConfigurationBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination::DeliveryDestinationBuilder;

+#[cfg(any(
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_put_delivery_destination_policy"
+))]
 pub use crate::types::_policy::PolicyBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::_delivery_source::DeliverySourceBuilder;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_query_statistics::QueryStatisticsBuilder;

+#[cfg(any(feature = "op_describe_account_policies", feature = "op_put_account_policy"))]
 pub use crate::types::_account_policy::AccountPolicyBuilder;

+#[cfg(any(
+    feature = "op_describe_delivery_destinations",
+    feature = "op_get_delivery_destination",
+    feature = "op_put_delivery_destination"
+))]
 pub use crate::types::_delivery_destination_configuration::DeliveryDestinationConfigurationBuilder;

+#[cfg(any(feature = "op_describe_destinations", feature = "op_put_destination"))]
 pub use crate::types::_destination::DestinationBuilder;

+#[cfg(any(feature = "op_describe_index_policies", feature = "op_put_index_policy"))]
 pub use crate::types::_index_policy::IndexPolicyBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_entity::EntityBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_log_events_info::RejectedLogEventsInfoBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_rejected_entity_info::RejectedEntityInfoBuilder;

+#[cfg(any(feature = "op_describe_resource_policies", feature = "op_put_resource_policy"))]
 pub use crate::types::_resource_policy::ResourcePolicyBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error::QueryCompileErrorBuilder;

+#[cfg(feature = "op_update_anomaly")]
 pub use crate::types::_suppression_period::SuppressionPeriodBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_s3_configuration::S3ConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_scheduled_query",
+    feature = "op_get_scheduled_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::_lookup_table_configuration::LookupTableConfigurationBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template::ConfigurationTemplateBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task::ExportTaskBuilder;

+#[cfg(feature = "op_describe_field_indexes")]
 pub use crate::types::_field_index::FieldIndexBuilder;

+#[cfg(feature = "op_describe_import_task_batches")]
 pub use crate::types::_import_batch::ImportBatchBuilder;

+#[cfg(feature = "op_describe_import_tasks")]
 pub use crate::types::_import::ImportBuilder;

+#[cfg(feature = "op_describe_log_groups")]
 pub use crate::types::_log_group::LogGroupBuilder;

+#[cfg(feature = "op_describe_log_streams")]
 pub use crate::types::_log_stream::LogStreamBuilder;

+#[cfg(feature = "op_describe_lookup_tables")]
 pub use crate::types::_lookup_table::LookupTableBuilder;

+#[cfg(feature = "op_describe_metric_filters")]
 pub use crate::types::_metric_filter::MetricFilterBuilder;

+#[cfg(feature = "op_describe_queries")]
 pub use crate::types::_query_info::QueryInfoBuilder;

+#[cfg(feature = "op_describe_query_definitions")]
 pub use crate::types::_query_definition::QueryDefinitionBuilder;

+#[cfg(feature = "op_describe_subscription_filters")]
 pub use crate::types::_subscription_filter::SubscriptionFilterBuilder;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_filtered_log_event::FilteredLogEventBuilder;

+#[cfg(feature = "op_filter_log_events")]
 pub use crate::types::_searched_log_stream::SearchedLogStreamBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_integration_details::OpenSearchIntegrationDetailsBuilder;

+#[cfg(feature = "op_get_log_events")]
 pub use crate::types::_output_log_event::OutputLogEventBuilder;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_fields_list_item::LogFieldsListItemBuilder;

+#[cfg(feature = "op_get_log_group_fields")]
 pub use crate::types::_log_group_field::LogGroupFieldBuilder;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::_fields_data::FieldsDataBuilder;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_trigger_history_record::TriggerHistoryRecordBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_processor::ProcessorBuilder;

+#[cfg(any(feature = "op_list_aggregate_log_group_summaries", feature = "op_list_log_groups"))]
 pub use crate::types::_data_source_filter::DataSourceFilterBuilder;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_aggregate_log_group_summary::AggregateLogGroupSummaryBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_anomaly::AnomalyBuilder;

+#[cfg(feature = "op_list_integrations")]
 pub use crate::types::_integration_summary::IntegrationSummaryBuilder;

+#[cfg(feature = "op_list_log_anomaly_detectors")]
 pub use crate::types::_anomaly_detector::AnomalyDetectorBuilder;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_tag_filter::TagFilterBuilder;

+#[cfg(feature = "op_list_log_groups")]
 pub use crate::types::_log_group_summary::LogGroupSummaryBuilder;

+#[cfg(feature = "op_list_scheduled_queries")]
 pub use crate::types::_scheduled_query_summary::ScheduledQuerySummaryBuilder;

+#[cfg(feature = "op_list_sources_for_s3_table_integration")]
 pub use crate::types::_s3_table_integration_source::S3TableIntegrationSourceBuilder;

+#[cfg(feature = "op_list_syslog_configurations")]
 pub use crate::types::_syslog_configuration::SyslogConfigurationBuilder;

+#[cfg(feature = "op_put_integration")]
 pub use crate::types::_open_search_resource_config::OpenSearchResourceConfigBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::_input_log_event::InputLogEventBuilder;

+#[cfg(any(feature = "op_describe_metric_filters", feature = "op_put_metric_filter"))]
 pub use crate::types::_metric_transformation::MetricTransformationBuilder;

+#[cfg(any(feature = "op_describe_query_definitions", feature = "op_put_query_definition"))]
 pub use crate::types::_query_parameter::QueryParameterBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_start::LiveTailSessionStartBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_update::LiveTailSessionUpdateBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::_query_compile_error_location::QueryCompileErrorLocationBuilder;

+#[cfg(feature = "op_test_metric_filter")]
 pub use crate::types::_metric_filter_match_record::MetricFilterMatchRecordBuilder;

+#[cfg(feature = "op_test_transformer")]
 pub use crate::types::_transformed_log_record::TransformedLogRecordBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_configuration_template_delivery_config_values::ConfigurationTemplateDeliveryConfigValuesBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_s3_tables_integration::S3TablesIntegrationBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_status::ExportTaskStatusBuilder;

+#[cfg(feature = "op_describe_export_tasks")]
 pub use crate::types::_export_task_execution_info::ExportTaskExecutionInfoBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_source::OpenSearchDataSourceBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_application::OpenSearchApplicationBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_collection::OpenSearchCollectionBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_workspace::OpenSearchWorkspaceBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_encryption_policy::OpenSearchEncryptionPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_network_policy::OpenSearchNetworkPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_data_access_policy::OpenSearchDataAccessPolicyBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_lifecycle_policy::OpenSearchLifecyclePolicyBuilder;

+#[cfg(feature = "op_get_log_fields")]
 pub use crate::types::_log_field_type::LogFieldTypeBuilder;

+#[cfg(feature = "op_get_query_results")]
 pub use crate::types::_result_field::ResultFieldBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_keys::AddKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value::CopyValueBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_csv::CsvBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_date_time_converter::DateTimeConverterBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_delete_keys::DeleteKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_grok::GrokBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_list_to_map::ListToMapBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_lower_case_string::LowerCaseStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_keys::MoveKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_cloudfront::ParseCloudfrontBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_json::ParseJsonBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_key_value::ParseKeyValueBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_route53::ParseRoute53Builder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_to_ocsf::ParseToOcsfBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_postgres::ParsePostgresBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_vpc::ParseVpcBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_parse_waf::ParseWafBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_keys::RenameKeysBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string::SplitStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string::SubstituteStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_trim_string::TrimStringBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter::TypeConverterBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_upper_case_string::UpperCaseStringBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_metadata::LiveTailSessionMetadataBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_record_field::RecordFieldBuilder;

+#[cfg(feature = "op_describe_configuration_templates")]
 pub use crate::types::_delivery_source_configuration_schema::DeliverySourceConfigurationSchemaBuilder;

+#[cfg(feature = "op_get_integration")]
 pub use crate::types::_open_search_resource_status::OpenSearchResourceStatusBuilder;

+#[cfg(feature = "op_get_scheduled_query_history")]
 pub use crate::types::_scheduled_query_destination::ScheduledQueryDestinationBuilder;

+#[cfg(feature = "op_list_aggregate_log_group_summaries")]
 pub use crate::types::_grouping_identifier::GroupingIdentifierBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_log_event::LogEventBuilder;

+#[cfg(feature = "op_list_anomalies")]
 pub use crate::types::_pattern_token::PatternTokenBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::_live_tail_session_log_event::LiveTailSessionLogEventBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_add_key_entry::AddKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_copy_value_entry::CopyValueEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_move_key_entry::MoveKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_rename_key_entry::RenameKeyEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_split_string_entry::SplitStringEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_substitute_string_entry::SubstituteStringEntryBuilder;

+#[cfg(any(
+    feature = "op_get_transformer",
+    feature = "op_put_transformer",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::_type_converter_entry::TypeConverterEntryBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,46 +1,584 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::error::_operation_aborted_exception::OperationAbortedException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundException;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingException;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_validation_exception::ValidationException;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::error::_invalid_operation_exception::InvalidOperationException;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededException;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub use crate::types::error::_resource_already_exists_exception::ResourceAlreadyExistsException;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::error::_internal_streaming_exception::InternalStreamingException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_data_already_accepted_exception::DataAlreadyAcceptedException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_invalid_sequence_token_exception::InvalidSequenceTokenException;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_unrecognized_client_exception::UnrecognizedClientException;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_timeout_exception::SessionTimeoutException;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_streaming_exception::SessionStreamingException;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::error::_malformed_query_exception::MalformedQueryException;

+#[cfg(feature = "op_tag_resource")]
 pub use crate::types::error::_too_many_tags_exception::TooManyTagsException;

+#[cfg(feature = "op_get_log_object")]
 /// Error type for the `GetLogObjectResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -58,6 +596,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_get_log_object")]
 impl GetLogObjectResponseStreamError {
     /// Creates the `GetLogObjectResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -93,6 +632,7 @@
         matches!(self, Self::InternalStreamingException(_))
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::std::error::Error for GetLogObjectResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -101,6 +641,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::std::fmt::Display for GetLogObjectResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -117,6 +658,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for GetLogObjectResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -125,6 +667,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for GetLogObjectResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -135,6 +678,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for GetLogObjectResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -146,6 +690,7 @@
         })
     }
 }
+#[cfg(feature = "op_get_log_object")]
 impl ::aws_types::request_id::RequestId for crate::types::error::GetLogObjectResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -152,6 +697,7 @@
     }
 }

+#[cfg(feature = "op_start_live_tail")]
 /// Error type for the `StartLiveTailResponseStreamError` operation.
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
@@ -171,6 +717,7 @@
     )]
     Unhandled(crate::error::sealed_unhandled::Unhandled),
 }
+#[cfg(feature = "op_start_live_tail")]
 impl StartLiveTailResponseStreamError {
     /// Creates the `StartLiveTailResponseStreamError::Unhandled` variant from any error type.
     pub fn unhandled(
@@ -211,6 +758,7 @@
         matches!(self, Self::SessionStreamingException(_))
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::std::error::Error for StartLiveTailResponseStreamError {
     fn source(&self) -> ::std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
@@ -220,6 +768,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::std::fmt::Display for StartLiveTailResponseStreamError {
     fn fmt(&self, f: &mut ::std::fmt::Formatter<'_>) -> ::std::fmt::Result {
         match self {
@@ -237,6 +786,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_types::retry::ProvideErrorKind for StartLiveTailResponseStreamError {
     fn code(&self) -> ::std::option::Option<&str> {
         ::aws_smithy_types::error::metadata::ProvideErrorMetadata::code(self)
@@ -245,6 +795,7 @@
         ::std::option::Option::None
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for StartLiveTailResponseStreamError {
     fn meta(&self) -> &::aws_smithy_types::error::ErrorMetadata {
         match self {
@@ -258,6 +809,7 @@
         }
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_smithy_runtime_api::client::result::CreateUnhandledError for StartLiveTailResponseStreamError {
     fn create_unhandled_error(
         source: ::std::boxed::Box<dyn ::std::error::Error + ::std::marker::Send + ::std::marker::Sync + 'static>,
@@ -269,6 +821,7 @@
         })
     }
 }
+#[cfg(feature = "op_start_live_tail")]
 impl ::aws_types::request_id::RequestId for crate::types::error::StartLiveTailResponseStreamError {
     fn request_id(&self) -> Option<&str> {
         self.meta().request_id()
@@ -275,46 +828,583 @@
     }
 }

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _access_denied_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 mod _conflict_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _data_already_accepted_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 mod _internal_server_exception;

+#[cfg(feature = "op_get_log_object")]
 mod _internal_streaming_exception;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 mod _invalid_operation_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 mod _invalid_parameter_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _invalid_sequence_token_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 mod _limit_exceeded_exception;

+#[cfg(feature = "op_start_query")]
 mod _malformed_query_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 mod _operation_aborted_exception;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 mod _resource_already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _resource_not_found_exception;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 mod _service_quota_exceeded_exception;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 mod _service_unavailable_exception;

+#[cfg(feature = "op_start_live_tail")]
 mod _session_streaming_exception;

+#[cfg(feature = "op_start_live_tail")]
 mod _session_timeout_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 mod _throttling_exception;

+#[cfg(feature = "op_tag_resource")]
 mod _too_many_tags_exception;

+#[cfg(feature = "op_put_log_events")]
 mod _unrecognized_client_exception;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 mod _validation_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,42 +1,579 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_invalid_parameter_exception::InvalidParameterExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_disassociate_kms_key",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_fields",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_update_anomaly",
+    feature = "op_update_log_anomaly_detector"
+))]
 pub use crate::types::error::_operation_aborted_exception::OperationAbortedExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_import_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_stream",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_anomalies",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_index_policy",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_log_group",
+    feature = "op_tag_resource",
+    feature = "op_untag_log_group",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_resource_not_found_exception::ResourceNotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_kms_key",
+    feature = "op_cancel_export_task",
+    feature = "op_create_delivery",
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_account_policy",
+    feature = "op_delete_data_protection_policy",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_destination",
+    feature = "op_delete_index_policy",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_anomaly_detector",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_metric_filter",
+    feature = "op_delete_query_definition",
+    feature = "op_delete_resource_policy",
+    feature = "op_delete_retention_policy",
+    feature = "op_delete_subscription_filter",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_account_policies",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_destinations",
+    feature = "op_describe_export_tasks",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_describe_log_groups",
+    feature = "op_describe_log_streams",
+    feature = "op_describe_lookup_tables",
+    feature = "op_describe_metric_filters",
+    feature = "op_describe_queries",
+    feature = "op_describe_query_definitions",
+    feature = "op_describe_resource_policies",
+    feature = "op_describe_subscription_filters",
+    feature = "op_disassociate_kms_key",
+    feature = "op_filter_log_events",
+    feature = "op_get_data_protection_policy",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_integration",
+    feature = "op_get_log_anomaly_detector",
+    feature = "op_get_log_events",
+    feature = "op_get_log_fields",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_record",
+    feature = "op_get_lookup_table",
+    feature = "op_get_query_results",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_get_transformer",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_anomalies",
+    feature = "op_list_integrations",
+    feature = "op_list_log_anomaly_detectors",
+    feature = "op_list_log_groups",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_syslog_configurations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tags_log_group",
+    feature = "op_put_account_policy",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_destination",
+    feature = "op_put_destination_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_log_events",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_retention_policy",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_query",
+    feature = "op_stop_query",
+    feature = "op_tag_resource",
+    feature = "op_test_metric_filter",
+    feature = "op_test_transformer",
+    feature = "op_untag_resource",
+    feature = "op_update_anomaly",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_log_anomaly_detector",
+    feature = "op_update_lookup_table"
+))]
 pub use crate::types::error::_service_unavailable_exception::ServiceUnavailableExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_lookup_table",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_describe_lookup_tables",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_log_object",
+    feature = "op_get_lookup_table",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_get_storage_tier_policy",
+    feature = "op_list_log_groups_for_query",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_storage_tier_policy",
+    feature = "op_put_syslog_configuration",
+    feature = "op_start_live_tail",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_access_denied_exception::AccessDeniedExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_scheduled_query",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_internal_server_exception::InternalServerExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_cancel_import_task",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_scheduled_query",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source",
+    feature = "op_put_syslog_configuration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_throttling_exception::ThrottlingExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_source_to_s3_table_integration",
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_lookup_table",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_delete_integration",
+    feature = "op_delete_log_group",
+    feature = "op_delete_log_stream",
+    feature = "op_delete_scheduled_query",
+    feature = "op_describe_configuration_templates",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_disassociate_source_from_s3_table_integration",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_destination_policy",
+    feature = "op_get_delivery_source",
+    feature = "op_get_scheduled_query",
+    feature = "op_get_scheduled_query_history",
+    feature = "op_list_aggregate_log_group_summaries",
+    feature = "op_list_scheduled_queries",
+    feature = "op_list_sources_for_s3_table_integration",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_put_integration",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_lookup_table",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_validation_exception::ValidationExceptionBuilder;

+#[cfg(any(
+    feature = "op_cancel_export_task",
+    feature = "op_cancel_import_task",
+    feature = "op_create_import_task",
+    feature = "op_delete_syslog_configuration",
+    feature = "op_delete_transformer",
+    feature = "op_describe_import_task_batches",
+    feature = "op_describe_import_tasks",
+    feature = "op_get_log_object",
+    feature = "op_get_transformer",
+    feature = "op_list_syslog_configurations",
+    feature = "op_put_bearer_token_authentication",
+    feature = "op_put_log_group_deletion_protection",
+    feature = "op_put_metric_filter",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_syslog_configuration",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_test_transformer"
+))]
 pub use crate::types::error::_invalid_operation_exception::InvalidOperationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_import_task",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_destination_policy",
+    feature = "op_delete_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_destination_policy",
+    feature = "op_put_delivery_source",
+    feature = "op_update_delivery_configuration",
+    feature = "op_update_scheduled_query"
+))]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_delivery",
+    feature = "op_create_scheduled_query",
+    feature = "op_delete_delivery",
+    feature = "op_delete_delivery_destination",
+    feature = "op_delete_delivery_source",
+    feature = "op_describe_deliveries",
+    feature = "op_describe_delivery_destinations",
+    feature = "op_describe_delivery_sources",
+    feature = "op_get_delivery",
+    feature = "op_get_delivery_destination",
+    feature = "op_get_delivery_source",
+    feature = "op_put_delivery_destination",
+    feature = "op_put_delivery_source"
+))]
 pub use crate::types::error::_service_quota_exceeded_exception::ServiceQuotaExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_anomaly_detector",
+    feature = "op_create_log_group",
+    feature = "op_create_lookup_table",
+    feature = "op_delete_index_policy",
+    feature = "op_describe_field_indexes",
+    feature = "op_describe_index_policies",
+    feature = "op_get_log_group_fields",
+    feature = "op_get_log_object",
+    feature = "op_get_log_record",
+    feature = "op_put_account_policy",
+    feature = "op_put_data_protection_policy",
+    feature = "op_put_index_policy",
+    feature = "op_put_integration",
+    feature = "op_put_metric_filter",
+    feature = "op_put_query_definition",
+    feature = "op_put_resource_policy",
+    feature = "op_put_subscription_filter",
+    feature = "op_put_transformer",
+    feature = "op_start_live_tail",
+    feature = "op_start_query"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_export_task",
+    feature = "op_create_log_group",
+    feature = "op_create_log_stream",
+    feature = "op_create_lookup_table"
+))]
 pub use crate::types::error::_resource_already_exists_exception::ResourceAlreadyExistsExceptionBuilder;

+#[cfg(feature = "op_get_log_object")]
 pub use crate::types::error::_internal_streaming_exception::InternalStreamingExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_data_already_accepted_exception::DataAlreadyAcceptedExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_invalid_sequence_token_exception::InvalidSequenceTokenExceptionBuilder;

+#[cfg(feature = "op_put_log_events")]
 pub use crate::types::error::_unrecognized_client_exception::UnrecognizedClientExceptionBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_timeout_exception::SessionTimeoutExceptionBuilder;

+#[cfg(feature = "op_start_live_tail")]
 pub use crate::types::error::_session_streaming_exception::SessionStreamingExceptionBuilder;

+#[cfg(feature = "op_start_query")]
 pub use crate::types::error::_malformed_query_exception::MalformedQueryExceptionBuilder;

+#[cfg(feature = "op_tag_resource")]
 pub use crate::types::error::_too_many_tags_exception::TooManyTagsExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
