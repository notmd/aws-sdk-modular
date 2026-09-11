# AWS SDK modularizer diff

- repository: `https://github.com/awslabs/aws-sdk-rust`
- revision: `26155f26ed36d90263a2c9058a67b08543c96f85`
- service: `sdk/sesv2`
- model: `aws-models/sesv2.json`
- package: `aws-sdk-sesv2`
- library: `aws_sdk_sesv2`
- tests exclusion: `tests/**` is excluded from the comparison.

## Operations

- `op_associate_email_identity_certificate`: `AssociateEmailIdentityCertificate`
- `op_batch_get_metric_data`: `BatchGetMetricData`
- `op_cancel_export_job`: `CancelExportJob`
- `op_create_configuration_set`: `CreateConfigurationSet`
- `op_create_configuration_set_event_destination`: `CreateConfigurationSetEventDestination`
- `op_create_contact`: `CreateContact`
- `op_create_contact_list`: `CreateContactList`
- `op_create_custom_verification_email_template`: `CreateCustomVerificationEmailTemplate`
- `op_create_dedicated_ip_pool`: `CreateDedicatedIpPool`
- `op_create_deliverability_test_report`: `CreateDeliverabilityTestReport`
- `op_create_email_identity`: `CreateEmailIdentity`
- `op_create_email_identity_policy`: `CreateEmailIdentityPolicy`
- `op_create_email_template`: `CreateEmailTemplate`
- `op_create_export_job`: `CreateExportJob`
- `op_create_import_job`: `CreateImportJob`
- `op_create_multi_region_endpoint`: `CreateMultiRegionEndpoint`
- `op_create_tenant`: `CreateTenant`
- `op_create_tenant_resource_association`: `CreateTenantResourceAssociation`
- `op_delete_configuration_set`: `DeleteConfigurationSet`
- `op_delete_configuration_set_event_destination`: `DeleteConfigurationSetEventDestination`
- `op_delete_contact`: `DeleteContact`
- `op_delete_contact_list`: `DeleteContactList`
- `op_delete_custom_verification_email_template`: `DeleteCustomVerificationEmailTemplate`
- `op_delete_dedicated_ip_pool`: `DeleteDedicatedIpPool`
- `op_delete_email_identity`: `DeleteEmailIdentity`
- `op_delete_email_identity_policy`: `DeleteEmailIdentityPolicy`
- `op_delete_email_template`: `DeleteEmailTemplate`
- `op_delete_multi_region_endpoint`: `DeleteMultiRegionEndpoint`
- `op_delete_suppressed_destination`: `DeleteSuppressedDestination`
- `op_delete_tenant`: `DeleteTenant`
- `op_delete_tenant_resource_association`: `DeleteTenantResourceAssociation`
- `op_disassociate_email_identity_certificate`: `DisassociateEmailIdentityCertificate`
- `op_get_account`: `GetAccount`
- `op_get_blacklist_reports`: `GetBlacklistReports`
- `op_get_configuration_set`: `GetConfigurationSet`
- `op_get_configuration_set_event_destinations`: `GetConfigurationSetEventDestinations`
- `op_get_contact`: `GetContact`
- `op_get_contact_list`: `GetContactList`
- `op_get_custom_verification_email_template`: `GetCustomVerificationEmailTemplate`
- `op_get_dedicated_ip`: `GetDedicatedIp`
- `op_get_dedicated_ip_pool`: `GetDedicatedIpPool`
- `op_get_dedicated_ips`: `GetDedicatedIps`
- `op_get_deliverability_dashboard_options`: `GetDeliverabilityDashboardOptions`
- `op_get_deliverability_test_report`: `GetDeliverabilityTestReport`
- `op_get_domain_deliverability_campaign`: `GetDomainDeliverabilityCampaign`
- `op_get_domain_statistics_report`: `GetDomainStatisticsReport`
- `op_get_email_address_insights`: `GetEmailAddressInsights`
- `op_get_email_identity`: `GetEmailIdentity`
- `op_get_email_identity_policies`: `GetEmailIdentityPolicies`
- `op_get_email_template`: `GetEmailTemplate`
- `op_get_export_job`: `GetExportJob`
- `op_get_import_job`: `GetImportJob`
- `op_get_message_insights`: `GetMessageInsights`
- `op_get_multi_region_endpoint`: `GetMultiRegionEndpoint`
- `op_get_reputation_entity`: `GetReputationEntity`
- `op_get_suppressed_destination`: `GetSuppressedDestination`
- `op_get_tenant`: `GetTenant`
- `op_list_configuration_sets`: `ListConfigurationSets`
- `op_list_contact_lists`: `ListContactLists`
- `op_list_contacts`: `ListContacts`
- `op_list_custom_verification_email_templates`: `ListCustomVerificationEmailTemplates`
- `op_list_dedicated_ip_pools`: `ListDedicatedIpPools`
- `op_list_deliverability_test_reports`: `ListDeliverabilityTestReports`
- `op_list_domain_deliverability_campaigns`: `ListDomainDeliverabilityCampaigns`
- `op_list_email_identities`: `ListEmailIdentities`
- `op_list_email_identity_certificates`: `ListEmailIdentityCertificates`
- `op_list_email_templates`: `ListEmailTemplates`
- `op_list_export_jobs`: `ListExportJobs`
- `op_list_import_jobs`: `ListImportJobs`
- `op_list_multi_region_endpoints`: `ListMultiRegionEndpoints`
- `op_list_recommendations`: `ListRecommendations`
- `op_list_reputation_entities`: `ListReputationEntities`
- `op_list_resource_tenants`: `ListResourceTenants`
- `op_list_suppressed_destinations`: `ListSuppressedDestinations`
- `op_list_tags_for_resource`: `ListTagsForResource`
- `op_list_tenant_resources`: `ListTenantResources`
- `op_list_tenants`: `ListTenants`
- `op_put_account_dedicated_ip_warmup_attributes`: `PutAccountDedicatedIpWarmupAttributes`
- `op_put_account_details`: `PutAccountDetails`
- `op_put_account_pricing_attributes`: `PutAccountPricingAttributes`
- `op_put_account_sending_attributes`: `PutAccountSendingAttributes`
- `op_put_account_suppression_attributes`: `PutAccountSuppressionAttributes`
- `op_put_account_vdm_attributes`: `PutAccountVdmAttributes`
- `op_put_configuration_set_archiving_options`: `PutConfigurationSetArchivingOptions`
- `op_put_configuration_set_delivery_options`: `PutConfigurationSetDeliveryOptions`
- `op_put_configuration_set_reputation_options`: `PutConfigurationSetReputationOptions`
- `op_put_configuration_set_sending_options`: `PutConfigurationSetSendingOptions`
- `op_put_configuration_set_suppression_options`: `PutConfigurationSetSuppressionOptions`
- `op_put_configuration_set_tracking_options`: `PutConfigurationSetTrackingOptions`
- `op_put_configuration_set_vdm_options`: `PutConfigurationSetVdmOptions`
- `op_put_dedicated_ip_in_pool`: `PutDedicatedIpInPool`
- `op_put_dedicated_ip_pool_scaling_attributes`: `PutDedicatedIpPoolScalingAttributes`
- `op_put_dedicated_ip_warmup_attributes`: `PutDedicatedIpWarmupAttributes`
- `op_put_deliverability_dashboard_option`: `PutDeliverabilityDashboardOption`
- `op_put_email_identity_configuration_set_attributes`: `PutEmailIdentityConfigurationSetAttributes`
- `op_put_email_identity_dkim_attributes`: `PutEmailIdentityDkimAttributes`
- `op_put_email_identity_dkim_signing_attributes`: `PutEmailIdentityDkimSigningAttributes`
- `op_put_email_identity_feedback_attributes`: `PutEmailIdentityFeedbackAttributes`
- `op_put_email_identity_mail_from_attributes`: `PutEmailIdentityMailFromAttributes`
- `op_put_suppressed_destination`: `PutSuppressedDestination`
- `op_put_tenant_suppression_attributes`: `PutTenantSuppressionAttributes`
- `op_send_bulk_email`: `SendBulkEmail`
- `op_send_custom_verification_email`: `SendCustomVerificationEmail`
- `op_send_email`: `SendEmail`
- `op_tag_resource`: `TagResource`
- `op_test_render_email_template`: `TestRenderEmailTemplate`
- `op_untag_resource`: `UntagResource`
- `op_update_configuration_set`: `UpdateConfigurationSet`
- `op_update_configuration_set_event_destination`: `UpdateConfigurationSetEventDestination`
- `op_update_contact`: `UpdateContact`
- `op_update_contact_list`: `UpdateContactList`
- `op_update_custom_verification_email_template`: `UpdateCustomVerificationEmailTemplate`
- `op_update_email_identity_policy`: `UpdateEmailIdentityPolicy`
- `op_update_email_template`: `UpdateEmailTemplate`
- `op_update_reputation_entity_customer_managed_status`: `UpdateReputationEntityCustomerManagedStatus`
- `op_update_reputation_entity_policy`: `UpdateReputationEntityPolicy`

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
@@ -84,11 +73,9 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -108,3 +95,119 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["sigv4a", "rustls", "default-https-client", "rt-tokio"]
+op_associate_email_identity_certificate = []
+op_batch_get_metric_data = []
+op_cancel_export_job = []
+op_create_configuration_set = []
+op_create_configuration_set_event_destination = []
+op_create_contact = []
+op_create_contact_list = []
+op_create_custom_verification_email_template = []
+op_create_dedicated_ip_pool = []
+op_create_deliverability_test_report = []
+op_create_email_identity = []
+op_create_email_identity_policy = []
+op_create_email_template = []
+op_create_export_job = []
+op_create_import_job = []
+op_create_multi_region_endpoint = []
+op_create_tenant = []
+op_create_tenant_resource_association = []
+op_delete_configuration_set = []
+op_delete_configuration_set_event_destination = []
+op_delete_contact = []
+op_delete_contact_list = []
+op_delete_custom_verification_email_template = []
+op_delete_dedicated_ip_pool = []
+op_delete_email_identity = []
+op_delete_email_identity_policy = []
+op_delete_email_template = []
+op_delete_multi_region_endpoint = []
+op_delete_suppressed_destination = []
+op_delete_tenant = []
+op_delete_tenant_resource_association = []
+op_disassociate_email_identity_certificate = []
+op_get_account = []
+op_get_blacklist_reports = []
+op_get_configuration_set = []
+op_get_configuration_set_event_destinations = []
+op_get_contact = []
+op_get_contact_list = []
+op_get_custom_verification_email_template = []
+op_get_dedicated_ip = []
+op_get_dedicated_ip_pool = []
+op_get_dedicated_ips = []
+op_get_deliverability_dashboard_options = []
+op_get_deliverability_test_report = []
+op_get_domain_deliverability_campaign = []
+op_get_domain_statistics_report = []
+op_get_email_address_insights = []
+op_get_email_identity = []
+op_get_email_identity_policies = []
+op_get_email_template = []
+op_get_export_job = []
+op_get_import_job = []
+op_get_message_insights = []
+op_get_multi_region_endpoint = []
+op_get_reputation_entity = []
+op_get_suppressed_destination = []
+op_get_tenant = []
+op_list_configuration_sets = []
+op_list_contact_lists = []
+op_list_contacts = []
+op_list_custom_verification_email_templates = []
+op_list_dedicated_ip_pools = []
+op_list_deliverability_test_reports = []
+op_list_domain_deliverability_campaigns = []
+op_list_email_identities = []
+op_list_email_identity_certificates = []
+op_list_email_templates = []
+op_list_export_jobs = []
+op_list_import_jobs = []
+op_list_multi_region_endpoints = []
+op_list_recommendations = []
+op_list_reputation_entities = []
+op_list_resource_tenants = []
+op_list_suppressed_destinations = []
+op_list_tags_for_resource = []
+op_list_tenant_resources = []
+op_list_tenants = []
+op_put_account_dedicated_ip_warmup_attributes = []
+op_put_account_details = []
+op_put_account_pricing_attributes = []
+op_put_account_sending_attributes = []
+op_put_account_suppression_attributes = []
+op_put_account_vdm_attributes = []
+op_put_configuration_set_archiving_options = []
+op_put_configuration_set_delivery_options = []
+op_put_configuration_set_reputation_options = []
+op_put_configuration_set_sending_options = []
+op_put_configuration_set_suppression_options = []
+op_put_configuration_set_tracking_options = []
+op_put_configuration_set_vdm_options = []
+op_put_dedicated_ip_in_pool = []
+op_put_dedicated_ip_pool_scaling_attributes = []
+op_put_dedicated_ip_warmup_attributes = []
+op_put_deliverability_dashboard_option = []
+op_put_email_identity_configuration_set_attributes = []
+op_put_email_identity_dkim_attributes = []
+op_put_email_identity_dkim_signing_attributes = []
+op_put_email_identity_feedback_attributes = []
+op_put_email_identity_mail_from_attributes = []
+op_put_suppressed_destination = []
+op_put_tenant_suppression_attributes = []
+op_send_bulk_email = []
+op_send_custom_verification_email = []
+op_send_email = []
+op_tag_resource = []
+op_test_render_email_template = []
+op_untag_resource = []
+op_update_configuration_set = []
+op_update_configuration_set_event_destination = []
+op_update_contact = []
+op_update_contact_list = []
+op_update_custom_verification_email_template = []
+op_update_email_identity_policy = []
+op_update_email_template = []
+op_update_reputation_entity_customer_managed_status = []
+op_update_reputation_entity_policy = []
```

### `src/client.rs`

```diff
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,40 +136,58 @@
     }
 }

+#[cfg(feature = "op_associate_email_identity_certificate")]
 mod associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 mod cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 mod create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 mod create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 mod create_contact;

+#[cfg(feature = "op_create_contact_list")]
 mod create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 mod create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 mod create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 mod create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 mod create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 mod create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 mod create_email_template;

+#[cfg(feature = "op_create_export_job")]
 mod create_export_job;

+#[cfg(feature = "op_create_import_job")]
 mod create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 mod create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 mod create_tenant_resource_association;

 /// Operation customization and supporting types.
@@ -199,198 +217,296 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_configuration_set")]
 mod delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 mod delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 mod delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 mod delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 mod delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 mod delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 mod delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 mod delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 mod delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 mod delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 mod delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 mod delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 mod delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 mod disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 mod get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 mod get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 mod get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 mod get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 mod get_contact;

+#[cfg(feature = "op_get_contact_list")]
 mod get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 mod get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 mod get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 mod get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 mod get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 mod get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 mod get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 mod get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 mod get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 mod get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 mod get_email_template;

+#[cfg(feature = "op_get_export_job")]
 mod get_export_job;

+#[cfg(feature = "op_get_import_job")]
 mod get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 mod get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 mod get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 mod get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 mod get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 mod list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 mod list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 mod list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 mod list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 mod list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 mod list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 mod list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 mod list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 mod list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 mod list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 mod list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 mod list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 mod list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 mod list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 mod list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 mod list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 mod list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 mod put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 mod put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 mod put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 mod put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 mod put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 mod put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 mod put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 mod put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 mod put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 mod put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 mod put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 mod put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 mod put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 mod put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 mod put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 mod put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 mod put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 mod put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 mod put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 mod put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 mod put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 mod put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 mod put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 mod put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 mod send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 mod send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 mod send_email;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 mod test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 mod update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 mod update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 mod update_contact;

+#[cfg(feature = "op_update_contact_list")]
 mod update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 mod update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 mod update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 mod update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 mod update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 mod update_reputation_entity_policy;
```

### `src/error_meta.rs`

```diff
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,30 +3,439 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the account's ability to send email has been permanently restricted.</p>
     AccountSuspendedException(crate::types::error::AccountSuspendedException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_put_deliverability_dashboard_option"
+    ))]
     /// <p>The resource specified in your request already exists.</p>
     AlreadyExistsException(crate::types::error::AlreadyExistsException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_account",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_address_insights",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_configuration_sets",
+        feature = "op_list_contact_lists",
+        feature = "op_list_contacts",
+        feature = "op_list_custom_verification_email_templates",
+        feature = "op_list_dedicated_ip_pools",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identities",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_email_templates",
+        feature = "op_list_export_jobs",
+        feature = "op_list_import_jobs",
+        feature = "op_list_multi_region_endpoints",
+        feature = "op_list_recommendations",
+        feature = "op_list_reputation_entities",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_list_tenants",
+        feature = "op_put_account_dedicated_ip_warmup_attributes",
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_put_account_sending_attributes",
+        feature = "op_put_account_suppression_attributes",
+        feature = "op_put_account_vdm_attributes",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>The input you provided is invalid.</p>
     BadRequestException(crate::types::error::BadRequestException),
+    #[cfg(any(
+        feature = "op_create_configuration_set",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list"
+    ))]
     /// <p>The resource is being modified by another operation or thread.</p>
     ConcurrentModificationException(crate::types::error::ConcurrentModificationException),
+    #[cfg(any(
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>If there is already an ongoing account details update under review.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_batch_get_metric_data")]
     /// <p>The request couldn't be processed because an error occurred with the Amazon SES API v2.</p>
     InternalServiceErrorException(crate::types::error::InternalServiceErrorException),
+    #[cfg(feature = "op_list_suppressed_destinations")]
     /// <p>The specified request includes an invalid or expired token.</p>
     InvalidNextTokenException(crate::types::error::InvalidNextTokenException),
+    #[cfg(any(
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>There are too many instances of the specified resource type.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the sending domain isn't verified.</p>
     MailFromDomainNotVerifiedException(crate::types::error::MailFromDomainNotVerifiedException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because it contains invalid content.</p>
     MessageRejected(crate::types::error::MessageRejected),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_export_job",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_contacts",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_recommendations",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template"
+    ))]
     /// <p>The resource you attempted to access doesn't exist.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the account's ability to send email is currently paused.</p>
     SendingPausedException(crate::types::error::SendingPausedException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_account",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_address_insights",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_configuration_sets",
+        feature = "op_list_contact_lists",
+        feature = "op_list_contacts",
+        feature = "op_list_custom_verification_email_templates",
+        feature = "op_list_dedicated_ip_pools",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identities",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_email_templates",
+        feature = "op_list_export_jobs",
+        feature = "op_list_import_jobs",
+        feature = "op_list_multi_region_endpoints",
+        feature = "op_list_recommendations",
+        feature = "op_list_reputation_entities",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_list_tenants",
+        feature = "op_put_account_dedicated_ip_warmup_attributes",
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_put_account_sending_attributes",
+        feature = "op_put_account_suppression_attributes",
+        feature = "op_put_account_vdm_attributes",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>Too many requests have been made to the operation.</p>
     TooManyRequestsException(crate::types::error::TooManyRequestsException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -43,18 +452,427 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Error::AccountSuspendedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Error::AlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::BadRequestException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Error::ConcurrentModificationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Error::InternalServiceErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Error::InvalidNextTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MailFromDomainNotVerifiedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MessageRejected(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::SendingPausedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::TooManyRequestsException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -79,23 +897,433 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Self::AccountSuspendedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Self::AlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::BadRequestException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Self::ConcurrentModificationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Self::InternalServiceErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Self::InvalidNextTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MailFromDomainNotVerifiedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MessageRejected(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::SendingPausedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::TooManyRequestsException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_associate_email_identity_certificate")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -121,6 +1349,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_email_identity_certificate")]
 impl From<crate::operation::associate_email_identity_certificate::AssociateEmailIdentityCertificateError> for Error {
     fn from(
         err: crate::operation::associate_email_identity_certificate::AssociateEmailIdentityCertificateError,
@@ -144,6 +1373,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_metric_data")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -169,6 +1399,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_metric_data")]
 impl From<crate::operation::batch_get_metric_data::BatchGetMetricDataError> for Error {
     fn from(err: crate::operation::batch_get_metric_data::BatchGetMetricDataError) -> Self {
         match err {
@@ -190,6 +1421,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -215,6 +1447,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_job")]
 impl From<crate::operation::cancel_export_job::CancelExportJobError> for Error {
     fn from(err: crate::operation::cancel_export_job::CancelExportJobError) -> Self {
         match err {
@@ -231,6 +1464,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -256,6 +1490,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set")]
 impl From<crate::operation::create_configuration_set::CreateConfigurationSetError> for Error {
     fn from(err: crate::operation::create_configuration_set::CreateConfigurationSetError) -> Self {
         match err {
@@ -277,6 +1512,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -302,6 +1538,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set_event_destination")]
 impl From<crate::operation::create_configuration_set_event_destination::CreateConfigurationSetEventDestinationError>
     for Error
 {
@@ -330,6 +1567,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_contact::CreateContactError, R>>
     for Error
@@ -351,6 +1589,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact")]
 impl From<crate::operation::create_contact::CreateContactError> for Error {
     fn from(err: crate::operation::create_contact::CreateContactError) -> Self {
         match err {
@@ -370,6 +1609,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -395,6 +1635,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact_list")]
 impl From<crate::operation::create_contact_list::CreateContactListError> for Error {
     fn from(err: crate::operation::create_contact_list::CreateContactListError) -> Self {
         match err {
@@ -414,6 +1655,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -439,6 +1681,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_verification_email_template")]
 impl From<crate::operation::create_custom_verification_email_template::CreateCustomVerificationEmailTemplateError>
     for Error
 {
@@ -467,6 +1710,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -492,6 +1736,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_dedicated_ip_pool")]
 impl From<crate::operation::create_dedicated_ip_pool::CreateDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::create_dedicated_ip_pool::CreateDedicatedIpPoolError) -> Self {
         match err {
@@ -516,6 +1761,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_deliverability_test_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -541,6 +1787,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_deliverability_test_report")]
 impl From<crate::operation::create_deliverability_test_report::CreateDeliverabilityTestReportError> for Error {
     fn from(err: crate::operation::create_deliverability_test_report::CreateDeliverabilityTestReportError) -> Self {
         match err {
@@ -575,6 +1822,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -600,6 +1848,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity")]
 impl From<crate::operation::create_email_identity::CreateEmailIdentityError> for Error {
     fn from(err: crate::operation::create_email_identity::CreateEmailIdentityError) -> Self {
         match err {
@@ -627,6 +1876,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -652,6 +1902,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity_policy")]
 impl From<crate::operation::create_email_identity_policy::CreateEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::create_email_identity_policy::CreateEmailIdentityPolicyError) -> Self {
         match err {
@@ -674,6 +1925,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -699,6 +1951,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_template")]
 impl From<crate::operation::create_email_template::CreateEmailTemplateError> for Error {
     fn from(err: crate::operation::create_email_template::CreateEmailTemplateError) -> Self {
         match err {
@@ -720,6 +1973,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -745,6 +1999,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_job")]
 impl From<crate::operation::create_export_job::CreateExportJobError> for Error {
     fn from(err: crate::operation::create_export_job::CreateExportJobError) -> Self {
         match err {
@@ -764,6 +2019,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -789,6 +2045,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_job")]
 impl From<crate::operation::create_import_job::CreateImportJobError> for Error {
     fn from(err: crate::operation::create_import_job::CreateImportJobError) -> Self {
         match err {
@@ -805,6 +2062,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -830,6 +2088,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_multi_region_endpoint")]
 impl From<crate::operation::create_multi_region_endpoint::CreateMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::create_multi_region_endpoint::CreateMultiRegionEndpointError) -> Self {
         match err {
@@ -849,6 +2108,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_tenant::CreateTenantError, R>>
     for Error
 where
@@ -866,6 +2126,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant")]
 impl From<crate::operation::create_tenant::CreateTenantError> for Error {
     fn from(err: crate::operation::create_tenant::CreateTenantError) -> Self {
         match err {
@@ -885,6 +2146,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant_resource_association")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -910,6 +2172,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant_resource_association")]
 impl From<crate::operation::create_tenant_resource_association::CreateTenantResourceAssociationError> for Error {
     fn from(err: crate::operation::create_tenant_resource_association::CreateTenantResourceAssociationError) -> Self {
         match err {
@@ -929,6 +2192,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -954,6 +2218,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set")]
 impl From<crate::operation::delete_configuration_set::DeleteConfigurationSetError> for Error {
     fn from(err: crate::operation::delete_configuration_set::DeleteConfigurationSetError) -> Self {
         match err {
@@ -969,6 +2234,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -994,6 +2260,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 impl From<crate::operation::delete_configuration_set_event_destination::DeleteConfigurationSetEventDestinationError>
     for Error
 {
@@ -1016,6 +2283,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_contact::DeleteContactError, R>>
     for Error
@@ -1037,6 +2305,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact")]
 impl From<crate::operation::delete_contact::DeleteContactError> for Error {
     fn from(err: crate::operation::delete_contact::DeleteContactError) -> Self {
         match err {
@@ -1053,6 +2322,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1078,6 +2348,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact_list")]
 impl From<crate::operation::delete_contact_list::DeleteContactListError> for Error {
     fn from(err: crate::operation::delete_contact_list::DeleteContactListError) -> Self {
         match err {
@@ -1097,6 +2368,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1122,6 +2394,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_verification_email_template")]
 impl From<crate::operation::delete_custom_verification_email_template::DeleteCustomVerificationEmailTemplateError>
     for Error
 {
@@ -1144,6 +2417,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1169,6 +2443,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 impl From<crate::operation::delete_dedicated_ip_pool::DeleteDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::delete_dedicated_ip_pool::DeleteDedicatedIpPoolError) -> Self {
         match err {
@@ -1190,6 +2465,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1215,6 +2491,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity")]
 impl From<crate::operation::delete_email_identity::DeleteEmailIdentityError> for Error {
     fn from(err: crate::operation::delete_email_identity::DeleteEmailIdentityError) -> Self {
         match err {
@@ -1236,6 +2513,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1261,6 +2539,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity_policy")]
 impl From<crate::operation::delete_email_identity_policy::DeleteEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::delete_email_identity_policy::DeleteEmailIdentityPolicyError) -> Self {
         match err {
@@ -1277,6 +2556,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1302,6 +2582,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_template")]
 impl From<crate::operation::delete_email_template::DeleteEmailTemplateError> for Error {
     fn from(err: crate::operation::delete_email_template::DeleteEmailTemplateError) -> Self {
         match err {
@@ -1320,6 +2601,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1345,6 +2627,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_multi_region_endpoint")]
 impl From<crate::operation::delete_multi_region_endpoint::DeleteMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::delete_multi_region_endpoint::DeleteMultiRegionEndpointError) -> Self {
         match err {
@@ -1364,6 +2647,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1389,6 +2673,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_suppressed_destination")]
 impl From<crate::operation::delete_suppressed_destination::DeleteSuppressedDestinationError> for Error {
     fn from(err: crate::operation::delete_suppressed_destination::DeleteSuppressedDestinationError) -> Self {
         match err {
@@ -1405,6 +2690,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_tenant::DeleteTenantError, R>>
     for Error
 where
@@ -1422,6 +2708,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant")]
 impl From<crate::operation::delete_tenant::DeleteTenantError> for Error {
     fn from(err: crate::operation::delete_tenant::DeleteTenantError) -> Self {
         match err {
@@ -1438,6 +2725,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant_resource_association")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1463,6 +2751,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant_resource_association")]
 impl From<crate::operation::delete_tenant_resource_association::DeleteTenantResourceAssociationError> for Error {
     fn from(err: crate::operation::delete_tenant_resource_association::DeleteTenantResourceAssociationError) -> Self {
         match err {
@@ -1479,6 +2768,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1504,6 +2794,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 impl From<crate::operation::disassociate_email_identity_certificate::DisassociateEmailIdentityCertificateError>
     for Error
 {
@@ -1526,6 +2817,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_account")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_account::GetAccountError, R>>
     for Error
 where
@@ -1543,6 +2835,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_account")]
 impl From<crate::operation::get_account::GetAccountError> for Error {
     fn from(err: crate::operation::get_account::GetAccountError) -> Self {
         match err {
@@ -1556,6 +2849,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_blacklist_reports")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1581,6 +2875,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_blacklist_reports")]
 impl From<crate::operation::get_blacklist_reports::GetBlacklistReportsError> for Error {
     fn from(err: crate::operation::get_blacklist_reports::GetBlacklistReportsError) -> Self {
         match err {
@@ -1599,6 +2894,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1624,6 +2920,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set")]
 impl From<crate::operation::get_configuration_set::GetConfigurationSetError> for Error {
     fn from(err: crate::operation::get_configuration_set::GetConfigurationSetError) -> Self {
         match err {
@@ -1642,6 +2939,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1667,6 +2965,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 impl From<crate::operation::get_configuration_set_event_destinations::GetConfigurationSetEventDestinationsError>
     for Error
 {
@@ -1689,6 +2988,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_contact::GetContactError, R>>
     for Error
 where
@@ -1706,6 +3006,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact")]
 impl From<crate::operation::get_contact::GetContactError> for Error {
     fn from(err: crate::operation::get_contact::GetContactError) -> Self {
         match err {
@@ -1720,6 +3021,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact_list")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_contact_list::GetContactListError, R>>
     for Error
@@ -1741,6 +3043,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact_list")]
 impl From<crate::operation::get_contact_list::GetContactListError> for Error {
     fn from(err: crate::operation::get_contact_list::GetContactListError) -> Self {
         match err {
@@ -1757,6 +3060,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1782,6 +3086,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_custom_verification_email_template")]
 impl From<crate::operation::get_custom_verification_email_template::GetCustomVerificationEmailTemplateError> for Error {
     fn from(
         err: crate::operation::get_custom_verification_email_template::GetCustomVerificationEmailTemplateError,
@@ -1802,6 +3107,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_dedicated_ip::GetDedicatedIpError, R>>
     for Error
@@ -1823,6 +3129,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip")]
 impl From<crate::operation::get_dedicated_ip::GetDedicatedIpError> for Error {
     fn from(err: crate::operation::get_dedicated_ip::GetDedicatedIpError) -> Self {
         match err {
@@ -1839,6 +3146,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1864,6 +3172,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip_pool")]
 impl From<crate::operation::get_dedicated_ip_pool::GetDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::get_dedicated_ip_pool::GetDedicatedIpPoolError) -> Self {
         match err {
@@ -1882,6 +3191,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ips")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1907,6 +3217,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ips")]
 impl From<crate::operation::get_dedicated_ips::GetDedicatedIpsError> for Error {
     fn from(err: crate::operation::get_dedicated_ips::GetDedicatedIpsError) -> Self {
         match err {
@@ -1923,6 +3234,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1948,6 +3260,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 impl From<crate::operation::get_deliverability_dashboard_options::GetDeliverabilityDashboardOptionsError> for Error {
     fn from(
         err: crate::operation::get_deliverability_dashboard_options::GetDeliverabilityDashboardOptionsError,
@@ -1968,6 +3281,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_test_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1993,6 +3307,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_test_report")]
 impl From<crate::operation::get_deliverability_test_report::GetDeliverabilityTestReportError> for Error {
     fn from(err: crate::operation::get_deliverability_test_report::GetDeliverabilityTestReportError) -> Self {
         match err {
@@ -2009,6 +3324,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2034,6 +3350,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 impl From<crate::operation::get_domain_deliverability_campaign::GetDomainDeliverabilityCampaignError> for Error {
     fn from(err: crate::operation::get_domain_deliverability_campaign::GetDomainDeliverabilityCampaignError) -> Self {
         match err {
@@ -2050,6 +3367,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_statistics_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2075,6 +3393,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_statistics_report")]
 impl From<crate::operation::get_domain_statistics_report::GetDomainStatisticsReportError> for Error {
     fn from(err: crate::operation::get_domain_statistics_report::GetDomainStatisticsReportError) -> Self {
         match err {
@@ -2091,6 +3410,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_address_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2116,6 +3436,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_address_insights")]
 impl From<crate::operation::get_email_address_insights::GetEmailAddressInsightsError> for Error {
     fn from(err: crate::operation::get_email_address_insights::GetEmailAddressInsightsError) -> Self {
         match err {
@@ -2131,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2156,6 +3478,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity")]
 impl From<crate::operation::get_email_identity::GetEmailIdentityError> for Error {
     fn from(err: crate::operation::get_email_identity::GetEmailIdentityError) -> Self {
         match err {
@@ -2172,6 +3495,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2197,6 +3521,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity_policies")]
 impl From<crate::operation::get_email_identity_policies::GetEmailIdentityPoliciesError> for Error {
     fn from(err: crate::operation::get_email_identity_policies::GetEmailIdentityPoliciesError) -> Self {
         match err {
@@ -2215,6 +3540,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2240,6 +3566,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_template")]
 impl From<crate::operation::get_email_template::GetEmailTemplateError> for Error {
     fn from(err: crate::operation::get_email_template::GetEmailTemplateError) -> Self {
         match err {
@@ -2256,6 +3583,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_export_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_export_job::GetExportJobError, R>>
     for Error
 where
@@ -2273,6 +3601,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_export_job")]
 impl From<crate::operation::get_export_job::GetExportJobError> for Error {
     fn from(err: crate::operation::get_export_job::GetExportJobError) -> Self {
         match err {
@@ -2289,6 +3618,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_import_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_import_job::GetImportJobError, R>>
     for Error
 where
@@ -2306,6 +3636,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_import_job")]
 impl From<crate::operation::get_import_job::GetImportJobError> for Error {
     fn from(err: crate::operation::get_import_job::GetImportJobError) -> Self {
         match err {
@@ -2322,6 +3653,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_message_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2347,6 +3679,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_message_insights")]
 impl From<crate::operation::get_message_insights::GetMessageInsightsError> for Error {
     fn from(err: crate::operation::get_message_insights::GetMessageInsightsError) -> Self {
         match err {
@@ -2365,6 +3698,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2390,6 +3724,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_multi_region_endpoint")]
 impl From<crate::operation::get_multi_region_endpoint::GetMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::get_multi_region_endpoint::GetMultiRegionEndpointError) -> Self {
         match err {
@@ -2408,6 +3743,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_reputation_entity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2433,6 +3769,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_reputation_entity")]
 impl From<crate::operation::get_reputation_entity::GetReputationEntityError> for Error {
     fn from(err: crate::operation::get_reputation_entity::GetReputationEntityError) -> Self {
         match err {
@@ -2451,6 +3788,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2476,6 +3814,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_suppressed_destination")]
 impl From<crate::operation::get_suppressed_destination::GetSuppressedDestinationError> for Error {
     fn from(err: crate::operation::get_suppressed_destination::GetSuppressedDestinationError) -> Self {
         match err {
@@ -2494,6 +3833,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_tenant::GetTenantError, R>>
     for Error
 where
@@ -2511,6 +3851,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_tenant")]
 impl From<crate::operation::get_tenant::GetTenantError> for Error {
     fn from(err: crate::operation::get_tenant::GetTenantError) -> Self {
         match err {
@@ -2525,6 +3866,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_configuration_sets")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2550,6 +3892,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_configuration_sets")]
 impl From<crate::operation::list_configuration_sets::ListConfigurationSetsError> for Error {
     fn from(err: crate::operation::list_configuration_sets::ListConfigurationSetsError) -> Self {
         match err {
@@ -2565,6 +3908,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contact_lists")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2590,6 +3934,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contact_lists")]
 impl From<crate::operation::list_contact_lists::ListContactListsError> for Error {
     fn from(err: crate::operation::list_contact_lists::ListContactListsError) -> Self {
         match err {
@@ -2603,6 +3948,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contacts")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_contacts::ListContactsError, R>>
     for Error
 where
@@ -2620,6 +3966,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contacts")]
 impl From<crate::operation::list_contacts::ListContactsError> for Error {
     fn from(err: crate::operation::list_contacts::ListContactsError) -> Self {
         match err {
@@ -2636,6 +3983,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_custom_verification_email_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2661,6 +4009,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_custom_verification_email_templates")]
 impl From<crate::operation::list_custom_verification_email_templates::ListCustomVerificationEmailTemplatesError>
     for Error
 {
@@ -2680,6 +4029,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dedicated_ip_pools")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2705,6 +4055,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dedicated_ip_pools")]
 impl From<crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsError> for Error {
     fn from(err: crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsError) -> Self {
         match err {
@@ -2720,6 +4071,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_deliverability_test_reports")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2745,6 +4097,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_deliverability_test_reports")]
 impl From<crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsError> for Error {
     fn from(err: crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsError) -> Self {
         match err {
@@ -2761,6 +4114,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2786,6 +4140,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 impl From<crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsError> for Error {
     fn from(
         err: crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsError,
@@ -2806,6 +4161,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identities")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2831,6 +4187,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identities")]
 impl From<crate::operation::list_email_identities::ListEmailIdentitiesError> for Error {
     fn from(err: crate::operation::list_email_identities::ListEmailIdentitiesError) -> Self {
         match err {
@@ -2846,6 +4203,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identity_certificates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2871,6 +4229,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identity_certificates")]
 impl From<crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesError> for Error {
     fn from(err: crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesError) -> Self {
         match err {
@@ -2887,6 +4246,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2912,6 +4272,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_templates")]
 impl From<crate::operation::list_email_templates::ListEmailTemplatesError> for Error {
     fn from(err: crate::operation::list_email_templates::ListEmailTemplatesError) -> Self {
         match err {
@@ -2927,6 +4288,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_export_jobs")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_export_jobs::ListExportJobsError, R>>
     for Error
@@ -2948,6 +4310,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_export_jobs")]
 impl From<crate::operation::list_export_jobs::ListExportJobsError> for Error {
     fn from(err: crate::operation::list_export_jobs::ListExportJobsError) -> Self {
         match err {
@@ -2961,6 +4324,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_import_jobs")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_import_jobs::ListImportJobsError, R>>
     for Error
@@ -2982,6 +4346,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_import_jobs")]
 impl From<crate::operation::list_import_jobs::ListImportJobsError> for Error {
     fn from(err: crate::operation::list_import_jobs::ListImportJobsError) -> Self {
         match err {
@@ -2995,6 +4360,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_multi_region_endpoints")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3020,6 +4386,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_multi_region_endpoints")]
 impl From<crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsError> for Error {
     fn from(err: crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsError) -> Self {
         match err {
@@ -3035,6 +4402,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_recommendations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3060,6 +4428,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_recommendations")]
 impl From<crate::operation::list_recommendations::ListRecommendationsError> for Error {
     fn from(err: crate::operation::list_recommendations::ListRecommendationsError) -> Self {
         match err {
@@ -3078,6 +4447,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_reputation_entities")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3103,6 +4473,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_reputation_entities")]
 impl From<crate::operation::list_reputation_entities::ListReputationEntitiesError> for Error {
     fn from(err: crate::operation::list_reputation_entities::ListReputationEntitiesError) -> Self {
         match err {
@@ -3118,6 +4489,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tenants")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3143,6 +4515,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tenants")]
 impl From<crate::operation::list_resource_tenants::ListResourceTenantsError> for Error {
     fn from(err: crate::operation::list_resource_tenants::ListResourceTenantsError) -> Self {
         match err {
@@ -3161,6 +4534,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_suppressed_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3186,6 +4560,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_suppressed_destinations")]
 impl From<crate::operation::list_suppressed_destinations::ListSuppressedDestinationsError> for Error {
     fn from(err: crate::operation::list_suppressed_destinations::ListSuppressedDestinationsError) -> Self {
         match err {
@@ -3205,6 +4580,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3230,6 +4606,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -3248,6 +4625,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenant_resources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3273,6 +4651,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenant_resources")]
 impl From<crate::operation::list_tenant_resources::ListTenantResourcesError> for Error {
     fn from(err: crate::operation::list_tenant_resources::ListTenantResourcesError) -> Self {
         match err {
@@ -3291,6 +4670,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenants")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_tenants::ListTenantsError, R>>
     for Error
 where
@@ -3308,6 +4688,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenants")]
 impl From<crate::operation::list_tenants::ListTenantsError> for Error {
     fn from(err: crate::operation::list_tenants::ListTenantsError) -> Self {
         match err {
@@ -3321,6 +4702,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3346,6 +4728,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 impl From<crate::operation::put_account_dedicated_ip_warmup_attributes::PutAccountDedicatedIpWarmupAttributesError>
     for Error
 {
@@ -3365,6 +4748,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_details")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3390,6 +4774,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_details")]
 impl From<crate::operation::put_account_details::PutAccountDetailsError> for Error {
     fn from(err: crate::operation::put_account_details::PutAccountDetailsError) -> Self {
         match err {
@@ -3406,6 +4791,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_pricing_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3431,6 +4817,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_pricing_attributes")]
 impl From<crate::operation::put_account_pricing_attributes::PutAccountPricingAttributesError> for Error {
     fn from(err: crate::operation::put_account_pricing_attributes::PutAccountPricingAttributesError) -> Self {
         match err {
@@ -3447,6 +4834,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_sending_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3472,6 +4860,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_sending_attributes")]
 impl From<crate::operation::put_account_sending_attributes::PutAccountSendingAttributesError> for Error {
     fn from(err: crate::operation::put_account_sending_attributes::PutAccountSendingAttributesError) -> Self {
         match err {
@@ -3485,6 +4874,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_suppression_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3510,6 +4900,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_suppression_attributes")]
 impl From<crate::operation::put_account_suppression_attributes::PutAccountSuppressionAttributesError> for Error {
     fn from(err: crate::operation::put_account_suppression_attributes::PutAccountSuppressionAttributesError) -> Self {
         match err {
@@ -3523,6 +4914,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_vdm_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3548,6 +4940,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_vdm_attributes")]
 impl From<crate::operation::put_account_vdm_attributes::PutAccountVdmAttributesError> for Error {
     fn from(err: crate::operation::put_account_vdm_attributes::PutAccountVdmAttributesError) -> Self {
         match err {
@@ -3563,6 +4956,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3588,6 +4982,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 impl From<crate::operation::put_configuration_set_archiving_options::PutConfigurationSetArchivingOptionsError>
     for Error
 {
@@ -3610,6 +5005,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3635,6 +5031,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 impl From<crate::operation::put_configuration_set_delivery_options::PutConfigurationSetDeliveryOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_delivery_options::PutConfigurationSetDeliveryOptionsError,
@@ -3655,6 +5052,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3680,6 +5078,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 impl From<crate::operation::put_configuration_set_reputation_options::PutConfigurationSetReputationOptionsError>
     for Error
 {
@@ -3702,6 +5101,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_sending_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3727,6 +5127,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_sending_options")]
 impl From<crate::operation::put_configuration_set_sending_options::PutConfigurationSetSendingOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_sending_options::PutConfigurationSetSendingOptionsError,
@@ -3747,6 +5148,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3772,6 +5174,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 impl From<crate::operation::put_configuration_set_suppression_options::PutConfigurationSetSuppressionOptionsError>
     for Error
 {
@@ -3794,6 +5197,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3819,6 +5223,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 impl From<crate::operation::put_configuration_set_tracking_options::PutConfigurationSetTrackingOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_tracking_options::PutConfigurationSetTrackingOptionsError,
@@ -3839,6 +5244,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3864,6 +5270,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 impl From<crate::operation::put_configuration_set_vdm_options::PutConfigurationSetVdmOptionsError> for Error {
     fn from(err: crate::operation::put_configuration_set_vdm_options::PutConfigurationSetVdmOptionsError) -> Self {
         match err {
@@ -3880,6 +5287,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3905,6 +5313,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 impl From<crate::operation::put_dedicated_ip_in_pool::PutDedicatedIpInPoolError> for Error {
     fn from(err: crate::operation::put_dedicated_ip_in_pool::PutDedicatedIpInPoolError) -> Self {
         match err {
@@ -3923,6 +5332,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3948,6 +5358,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 impl From<crate::operation::put_dedicated_ip_pool_scaling_attributes::PutDedicatedIpPoolScalingAttributesError>
     for Error
 {
@@ -3973,6 +5384,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3998,6 +5410,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 impl From<crate::operation::put_dedicated_ip_warmup_attributes::PutDedicatedIpWarmupAttributesError> for Error {
     fn from(err: crate::operation::put_dedicated_ip_warmup_attributes::PutDedicatedIpWarmupAttributesError) -> Self {
         match err {
@@ -4014,6 +5427,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4039,6 +5453,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 impl From<crate::operation::put_deliverability_dashboard_option::PutDeliverabilityDashboardOptionError> for Error {
     fn from(err: crate::operation::put_deliverability_dashboard_option::PutDeliverabilityDashboardOptionError) -> Self {
         match err {
@@ -4061,6 +5476,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4086,6 +5502,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 impl From<crate::operation::put_email_identity_configuration_set_attributes::PutEmailIdentityConfigurationSetAttributesError> for Error {
     fn from(err: crate::operation::put_email_identity_configuration_set_attributes::PutEmailIdentityConfigurationSetAttributesError) -> Self {
         match err {
@@ -4096,6 +5513,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4121,6 +5539,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 impl From<crate::operation::put_email_identity_dkim_attributes::PutEmailIdentityDkimAttributesError> for Error {
     fn from(err: crate::operation::put_email_identity_dkim_attributes::PutEmailIdentityDkimAttributesError) -> Self {
         match err {
@@ -4137,6 +5556,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4162,6 +5582,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 impl From<crate::operation::put_email_identity_dkim_signing_attributes::PutEmailIdentityDkimSigningAttributesError>
     for Error
 {
@@ -4184,6 +5605,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4209,6 +5631,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 impl From<crate::operation::put_email_identity_feedback_attributes::PutEmailIdentityFeedbackAttributesError> for Error {
     fn from(
         err: crate::operation::put_email_identity_feedback_attributes::PutEmailIdentityFeedbackAttributesError,
@@ -4229,6 +5652,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4254,6 +5678,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 impl From<crate::operation::put_email_identity_mail_from_attributes::PutEmailIdentityMailFromAttributesError>
     for Error
 {
@@ -4276,6 +5701,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4301,6 +5727,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_suppressed_destination")]
 impl From<crate::operation::put_suppressed_destination::PutSuppressedDestinationError> for Error {
     fn from(err: crate::operation::put_suppressed_destination::PutSuppressedDestinationError) -> Self {
         match err {
@@ -4319,6 +5746,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4344,6 +5772,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 impl From<crate::operation::put_tenant_suppression_attributes::PutTenantSuppressionAttributesError> for Error {
     fn from(err: crate::operation::put_tenant_suppression_attributes::PutTenantSuppressionAttributesError) -> Self {
         match err {
@@ -4360,6 +5789,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_bulk_email")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_bulk_email::SendBulkEmailError, R>>
     for Error
@@ -4381,6 +5811,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_bulk_email")]
 impl From<crate::operation::send_bulk_email::SendBulkEmailError> for Error {
     fn from(err: crate::operation::send_bulk_email::SendBulkEmailError) -> Self {
         match err {
@@ -4412,6 +5843,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_custom_verification_email")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4437,6 +5869,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_custom_verification_email")]
 impl From<crate::operation::send_custom_verification_email::SendCustomVerificationEmailError> for Error {
     fn from(err: crate::operation::send_custom_verification_email::SendCustomVerificationEmailError) -> Self {
         match err {
@@ -4465,6 +5898,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_email")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_email::SendEmailError, R>>
     for Error
 where
@@ -4482,6 +5916,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_email")]
 impl From<crate::operation::send_email::SendEmailError> for Error {
     fn from(err: crate::operation::send_email::SendEmailError) -> Self {
         match err {
@@ -4509,6 +5944,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -4526,6 +5962,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -4545,6 +5982,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_render_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4570,6 +6008,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_render_email_template")]
 impl From<crate::operation::test_render_email_template::TestRenderEmailTemplateError> for Error {
     fn from(err: crate::operation::test_render_email_template::TestRenderEmailTemplateError) -> Self {
         match err {
@@ -4588,6 +6027,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -4609,6 +6049,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -4628,6 +6069,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4653,6 +6095,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set")]
 impl From<crate::operation::update_configuration_set::UpdateConfigurationSetError> for Error {
     fn from(err: crate::operation::update_configuration_set::UpdateConfigurationSetError) -> Self {
         match err {
@@ -4671,6 +6114,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4696,6 +6140,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set_event_destination")]
 impl From<crate::operation::update_configuration_set_event_destination::UpdateConfigurationSetEventDestinationError>
     for Error
 {
@@ -4718,6 +6163,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_contact::UpdateContactError, R>>
     for Error
@@ -4739,6 +6185,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact")]
 impl From<crate::operation::update_contact::UpdateContactError> for Error {
     fn from(err: crate::operation::update_contact::UpdateContactError) -> Self {
         match err {
@@ -4758,6 +6205,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4783,6 +6231,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact_list")]
 impl From<crate::operation::update_contact_list::UpdateContactListError> for Error {
     fn from(err: crate::operation::update_contact_list::UpdateContactListError) -> Self {
         match err {
@@ -4802,6 +6251,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4827,6 +6277,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_verification_email_template")]
 impl From<crate::operation::update_custom_verification_email_template::UpdateCustomVerificationEmailTemplateError>
     for Error
 {
@@ -4849,6 +6300,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4874,6 +6326,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_identity_policy")]
 impl From<crate::operation::update_email_identity_policy::UpdateEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::update_email_identity_policy::UpdateEmailIdentityPolicyError) -> Self {
         match err {
@@ -4890,6 +6343,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4915,6 +6369,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_template")]
 impl From<crate::operation::update_email_template::UpdateEmailTemplateError> for Error {
     fn from(err: crate::operation::update_email_template::UpdateEmailTemplateError) -> Self {
         match err {
@@ -4933,6 +6388,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4958,6 +6414,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 impl From<crate::operation::update_reputation_entity_customer_managed_status::UpdateReputationEntityCustomerManagedStatusError> for Error {
     fn from(err: crate::operation::update_reputation_entity_customer_managed_status::UpdateReputationEntityCustomerManagedStatusError) -> Self {
         match err {
@@ -4968,6 +6425,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4993,6 +6451,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_policy")]
 impl From<crate::operation::update_reputation_entity_policy::UpdateReputationEntityPolicyError> for Error {
     fn from(err: crate::operation::update_reputation_entity_policy::UpdateReputationEntityPolicyError) -> Self {
         match err {
@@ -5012,18 +6471,427 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Error::AccountSuspendedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Error::AlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::BadRequestException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Error::ConcurrentModificationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Error::InternalServiceErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Error::InvalidNextTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MailFromDomainNotVerifiedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MessageRejected(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::SendingPausedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::TooManyRequestsException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -5032,18 +6900,427 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Self::AccountSuspendedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Self::AlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::BadRequestException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Self::ConcurrentModificationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Self::InternalServiceErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Self::InvalidNextTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MailFromDomainNotVerifiedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MessageRejected(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::SendingPausedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::TooManyRequestsException(e) => e.request_id(),
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
+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) fn reflens_get_dedicated_ips_output_output_next_token(
     input: &crate::operation::get_dedicated_ips::GetDedicatedIpsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) fn reflens_list_configuration_sets_output_output_next_token(
     input: &crate::operation::list_configuration_sets::ListConfigurationSetsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) fn reflens_list_contact_lists_output_output_next_token(
     input: &crate::operation::list_contact_lists::ListContactListsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_contacts")]
 pub(crate) fn reflens_list_contacts_output_output_next_token(
     input: &crate::operation::list_contacts::ListContactsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) fn reflens_list_custom_verification_email_templates_output_output_next_token(
     input: &crate::operation::list_custom_verification_email_templates::ListCustomVerificationEmailTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) fn reflens_list_dedicated_ip_pools_output_output_next_token(
     input: &crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) fn reflens_list_deliverability_test_reports_output_output_next_token(
     input: &crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) fn reflens_list_domain_deliverability_campaigns_output_output_next_token(
     input: &crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) fn reflens_list_email_identities_output_output_next_token(
     input: &crate::operation::list_email_identities::ListEmailIdentitiesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) fn reflens_list_email_identity_certificates_output_output_next_token(
     input: &crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) fn reflens_list_email_templates_output_output_next_token(
     input: &crate::operation::list_email_templates::ListEmailTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -109,6 +120,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) fn reflens_list_export_jobs_output_output_next_token(
     input: &crate::operation::list_export_jobs::ListExportJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -119,6 +131,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) fn reflens_list_import_jobs_output_output_next_token(
     input: &crate::operation::list_import_jobs::ListImportJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -129,6 +142,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) fn reflens_list_multi_region_endpoints_output_output_next_token(
     input: &crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -139,6 +153,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) fn reflens_list_recommendations_output_output_next_token(
     input: &crate::operation::list_recommendations::ListRecommendationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -149,6 +164,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) fn reflens_list_reputation_entities_output_output_next_token(
     input: &crate::operation::list_reputation_entities::ListReputationEntitiesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -159,6 +175,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) fn reflens_list_resource_tenants_output_output_next_token(
     input: &crate::operation::list_resource_tenants::ListResourceTenantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -169,6 +186,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) fn reflens_list_suppressed_destinations_output_output_next_token(
     input: &crate::operation::list_suppressed_destinations::ListSuppressedDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -179,6 +197,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) fn reflens_list_tenant_resources_output_output_next_token(
     input: &crate::operation::list_tenant_resources::ListTenantResourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -189,6 +208,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenants")]
 pub(crate) fn reflens_list_tenants_output_output_next_token(
     input: &crate::operation::list_tenants::ListTenantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -199,6 +219,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) fn lens_list_email_identity_certificates_output_output_certificates(
     input: crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::IdentityCertificate>> {
@@ -206,6 +227,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) fn lens_list_multi_region_endpoints_output_output_multi_region_endpoints(
     input: crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::MultiRegionEndpoint>> {
@@ -213,6 +235,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) fn lens_list_reputation_entities_output_output_reputation_entities(
     input: crate::operation::list_reputation_entities::ListReputationEntitiesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ReputationEntity>> {
@@ -220,6 +243,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) fn lens_list_resource_tenants_output_output_resource_tenants(
     input: crate::operation::list_resource_tenants::ListResourceTenantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ResourceTenantMetadata>> {
@@ -227,6 +251,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) fn lens_list_tenant_resources_output_output_tenant_resources(
     input: crate::operation::list_tenant_resources::ListTenantResourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TenantResource>> {
@@ -234,6 +259,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenants")]
 pub(crate) fn lens_list_tenants_output_output_tenants(
     input: crate::operation::list_tenants::ListTenantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TenantInfo>> {
```

### `src/operation.rs`

```diff
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,350 +1,466 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_associate_email_identity_certificate")]
 /// Types for the `AssociateEmailIdentityCertificate` operation.
 pub mod associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 /// Types for the `BatchGetMetricData` operation.
 pub mod batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 /// Types for the `CancelExportJob` operation.
 pub mod cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 /// Types for the `CreateConfigurationSet` operation.
 pub mod create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 /// Types for the `CreateConfigurationSetEventDestination` operation.
 pub mod create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 /// Types for the `CreateContact` operation.
 pub mod create_contact;

+#[cfg(feature = "op_create_contact_list")]
 /// Types for the `CreateContactList` operation.
 pub mod create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 /// Types for the `CreateCustomVerificationEmailTemplate` operation.
 pub mod create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 /// Types for the `CreateDedicatedIpPool` operation.
 pub mod create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 /// Types for the `CreateDeliverabilityTestReport` operation.
 pub mod create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 /// Types for the `CreateEmailIdentity` operation.
 pub mod create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 /// Types for the `CreateEmailIdentityPolicy` operation.
 pub mod create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 /// Types for the `CreateEmailTemplate` operation.
 pub mod create_email_template;

+#[cfg(feature = "op_create_export_job")]
 /// Types for the `CreateExportJob` operation.
 pub mod create_export_job;

+#[cfg(feature = "op_create_import_job")]
 /// Types for the `CreateImportJob` operation.
 pub mod create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 /// Types for the `CreateMultiRegionEndpoint` operation.
 pub mod create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 /// Types for the `CreateTenant` operation.
 pub mod create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 /// Types for the `CreateTenantResourceAssociation` operation.
 pub mod create_tenant_resource_association;

+#[cfg(feature = "op_delete_configuration_set")]
 /// Types for the `DeleteConfigurationSet` operation.
 pub mod delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 /// Types for the `DeleteConfigurationSetEventDestination` operation.
 pub mod delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 /// Types for the `DeleteContact` operation.
 pub mod delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 /// Types for the `DeleteContactList` operation.
 pub mod delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 /// Types for the `DeleteCustomVerificationEmailTemplate` operation.
 pub mod delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 /// Types for the `DeleteDedicatedIpPool` operation.
 pub mod delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 /// Types for the `DeleteEmailIdentity` operation.
 pub mod delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 /// Types for the `DeleteEmailIdentityPolicy` operation.
 pub mod delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 /// Types for the `DeleteEmailTemplate` operation.
 pub mod delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 /// Types for the `DeleteMultiRegionEndpoint` operation.
 pub mod delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 /// Types for the `DeleteSuppressedDestination` operation.
 pub mod delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 /// Types for the `DeleteTenant` operation.
 pub mod delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 /// Types for the `DeleteTenantResourceAssociation` operation.
 pub mod delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 /// Types for the `DisassociateEmailIdentityCertificate` operation.
 pub mod disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 /// Types for the `GetAccount` operation.
 pub mod get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 /// Types for the `GetBlacklistReports` operation.
 pub mod get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 /// Types for the `GetConfigurationSet` operation.
 pub mod get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 /// Types for the `GetConfigurationSetEventDestinations` operation.
 pub mod get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 /// Types for the `GetContact` operation.
 pub mod get_contact;

+#[cfg(feature = "op_get_contact_list")]
 /// Types for the `GetContactList` operation.
 pub mod get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 /// Types for the `GetCustomVerificationEmailTemplate` operation.
 pub mod get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 /// Types for the `GetDedicatedIp` operation.
 pub mod get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 /// Types for the `GetDedicatedIpPool` operation.
 pub mod get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 /// Types for the `GetDedicatedIps` operation.
 pub mod get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 /// Types for the `GetDeliverabilityDashboardOptions` operation.
 pub mod get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 /// Types for the `GetDeliverabilityTestReport` operation.
 pub mod get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 /// Types for the `GetDomainDeliverabilityCampaign` operation.
 pub mod get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 /// Types for the `GetDomainStatisticsReport` operation.
 pub mod get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 /// Types for the `GetEmailAddressInsights` operation.
 pub mod get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 /// Types for the `GetEmailIdentity` operation.
 pub mod get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 /// Types for the `GetEmailIdentityPolicies` operation.
 pub mod get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 /// Types for the `GetEmailTemplate` operation.
 pub mod get_email_template;

+#[cfg(feature = "op_get_export_job")]
 /// Types for the `GetExportJob` operation.
 pub mod get_export_job;

+#[cfg(feature = "op_get_import_job")]
 /// Types for the `GetImportJob` operation.
 pub mod get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 /// Types for the `GetMessageInsights` operation.
 pub mod get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 /// Types for the `GetMultiRegionEndpoint` operation.
 pub mod get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 /// Types for the `GetReputationEntity` operation.
 pub mod get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 /// Types for the `GetSuppressedDestination` operation.
 pub mod get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 /// Types for the `GetTenant` operation.
 pub mod get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 /// Types for the `ListConfigurationSets` operation.
 pub mod list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 /// Types for the `ListContactLists` operation.
 pub mod list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 /// Types for the `ListContacts` operation.
 pub mod list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 /// Types for the `ListCustomVerificationEmailTemplates` operation.
 pub mod list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 /// Types for the `ListDedicatedIpPools` operation.
 pub mod list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 /// Types for the `ListDeliverabilityTestReports` operation.
 pub mod list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 /// Types for the `ListDomainDeliverabilityCampaigns` operation.
 pub mod list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 /// Types for the `ListEmailIdentities` operation.
 pub mod list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 /// Types for the `ListEmailIdentityCertificates` operation.
 pub mod list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 /// Types for the `ListEmailTemplates` operation.
 pub mod list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 /// Types for the `ListExportJobs` operation.
 pub mod list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 /// Types for the `ListImportJobs` operation.
 pub mod list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 /// Types for the `ListMultiRegionEndpoints` operation.
 pub mod list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 /// Types for the `ListRecommendations` operation.
 pub mod list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 /// Types for the `ListReputationEntities` operation.
 pub mod list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 /// Types for the `ListResourceTenants` operation.
 pub mod list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 /// Types for the `ListSuppressedDestinations` operation.
 pub mod list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 /// Types for the `ListTenantResources` operation.
 pub mod list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 /// Types for the `ListTenants` operation.
 pub mod list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 /// Types for the `PutAccountDedicatedIpWarmupAttributes` operation.
 pub mod put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 /// Types for the `PutAccountDetails` operation.
 pub mod put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 /// Types for the `PutAccountPricingAttributes` operation.
 pub mod put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 /// Types for the `PutAccountSendingAttributes` operation.
 pub mod put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 /// Types for the `PutAccountSuppressionAttributes` operation.
 pub mod put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 /// Types for the `PutAccountVdmAttributes` operation.
 pub mod put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 /// Types for the `PutConfigurationSetArchivingOptions` operation.
 pub mod put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 /// Types for the `PutConfigurationSetDeliveryOptions` operation.
 pub mod put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 /// Types for the `PutConfigurationSetReputationOptions` operation.
 pub mod put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 /// Types for the `PutConfigurationSetSendingOptions` operation.
 pub mod put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 /// Types for the `PutConfigurationSetSuppressionOptions` operation.
 pub mod put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 /// Types for the `PutConfigurationSetTrackingOptions` operation.
 pub mod put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 /// Types for the `PutConfigurationSetVdmOptions` operation.
 pub mod put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 /// Types for the `PutDedicatedIpInPool` operation.
 pub mod put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 /// Types for the `PutDedicatedIpPoolScalingAttributes` operation.
 pub mod put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 /// Types for the `PutDedicatedIpWarmupAttributes` operation.
 pub mod put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 /// Types for the `PutDeliverabilityDashboardOption` operation.
 pub mod put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 /// Types for the `PutEmailIdentityConfigurationSetAttributes` operation.
 pub mod put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 /// Types for the `PutEmailIdentityDkimAttributes` operation.
 pub mod put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 /// Types for the `PutEmailIdentityDkimSigningAttributes` operation.
 pub mod put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 /// Types for the `PutEmailIdentityFeedbackAttributes` operation.
 pub mod put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 /// Types for the `PutEmailIdentityMailFromAttributes` operation.
 pub mod put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 /// Types for the `PutSuppressedDestination` operation.
 pub mod put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 /// Types for the `PutTenantSuppressionAttributes` operation.
 pub mod put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 /// Types for the `SendBulkEmail` operation.
 pub mod send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 /// Types for the `SendCustomVerificationEmail` operation.
 pub mod send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 /// Types for the `SendEmail` operation.
 pub mod send_email;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 /// Types for the `TestRenderEmailTemplate` operation.
 pub mod test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 /// Types for the `UpdateConfigurationSet` operation.
 pub mod update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 /// Types for the `UpdateConfigurationSetEventDestination` operation.
 pub mod update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 /// Types for the `UpdateContact` operation.
 pub mod update_contact;

+#[cfg(feature = "op_update_contact_list")]
 /// Types for the `UpdateContactList` operation.
 pub mod update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 /// Types for the `UpdateCustomVerificationEmailTemplate` operation.
 pub mod update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 /// Types for the `UpdateEmailIdentityPolicy` operation.
 pub mod update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 /// Types for the `UpdateEmailTemplate` operation.
 pub mod update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 /// Types for the `UpdateReputationEntityCustomerManagedStatus` operation.
 pub mod update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 /// Types for the `UpdateReputationEntityPolicy` operation.
 pub mod update_reputation_entity_policy;
```

### `src/protocol_serde.rs`

```diff
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,122 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +135,124 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,238 +264,472 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_associate_email_identity_certificate")]
 pub(crate) mod shape_associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 pub(crate) mod shape_cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 pub(crate) mod shape_create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 pub(crate) mod shape_create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 pub(crate) mod shape_create_contact;

+#[cfg(feature = "op_create_contact_list")]
 pub(crate) mod shape_create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 pub(crate) mod shape_create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 pub(crate) mod shape_create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) mod shape_create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 pub(crate) mod shape_create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 pub(crate) mod shape_create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 pub(crate) mod shape_create_email_template;

+#[cfg(feature = "op_create_export_job")]
 pub(crate) mod shape_create_export_job;

+#[cfg(feature = "op_create_import_job")]
 pub(crate) mod shape_create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 pub(crate) mod shape_create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 pub(crate) mod shape_create_tenant_resource_association;

+#[cfg(feature = "op_delete_configuration_set")]
 pub(crate) mod shape_delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 pub(crate) mod shape_delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 pub(crate) mod shape_delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 pub(crate) mod shape_delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 pub(crate) mod shape_delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 pub(crate) mod shape_delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 pub(crate) mod shape_delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 pub(crate) mod shape_delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 pub(crate) mod shape_delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 pub(crate) mod shape_delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 pub(crate) mod shape_delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 pub(crate) mod shape_delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 pub(crate) mod shape_delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 pub(crate) mod shape_disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 pub(crate) mod shape_get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 pub(crate) mod shape_get_contact;

+#[cfg(feature = "op_get_contact_list")]
 pub(crate) mod shape_get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 pub(crate) mod shape_get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 pub(crate) mod shape_get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) mod shape_get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) mod shape_get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) mod shape_get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 pub(crate) mod shape_get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 pub(crate) mod shape_get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 pub(crate) mod shape_get_email_template;

+#[cfg(feature = "op_get_export_job")]
 pub(crate) mod shape_get_export_job;

+#[cfg(feature = "op_get_import_job")]
 pub(crate) mod shape_get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 pub(crate) mod shape_get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) mod shape_list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) mod shape_list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) mod shape_list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) mod shape_list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 pub(crate) mod shape_put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 pub(crate) mod shape_put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 pub(crate) mod shape_put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 pub(crate) mod shape_put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 pub(crate) mod shape_put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 pub(crate) mod shape_put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 pub(crate) mod shape_put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 pub(crate) mod shape_put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 pub(crate) mod shape_put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 pub(crate) mod shape_put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 pub(crate) mod shape_put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 pub(crate) mod shape_put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 pub(crate) mod shape_put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 pub(crate) mod shape_put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 pub(crate) mod shape_put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 pub(crate) mod shape_put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 pub(crate) mod shape_put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 pub(crate) mod shape_put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 pub(crate) mod shape_put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 pub(crate) mod shape_put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 pub(crate) mod shape_send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_send_email;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) mod shape_test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 pub(crate) mod shape_update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 pub(crate) mod shape_update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 pub(crate) mod shape_update_contact;

+#[cfg(feature = "op_update_contact_list")]
 pub(crate) mod shape_update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 pub(crate) mod shape_update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 pub(crate) mod shape_update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 pub(crate) mod shape_update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 pub(crate) mod shape_update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 pub(crate) mod shape_update_reputation_entity_policy;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -268,522 +738,1364 @@
     }
 }

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_account_suspended_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_already_exists_exception;

+#[cfg(feature = "op_associate_email_identity_certificate")]
 pub(crate) mod shape_associate_email_identity_certificate_input;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_bad_request_exception;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data_input;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub(crate) mod shape_concurrent_modification_exception;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 pub(crate) mod shape_create_configuration_set_event_destination_input;

+#[cfg(feature = "op_create_configuration_set")]
 pub(crate) mod shape_create_configuration_set_input;

+#[cfg(feature = "op_create_contact")]
 pub(crate) mod shape_create_contact_input;

+#[cfg(feature = "op_create_contact_list")]
 pub(crate) mod shape_create_contact_list_input;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 pub(crate) mod shape_create_custom_verification_email_template_input;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 pub(crate) mod shape_create_dedicated_ip_pool_input;

+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) mod shape_create_deliverability_test_report_input;

+#[cfg(feature = "op_create_email_identity")]
 pub(crate) mod shape_create_email_identity_input;

+#[cfg(feature = "op_create_email_identity_policy")]
 pub(crate) mod shape_create_email_identity_policy_input;

+#[cfg(feature = "op_create_email_template")]
 pub(crate) mod shape_create_email_template_input;

+#[cfg(feature = "op_create_export_job")]
 pub(crate) mod shape_create_export_job_input;

+#[cfg(feature = "op_create_import_job")]
 pub(crate) mod shape_create_import_job_input;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_create_multi_region_endpoint_input;

+#[cfg(feature = "op_create_tenant")]
 pub(crate) mod shape_create_tenant_input;

+#[cfg(feature = "op_create_tenant_resource_association")]
 pub(crate) mod shape_create_tenant_resource_association_input;

+#[cfg(feature = "op_delete_tenant")]
 pub(crate) mod shape_delete_tenant_input;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 pub(crate) mod shape_delete_tenant_resource_association_input;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 pub(crate) mod shape_disassociate_email_identity_certificate_input;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_get_email_address_insights_input;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_get_tenant_input;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_internal_service_error_exception;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_invalid_next_token_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts_input;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_list_email_identity_certificates_input;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_list_export_jobs_input;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_list_import_jobs_input;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_list_recommendations_input;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_list_reputation_entities_input;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_list_resource_tenants_input;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_list_tenant_resources_input;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_list_tenants_input;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_mail_from_domain_not_verified_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_rejected;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_account_dedicated_ip_warmup_attributes_input;

+#[cfg(feature = "op_put_account_details")]
 pub(crate) mod shape_put_account_details_input;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 pub(crate) mod shape_put_account_pricing_attributes_input;

+#[cfg(feature = "op_put_account_sending_attributes")]
 pub(crate) mod shape_put_account_sending_attributes_input;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 pub(crate) mod shape_put_account_suppression_attributes_input;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 pub(crate) mod shape_put_account_vdm_attributes_input;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 pub(crate) mod shape_put_configuration_set_archiving_options_input;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 pub(crate) mod shape_put_configuration_set_delivery_options_input;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 pub(crate) mod shape_put_configuration_set_reputation_options_input;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 pub(crate) mod shape_put_configuration_set_sending_options_input;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 pub(crate) mod shape_put_configuration_set_suppression_options_input;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 pub(crate) mod shape_put_configuration_set_tracking_options_input;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 pub(crate) mod shape_put_configuration_set_vdm_options_input;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 pub(crate) mod shape_put_dedicated_ip_in_pool_input;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 pub(crate) mod shape_put_dedicated_ip_pool_scaling_attributes_input;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_dedicated_ip_warmup_attributes_input;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 pub(crate) mod shape_put_deliverability_dashboard_option_input;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 pub(crate) mod shape_put_email_identity_configuration_set_attributes_input;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_attributes_input;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_signing_attributes_input;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 pub(crate) mod shape_put_email_identity_feedback_attributes_input;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 pub(crate) mod shape_put_email_identity_mail_from_attributes_input;

+#[cfg(feature = "op_put_suppressed_destination")]
 pub(crate) mod shape_put_suppressed_destination_input;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 pub(crate) mod shape_put_tenant_suppression_attributes_input;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_send_bulk_email_input;

+#[cfg(feature = "op_send_custom_verification_email")]
 pub(crate) mod shape_send_custom_verification_email_input;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_send_email_input;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_sending_paused_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) mod shape_test_render_email_template_input;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_too_many_requests_exception;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 pub(crate) mod shape_update_configuration_set_event_destination_input;

+#[cfg(feature = "op_update_configuration_set")]
 pub(crate) mod shape_update_configuration_set_input;

+#[cfg(feature = "op_update_contact")]
 pub(crate) mod shape_update_contact_input;

+#[cfg(feature = "op_update_contact_list")]
 pub(crate) mod shape_update_contact_list_input;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 pub(crate) mod shape_update_custom_verification_email_template_input;

+#[cfg(feature = "op_update_email_identity_policy")]
 pub(crate) mod shape_update_email_identity_policy_input;

+#[cfg(feature = "op_update_email_template")]
 pub(crate) mod shape_update_email_template_input;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 pub(crate) mod shape_update_reputation_entity_customer_managed_status_input;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 pub(crate) mod shape_update_reputation_entity_policy_input;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_account_details;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_archiving_options;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data_query;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_report;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry_result_list;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_configuration_overrides;

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) mod shape_configuration_set_name_list;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_custom_verification_email_templates_list;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_daily_volumes;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub(crate) mod shape_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) mod shape_dedicated_ip_list;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) mod shape_dedicated_ip_pool;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub(crate) mod shape_deliverability_test_report;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) mod shape_deliverability_test_reports;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_delivery_options;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_destination;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_details;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub(crate) mod shape_dkim_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub(crate) mod shape_dkim_signing_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub(crate) mod shape_dns_token_list;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_domain_deliverability_campaign;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) mod shape_domain_deliverability_campaign_list;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_domain_deliverability_tracking_option;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) mod shape_domain_deliverability_tracking_options;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_email_content;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_email_insights_list;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub(crate) mod shape_email_template_content;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_email_template_metadata_list;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_event_destination_definition;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_destinations;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_destination;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_export_job_summary_list;

+#[cfg(feature = "op_get_export_job")]
 pub(crate) mod shape_export_statistics;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub(crate) mod shape_failure_info;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_identity_certificate_list;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_identity_info_list;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub(crate) mod shape_import_data_source;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_import_destination;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_import_job_summary_list;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_isp_placements;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts_filter;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_list_management_options;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_list_of_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_of_contacts;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) mod shape_list_of_dedicated_ip_pools;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_mail_from_attributes;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_mailbox_validation;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_message_security_options;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_tag;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_message_tag_list;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_error_list;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_result_list;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_multi_region_endpoints;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_overall_volume;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_placement_statistics;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_get_email_identity_policies"))]
 pub(crate) mod shape_policy_map;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_pricing_attributes;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_recommendations_list;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_reputation_entities_list;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub(crate) mod shape_reputation_entity;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_reputation_options;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_resource_tenant_metadata_list;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_routes;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_send_quota;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_sending_options;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_suppressed_destination;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_suppressed_destination_summaries;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_suppression_attributes;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_suppression_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub(crate) mod shape_suppression_validation_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_validation_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource"
+))]
 pub(crate) mod shape_tag_list;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_tenant;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_tenant_info_list;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_tenant_resource_list;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub(crate) mod shape_tenant_suppression_attributes;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub(crate) mod shape_topic;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub(crate) mod shape_topic_preference;

+#[cfg(any(feature = "op_get_contact", feature = "op_list_contacts"))]
 pub(crate) mod shape_topic_preference_list;

+#[cfg(feature = "op_get_contact_list")]
 pub(crate) mod shape_topics;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_tracking_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_vdm_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_vdm_options;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_verification_info;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_additional_contact_email_addresses;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_entries;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry_result;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_destination;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_contact;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_contact_list;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_contact_list_destination;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_custom_verification_email_template_metadata;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_daily_volume;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_dashboard_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_dashboard_options;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_domain_isp_placements;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_email_address_insights_mailbox_evaluations;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_email_address_insights_verdict;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_email_insights;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_email_template_metadata;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_esps;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_event_bridge_destination;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_destination;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_export_job_summary;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_guardian_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_guardian_options;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_identity_certificate;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_identity_info;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_import_job_summary;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_inbox_placement_tracking_option;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_ip_list;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_isp_placement;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_kinesis_firehose_destination;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_message;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_header;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_message_insights_data_source;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_error;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_result;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_metrics_data_source;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_multi_region_endpoint;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_pinpoint_destination;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_raw_message;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_recommendation;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_replacement_email_content;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_resource_tenant_metadata;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_review_details;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_route;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_route_details;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_sns_destination;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_soa_record;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub(crate) mod shape_status_record;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_suppressed_destination_attributes;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_suppressed_destination_summary;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_condition_threshold;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_suppression_list_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant"
+))]
 pub(crate) mod shape_suppression_list_reasons;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_template;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_tenant_info;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_tenant_resource;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_topic_filter;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_tracking_configuration_overrides;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_volume_statistics;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_attachment;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_entry;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_body;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_dimension_configuration;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_content;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_default_signing_scheme;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_domain_isp_placement;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_types;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_dimensions;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_metric;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_metrics;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_insights_events;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_message_insights_filters;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_value_list;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_regions;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_replacement_template;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_smime_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_confidence_threshold;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_timestamp_list;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_dimension_configurations;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_email_address_filter_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_email_subject_filter_list;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub(crate) mod shape_export_dimension_value;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_insights_event;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_isp_filter_list;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_isp_name_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_last_delivery_event_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_last_engagement_event_list;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_event_details;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_bounce;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_complaint;
```

### `src/serde_util.rs`

```diff
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) fn create_deliverability_test_report_output_output_correct_errors(
     mut builder: crate::operation::create_deliverability_test_report::builders::CreateDeliverabilityTestReportOutputBuilder,
 ) -> crate::operation::create_deliverability_test_report::builders::CreateDeliverabilityTestReportOutputBuilder {
@@ -13,6 +14,7 @@
     builder
 }

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) fn get_blacklist_reports_output_output_correct_errors(
     mut builder: crate::operation::get_blacklist_reports::builders::GetBlacklistReportsOutputBuilder,
 ) -> crate::operation::get_blacklist_reports::builders::GetBlacklistReportsOutputBuilder {
@@ -22,6 +24,7 @@
     builder
 }

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) fn get_deliverability_dashboard_options_output_output_correct_errors(
     mut builder: crate::operation::get_deliverability_dashboard_options::builders::GetDeliverabilityDashboardOptionsOutputBuilder,
 ) -> crate::operation::get_deliverability_dashboard_options::builders::GetDeliverabilityDashboardOptionsOutputBuilder {
@@ -31,6 +34,7 @@
     builder
 }

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) fn get_deliverability_test_report_output_output_correct_errors(
     mut builder: crate::operation::get_deliverability_test_report::builders::GetDeliverabilityTestReportOutputBuilder,
 ) -> crate::operation::get_deliverability_test_report::builders::GetDeliverabilityTestReportOutputBuilder {
@@ -52,6 +56,7 @@
     builder
 }

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 pub(crate) fn get_domain_deliverability_campaign_output_output_correct_errors(
     mut builder: crate::operation::get_domain_deliverability_campaign::builders::GetDomainDeliverabilityCampaignOutputBuilder,
 ) -> crate::operation::get_domain_deliverability_campaign::builders::GetDomainDeliverabilityCampaignOutputBuilder {
@@ -64,6 +69,7 @@
     builder
 }

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) fn get_domain_statistics_report_output_output_correct_errors(
     mut builder: crate::operation::get_domain_statistics_report::builders::GetDomainStatisticsReportOutputBuilder,
 ) -> crate::operation::get_domain_statistics_report::builders::GetDomainStatisticsReportOutputBuilder {
@@ -79,6 +85,7 @@
     builder
 }

+#[cfg(feature = "op_get_email_template")]
 pub(crate) fn get_email_template_output_output_correct_errors(
     mut builder: crate::operation::get_email_template::builders::GetEmailTemplateOutputBuilder,
 ) -> crate::operation::get_email_template::builders::GetEmailTemplateOutputBuilder {
@@ -94,6 +101,7 @@
     builder
 }

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) fn get_suppressed_destination_output_output_correct_errors(
     mut builder: crate::operation::get_suppressed_destination::builders::GetSuppressedDestinationOutputBuilder,
 ) -> crate::operation::get_suppressed_destination::builders::GetSuppressedDestinationOutputBuilder {
@@ -108,6 +116,7 @@
     builder
 }

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) fn list_deliverability_test_reports_output_output_correct_errors(
     mut builder: crate::operation::list_deliverability_test_reports::builders::ListDeliverabilityTestReportsOutputBuilder,
 ) -> crate::operation::list_deliverability_test_reports::builders::ListDeliverabilityTestReportsOutputBuilder {
@@ -117,6 +126,7 @@
     builder
 }

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) fn list_domain_deliverability_campaigns_output_output_correct_errors(
     mut builder: crate::operation::list_domain_deliverability_campaigns::builders::ListDomainDeliverabilityCampaignsOutputBuilder,
 ) -> crate::operation::list_domain_deliverability_campaigns::builders::ListDomainDeliverabilityCampaignsOutputBuilder {
@@ -126,6 +136,7 @@
     builder
 }

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) fn list_tags_for_resource_output_output_correct_errors(
     mut builder: crate::operation::list_tags_for_resource::builders::ListTagsForResourceOutputBuilder,
 ) -> crate::operation::list_tags_for_resource::builders::ListTagsForResourceOutputBuilder {
@@ -135,6 +146,7 @@
     builder
 }

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) fn send_bulk_email_output_output_correct_errors(
     mut builder: crate::operation::send_bulk_email::builders::SendBulkEmailOutputBuilder,
 ) -> crate::operation::send_bulk_email::builders::SendBulkEmailOutputBuilder {
@@ -144,6 +156,7 @@
     builder
 }

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) fn test_render_email_template_output_output_correct_errors(
     mut builder: crate::operation::test_render_email_template::builders::TestRenderEmailTemplateOutputBuilder,
 ) -> crate::operation::test_render_email_template::builders::TestRenderEmailTemplateOutputBuilder {
@@ -153,6 +166,7 @@
     builder
 }

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) fn suppressed_destination_correct_errors(
     mut builder: crate::types::builders::SuppressedDestinationBuilder,
 ) -> crate::types::builders::SuppressedDestinationBuilder {
@@ -168,6 +182,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub(crate) fn dedicated_ip_correct_errors(
     mut builder: crate::types::builders::DedicatedIpBuilder,
 ) -> crate::types::builders::DedicatedIpBuilder {
@@ -183,6 +198,7 @@
     builder
 }

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) fn dedicated_ip_pool_correct_errors(
     mut builder: crate::types::builders::DedicatedIpPoolBuilder,
 ) -> crate::types::builders::DedicatedIpPoolBuilder {
@@ -195,6 +211,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn export_destination_correct_errors(
     mut builder: crate::types::builders::ExportDestinationBuilder,
 ) -> crate::types::builders::ExportDestinationBuilder {
@@ -204,6 +221,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub(crate) fn import_data_source_correct_errors(
     mut builder: crate::types::builders::ImportDataSourceBuilder,
 ) -> crate::types::builders::ImportDataSourceBuilder {
@@ -216,6 +234,7 @@
     builder
 }

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) fn mail_from_attributes_correct_errors(
     mut builder: crate::types::builders::MailFromAttributesBuilder,
 ) -> crate::types::builders::MailFromAttributesBuilder {
@@ -231,6 +250,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) fn tracking_options_correct_errors(
     mut builder: crate::types::builders::TrackingOptionsBuilder,
 ) -> crate::types::builders::TrackingOptionsBuilder {
@@ -240,6 +260,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) fn vdm_attributes_correct_errors(
     mut builder: crate::types::builders::VdmAttributesBuilder,
 ) -> crate::types::builders::VdmAttributesBuilder {
@@ -249,6 +270,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) fn contact_list_destination_correct_errors(
     mut builder: crate::types::builders::ContactListDestinationBuilder,
 ) -> crate::types::builders::ContactListDestinationBuilder {
@@ -261,6 +287,7 @@
     builder
 }

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) fn event_destination_correct_errors(
     mut builder: crate::types::builders::EventDestinationBuilder,
 ) -> crate::types::builders::EventDestinationBuilder {
@@ -273,6 +300,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn message_insights_data_source_correct_errors(
     mut builder: crate::types::builders::MessageInsightsDataSourceBuilder,
 ) -> crate::types::builders::MessageInsightsDataSourceBuilder {
@@ -285,6 +313,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) fn message_tag_correct_errors(
     mut builder: crate::types::builders::MessageTagBuilder,
 ) -> crate::types::builders::MessageTagBuilder {
@@ -297,6 +330,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn metrics_data_source_correct_errors(
     mut builder: crate::types::builders::MetricsDataSourceBuilder,
 ) -> crate::types::builders::MetricsDataSourceBuilder {
@@ -318,6 +352,7 @@
     builder
 }

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) fn route_correct_errors(
     mut builder: crate::types::builders::RouteBuilder,
 ) -> crate::types::builders::RouteBuilder {
@@ -327,6 +362,7 @@
     builder
 }

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) fn suppressed_destination_summary_correct_errors(
     mut builder: crate::types::builders::SuppressedDestinationSummaryBuilder,
 ) -> crate::types::builders::SuppressedDestinationSummaryBuilder {
@@ -342,6 +378,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) fn suppression_list_destination_correct_errors(
     mut builder: crate::types::builders::SuppressionListDestinationBuilder,
 ) -> crate::types::builders::SuppressionListDestinationBuilder {
@@ -353,6 +394,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub(crate) fn suppression_validation_attributes_correct_errors(
     mut builder: crate::types::builders::SuppressionValidationAttributesBuilder,
 ) -> crate::types::builders::SuppressionValidationAttributesBuilder {
@@ -367,6 +409,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_validation_options_correct_errors(
     mut builder: crate::types::builders::SuppressionValidationOptionsBuilder,
 ) -> crate::types::builders::SuppressionValidationOptionsBuilder {
@@ -381,6 +428,26 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
@@ -393,6 +460,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub(crate) fn topic_correct_errors(
     mut builder: crate::types::builders::TopicBuilder,
 ) -> crate::types::builders::TopicBuilder {
@@ -408,6 +480,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub(crate) fn topic_preference_correct_errors(
     mut builder: crate::types::builders::TopicPreferenceBuilder,
 ) -> crate::types::builders::TopicPreferenceBuilder {
@@ -420,6 +498,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn cloud_watch_destination_correct_errors(
     mut builder: crate::types::builders::CloudWatchDestinationBuilder,
 ) -> crate::types::builders::CloudWatchDestinationBuilder {
@@ -429,6 +512,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn event_bridge_destination_correct_errors(
     mut builder: crate::types::builders::EventBridgeDestinationBuilder,
 ) -> crate::types::builders::EventBridgeDestinationBuilder {
@@ -438,6 +526,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn kinesis_firehose_destination_correct_errors(
     mut builder: crate::types::builders::KinesisFirehoseDestinationBuilder,
 ) -> crate::types::builders::KinesisFirehoseDestinationBuilder {
@@ -450,6 +543,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn sns_destination_correct_errors(
     mut builder: crate::types::builders::SnsDestinationBuilder,
 ) -> crate::types::builders::SnsDestinationBuilder {
@@ -459,6 +557,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_condition_threshold_correct_errors(
     mut builder: crate::types::builders::SuppressionConditionThresholdBuilder,
 ) -> crate::types::builders::SuppressionConditionThresholdBuilder {
@@ -468,6 +573,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_confidence_threshold_correct_errors(
     mut builder: crate::types::builders::SuppressionConfidenceThresholdBuilder,
 ) -> crate::types::builders::SuppressionConfidenceThresholdBuilder {
@@ -479,6 +591,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn cloud_watch_dimension_configuration_correct_errors(
     mut builder: crate::types::builders::CloudWatchDimensionConfigurationBuilder,
 ) -> crate::types::builders::CloudWatchDimensionConfigurationBuilder {
```

### `src/types.rs`

```diff
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,706 +1,1654 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_tracking_options::TrackingOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_delivery_options::DeliveryOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_reputation_options::ReputationOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_sending_options::SendingOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_suppression_options::SuppressionOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_vdm_options::VdmOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_archiving_options::ArchivingOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_message_security_options::MessageSecurityOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_destination_definition::EventDestinationDefinition;

+#[cfg(any(
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes"
+))]
 pub use crate::types::_scaling_mode::ScalingMode;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_email_content::EmailContent;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_status::DeliverabilityTestStatus;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes::DkimSigningAttributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_list_email_identities"
+))]
 pub use crate::types::_identity_type::IdentityType;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub use crate::types::_dkim_attributes::DkimAttributes;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::_email_template_content::EmailTemplateContent;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_data_source::ExportDataSource;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_destination::ExportDestination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_import_destination::ImportDestination;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub use crate::types::_import_data_source::ImportDataSource;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_details::Details;

+#[cfg(any(
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_list_multi_region_endpoints"
+))]
 pub use crate::types::_status::Status;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub use crate::types::_tenant_suppression_attributes::TenantSuppressionAttributes;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_tenant",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status"
+))]
 pub use crate::types::_sending_status::SendingStatus;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_send_quota::SendQuota;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_suppression_attributes::SuppressionAttributes;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_account_details::AccountDetails;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_vdm_attributes::VdmAttributes;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_pricing_attributes::PricingAttributes;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_dedicated_ip::DedicatedIp;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub use crate::types::_dedicated_ip_pool::DedicatedIpPool;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub use crate::types::_deliverability_dashboard_account_status::DeliverabilityDashboardAccountStatus;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_report::DeliverabilityTestReport;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_placement_statistics::PlacementStatistics;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub use crate::types::_domain_deliverability_campaign::DomainDeliverabilityCampaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_overall_volume::OverallVolume;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_mailbox_validation::MailboxValidation;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_attributes::MailFromAttributes;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_list_email_identities"))]
 pub use crate::types::_verification_status::VerificationStatus;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_info::VerificationInfo;

+#[cfg(any(feature = "op_get_export_job", feature = "op_list_export_jobs"))]
 pub use crate::types::_export_source_type::ExportSourceType;

+#[cfg(any(
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_job_status::JobStatus;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub use crate::types::_failure_info::FailureInfo;

+#[cfg(feature = "op_get_export_job")]
 pub use crate::types::_export_statistics::ExportStatistics;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::_reputation_entity_type::ReputationEntityType;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_reputation_entity::ReputationEntity;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination::SuppressedDestination;

+#[cfg(feature = "op_get_tenant")]
 pub use crate::types::_tenant::Tenant;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_list_contacts_filter::ListContactsFilter;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_destination_type::ImportDestinationType;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 pub use crate::types::_mail_type::MailType;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 pub use crate::types::_contact_language::ContactLanguage;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_pricing_attributes"))]
 pub use crate::types::_pricing_plan::PricingPlan;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub use crate::types::_suppression_validation_attributes::SuppressionValidationAttributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_delivery_options"
+))]
 pub use crate::types::_tls_policy::TlsPolicy;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 pub use crate::types::_suppression_list_scope::SuppressionListScope;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_validation_options::SuppressionValidationOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_tracking_options"
+))]
 pub use crate::types::_https_policy::HttpsPolicy;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes_origin::DkimSigningAttributesOrigin;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_status::DkimStatus;

+#[cfg(any(
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_mail_from_attributes"
+))]
 pub use crate::types::_behavior_on_mx_failure::BehaviorOnMxFailure;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 pub use crate::types::_suppression_list_reason::SuppressionListReason;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_content::BulkEmailContent;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_configuration_overrides::ConfigurationOverrides;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_destination::Destination;

+#[cfg(feature = "op_send_email")]
 pub use crate::types::_list_management_options::ListManagementOptions;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_batch_get_metric_data_query::BatchGetMetricDataQuery;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_result::MetricDataResult;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_error::MetricDataError;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_dashboard_options::DashboardOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_guardian_options::GuardianOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_signing_scheme::SigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_kinesis_firehose_destination::KinesisFirehoseDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_destination::CloudWatchDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_sns_destination::SnsDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_bridge_destination::EventBridgeDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_pinpoint_destination::PinpointDestination;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub use crate::types::_topic_preference::TopicPreference;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_topic::Topic;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_message::Message;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_raw_message::RawMessage;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_template::Template;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_key_length::DkimSigningKeyLength;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metrics_data_source::MetricsDataSource;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_data_source::MessageInsightsDataSource;

+#[cfg(any(
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job"
+))]
 pub use crate::types::_data_format::DataFormat;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_destination::SuppressionListDestination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_destination::ContactListDestination;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_details::ReviewDetails;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_feature_status::FeatureStatus;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_dashboard_attributes::DashboardAttributes;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_guardian_attributes::GuardianAttributes;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub use crate::types::_event_destination::EventDestination;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_warmup_status::WarmupStatus;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_domain_deliverability_tracking_option::DomainDeliverabilityTrackingOption;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_isp_placement::IspPlacement;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_volume_statistics::VolumeStatistics;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_daily_volume::DailyVolume;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_verdict::EmailAddressInsightsVerdict;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_mailbox_evaluations::EmailAddressInsightsMailboxEvaluations;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_domain_status::MailFromDomainStatus;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_error::VerificationError;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_soa_record::SoaRecord;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_tag::MessageTag;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_email_insights::EmailInsights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub use crate::types::_route::Route;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_status_record::StatusRecord;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities"
+))]
 pub use crate::types::_recommendation_impact::RecommendationImpact;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination_attributes::SuppressedDestinationAttributes;

+#[cfg(feature = "op_list_contact_lists")]
 pub use crate::types::_contact_list::ContactList;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_list_contacts",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_subscription_status::SubscriptionStatus;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_topic_filter::TopicFilter;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_contact::Contact;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub use crate::types::_custom_verification_email_template_metadata::CustomVerificationEmailTemplateMetadata;

+#[cfg(feature = "op_list_email_identities")]
 pub use crate::types::_identity_info::IdentityInfo;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate::IdentityCertificate;

+#[cfg(feature = "op_list_email_templates")]
 pub use crate::types::_email_template_metadata::EmailTemplateMetadata;

+#[cfg(feature = "op_list_export_jobs")]
 pub use crate::types::_export_job_summary::ExportJobSummary;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_job_summary::ImportJobSummary;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub use crate::types::_multi_region_endpoint::MultiRegionEndpoint;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_list_recommendations_filter_key::ListRecommendationsFilterKey;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation::Recommendation;

+#[cfg(feature = "op_list_reputation_entities")]
 pub use crate::types::_reputation_entity_filter_key::ReputationEntityFilterKey;

+#[cfg(feature = "op_list_resource_tenants")]
 pub use crate::types::_resource_tenant_metadata::ResourceTenantMetadata;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::_suppressed_destination_summary::SuppressedDestinationSummary;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_list_tenant_resources_filter_key::ListTenantResourcesFilterKey;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_tenant_resource::TenantResource;

+#[cfg(feature = "op_list_tenants")]
 pub use crate::types::_tenant_info::TenantInfo;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_condition_threshold::SuppressionConditionThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry::BulkEmailEntry;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_tracking_configuration_overrides::TrackingConfigurationOverrides;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry_result::BulkEmailEntryResult;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric_namespace::MetricNamespace;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric::Metric;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_query_error_code::QueryErrorCode;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_default_signing_scheme::DefaultSigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_smime_signing_scheme::SmimeSigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_message_insights",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_type::EventType;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_content::Content;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_body::Body;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_filters::MessageInsightsFilters;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_import_action::SuppressionListImportAction;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_import_action::ContactListImportAction;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_route_details::RouteDetails;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_status::ReviewStatus;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub use crate::types::_blacklist_entry::BlacklistEntry;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_inbox_placement_tracking_option::InboxPlacementTrackingOption;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_domain_isp_placement::DomainIspPlacement;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_confidence_verdict::EmailAddressInsightsConfidenceVerdict;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate_status::IdentityCertificateStatus;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation_type::RecommendationType;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation_status::RecommendationStatus;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_resource_type::ResourceType;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_threshold::SuppressionConfidenceThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_email_content::ReplacementEmailContent;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_status::BulkEmailStatus;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric_dimension_name::MetricDimensionName;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_signature_format::SignatureFormat;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_dimension_configuration::CloudWatchDimensionConfiguration;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_header::MessageHeader;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment::Attachment;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_metric::ExportMetric;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_insights_event::InsightsEvent;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_verdict_threshold::SuppressionConfidenceVerdictThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_template::ReplacementTemplate;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_dimension_value_source::DimensionValueSource;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment_content_disposition::AttachmentContentDisposition;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment_content_transfer_encoding::AttachmentContentTransferEncoding;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metric_aggregation::MetricAggregation;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_delivery_event_type::DeliveryEventType;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_engagement_event_type::EngagementEventType;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_event_details::EventDetails;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce::Bounce;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_complaint::Complaint;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce_type::BounceType;

+#[cfg(feature = "op_get_account")]
 mod _account_details;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _archiving_options;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment_content_disposition;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment_content_transfer_encoding;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _batch_get_metric_data_query;

+#[cfg(any(
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_mail_from_attributes"
+))]
 mod _behavior_on_mx_failure;

+#[cfg(feature = "op_get_blacklist_reports")]
 mod _blacklist_entry;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _body;

+#[cfg(feature = "op_get_message_insights")]
 mod _bounce;

+#[cfg(feature = "op_get_message_insights")]
 mod _bounce_type;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_entry;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_entry_result;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_status;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _cloud_watch_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _cloud_watch_dimension_configuration;

+#[cfg(feature = "op_get_message_insights")]
 mod _complaint;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _configuration_overrides;

+#[cfg(feature = "op_list_contacts")]
 mod _contact;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 mod _contact_language;

+#[cfg(feature = "op_list_contact_lists")]
 mod _contact_list;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _contact_list_destination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _contact_list_import_action;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _content;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 mod _custom_verification_email_template_metadata;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _daily_volume;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _dashboard_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _dashboard_options;

+#[cfg(any(
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job"
+))]
 mod _data_format;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 mod _dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 mod _dedicated_ip_pool;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _default_signing_scheme;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 mod _deliverability_dashboard_account_status;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 mod _deliverability_test_report;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 mod _deliverability_test_status;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _delivery_event_type;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _delivery_options;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _destination;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod _details;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _dimension_value_source;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 mod _dkim_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_attributes_origin;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_key_length;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_status;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 mod _domain_deliverability_campaign;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _domain_deliverability_tracking_option;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _domain_isp_placement;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_confidence_verdict;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_mailbox_evaluations;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_verdict;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _email_content;

+#[cfg(feature = "op_get_message_insights")]
 mod _email_insights;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 mod _email_template_content;

+#[cfg(feature = "op_list_email_templates")]
 mod _email_template_metadata;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _engagement_event_type;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_bridge_destination;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 mod _event_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_destination_definition;

+#[cfg(feature = "op_get_message_insights")]
 mod _event_details;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_message_insights",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_type;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_destination;

+#[cfg(feature = "op_list_export_jobs")]
 mod _export_job_summary;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_metric;

+#[cfg(any(feature = "op_get_export_job", feature = "op_list_export_jobs"))]
 mod _export_source_type;

+#[cfg(feature = "op_get_export_job")]
 mod _export_statistics;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 mod _failure_info;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _feature_status;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _guardian_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _guardian_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_tracking_options"
+))]
 mod _https_policy;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod _identity_certificate;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod _identity_certificate_status;

+#[cfg(feature = "op_list_email_identities")]
 mod _identity_info;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_list_email_identities"
+))]
 mod _identity_type;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 mod _import_data_source;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _import_destination;

+#[cfg(feature = "op_list_import_jobs")]
 mod _import_destination_type;

+#[cfg(feature = "op_list_import_jobs")]
 mod _import_job_summary;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _inbox_placement_tracking_option;

+#[cfg(feature = "op_get_message_insights")]
 mod _insights_event;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod _isp_placement;

+#[cfg(any(
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs"
+))]
 mod _job_status;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _kinesis_firehose_destination;

+#[cfg(feature = "op_list_contacts")]
 mod _list_contacts_filter;

+#[cfg(feature = "op_send_email")]
 mod _list_management_options;

+#[cfg(feature = "op_list_recommendations")]
 mod _list_recommendations_filter_key;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _list_tenant_resources_filter_key;

+#[cfg(feature = "op_get_email_identity")]
 mod _mail_from_attributes;

+#[cfg(feature = "op_get_email_identity")]
 mod _mail_from_domain_status;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 mod _mail_type;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _mailbox_validation;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _message;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _message_header;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _message_insights_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _message_insights_filters;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _message_security_options;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _message_tag;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _metric_aggregation;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _metric_data_error;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _metric_data_result;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric_dimension_name;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric_namespace;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _metrics_data_source;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 mod _multi_region_endpoint;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _overall_volume;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _pinpoint_destination;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod _placement_statistics;

+#[cfg(feature = "op_get_account")]
 mod _pricing_attributes;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_pricing_attributes"))]
 mod _pricing_plan;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _query_error_code;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _raw_message;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities"
+))]
 mod _recommendation_impact;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation_status;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation_type;

+#[cfg(feature = "op_send_bulk_email")]
 mod _replacement_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 mod _replacement_template;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 mod _reputation_entity;

+#[cfg(feature = "op_list_reputation_entities")]
 mod _reputation_entity_filter_key;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _reputation_entity_type;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _reputation_options;

+#[cfg(feature = "op_list_resource_tenants")]
 mod _resource_tenant_metadata;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _resource_type;

+#[cfg(feature = "op_get_account")]
 mod _review_details;

+#[cfg(feature = "op_get_account")]
 mod _review_status;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 mod _route;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod _route_details;

+#[cfg(any(
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes"
+))]
 mod _scaling_mode;

+#[cfg(feature = "op_get_account")]
 mod _send_quota;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _sending_options;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_tenant",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status"
+))]
 mod _sending_status;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _signature_format;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _smime_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _sns_destination;

+#[cfg(feature = "op_get_email_identity")]
 mod _soa_record;

+#[cfg(any(
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_list_multi_region_endpoints"
+))]
 mod _status;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 mod _status_record;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_list_contacts",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 mod _subscription_status;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod _suppressed_destination;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod _suppressed_destination_attributes;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod _suppressed_destination_summary;

+#[cfg(feature = "op_get_account")]
 mod _suppression_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_condition_threshold;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_confidence_threshold;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_confidence_verdict_threshold;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _suppression_list_destination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _suppression_list_import_action;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 mod _suppression_list_reason;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 mod _suppression_list_scope;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _suppression_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 mod _suppression_validation_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_validation_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _template;

+#[cfg(feature = "op_get_tenant")]
 mod _tenant;

+#[cfg(feature = "op_list_tenants")]
 mod _tenant_info;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _tenant_resource;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 mod _tenant_suppression_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_delivery_options"
+))]
 mod _tls_policy;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 mod _topic;

+#[cfg(feature = "op_list_contacts")]
 mod _topic_filter;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 mod _topic_preference;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _tracking_configuration_overrides;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _tracking_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _vdm_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _vdm_options;

+#[cfg(feature = "op_get_email_identity")]
 mod _verification_error;

+#[cfg(feature = "op_get_email_identity")]
 mod _verification_info;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_list_email_identities"))]
 mod _verification_status;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _volume_statistics;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 mod _warmup_status;

 /// Builders
```

### `src/types/builders.rs`

```diff
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,240 +1,505 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_tracking_options::TrackingOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_delivery_options::DeliveryOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_reputation_options::ReputationOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_sending_options::SendingOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_suppression_options::SuppressionOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_vdm_options::VdmOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_archiving_options::ArchivingOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_message_security_options::MessageSecurityOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_destination_definition::EventDestinationDefinitionBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_email_content::EmailContentBuilder;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes::DkimSigningAttributesBuilder;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub use crate::types::_dkim_attributes::DkimAttributesBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::_email_template_content::EmailTemplateContentBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_data_source::ExportDataSourceBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_destination::ExportDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_import_destination::ImportDestinationBuilder;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub use crate::types::_import_data_source::ImportDataSourceBuilder;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_details::DetailsBuilder;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub use crate::types::_tenant_suppression_attributes::TenantSuppressionAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_send_quota::SendQuotaBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_suppression_attributes::SuppressionAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_account_details::AccountDetailsBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_vdm_attributes::VdmAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_pricing_attributes::PricingAttributesBuilder;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_dedicated_ip::DedicatedIpBuilder;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub use crate::types::_dedicated_ip_pool::DedicatedIpPoolBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_report::DeliverabilityTestReportBuilder;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_placement_statistics::PlacementStatisticsBuilder;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub use crate::types::_domain_deliverability_campaign::DomainDeliverabilityCampaignBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_overall_volume::OverallVolumeBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_mailbox_validation::MailboxValidationBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_attributes::MailFromAttributesBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_info::VerificationInfoBuilder;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub use crate::types::_failure_info::FailureInfoBuilder;

+#[cfg(feature = "op_get_export_job")]
 pub use crate::types::_export_statistics::ExportStatisticsBuilder;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_reputation_entity::ReputationEntityBuilder;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination::SuppressedDestinationBuilder;

+#[cfg(feature = "op_get_tenant")]
 pub use crate::types::_tenant::TenantBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_list_contacts_filter::ListContactsFilterBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub use crate::types::_suppression_validation_attributes::SuppressionValidationAttributesBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_validation_options::SuppressionValidationOptionsBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_content::BulkEmailContentBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_configuration_overrides::ConfigurationOverridesBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_destination::DestinationBuilder;

+#[cfg(feature = "op_send_email")]
 pub use crate::types::_list_management_options::ListManagementOptionsBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_batch_get_metric_data_query::BatchGetMetricDataQueryBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_result::MetricDataResultBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_error::MetricDataErrorBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_dashboard_options::DashboardOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_guardian_options::GuardianOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_kinesis_firehose_destination::KinesisFirehoseDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_destination::CloudWatchDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_sns_destination::SnsDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_bridge_destination::EventBridgeDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_pinpoint_destination::PinpointDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub use crate::types::_topic_preference::TopicPreferenceBuilder;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_topic::TopicBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_raw_message::RawMessageBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_template::TemplateBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metrics_data_source::MetricsDataSourceBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_data_source::MessageInsightsDataSourceBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_destination::SuppressionListDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_destination::ContactListDestinationBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_details::ReviewDetailsBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_dashboard_attributes::DashboardAttributesBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_guardian_attributes::GuardianAttributesBuilder;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub use crate::types::_event_destination::EventDestinationBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_domain_deliverability_tracking_option::DomainDeliverabilityTrackingOptionBuilder;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_isp_placement::IspPlacementBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_volume_statistics::VolumeStatisticsBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_daily_volume::DailyVolumeBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_verdict::EmailAddressInsightsVerdictBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_mailbox_evaluations::EmailAddressInsightsMailboxEvaluationsBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_soa_record::SoaRecordBuilder;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_tag::MessageTagBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_email_insights::EmailInsightsBuilder;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub use crate::types::_route::RouteBuilder;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_status_record::StatusRecordBuilder;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination_attributes::SuppressedDestinationAttributesBuilder;

+#[cfg(feature = "op_list_contact_lists")]
 pub use crate::types::_contact_list::ContactListBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_topic_filter::TopicFilterBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_contact::ContactBuilder;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub use crate::types::_custom_verification_email_template_metadata::CustomVerificationEmailTemplateMetadataBuilder;

+#[cfg(feature = "op_list_email_identities")]
 pub use crate::types::_identity_info::IdentityInfoBuilder;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate::IdentityCertificateBuilder;

+#[cfg(feature = "op_list_email_templates")]
 pub use crate::types::_email_template_metadata::EmailTemplateMetadataBuilder;

+#[cfg(feature = "op_list_export_jobs")]
 pub use crate::types::_export_job_summary::ExportJobSummaryBuilder;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_job_summary::ImportJobSummaryBuilder;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub use crate::types::_multi_region_endpoint::MultiRegionEndpointBuilder;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation::RecommendationBuilder;

+#[cfg(feature = "op_list_resource_tenants")]
 pub use crate::types::_resource_tenant_metadata::ResourceTenantMetadataBuilder;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::_suppressed_destination_summary::SuppressedDestinationSummaryBuilder;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_tenant_resource::TenantResourceBuilder;

+#[cfg(feature = "op_list_tenants")]
 pub use crate::types::_tenant_info::TenantInfoBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_condition_threshold::SuppressionConditionThresholdBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry::BulkEmailEntryBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_tracking_configuration_overrides::TrackingConfigurationOverridesBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry_result::BulkEmailEntryResultBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_default_signing_scheme::DefaultSigningSchemeBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_smime_signing_scheme::SmimeSigningSchemeBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_content::ContentBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_body::BodyBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_filters::MessageInsightsFiltersBuilder;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_route_details::RouteDetailsBuilder;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub use crate::types::_blacklist_entry::BlacklistEntryBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_inbox_placement_tracking_option::InboxPlacementTrackingOptionBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_domain_isp_placement::DomainIspPlacementBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_threshold::SuppressionConfidenceThresholdBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_email_content::ReplacementEmailContentBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_dimension_configuration::CloudWatchDimensionConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_header::MessageHeaderBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment::AttachmentBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_metric::ExportMetricBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_insights_event::InsightsEventBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_template::ReplacementTemplateBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_event_details::EventDetailsBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce::BounceBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_complaint::ComplaintBuilder;
```

### `src/types/error.rs`

```diff
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,54 +1,872 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_bad_request_exception::BadRequestException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsException;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::error::_internal_service_error_exception::InternalServiceErrorException;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::error::_concurrent_modification_exception::ConcurrentModificationException;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_account_suspended_exception::AccountSuspendedException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_mail_from_domain_not_verified_exception::MailFromDomainNotVerifiedException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_message_rejected::MessageRejected;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_sending_paused_exception::SendingPausedException;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::error::_invalid_next_token_exception::InvalidNextTokenException;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _account_suspended_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _bad_request_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 mod _concurrent_modification_exception;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _conflict_exception;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _internal_service_error_exception;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod _invalid_next_token_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _mail_from_domain_not_verified_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _message_rejected;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 mod _not_found_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _sending_paused_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _too_many_requests_exception;

 /// Builders
```

### `src/types/error/builders.rs`

```diff
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,26 +1,435 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_bad_request_exception::BadRequestExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsExceptionBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::error::_internal_service_error_exception::InternalServiceErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::error::_concurrent_modification_exception::ConcurrentModificationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_account_suspended_exception::AccountSuspendedExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_mail_from_domain_not_verified_exception::MailFromDomainNotVerifiedExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_message_rejected::MessageRejectedBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_sending_paused_exception::SendingPausedExceptionBuilder;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::error::_invalid_next_token_exception::InvalidNextTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;
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
@@ -84,11 +73,9 @@
 [dependencies.tracing]
 version = "0.1"
 [dev-dependencies.aws-config]
-path = "../aws-config"
 version = "1.12.0"

 [dev-dependencies.aws-credential-types]
-path = "../aws-credential-types"
 features = ["test-util"]
 version = "1.3.0"

@@ -108,3 +95,119 @@
 test-util = ["aws-credential-types/test-util", "aws-smithy-runtime/legacy-test-util", "aws-smithy-runtime/test-util"]
 gated-tests = []
 default = ["sigv4a", "rustls", "default-https-client", "rt-tokio"]
+op_associate_email_identity_certificate = []
+op_batch_get_metric_data = []
+op_cancel_export_job = []
+op_create_configuration_set = []
+op_create_configuration_set_event_destination = []
+op_create_contact = []
+op_create_contact_list = []
+op_create_custom_verification_email_template = []
+op_create_dedicated_ip_pool = []
+op_create_deliverability_test_report = []
+op_create_email_identity = []
+op_create_email_identity_policy = []
+op_create_email_template = []
+op_create_export_job = []
+op_create_import_job = []
+op_create_multi_region_endpoint = []
+op_create_tenant = []
+op_create_tenant_resource_association = []
+op_delete_configuration_set = []
+op_delete_configuration_set_event_destination = []
+op_delete_contact = []
+op_delete_contact_list = []
+op_delete_custom_verification_email_template = []
+op_delete_dedicated_ip_pool = []
+op_delete_email_identity = []
+op_delete_email_identity_policy = []
+op_delete_email_template = []
+op_delete_multi_region_endpoint = []
+op_delete_suppressed_destination = []
+op_delete_tenant = []
+op_delete_tenant_resource_association = []
+op_disassociate_email_identity_certificate = []
+op_get_account = []
+op_get_blacklist_reports = []
+op_get_configuration_set = []
+op_get_configuration_set_event_destinations = []
+op_get_contact = []
+op_get_contact_list = []
+op_get_custom_verification_email_template = []
+op_get_dedicated_ip = []
+op_get_dedicated_ip_pool = []
+op_get_dedicated_ips = []
+op_get_deliverability_dashboard_options = []
+op_get_deliverability_test_report = []
+op_get_domain_deliverability_campaign = []
+op_get_domain_statistics_report = []
+op_get_email_address_insights = []
+op_get_email_identity = []
+op_get_email_identity_policies = []
+op_get_email_template = []
+op_get_export_job = []
+op_get_import_job = []
+op_get_message_insights = []
+op_get_multi_region_endpoint = []
+op_get_reputation_entity = []
+op_get_suppressed_destination = []
+op_get_tenant = []
+op_list_configuration_sets = []
+op_list_contact_lists = []
+op_list_contacts = []
+op_list_custom_verification_email_templates = []
+op_list_dedicated_ip_pools = []
+op_list_deliverability_test_reports = []
+op_list_domain_deliverability_campaigns = []
+op_list_email_identities = []
+op_list_email_identity_certificates = []
+op_list_email_templates = []
+op_list_export_jobs = []
+op_list_import_jobs = []
+op_list_multi_region_endpoints = []
+op_list_recommendations = []
+op_list_reputation_entities = []
+op_list_resource_tenants = []
+op_list_suppressed_destinations = []
+op_list_tags_for_resource = []
+op_list_tenant_resources = []
+op_list_tenants = []
+op_put_account_dedicated_ip_warmup_attributes = []
+op_put_account_details = []
+op_put_account_pricing_attributes = []
+op_put_account_sending_attributes = []
+op_put_account_suppression_attributes = []
+op_put_account_vdm_attributes = []
+op_put_configuration_set_archiving_options = []
+op_put_configuration_set_delivery_options = []
+op_put_configuration_set_reputation_options = []
+op_put_configuration_set_sending_options = []
+op_put_configuration_set_suppression_options = []
+op_put_configuration_set_tracking_options = []
+op_put_configuration_set_vdm_options = []
+op_put_dedicated_ip_in_pool = []
+op_put_dedicated_ip_pool_scaling_attributes = []
+op_put_dedicated_ip_warmup_attributes = []
+op_put_deliverability_dashboard_option = []
+op_put_email_identity_configuration_set_attributes = []
+op_put_email_identity_dkim_attributes = []
+op_put_email_identity_dkim_signing_attributes = []
+op_put_email_identity_feedback_attributes = []
+op_put_email_identity_mail_from_attributes = []
+op_put_suppressed_destination = []
+op_put_tenant_suppression_attributes = []
+op_send_bulk_email = []
+op_send_custom_verification_email = []
+op_send_email = []
+op_tag_resource = []
+op_test_render_email_template = []
+op_untag_resource = []
+op_update_configuration_set = []
+op_update_configuration_set_event_destination = []
+op_update_contact = []
+op_update_contact_list = []
+op_update_custom_verification_email_template = []
+op_update_email_identity_policy = []
+op_update_email_template = []
+op_update_reputation_entity_customer_managed_status = []
+op_update_reputation_entity_policy = []
diff --git a/src/client.rs b/src/client.rs
--- a/src/client.rs
+++ b/src/client.rs
@@ -136,40 +136,58 @@
     }
 }

+#[cfg(feature = "op_associate_email_identity_certificate")]
 mod associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 mod cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 mod create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 mod create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 mod create_contact;

+#[cfg(feature = "op_create_contact_list")]
 mod create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 mod create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 mod create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 mod create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 mod create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 mod create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 mod create_email_template;

+#[cfg(feature = "op_create_export_job")]
 mod create_export_job;

+#[cfg(feature = "op_create_import_job")]
 mod create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 mod create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 mod create_tenant_resource_association;

 /// Operation customization and supporting types.
@@ -199,198 +217,296 @@
 /// ```
 pub mod customize;

+#[cfg(feature = "op_delete_configuration_set")]
 mod delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 mod delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 mod delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 mod delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 mod delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 mod delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 mod delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 mod delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 mod delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 mod delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 mod delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 mod delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 mod delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 mod disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 mod get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 mod get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 mod get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 mod get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 mod get_contact;

+#[cfg(feature = "op_get_contact_list")]
 mod get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 mod get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 mod get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 mod get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 mod get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 mod get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 mod get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 mod get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 mod get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 mod get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 mod get_email_template;

+#[cfg(feature = "op_get_export_job")]
 mod get_export_job;

+#[cfg(feature = "op_get_import_job")]
 mod get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 mod get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 mod get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 mod get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 mod get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 mod list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 mod list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 mod list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 mod list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 mod list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 mod list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 mod list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 mod list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 mod list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 mod list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 mod list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 mod list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 mod list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 mod list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 mod list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 mod list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 mod list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 mod list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 mod put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 mod put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 mod put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 mod put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 mod put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 mod put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 mod put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 mod put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 mod put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 mod put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 mod put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 mod put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 mod put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 mod put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 mod put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 mod put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 mod put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 mod put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 mod put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 mod put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 mod put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 mod put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 mod put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 mod put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 mod send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 mod send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 mod send_email;

+#[cfg(feature = "op_tag_resource")]
 mod tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 mod test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 mod untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 mod update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 mod update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 mod update_contact;

+#[cfg(feature = "op_update_contact_list")]
 mod update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 mod update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 mod update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 mod update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 mod update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 mod update_reputation_entity_policy;
diff --git a/src/error_meta.rs b/src/error_meta.rs
--- a/src/error_meta.rs
+++ b/src/error_meta.rs
@@ -3,30 +3,439 @@
 #[non_exhaustive]
 #[derive(::std::fmt::Debug)]
 pub enum Error {
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the account's ability to send email has been permanently restricted.</p>
     AccountSuspendedException(crate::types::error::AccountSuspendedException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_put_deliverability_dashboard_option"
+    ))]
     /// <p>The resource specified in your request already exists.</p>
     AlreadyExistsException(crate::types::error::AlreadyExistsException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_account",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_address_insights",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_configuration_sets",
+        feature = "op_list_contact_lists",
+        feature = "op_list_contacts",
+        feature = "op_list_custom_verification_email_templates",
+        feature = "op_list_dedicated_ip_pools",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identities",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_email_templates",
+        feature = "op_list_export_jobs",
+        feature = "op_list_import_jobs",
+        feature = "op_list_multi_region_endpoints",
+        feature = "op_list_recommendations",
+        feature = "op_list_reputation_entities",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_list_tenants",
+        feature = "op_put_account_dedicated_ip_warmup_attributes",
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_put_account_sending_attributes",
+        feature = "op_put_account_suppression_attributes",
+        feature = "op_put_account_vdm_attributes",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>The input you provided is invalid.</p>
     BadRequestException(crate::types::error::BadRequestException),
+    #[cfg(any(
+        feature = "op_create_configuration_set",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_tag_resource",
+        feature = "op_untag_resource",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list"
+    ))]
     /// <p>The resource is being modified by another operation or thread.</p>
     ConcurrentModificationException(crate::types::error::ConcurrentModificationException),
+    #[cfg(any(
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>If there is already an ongoing account details update under review.</p>
     ConflictException(crate::types::error::ConflictException),
+    #[cfg(feature = "op_batch_get_metric_data")]
     /// <p>The request couldn't be processed because an error occurred with the Amazon SES API v2.</p>
     InternalServiceErrorException(crate::types::error::InternalServiceErrorException),
+    #[cfg(feature = "op_list_suppressed_destinations")]
     /// <p>The specified request includes an invalid or expired token.</p>
     InvalidNextTokenException(crate::types::error::InvalidNextTokenException),
+    #[cfg(any(
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>There are too many instances of the specified resource type.</p>
     LimitExceededException(crate::types::error::LimitExceededException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the sending domain isn't verified.</p>
     MailFromDomainNotVerifiedException(crate::types::error::MailFromDomainNotVerifiedException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because it contains invalid content.</p>
     MessageRejected(crate::types::error::MessageRejected),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_export_job",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_contacts",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_recommendations",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template"
+    ))]
     /// <p>The resource you attempted to access doesn't exist.</p>
     NotFoundException(crate::types::error::NotFoundException),
+    #[cfg(any(
+        feature = "op_create_deliverability_test_report",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email"
+    ))]
     /// <p>The message can't be sent because the account's ability to send email is currently paused.</p>
     SendingPausedException(crate::types::error::SendingPausedException),
+    #[cfg(any(
+        feature = "op_associate_email_identity_certificate",
+        feature = "op_batch_get_metric_data",
+        feature = "op_cancel_export_job",
+        feature = "op_create_configuration_set",
+        feature = "op_create_configuration_set_event_destination",
+        feature = "op_create_contact",
+        feature = "op_create_contact_list",
+        feature = "op_create_custom_verification_email_template",
+        feature = "op_create_dedicated_ip_pool",
+        feature = "op_create_deliverability_test_report",
+        feature = "op_create_email_identity",
+        feature = "op_create_email_identity_policy",
+        feature = "op_create_email_template",
+        feature = "op_create_export_job",
+        feature = "op_create_import_job",
+        feature = "op_create_multi_region_endpoint",
+        feature = "op_create_tenant",
+        feature = "op_create_tenant_resource_association",
+        feature = "op_delete_configuration_set",
+        feature = "op_delete_configuration_set_event_destination",
+        feature = "op_delete_contact",
+        feature = "op_delete_contact_list",
+        feature = "op_delete_custom_verification_email_template",
+        feature = "op_delete_dedicated_ip_pool",
+        feature = "op_delete_email_identity",
+        feature = "op_delete_email_identity_policy",
+        feature = "op_delete_email_template",
+        feature = "op_delete_multi_region_endpoint",
+        feature = "op_delete_suppressed_destination",
+        feature = "op_delete_tenant",
+        feature = "op_delete_tenant_resource_association",
+        feature = "op_disassociate_email_identity_certificate",
+        feature = "op_get_account",
+        feature = "op_get_blacklist_reports",
+        feature = "op_get_configuration_set",
+        feature = "op_get_configuration_set_event_destinations",
+        feature = "op_get_contact",
+        feature = "op_get_contact_list",
+        feature = "op_get_custom_verification_email_template",
+        feature = "op_get_dedicated_ip",
+        feature = "op_get_dedicated_ip_pool",
+        feature = "op_get_dedicated_ips",
+        feature = "op_get_deliverability_dashboard_options",
+        feature = "op_get_deliverability_test_report",
+        feature = "op_get_domain_deliverability_campaign",
+        feature = "op_get_domain_statistics_report",
+        feature = "op_get_email_address_insights",
+        feature = "op_get_email_identity",
+        feature = "op_get_email_identity_policies",
+        feature = "op_get_email_template",
+        feature = "op_get_export_job",
+        feature = "op_get_import_job",
+        feature = "op_get_message_insights",
+        feature = "op_get_multi_region_endpoint",
+        feature = "op_get_reputation_entity",
+        feature = "op_get_suppressed_destination",
+        feature = "op_get_tenant",
+        feature = "op_list_configuration_sets",
+        feature = "op_list_contact_lists",
+        feature = "op_list_contacts",
+        feature = "op_list_custom_verification_email_templates",
+        feature = "op_list_dedicated_ip_pools",
+        feature = "op_list_deliverability_test_reports",
+        feature = "op_list_domain_deliverability_campaigns",
+        feature = "op_list_email_identities",
+        feature = "op_list_email_identity_certificates",
+        feature = "op_list_email_templates",
+        feature = "op_list_export_jobs",
+        feature = "op_list_import_jobs",
+        feature = "op_list_multi_region_endpoints",
+        feature = "op_list_recommendations",
+        feature = "op_list_reputation_entities",
+        feature = "op_list_resource_tenants",
+        feature = "op_list_suppressed_destinations",
+        feature = "op_list_tags_for_resource",
+        feature = "op_list_tenant_resources",
+        feature = "op_list_tenants",
+        feature = "op_put_account_dedicated_ip_warmup_attributes",
+        feature = "op_put_account_details",
+        feature = "op_put_account_pricing_attributes",
+        feature = "op_put_account_sending_attributes",
+        feature = "op_put_account_suppression_attributes",
+        feature = "op_put_account_vdm_attributes",
+        feature = "op_put_configuration_set_archiving_options",
+        feature = "op_put_configuration_set_delivery_options",
+        feature = "op_put_configuration_set_reputation_options",
+        feature = "op_put_configuration_set_sending_options",
+        feature = "op_put_configuration_set_suppression_options",
+        feature = "op_put_configuration_set_tracking_options",
+        feature = "op_put_configuration_set_vdm_options",
+        feature = "op_put_dedicated_ip_in_pool",
+        feature = "op_put_dedicated_ip_pool_scaling_attributes",
+        feature = "op_put_dedicated_ip_warmup_attributes",
+        feature = "op_put_deliverability_dashboard_option",
+        feature = "op_put_email_identity_configuration_set_attributes",
+        feature = "op_put_email_identity_dkim_attributes",
+        feature = "op_put_email_identity_dkim_signing_attributes",
+        feature = "op_put_email_identity_feedback_attributes",
+        feature = "op_put_email_identity_mail_from_attributes",
+        feature = "op_put_suppressed_destination",
+        feature = "op_put_tenant_suppression_attributes",
+        feature = "op_send_bulk_email",
+        feature = "op_send_custom_verification_email",
+        feature = "op_send_email",
+        feature = "op_tag_resource",
+        feature = "op_test_render_email_template",
+        feature = "op_untag_resource",
+        feature = "op_update_configuration_set",
+        feature = "op_update_configuration_set_event_destination",
+        feature = "op_update_contact",
+        feature = "op_update_contact_list",
+        feature = "op_update_custom_verification_email_template",
+        feature = "op_update_email_identity_policy",
+        feature = "op_update_email_template",
+        feature = "op_update_reputation_entity_customer_managed_status",
+        feature = "op_update_reputation_entity_policy"
+    ))]
     /// <p>Too many requests have been made to the operation.</p>
     TooManyRequestsException(crate::types::error::TooManyRequestsException),
     /// An unexpected error occurred (e.g., invalid JSON returned by the service or an unknown error code).
@@ -43,18 +452,427 @@
 impl ::std::fmt::Display for Error {
     fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Error::AccountSuspendedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Error::AlreadyExistsException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::BadRequestException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Error::ConcurrentModificationException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::ConflictException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Error::InternalServiceErrorException(inner) => inner.fmt(f),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Error::InvalidNextTokenException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::LimitExceededException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MailFromDomainNotVerifiedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MessageRejected(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Error::NotFoundException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::SendingPausedException(inner) => inner.fmt(f),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::TooManyRequestsException(inner) => inner.fmt(f),
             Error::Unhandled(_) => {
                 if let ::std::option::Option::Some(code) =
@@ -79,23 +897,433 @@
 impl ::aws_smithy_types::error::metadata::ProvideErrorMetadata for Error {
     fn meta(&self) -> &::aws_smithy_types::error::metadata::ErrorMetadata {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Self::AccountSuspendedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Self::AlreadyExistsException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::BadRequestException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Self::ConcurrentModificationException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::ConflictException(inner) => inner.meta(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Self::InternalServiceErrorException(inner) => inner.meta(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Self::InvalidNextTokenException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::LimitExceededException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MailFromDomainNotVerifiedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MessageRejected(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Self::NotFoundException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::SendingPausedException(inner) => inner.meta(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::TooManyRequestsException(inner) => inner.meta(),
             Self::Unhandled(inner) => &inner.meta,
         }
     }
 }
+#[cfg(feature = "op_associate_email_identity_certificate")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -121,6 +1349,7 @@
         }
     }
 }
+#[cfg(feature = "op_associate_email_identity_certificate")]
 impl From<crate::operation::associate_email_identity_certificate::AssociateEmailIdentityCertificateError> for Error {
     fn from(
         err: crate::operation::associate_email_identity_certificate::AssociateEmailIdentityCertificateError,
@@ -144,6 +1373,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_metric_data")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -169,6 +1399,7 @@
         }
     }
 }
+#[cfg(feature = "op_batch_get_metric_data")]
 impl From<crate::operation::batch_get_metric_data::BatchGetMetricDataError> for Error {
     fn from(err: crate::operation::batch_get_metric_data::BatchGetMetricDataError) -> Self {
         match err {
@@ -190,6 +1421,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -215,6 +1447,7 @@
         }
     }
 }
+#[cfg(feature = "op_cancel_export_job")]
 impl From<crate::operation::cancel_export_job::CancelExportJobError> for Error {
     fn from(err: crate::operation::cancel_export_job::CancelExportJobError) -> Self {
         match err {
@@ -231,6 +1464,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -256,6 +1490,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set")]
 impl From<crate::operation::create_configuration_set::CreateConfigurationSetError> for Error {
     fn from(err: crate::operation::create_configuration_set::CreateConfigurationSetError) -> Self {
         match err {
@@ -277,6 +1512,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -302,6 +1538,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_configuration_set_event_destination")]
 impl From<crate::operation::create_configuration_set_event_destination::CreateConfigurationSetEventDestinationError>
     for Error
 {
@@ -330,6 +1567,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_contact::CreateContactError, R>>
     for Error
@@ -351,6 +1589,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact")]
 impl From<crate::operation::create_contact::CreateContactError> for Error {
     fn from(err: crate::operation::create_contact::CreateContactError) -> Self {
         match err {
@@ -370,6 +1609,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -395,6 +1635,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_contact_list")]
 impl From<crate::operation::create_contact_list::CreateContactListError> for Error {
     fn from(err: crate::operation::create_contact_list::CreateContactListError) -> Self {
         match err {
@@ -414,6 +1655,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -439,6 +1681,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_custom_verification_email_template")]
 impl From<crate::operation::create_custom_verification_email_template::CreateCustomVerificationEmailTemplateError>
     for Error
 {
@@ -467,6 +1710,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -492,6 +1736,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_dedicated_ip_pool")]
 impl From<crate::operation::create_dedicated_ip_pool::CreateDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::create_dedicated_ip_pool::CreateDedicatedIpPoolError) -> Self {
         match err {
@@ -516,6 +1761,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_deliverability_test_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -541,6 +1787,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_deliverability_test_report")]
 impl From<crate::operation::create_deliverability_test_report::CreateDeliverabilityTestReportError> for Error {
     fn from(err: crate::operation::create_deliverability_test_report::CreateDeliverabilityTestReportError) -> Self {
         match err {
@@ -575,6 +1822,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -600,6 +1848,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity")]
 impl From<crate::operation::create_email_identity::CreateEmailIdentityError> for Error {
     fn from(err: crate::operation::create_email_identity::CreateEmailIdentityError) -> Self {
         match err {
@@ -627,6 +1876,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -652,6 +1902,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_identity_policy")]
 impl From<crate::operation::create_email_identity_policy::CreateEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::create_email_identity_policy::CreateEmailIdentityPolicyError) -> Self {
         match err {
@@ -674,6 +1925,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -699,6 +1951,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_email_template")]
 impl From<crate::operation::create_email_template::CreateEmailTemplateError> for Error {
     fn from(err: crate::operation::create_email_template::CreateEmailTemplateError) -> Self {
         match err {
@@ -720,6 +1973,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -745,6 +1999,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_export_job")]
 impl From<crate::operation::create_export_job::CreateExportJobError> for Error {
     fn from(err: crate::operation::create_export_job::CreateExportJobError) -> Self {
         match err {
@@ -764,6 +2019,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_job")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -789,6 +2045,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_import_job")]
 impl From<crate::operation::create_import_job::CreateImportJobError> for Error {
     fn from(err: crate::operation::create_import_job::CreateImportJobError) -> Self {
         match err {
@@ -805,6 +2062,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -830,6 +2088,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_multi_region_endpoint")]
 impl From<crate::operation::create_multi_region_endpoint::CreateMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::create_multi_region_endpoint::CreateMultiRegionEndpointError) -> Self {
         match err {
@@ -849,6 +2108,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::create_tenant::CreateTenantError, R>>
     for Error
 where
@@ -866,6 +2126,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant")]
 impl From<crate::operation::create_tenant::CreateTenantError> for Error {
     fn from(err: crate::operation::create_tenant::CreateTenantError) -> Self {
         match err {
@@ -885,6 +2146,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant_resource_association")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -910,6 +2172,7 @@
         }
     }
 }
+#[cfg(feature = "op_create_tenant_resource_association")]
 impl From<crate::operation::create_tenant_resource_association::CreateTenantResourceAssociationError> for Error {
     fn from(err: crate::operation::create_tenant_resource_association::CreateTenantResourceAssociationError) -> Self {
         match err {
@@ -929,6 +2192,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -954,6 +2218,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set")]
 impl From<crate::operation::delete_configuration_set::DeleteConfigurationSetError> for Error {
     fn from(err: crate::operation::delete_configuration_set::DeleteConfigurationSetError) -> Self {
         match err {
@@ -969,6 +2234,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -994,6 +2260,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 impl From<crate::operation::delete_configuration_set_event_destination::DeleteConfigurationSetEventDestinationError>
     for Error
 {
@@ -1016,6 +2283,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_contact::DeleteContactError, R>>
     for Error
@@ -1037,6 +2305,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact")]
 impl From<crate::operation::delete_contact::DeleteContactError> for Error {
     fn from(err: crate::operation::delete_contact::DeleteContactError) -> Self {
         match err {
@@ -1053,6 +2322,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1078,6 +2348,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_contact_list")]
 impl From<crate::operation::delete_contact_list::DeleteContactListError> for Error {
     fn from(err: crate::operation::delete_contact_list::DeleteContactListError) -> Self {
         match err {
@@ -1097,6 +2368,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1122,6 +2394,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_custom_verification_email_template")]
 impl From<crate::operation::delete_custom_verification_email_template::DeleteCustomVerificationEmailTemplateError>
     for Error
 {
@@ -1144,6 +2417,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1169,6 +2443,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 impl From<crate::operation::delete_dedicated_ip_pool::DeleteDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::delete_dedicated_ip_pool::DeleteDedicatedIpPoolError) -> Self {
         match err {
@@ -1190,6 +2465,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1215,6 +2491,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity")]
 impl From<crate::operation::delete_email_identity::DeleteEmailIdentityError> for Error {
     fn from(err: crate::operation::delete_email_identity::DeleteEmailIdentityError) -> Self {
         match err {
@@ -1236,6 +2513,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1261,6 +2539,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_identity_policy")]
 impl From<crate::operation::delete_email_identity_policy::DeleteEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::delete_email_identity_policy::DeleteEmailIdentityPolicyError) -> Self {
         match err {
@@ -1277,6 +2556,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1302,6 +2582,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_email_template")]
 impl From<crate::operation::delete_email_template::DeleteEmailTemplateError> for Error {
     fn from(err: crate::operation::delete_email_template::DeleteEmailTemplateError) -> Self {
         match err {
@@ -1320,6 +2601,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1345,6 +2627,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_multi_region_endpoint")]
 impl From<crate::operation::delete_multi_region_endpoint::DeleteMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::delete_multi_region_endpoint::DeleteMultiRegionEndpointError) -> Self {
         match err {
@@ -1364,6 +2647,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1389,6 +2673,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_suppressed_destination")]
 impl From<crate::operation::delete_suppressed_destination::DeleteSuppressedDestinationError> for Error {
     fn from(err: crate::operation::delete_suppressed_destination::DeleteSuppressedDestinationError) -> Self {
         match err {
@@ -1405,6 +2690,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::delete_tenant::DeleteTenantError, R>>
     for Error
 where
@@ -1422,6 +2708,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant")]
 impl From<crate::operation::delete_tenant::DeleteTenantError> for Error {
     fn from(err: crate::operation::delete_tenant::DeleteTenantError) -> Self {
         match err {
@@ -1438,6 +2725,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant_resource_association")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1463,6 +2751,7 @@
         }
     }
 }
+#[cfg(feature = "op_delete_tenant_resource_association")]
 impl From<crate::operation::delete_tenant_resource_association::DeleteTenantResourceAssociationError> for Error {
     fn from(err: crate::operation::delete_tenant_resource_association::DeleteTenantResourceAssociationError) -> Self {
         match err {
@@ -1479,6 +2768,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1504,6 +2794,7 @@
         }
     }
 }
+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 impl From<crate::operation::disassociate_email_identity_certificate::DisassociateEmailIdentityCertificateError>
     for Error
 {
@@ -1526,6 +2817,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_account")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_account::GetAccountError, R>>
     for Error
 where
@@ -1543,6 +2835,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_account")]
 impl From<crate::operation::get_account::GetAccountError> for Error {
     fn from(err: crate::operation::get_account::GetAccountError) -> Self {
         match err {
@@ -1556,6 +2849,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_blacklist_reports")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1581,6 +2875,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_blacklist_reports")]
 impl From<crate::operation::get_blacklist_reports::GetBlacklistReportsError> for Error {
     fn from(err: crate::operation::get_blacklist_reports::GetBlacklistReportsError) -> Self {
         match err {
@@ -1599,6 +2894,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1624,6 +2920,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set")]
 impl From<crate::operation::get_configuration_set::GetConfigurationSetError> for Error {
     fn from(err: crate::operation::get_configuration_set::GetConfigurationSetError) -> Self {
         match err {
@@ -1642,6 +2939,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1667,6 +2965,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 impl From<crate::operation::get_configuration_set_event_destinations::GetConfigurationSetEventDestinationsError>
     for Error
 {
@@ -1689,6 +2988,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_contact::GetContactError, R>>
     for Error
 where
@@ -1706,6 +3006,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact")]
 impl From<crate::operation::get_contact::GetContactError> for Error {
     fn from(err: crate::operation::get_contact::GetContactError) -> Self {
         match err {
@@ -1720,6 +3021,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact_list")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_contact_list::GetContactListError, R>>
     for Error
@@ -1741,6 +3043,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_contact_list")]
 impl From<crate::operation::get_contact_list::GetContactListError> for Error {
     fn from(err: crate::operation::get_contact_list::GetContactListError) -> Self {
         match err {
@@ -1757,6 +3060,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1782,6 +3086,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_custom_verification_email_template")]
 impl From<crate::operation::get_custom_verification_email_template::GetCustomVerificationEmailTemplateError> for Error {
     fn from(
         err: crate::operation::get_custom_verification_email_template::GetCustomVerificationEmailTemplateError,
@@ -1802,6 +3107,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_dedicated_ip::GetDedicatedIpError, R>>
     for Error
@@ -1823,6 +3129,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip")]
 impl From<crate::operation::get_dedicated_ip::GetDedicatedIpError> for Error {
     fn from(err: crate::operation::get_dedicated_ip::GetDedicatedIpError) -> Self {
         match err {
@@ -1839,6 +3146,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1864,6 +3172,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ip_pool")]
 impl From<crate::operation::get_dedicated_ip_pool::GetDedicatedIpPoolError> for Error {
     fn from(err: crate::operation::get_dedicated_ip_pool::GetDedicatedIpPoolError) -> Self {
         match err {
@@ -1882,6 +3191,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ips")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1907,6 +3217,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_dedicated_ips")]
 impl From<crate::operation::get_dedicated_ips::GetDedicatedIpsError> for Error {
     fn from(err: crate::operation::get_dedicated_ips::GetDedicatedIpsError) -> Self {
         match err {
@@ -1923,6 +3234,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1948,6 +3260,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 impl From<crate::operation::get_deliverability_dashboard_options::GetDeliverabilityDashboardOptionsError> for Error {
     fn from(
         err: crate::operation::get_deliverability_dashboard_options::GetDeliverabilityDashboardOptionsError,
@@ -1968,6 +3281,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_test_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -1993,6 +3307,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_deliverability_test_report")]
 impl From<crate::operation::get_deliverability_test_report::GetDeliverabilityTestReportError> for Error {
     fn from(err: crate::operation::get_deliverability_test_report::GetDeliverabilityTestReportError) -> Self {
         match err {
@@ -2009,6 +3324,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2034,6 +3350,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 impl From<crate::operation::get_domain_deliverability_campaign::GetDomainDeliverabilityCampaignError> for Error {
     fn from(err: crate::operation::get_domain_deliverability_campaign::GetDomainDeliverabilityCampaignError) -> Self {
         match err {
@@ -2050,6 +3367,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_statistics_report")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2075,6 +3393,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_domain_statistics_report")]
 impl From<crate::operation::get_domain_statistics_report::GetDomainStatisticsReportError> for Error {
     fn from(err: crate::operation::get_domain_statistics_report::GetDomainStatisticsReportError) -> Self {
         match err {
@@ -2091,6 +3410,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_address_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2116,6 +3436,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_address_insights")]
 impl From<crate::operation::get_email_address_insights::GetEmailAddressInsightsError> for Error {
     fn from(err: crate::operation::get_email_address_insights::GetEmailAddressInsightsError) -> Self {
         match err {
@@ -2131,6 +3452,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2156,6 +3478,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity")]
 impl From<crate::operation::get_email_identity::GetEmailIdentityError> for Error {
     fn from(err: crate::operation::get_email_identity::GetEmailIdentityError) -> Self {
         match err {
@@ -2172,6 +3495,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity_policies")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2197,6 +3521,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_identity_policies")]
 impl From<crate::operation::get_email_identity_policies::GetEmailIdentityPoliciesError> for Error {
     fn from(err: crate::operation::get_email_identity_policies::GetEmailIdentityPoliciesError) -> Self {
         match err {
@@ -2215,6 +3540,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2240,6 +3566,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_email_template")]
 impl From<crate::operation::get_email_template::GetEmailTemplateError> for Error {
     fn from(err: crate::operation::get_email_template::GetEmailTemplateError) -> Self {
         match err {
@@ -2256,6 +3583,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_export_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_export_job::GetExportJobError, R>>
     for Error
 where
@@ -2273,6 +3601,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_export_job")]
 impl From<crate::operation::get_export_job::GetExportJobError> for Error {
     fn from(err: crate::operation::get_export_job::GetExportJobError) -> Self {
         match err {
@@ -2289,6 +3618,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_import_job")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_import_job::GetImportJobError, R>>
     for Error
 where
@@ -2306,6 +3636,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_import_job")]
 impl From<crate::operation::get_import_job::GetImportJobError> for Error {
     fn from(err: crate::operation::get_import_job::GetImportJobError) -> Self {
         match err {
@@ -2322,6 +3653,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_message_insights")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2347,6 +3679,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_message_insights")]
 impl From<crate::operation::get_message_insights::GetMessageInsightsError> for Error {
     fn from(err: crate::operation::get_message_insights::GetMessageInsightsError) -> Self {
         match err {
@@ -2365,6 +3698,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_multi_region_endpoint")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2390,6 +3724,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_multi_region_endpoint")]
 impl From<crate::operation::get_multi_region_endpoint::GetMultiRegionEndpointError> for Error {
     fn from(err: crate::operation::get_multi_region_endpoint::GetMultiRegionEndpointError) -> Self {
         match err {
@@ -2408,6 +3743,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_reputation_entity")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2433,6 +3769,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_reputation_entity")]
 impl From<crate::operation::get_reputation_entity::GetReputationEntityError> for Error {
     fn from(err: crate::operation::get_reputation_entity::GetReputationEntityError) -> Self {
         match err {
@@ -2451,6 +3788,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2476,6 +3814,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_suppressed_destination")]
 impl From<crate::operation::get_suppressed_destination::GetSuppressedDestinationError> for Error {
     fn from(err: crate::operation::get_suppressed_destination::GetSuppressedDestinationError) -> Self {
         match err {
@@ -2494,6 +3833,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_tenant")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::get_tenant::GetTenantError, R>>
     for Error
 where
@@ -2511,6 +3851,7 @@
         }
     }
 }
+#[cfg(feature = "op_get_tenant")]
 impl From<crate::operation::get_tenant::GetTenantError> for Error {
     fn from(err: crate::operation::get_tenant::GetTenantError) -> Self {
         match err {
@@ -2525,6 +3866,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_configuration_sets")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2550,6 +3892,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_configuration_sets")]
 impl From<crate::operation::list_configuration_sets::ListConfigurationSetsError> for Error {
     fn from(err: crate::operation::list_configuration_sets::ListConfigurationSetsError) -> Self {
         match err {
@@ -2565,6 +3908,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contact_lists")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2590,6 +3934,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contact_lists")]
 impl From<crate::operation::list_contact_lists::ListContactListsError> for Error {
     fn from(err: crate::operation::list_contact_lists::ListContactListsError) -> Self {
         match err {
@@ -2603,6 +3948,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contacts")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_contacts::ListContactsError, R>>
     for Error
 where
@@ -2620,6 +3966,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_contacts")]
 impl From<crate::operation::list_contacts::ListContactsError> for Error {
     fn from(err: crate::operation::list_contacts::ListContactsError) -> Self {
         match err {
@@ -2636,6 +3983,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_custom_verification_email_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2661,6 +4009,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_custom_verification_email_templates")]
 impl From<crate::operation::list_custom_verification_email_templates::ListCustomVerificationEmailTemplatesError>
     for Error
 {
@@ -2680,6 +4029,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dedicated_ip_pools")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2705,6 +4055,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_dedicated_ip_pools")]
 impl From<crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsError> for Error {
     fn from(err: crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsError) -> Self {
         match err {
@@ -2720,6 +4071,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_deliverability_test_reports")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2745,6 +4097,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_deliverability_test_reports")]
 impl From<crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsError> for Error {
     fn from(err: crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsError) -> Self {
         match err {
@@ -2761,6 +4114,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2786,6 +4140,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 impl From<crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsError> for Error {
     fn from(
         err: crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsError,
@@ -2806,6 +4161,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identities")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2831,6 +4187,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identities")]
 impl From<crate::operation::list_email_identities::ListEmailIdentitiesError> for Error {
     fn from(err: crate::operation::list_email_identities::ListEmailIdentitiesError) -> Self {
         match err {
@@ -2846,6 +4203,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identity_certificates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2871,6 +4229,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_identity_certificates")]
 impl From<crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesError> for Error {
     fn from(err: crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesError) -> Self {
         match err {
@@ -2887,6 +4246,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_templates")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -2912,6 +4272,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_email_templates")]
 impl From<crate::operation::list_email_templates::ListEmailTemplatesError> for Error {
     fn from(err: crate::operation::list_email_templates::ListEmailTemplatesError) -> Self {
         match err {
@@ -2927,6 +4288,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_export_jobs")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_export_jobs::ListExportJobsError, R>>
     for Error
@@ -2948,6 +4310,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_export_jobs")]
 impl From<crate::operation::list_export_jobs::ListExportJobsError> for Error {
     fn from(err: crate::operation::list_export_jobs::ListExportJobsError) -> Self {
         match err {
@@ -2961,6 +4324,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_import_jobs")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_import_jobs::ListImportJobsError, R>>
     for Error
@@ -2982,6 +4346,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_import_jobs")]
 impl From<crate::operation::list_import_jobs::ListImportJobsError> for Error {
     fn from(err: crate::operation::list_import_jobs::ListImportJobsError) -> Self {
         match err {
@@ -2995,6 +4360,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_multi_region_endpoints")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3020,6 +4386,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_multi_region_endpoints")]
 impl From<crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsError> for Error {
     fn from(err: crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsError) -> Self {
         match err {
@@ -3035,6 +4402,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_recommendations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3060,6 +4428,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_recommendations")]
 impl From<crate::operation::list_recommendations::ListRecommendationsError> for Error {
     fn from(err: crate::operation::list_recommendations::ListRecommendationsError) -> Self {
         match err {
@@ -3078,6 +4447,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_reputation_entities")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3103,6 +4473,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_reputation_entities")]
 impl From<crate::operation::list_reputation_entities::ListReputationEntitiesError> for Error {
     fn from(err: crate::operation::list_reputation_entities::ListReputationEntitiesError) -> Self {
         match err {
@@ -3118,6 +4489,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tenants")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3143,6 +4515,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_resource_tenants")]
 impl From<crate::operation::list_resource_tenants::ListResourceTenantsError> for Error {
     fn from(err: crate::operation::list_resource_tenants::ListResourceTenantsError) -> Self {
         match err {
@@ -3161,6 +4534,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_suppressed_destinations")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3186,6 +4560,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_suppressed_destinations")]
 impl From<crate::operation::list_suppressed_destinations::ListSuppressedDestinationsError> for Error {
     fn from(err: crate::operation::list_suppressed_destinations::ListSuppressedDestinationsError) -> Self {
         match err {
@@ -3205,6 +4580,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3230,6 +4606,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tags_for_resource")]
 impl From<crate::operation::list_tags_for_resource::ListTagsForResourceError> for Error {
     fn from(err: crate::operation::list_tags_for_resource::ListTagsForResourceError) -> Self {
         match err {
@@ -3248,6 +4625,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenant_resources")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3273,6 +4651,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenant_resources")]
 impl From<crate::operation::list_tenant_resources::ListTenantResourcesError> for Error {
     fn from(err: crate::operation::list_tenant_resources::ListTenantResourcesError) -> Self {
         match err {
@@ -3291,6 +4670,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenants")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::list_tenants::ListTenantsError, R>>
     for Error
 where
@@ -3308,6 +4688,7 @@
         }
     }
 }
+#[cfg(feature = "op_list_tenants")]
 impl From<crate::operation::list_tenants::ListTenantsError> for Error {
     fn from(err: crate::operation::list_tenants::ListTenantsError) -> Self {
         match err {
@@ -3321,6 +4702,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3346,6 +4728,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 impl From<crate::operation::put_account_dedicated_ip_warmup_attributes::PutAccountDedicatedIpWarmupAttributesError>
     for Error
 {
@@ -3365,6 +4748,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_details")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3390,6 +4774,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_details")]
 impl From<crate::operation::put_account_details::PutAccountDetailsError> for Error {
     fn from(err: crate::operation::put_account_details::PutAccountDetailsError) -> Self {
         match err {
@@ -3406,6 +4791,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_pricing_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3431,6 +4817,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_pricing_attributes")]
 impl From<crate::operation::put_account_pricing_attributes::PutAccountPricingAttributesError> for Error {
     fn from(err: crate::operation::put_account_pricing_attributes::PutAccountPricingAttributesError) -> Self {
         match err {
@@ -3447,6 +4834,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_sending_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3472,6 +4860,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_sending_attributes")]
 impl From<crate::operation::put_account_sending_attributes::PutAccountSendingAttributesError> for Error {
     fn from(err: crate::operation::put_account_sending_attributes::PutAccountSendingAttributesError) -> Self {
         match err {
@@ -3485,6 +4874,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_suppression_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3510,6 +4900,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_suppression_attributes")]
 impl From<crate::operation::put_account_suppression_attributes::PutAccountSuppressionAttributesError> for Error {
     fn from(err: crate::operation::put_account_suppression_attributes::PutAccountSuppressionAttributesError) -> Self {
         match err {
@@ -3523,6 +4914,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_vdm_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3548,6 +4940,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_account_vdm_attributes")]
 impl From<crate::operation::put_account_vdm_attributes::PutAccountVdmAttributesError> for Error {
     fn from(err: crate::operation::put_account_vdm_attributes::PutAccountVdmAttributesError) -> Self {
         match err {
@@ -3563,6 +4956,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3588,6 +4982,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 impl From<crate::operation::put_configuration_set_archiving_options::PutConfigurationSetArchivingOptionsError>
     for Error
 {
@@ -3610,6 +5005,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3635,6 +5031,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 impl From<crate::operation::put_configuration_set_delivery_options::PutConfigurationSetDeliveryOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_delivery_options::PutConfigurationSetDeliveryOptionsError,
@@ -3655,6 +5052,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3680,6 +5078,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 impl From<crate::operation::put_configuration_set_reputation_options::PutConfigurationSetReputationOptionsError>
     for Error
 {
@@ -3702,6 +5101,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_sending_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3727,6 +5127,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_sending_options")]
 impl From<crate::operation::put_configuration_set_sending_options::PutConfigurationSetSendingOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_sending_options::PutConfigurationSetSendingOptionsError,
@@ -3747,6 +5148,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3772,6 +5174,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 impl From<crate::operation::put_configuration_set_suppression_options::PutConfigurationSetSuppressionOptionsError>
     for Error
 {
@@ -3794,6 +5197,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3819,6 +5223,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 impl From<crate::operation::put_configuration_set_tracking_options::PutConfigurationSetTrackingOptionsError> for Error {
     fn from(
         err: crate::operation::put_configuration_set_tracking_options::PutConfigurationSetTrackingOptionsError,
@@ -3839,6 +5244,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3864,6 +5270,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 impl From<crate::operation::put_configuration_set_vdm_options::PutConfigurationSetVdmOptionsError> for Error {
     fn from(err: crate::operation::put_configuration_set_vdm_options::PutConfigurationSetVdmOptionsError) -> Self {
         match err {
@@ -3880,6 +5287,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3905,6 +5313,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 impl From<crate::operation::put_dedicated_ip_in_pool::PutDedicatedIpInPoolError> for Error {
     fn from(err: crate::operation::put_dedicated_ip_in_pool::PutDedicatedIpInPoolError) -> Self {
         match err {
@@ -3923,6 +5332,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3948,6 +5358,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 impl From<crate::operation::put_dedicated_ip_pool_scaling_attributes::PutDedicatedIpPoolScalingAttributesError>
     for Error
 {
@@ -3973,6 +5384,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -3998,6 +5410,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 impl From<crate::operation::put_dedicated_ip_warmup_attributes::PutDedicatedIpWarmupAttributesError> for Error {
     fn from(err: crate::operation::put_dedicated_ip_warmup_attributes::PutDedicatedIpWarmupAttributesError) -> Self {
         match err {
@@ -4014,6 +5427,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4039,6 +5453,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 impl From<crate::operation::put_deliverability_dashboard_option::PutDeliverabilityDashboardOptionError> for Error {
     fn from(err: crate::operation::put_deliverability_dashboard_option::PutDeliverabilityDashboardOptionError) -> Self {
         match err {
@@ -4061,6 +5476,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4086,6 +5502,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 impl From<crate::operation::put_email_identity_configuration_set_attributes::PutEmailIdentityConfigurationSetAttributesError> for Error {
     fn from(err: crate::operation::put_email_identity_configuration_set_attributes::PutEmailIdentityConfigurationSetAttributesError) -> Self {
         match err {
@@ -4096,6 +5513,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4121,6 +5539,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 impl From<crate::operation::put_email_identity_dkim_attributes::PutEmailIdentityDkimAttributesError> for Error {
     fn from(err: crate::operation::put_email_identity_dkim_attributes::PutEmailIdentityDkimAttributesError) -> Self {
         match err {
@@ -4137,6 +5556,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4162,6 +5582,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 impl From<crate::operation::put_email_identity_dkim_signing_attributes::PutEmailIdentityDkimSigningAttributesError>
     for Error
 {
@@ -4184,6 +5605,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4209,6 +5631,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 impl From<crate::operation::put_email_identity_feedback_attributes::PutEmailIdentityFeedbackAttributesError> for Error {
     fn from(
         err: crate::operation::put_email_identity_feedback_attributes::PutEmailIdentityFeedbackAttributesError,
@@ -4229,6 +5652,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4254,6 +5678,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 impl From<crate::operation::put_email_identity_mail_from_attributes::PutEmailIdentityMailFromAttributesError>
     for Error
 {
@@ -4276,6 +5701,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_suppressed_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4301,6 +5727,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_suppressed_destination")]
 impl From<crate::operation::put_suppressed_destination::PutSuppressedDestinationError> for Error {
     fn from(err: crate::operation::put_suppressed_destination::PutSuppressedDestinationError) -> Self {
         match err {
@@ -4319,6 +5746,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4344,6 +5772,7 @@
         }
     }
 }
+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 impl From<crate::operation::put_tenant_suppression_attributes::PutTenantSuppressionAttributesError> for Error {
     fn from(err: crate::operation::put_tenant_suppression_attributes::PutTenantSuppressionAttributesError) -> Self {
         match err {
@@ -4360,6 +5789,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_bulk_email")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_bulk_email::SendBulkEmailError, R>>
     for Error
@@ -4381,6 +5811,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_bulk_email")]
 impl From<crate::operation::send_bulk_email::SendBulkEmailError> for Error {
     fn from(err: crate::operation::send_bulk_email::SendBulkEmailError) -> Self {
         match err {
@@ -4412,6 +5843,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_custom_verification_email")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4437,6 +5869,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_custom_verification_email")]
 impl From<crate::operation::send_custom_verification_email::SendCustomVerificationEmailError> for Error {
     fn from(err: crate::operation::send_custom_verification_email::SendCustomVerificationEmailError) -> Self {
         match err {
@@ -4465,6 +5898,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_email")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::send_email::SendEmailError, R>>
     for Error
 where
@@ -4482,6 +5916,7 @@
         }
     }
 }
+#[cfg(feature = "op_send_email")]
 impl From<crate::operation::send_email::SendEmailError> for Error {
     fn from(err: crate::operation::send_email::SendEmailError) -> Self {
         match err {
@@ -4509,6 +5944,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl<R> From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::tag_resource::TagResourceError, R>>
     for Error
 where
@@ -4526,6 +5962,7 @@
         }
     }
 }
+#[cfg(feature = "op_tag_resource")]
 impl From<crate::operation::tag_resource::TagResourceError> for Error {
     fn from(err: crate::operation::tag_resource::TagResourceError) -> Self {
         match err {
@@ -4545,6 +5982,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_render_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4570,6 +6008,7 @@
         }
     }
 }
+#[cfg(feature = "op_test_render_email_template")]
 impl From<crate::operation::test_render_email_template::TestRenderEmailTemplateError> for Error {
     fn from(err: crate::operation::test_render_email_template::TestRenderEmailTemplateError) -> Self {
         match err {
@@ -4588,6 +6027,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::untag_resource::UntagResourceError, R>>
     for Error
@@ -4609,6 +6049,7 @@
         }
     }
 }
+#[cfg(feature = "op_untag_resource")]
 impl From<crate::operation::untag_resource::UntagResourceError> for Error {
     fn from(err: crate::operation::untag_resource::UntagResourceError) -> Self {
         match err {
@@ -4628,6 +6069,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4653,6 +6095,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set")]
 impl From<crate::operation::update_configuration_set::UpdateConfigurationSetError> for Error {
     fn from(err: crate::operation::update_configuration_set::UpdateConfigurationSetError) -> Self {
         match err {
@@ -4671,6 +6114,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set_event_destination")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4696,6 +6140,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_configuration_set_event_destination")]
 impl From<crate::operation::update_configuration_set_event_destination::UpdateConfigurationSetEventDestinationError>
     for Error
 {
@@ -4718,6 +6163,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact")]
 impl<R>
     From<::aws_smithy_runtime_api::client::result::SdkError<crate::operation::update_contact::UpdateContactError, R>>
     for Error
@@ -4739,6 +6185,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact")]
 impl From<crate::operation::update_contact::UpdateContactError> for Error {
     fn from(err: crate::operation::update_contact::UpdateContactError) -> Self {
         match err {
@@ -4758,6 +6205,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact_list")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4783,6 +6231,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_contact_list")]
 impl From<crate::operation::update_contact_list::UpdateContactListError> for Error {
     fn from(err: crate::operation::update_contact_list::UpdateContactListError) -> Self {
         match err {
@@ -4802,6 +6251,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_verification_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4827,6 +6277,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_custom_verification_email_template")]
 impl From<crate::operation::update_custom_verification_email_template::UpdateCustomVerificationEmailTemplateError>
     for Error
 {
@@ -4849,6 +6300,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_identity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4874,6 +6326,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_identity_policy")]
 impl From<crate::operation::update_email_identity_policy::UpdateEmailIdentityPolicyError> for Error {
     fn from(err: crate::operation::update_email_identity_policy::UpdateEmailIdentityPolicyError) -> Self {
         match err {
@@ -4890,6 +6343,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_template")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4915,6 +6369,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_email_template")]
 impl From<crate::operation::update_email_template::UpdateEmailTemplateError> for Error {
     fn from(err: crate::operation::update_email_template::UpdateEmailTemplateError) -> Self {
         match err {
@@ -4933,6 +6388,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4958,6 +6414,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 impl From<crate::operation::update_reputation_entity_customer_managed_status::UpdateReputationEntityCustomerManagedStatusError> for Error {
     fn from(err: crate::operation::update_reputation_entity_customer_managed_status::UpdateReputationEntityCustomerManagedStatusError) -> Self {
         match err {
@@ -4968,6 +6425,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_policy")]
 impl<R>
     From<
         ::aws_smithy_runtime_api::client::result::SdkError<
@@ -4993,6 +6451,7 @@
         }
     }
 }
+#[cfg(feature = "op_update_reputation_entity_policy")]
 impl From<crate::operation::update_reputation_entity_policy::UpdateReputationEntityPolicyError> for Error {
     fn from(err: crate::operation::update_reputation_entity_policy::UpdateReputationEntityPolicyError) -> Self {
         match err {
@@ -5012,18 +6471,427 @@
 impl ::std::error::Error for Error {
     fn source(&self) -> std::option::Option<&(dyn ::std::error::Error + 'static)> {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Error::AccountSuspendedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Error::AlreadyExistsException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::BadRequestException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Error::ConcurrentModificationException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::ConflictException(inner) => inner.source(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Error::InternalServiceErrorException(inner) => inner.source(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Error::InvalidNextTokenException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::LimitExceededException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MailFromDomainNotVerifiedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::MessageRejected(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Error::NotFoundException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Error::SendingPausedException(inner) => inner.source(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Error::TooManyRequestsException(inner) => inner.source(),
             Error::Unhandled(inner) => ::std::option::Option::Some(&*inner.source),
         }
@@ -5032,18 +6900,427 @@
 impl ::aws_types::request_id::RequestId for Error {
     fn request_id(&self) -> Option<&str> {
         match self {
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_email"
+            ))]
             Self::AccountSuspendedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_put_deliverability_dashboard_option"
+            ))]
             Self::AlreadyExistsException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::BadRequestException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_tag_resource",
+                feature = "op_untag_resource",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list"
+            ))]
             Self::ConcurrentModificationException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::ConflictException(e) => e.request_id(),
+            #[cfg(feature = "op_batch_get_metric_data")]
             Self::InternalServiceErrorException(e) => e.request_id(),
+            #[cfg(feature = "op_list_suppressed_destinations")]
             Self::InvalidNextTokenException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::LimitExceededException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MailFromDomainNotVerifiedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::MessageRejected(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_export_job",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_contacts",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_recommendations",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template"
+            ))]
             Self::NotFoundException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_create_deliverability_test_report",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email"
+            ))]
             Self::SendingPausedException(e) => e.request_id(),
+            #[cfg(any(
+                feature = "op_associate_email_identity_certificate",
+                feature = "op_batch_get_metric_data",
+                feature = "op_cancel_export_job",
+                feature = "op_create_configuration_set",
+                feature = "op_create_configuration_set_event_destination",
+                feature = "op_create_contact",
+                feature = "op_create_contact_list",
+                feature = "op_create_custom_verification_email_template",
+                feature = "op_create_dedicated_ip_pool",
+                feature = "op_create_deliverability_test_report",
+                feature = "op_create_email_identity",
+                feature = "op_create_email_identity_policy",
+                feature = "op_create_email_template",
+                feature = "op_create_export_job",
+                feature = "op_create_import_job",
+                feature = "op_create_multi_region_endpoint",
+                feature = "op_create_tenant",
+                feature = "op_create_tenant_resource_association",
+                feature = "op_delete_configuration_set",
+                feature = "op_delete_configuration_set_event_destination",
+                feature = "op_delete_contact",
+                feature = "op_delete_contact_list",
+                feature = "op_delete_custom_verification_email_template",
+                feature = "op_delete_dedicated_ip_pool",
+                feature = "op_delete_email_identity",
+                feature = "op_delete_email_identity_policy",
+                feature = "op_delete_email_template",
+                feature = "op_delete_multi_region_endpoint",
+                feature = "op_delete_suppressed_destination",
+                feature = "op_delete_tenant",
+                feature = "op_delete_tenant_resource_association",
+                feature = "op_disassociate_email_identity_certificate",
+                feature = "op_get_account",
+                feature = "op_get_blacklist_reports",
+                feature = "op_get_configuration_set",
+                feature = "op_get_configuration_set_event_destinations",
+                feature = "op_get_contact",
+                feature = "op_get_contact_list",
+                feature = "op_get_custom_verification_email_template",
+                feature = "op_get_dedicated_ip",
+                feature = "op_get_dedicated_ip_pool",
+                feature = "op_get_dedicated_ips",
+                feature = "op_get_deliverability_dashboard_options",
+                feature = "op_get_deliverability_test_report",
+                feature = "op_get_domain_deliverability_campaign",
+                feature = "op_get_domain_statistics_report",
+                feature = "op_get_email_address_insights",
+                feature = "op_get_email_identity",
+                feature = "op_get_email_identity_policies",
+                feature = "op_get_email_template",
+                feature = "op_get_export_job",
+                feature = "op_get_import_job",
+                feature = "op_get_message_insights",
+                feature = "op_get_multi_region_endpoint",
+                feature = "op_get_reputation_entity",
+                feature = "op_get_suppressed_destination",
+                feature = "op_get_tenant",
+                feature = "op_list_configuration_sets",
+                feature = "op_list_contact_lists",
+                feature = "op_list_contacts",
+                feature = "op_list_custom_verification_email_templates",
+                feature = "op_list_dedicated_ip_pools",
+                feature = "op_list_deliverability_test_reports",
+                feature = "op_list_domain_deliverability_campaigns",
+                feature = "op_list_email_identities",
+                feature = "op_list_email_identity_certificates",
+                feature = "op_list_email_templates",
+                feature = "op_list_export_jobs",
+                feature = "op_list_import_jobs",
+                feature = "op_list_multi_region_endpoints",
+                feature = "op_list_recommendations",
+                feature = "op_list_reputation_entities",
+                feature = "op_list_resource_tenants",
+                feature = "op_list_suppressed_destinations",
+                feature = "op_list_tags_for_resource",
+                feature = "op_list_tenant_resources",
+                feature = "op_list_tenants",
+                feature = "op_put_account_dedicated_ip_warmup_attributes",
+                feature = "op_put_account_details",
+                feature = "op_put_account_pricing_attributes",
+                feature = "op_put_account_sending_attributes",
+                feature = "op_put_account_suppression_attributes",
+                feature = "op_put_account_vdm_attributes",
+                feature = "op_put_configuration_set_archiving_options",
+                feature = "op_put_configuration_set_delivery_options",
+                feature = "op_put_configuration_set_reputation_options",
+                feature = "op_put_configuration_set_sending_options",
+                feature = "op_put_configuration_set_suppression_options",
+                feature = "op_put_configuration_set_tracking_options",
+                feature = "op_put_configuration_set_vdm_options",
+                feature = "op_put_dedicated_ip_in_pool",
+                feature = "op_put_dedicated_ip_pool_scaling_attributes",
+                feature = "op_put_dedicated_ip_warmup_attributes",
+                feature = "op_put_deliverability_dashboard_option",
+                feature = "op_put_email_identity_configuration_set_attributes",
+                feature = "op_put_email_identity_dkim_attributes",
+                feature = "op_put_email_identity_dkim_signing_attributes",
+                feature = "op_put_email_identity_feedback_attributes",
+                feature = "op_put_email_identity_mail_from_attributes",
+                feature = "op_put_suppressed_destination",
+                feature = "op_put_tenant_suppression_attributes",
+                feature = "op_send_bulk_email",
+                feature = "op_send_custom_verification_email",
+                feature = "op_send_email",
+                feature = "op_tag_resource",
+                feature = "op_test_render_email_template",
+                feature = "op_untag_resource",
+                feature = "op_update_configuration_set",
+                feature = "op_update_configuration_set_event_destination",
+                feature = "op_update_contact",
+                feature = "op_update_contact_list",
+                feature = "op_update_custom_verification_email_template",
+                feature = "op_update_email_identity_policy",
+                feature = "op_update_email_template",
+                feature = "op_update_reputation_entity_customer_managed_status",
+                feature = "op_update_reputation_entity_policy"
+            ))]
             Self::TooManyRequestsException(e) => e.request_id(),
             Self::Unhandled(e) => e.meta.request_id(),
         }
diff --git a/src/lens.rs b/src/lens.rs
--- a/src/lens.rs
+++ b/src/lens.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) fn reflens_get_dedicated_ips_output_output_next_token(
     input: &crate::operation::get_dedicated_ips::GetDedicatedIpsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -9,6 +10,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) fn reflens_list_configuration_sets_output_output_next_token(
     input: &crate::operation::list_configuration_sets::ListConfigurationSetsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -19,6 +21,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) fn reflens_list_contact_lists_output_output_next_token(
     input: &crate::operation::list_contact_lists::ListContactListsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -29,6 +32,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_contacts")]
 pub(crate) fn reflens_list_contacts_output_output_next_token(
     input: &crate::operation::list_contacts::ListContactsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -39,6 +43,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) fn reflens_list_custom_verification_email_templates_output_output_next_token(
     input: &crate::operation::list_custom_verification_email_templates::ListCustomVerificationEmailTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -49,6 +54,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) fn reflens_list_dedicated_ip_pools_output_output_next_token(
     input: &crate::operation::list_dedicated_ip_pools::ListDedicatedIpPoolsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -59,6 +65,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) fn reflens_list_deliverability_test_reports_output_output_next_token(
     input: &crate::operation::list_deliverability_test_reports::ListDeliverabilityTestReportsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -69,6 +76,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) fn reflens_list_domain_deliverability_campaigns_output_output_next_token(
     input: &crate::operation::list_domain_deliverability_campaigns::ListDomainDeliverabilityCampaignsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -79,6 +87,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) fn reflens_list_email_identities_output_output_next_token(
     input: &crate::operation::list_email_identities::ListEmailIdentitiesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -89,6 +98,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) fn reflens_list_email_identity_certificates_output_output_next_token(
     input: &crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -99,6 +109,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) fn reflens_list_email_templates_output_output_next_token(
     input: &crate::operation::list_email_templates::ListEmailTemplatesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -109,6 +120,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) fn reflens_list_export_jobs_output_output_next_token(
     input: &crate::operation::list_export_jobs::ListExportJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -119,6 +131,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) fn reflens_list_import_jobs_output_output_next_token(
     input: &crate::operation::list_import_jobs::ListImportJobsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -129,6 +142,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) fn reflens_list_multi_region_endpoints_output_output_next_token(
     input: &crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -139,6 +153,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) fn reflens_list_recommendations_output_output_next_token(
     input: &crate::operation::list_recommendations::ListRecommendationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -149,6 +164,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) fn reflens_list_reputation_entities_output_output_next_token(
     input: &crate::operation::list_reputation_entities::ListReputationEntitiesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -159,6 +175,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) fn reflens_list_resource_tenants_output_output_next_token(
     input: &crate::operation::list_resource_tenants::ListResourceTenantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -169,6 +186,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) fn reflens_list_suppressed_destinations_output_output_next_token(
     input: &crate::operation::list_suppressed_destinations::ListSuppressedDestinationsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -179,6 +197,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) fn reflens_list_tenant_resources_output_output_next_token(
     input: &crate::operation::list_tenant_resources::ListTenantResourcesOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -189,6 +208,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenants")]
 pub(crate) fn reflens_list_tenants_output_output_next_token(
     input: &crate::operation::list_tenants::ListTenantsOutput,
 ) -> ::std::option::Option<&::std::string::String> {
@@ -199,6 +219,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) fn lens_list_email_identity_certificates_output_output_certificates(
     input: crate::operation::list_email_identity_certificates::ListEmailIdentityCertificatesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::IdentityCertificate>> {
@@ -206,6 +227,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) fn lens_list_multi_region_endpoints_output_output_multi_region_endpoints(
     input: crate::operation::list_multi_region_endpoints::ListMultiRegionEndpointsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::MultiRegionEndpoint>> {
@@ -213,6 +235,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) fn lens_list_reputation_entities_output_output_reputation_entities(
     input: crate::operation::list_reputation_entities::ListReputationEntitiesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ReputationEntity>> {
@@ -220,6 +243,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) fn lens_list_resource_tenants_output_output_resource_tenants(
     input: crate::operation::list_resource_tenants::ListResourceTenantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::ResourceTenantMetadata>> {
@@ -227,6 +251,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) fn lens_list_tenant_resources_output_output_tenant_resources(
     input: crate::operation::list_tenant_resources::ListTenantResourcesOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TenantResource>> {
@@ -234,6 +259,7 @@
     ::std::option::Option::Some(input)
 }

+#[cfg(feature = "op_list_tenants")]
 pub(crate) fn lens_list_tenants_output_output_tenants(
     input: crate::operation::list_tenants::ListTenantsOutput,
 ) -> ::std::option::Option<::std::vec::Vec<crate::types::TenantInfo>> {
diff --git a/src/operation.rs b/src/operation.rs
--- a/src/operation.rs
+++ b/src/operation.rs
@@ -1,350 +1,466 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
 pub use ::aws_types::request_id::RequestId;

+#[cfg(feature = "op_associate_email_identity_certificate")]
 /// Types for the `AssociateEmailIdentityCertificate` operation.
 pub mod associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 /// Types for the `BatchGetMetricData` operation.
 pub mod batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 /// Types for the `CancelExportJob` operation.
 pub mod cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 /// Types for the `CreateConfigurationSet` operation.
 pub mod create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 /// Types for the `CreateConfigurationSetEventDestination` operation.
 pub mod create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 /// Types for the `CreateContact` operation.
 pub mod create_contact;

+#[cfg(feature = "op_create_contact_list")]
 /// Types for the `CreateContactList` operation.
 pub mod create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 /// Types for the `CreateCustomVerificationEmailTemplate` operation.
 pub mod create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 /// Types for the `CreateDedicatedIpPool` operation.
 pub mod create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 /// Types for the `CreateDeliverabilityTestReport` operation.
 pub mod create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 /// Types for the `CreateEmailIdentity` operation.
 pub mod create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 /// Types for the `CreateEmailIdentityPolicy` operation.
 pub mod create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 /// Types for the `CreateEmailTemplate` operation.
 pub mod create_email_template;

+#[cfg(feature = "op_create_export_job")]
 /// Types for the `CreateExportJob` operation.
 pub mod create_export_job;

+#[cfg(feature = "op_create_import_job")]
 /// Types for the `CreateImportJob` operation.
 pub mod create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 /// Types for the `CreateMultiRegionEndpoint` operation.
 pub mod create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 /// Types for the `CreateTenant` operation.
 pub mod create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 /// Types for the `CreateTenantResourceAssociation` operation.
 pub mod create_tenant_resource_association;

+#[cfg(feature = "op_delete_configuration_set")]
 /// Types for the `DeleteConfigurationSet` operation.
 pub mod delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 /// Types for the `DeleteConfigurationSetEventDestination` operation.
 pub mod delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 /// Types for the `DeleteContact` operation.
 pub mod delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 /// Types for the `DeleteContactList` operation.
 pub mod delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 /// Types for the `DeleteCustomVerificationEmailTemplate` operation.
 pub mod delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 /// Types for the `DeleteDedicatedIpPool` operation.
 pub mod delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 /// Types for the `DeleteEmailIdentity` operation.
 pub mod delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 /// Types for the `DeleteEmailIdentityPolicy` operation.
 pub mod delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 /// Types for the `DeleteEmailTemplate` operation.
 pub mod delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 /// Types for the `DeleteMultiRegionEndpoint` operation.
 pub mod delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 /// Types for the `DeleteSuppressedDestination` operation.
 pub mod delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 /// Types for the `DeleteTenant` operation.
 pub mod delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 /// Types for the `DeleteTenantResourceAssociation` operation.
 pub mod delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 /// Types for the `DisassociateEmailIdentityCertificate` operation.
 pub mod disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 /// Types for the `GetAccount` operation.
 pub mod get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 /// Types for the `GetBlacklistReports` operation.
 pub mod get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 /// Types for the `GetConfigurationSet` operation.
 pub mod get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 /// Types for the `GetConfigurationSetEventDestinations` operation.
 pub mod get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 /// Types for the `GetContact` operation.
 pub mod get_contact;

+#[cfg(feature = "op_get_contact_list")]
 /// Types for the `GetContactList` operation.
 pub mod get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 /// Types for the `GetCustomVerificationEmailTemplate` operation.
 pub mod get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 /// Types for the `GetDedicatedIp` operation.
 pub mod get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 /// Types for the `GetDedicatedIpPool` operation.
 pub mod get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 /// Types for the `GetDedicatedIps` operation.
 pub mod get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 /// Types for the `GetDeliverabilityDashboardOptions` operation.
 pub mod get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 /// Types for the `GetDeliverabilityTestReport` operation.
 pub mod get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 /// Types for the `GetDomainDeliverabilityCampaign` operation.
 pub mod get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 /// Types for the `GetDomainStatisticsReport` operation.
 pub mod get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 /// Types for the `GetEmailAddressInsights` operation.
 pub mod get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 /// Types for the `GetEmailIdentity` operation.
 pub mod get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 /// Types for the `GetEmailIdentityPolicies` operation.
 pub mod get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 /// Types for the `GetEmailTemplate` operation.
 pub mod get_email_template;

+#[cfg(feature = "op_get_export_job")]
 /// Types for the `GetExportJob` operation.
 pub mod get_export_job;

+#[cfg(feature = "op_get_import_job")]
 /// Types for the `GetImportJob` operation.
 pub mod get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 /// Types for the `GetMessageInsights` operation.
 pub mod get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 /// Types for the `GetMultiRegionEndpoint` operation.
 pub mod get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 /// Types for the `GetReputationEntity` operation.
 pub mod get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 /// Types for the `GetSuppressedDestination` operation.
 pub mod get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 /// Types for the `GetTenant` operation.
 pub mod get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 /// Types for the `ListConfigurationSets` operation.
 pub mod list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 /// Types for the `ListContactLists` operation.
 pub mod list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 /// Types for the `ListContacts` operation.
 pub mod list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 /// Types for the `ListCustomVerificationEmailTemplates` operation.
 pub mod list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 /// Types for the `ListDedicatedIpPools` operation.
 pub mod list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 /// Types for the `ListDeliverabilityTestReports` operation.
 pub mod list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 /// Types for the `ListDomainDeliverabilityCampaigns` operation.
 pub mod list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 /// Types for the `ListEmailIdentities` operation.
 pub mod list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 /// Types for the `ListEmailIdentityCertificates` operation.
 pub mod list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 /// Types for the `ListEmailTemplates` operation.
 pub mod list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 /// Types for the `ListExportJobs` operation.
 pub mod list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 /// Types for the `ListImportJobs` operation.
 pub mod list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 /// Types for the `ListMultiRegionEndpoints` operation.
 pub mod list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 /// Types for the `ListRecommendations` operation.
 pub mod list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 /// Types for the `ListReputationEntities` operation.
 pub mod list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 /// Types for the `ListResourceTenants` operation.
 pub mod list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 /// Types for the `ListSuppressedDestinations` operation.
 pub mod list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 /// Types for the `ListTagsForResource` operation.
 pub mod list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 /// Types for the `ListTenantResources` operation.
 pub mod list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 /// Types for the `ListTenants` operation.
 pub mod list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 /// Types for the `PutAccountDedicatedIpWarmupAttributes` operation.
 pub mod put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 /// Types for the `PutAccountDetails` operation.
 pub mod put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 /// Types for the `PutAccountPricingAttributes` operation.
 pub mod put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 /// Types for the `PutAccountSendingAttributes` operation.
 pub mod put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 /// Types for the `PutAccountSuppressionAttributes` operation.
 pub mod put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 /// Types for the `PutAccountVdmAttributes` operation.
 pub mod put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 /// Types for the `PutConfigurationSetArchivingOptions` operation.
 pub mod put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 /// Types for the `PutConfigurationSetDeliveryOptions` operation.
 pub mod put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 /// Types for the `PutConfigurationSetReputationOptions` operation.
 pub mod put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 /// Types for the `PutConfigurationSetSendingOptions` operation.
 pub mod put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 /// Types for the `PutConfigurationSetSuppressionOptions` operation.
 pub mod put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 /// Types for the `PutConfigurationSetTrackingOptions` operation.
 pub mod put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 /// Types for the `PutConfigurationSetVdmOptions` operation.
 pub mod put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 /// Types for the `PutDedicatedIpInPool` operation.
 pub mod put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 /// Types for the `PutDedicatedIpPoolScalingAttributes` operation.
 pub mod put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 /// Types for the `PutDedicatedIpWarmupAttributes` operation.
 pub mod put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 /// Types for the `PutDeliverabilityDashboardOption` operation.
 pub mod put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 /// Types for the `PutEmailIdentityConfigurationSetAttributes` operation.
 pub mod put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 /// Types for the `PutEmailIdentityDkimAttributes` operation.
 pub mod put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 /// Types for the `PutEmailIdentityDkimSigningAttributes` operation.
 pub mod put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 /// Types for the `PutEmailIdentityFeedbackAttributes` operation.
 pub mod put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 /// Types for the `PutEmailIdentityMailFromAttributes` operation.
 pub mod put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 /// Types for the `PutSuppressedDestination` operation.
 pub mod put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 /// Types for the `PutTenantSuppressionAttributes` operation.
 pub mod put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 /// Types for the `SendBulkEmail` operation.
 pub mod send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 /// Types for the `SendCustomVerificationEmail` operation.
 pub mod send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 /// Types for the `SendEmail` operation.
 pub mod send_email;

+#[cfg(feature = "op_tag_resource")]
 /// Types for the `TagResource` operation.
 pub mod tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 /// Types for the `TestRenderEmailTemplate` operation.
 pub mod test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 /// Types for the `UntagResource` operation.
 pub mod untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 /// Types for the `UpdateConfigurationSet` operation.
 pub mod update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 /// Types for the `UpdateConfigurationSetEventDestination` operation.
 pub mod update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 /// Types for the `UpdateContact` operation.
 pub mod update_contact;

+#[cfg(feature = "op_update_contact_list")]
 /// Types for the `UpdateContactList` operation.
 pub mod update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 /// Types for the `UpdateCustomVerificationEmailTemplate` operation.
 pub mod update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 /// Types for the `UpdateEmailIdentityPolicy` operation.
 pub mod update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 /// Types for the `UpdateEmailTemplate` operation.
 pub mod update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 /// Types for the `UpdateReputationEntityCustomerManagedStatus` operation.
 pub mod update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 /// Types for the `UpdateReputationEntityPolicy` operation.
 pub mod update_reputation_entity_policy;
diff --git a/src/protocol_serde.rs b/src/protocol_serde.rs
--- a/src/protocol_serde.rs
+++ b/src/protocol_serde.rs
@@ -1,4 +1,122 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) fn type_erase_result<O, E>(
     result: ::std::result::Result<O, E>,
 ) -> ::std::result::Result<
@@ -17,6 +135,124 @@
         .map_err(::std::convert::Into::into)
 }

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub fn parse_http_error_metadata(
     _response_status: u16,
     response_headers: &::aws_smithy_runtime_api::http::Headers,
@@ -28,238 +264,472 @@
     crate::json_errors::parse_error_metadata(response_body, response_headers)
 }

+#[cfg(feature = "op_associate_email_identity_certificate")]
 pub(crate) mod shape_associate_email_identity_certificate;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data;

+#[cfg(feature = "op_cancel_export_job")]
 pub(crate) mod shape_cancel_export_job;

+#[cfg(feature = "op_create_configuration_set")]
 pub(crate) mod shape_create_configuration_set;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 pub(crate) mod shape_create_configuration_set_event_destination;

+#[cfg(feature = "op_create_contact")]
 pub(crate) mod shape_create_contact;

+#[cfg(feature = "op_create_contact_list")]
 pub(crate) mod shape_create_contact_list;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 pub(crate) mod shape_create_custom_verification_email_template;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 pub(crate) mod shape_create_dedicated_ip_pool;

+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) mod shape_create_deliverability_test_report;

+#[cfg(feature = "op_create_email_identity")]
 pub(crate) mod shape_create_email_identity;

+#[cfg(feature = "op_create_email_identity_policy")]
 pub(crate) mod shape_create_email_identity_policy;

+#[cfg(feature = "op_create_email_template")]
 pub(crate) mod shape_create_email_template;

+#[cfg(feature = "op_create_export_job")]
 pub(crate) mod shape_create_export_job;

+#[cfg(feature = "op_create_import_job")]
 pub(crate) mod shape_create_import_job;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_create_multi_region_endpoint;

+#[cfg(feature = "op_create_tenant")]
 pub(crate) mod shape_create_tenant;

+#[cfg(feature = "op_create_tenant_resource_association")]
 pub(crate) mod shape_create_tenant_resource_association;

+#[cfg(feature = "op_delete_configuration_set")]
 pub(crate) mod shape_delete_configuration_set;

+#[cfg(feature = "op_delete_configuration_set_event_destination")]
 pub(crate) mod shape_delete_configuration_set_event_destination;

+#[cfg(feature = "op_delete_contact")]
 pub(crate) mod shape_delete_contact;

+#[cfg(feature = "op_delete_contact_list")]
 pub(crate) mod shape_delete_contact_list;

+#[cfg(feature = "op_delete_custom_verification_email_template")]
 pub(crate) mod shape_delete_custom_verification_email_template;

+#[cfg(feature = "op_delete_dedicated_ip_pool")]
 pub(crate) mod shape_delete_dedicated_ip_pool;

+#[cfg(feature = "op_delete_email_identity")]
 pub(crate) mod shape_delete_email_identity;

+#[cfg(feature = "op_delete_email_identity_policy")]
 pub(crate) mod shape_delete_email_identity_policy;

+#[cfg(feature = "op_delete_email_template")]
 pub(crate) mod shape_delete_email_template;

+#[cfg(feature = "op_delete_multi_region_endpoint")]
 pub(crate) mod shape_delete_multi_region_endpoint;

+#[cfg(feature = "op_delete_suppressed_destination")]
 pub(crate) mod shape_delete_suppressed_destination;

+#[cfg(feature = "op_delete_tenant")]
 pub(crate) mod shape_delete_tenant;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 pub(crate) mod shape_delete_tenant_resource_association;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 pub(crate) mod shape_disassociate_email_identity_certificate;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_get_account;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_get_blacklist_reports;

+#[cfg(feature = "op_get_configuration_set")]
 pub(crate) mod shape_get_configuration_set;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_get_configuration_set_event_destinations;

+#[cfg(feature = "op_get_contact")]
 pub(crate) mod shape_get_contact;

+#[cfg(feature = "op_get_contact_list")]
 pub(crate) mod shape_get_contact_list;

+#[cfg(feature = "op_get_custom_verification_email_template")]
 pub(crate) mod shape_get_custom_verification_email_template;

+#[cfg(feature = "op_get_dedicated_ip")]
 pub(crate) mod shape_get_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) mod shape_get_dedicated_ip_pool;

+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) mod shape_get_dedicated_ips;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) mod shape_get_deliverability_dashboard_options;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_get_deliverability_test_report;

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 pub(crate) mod shape_get_domain_deliverability_campaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_get_domain_statistics_report;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_get_email_address_insights;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_get_email_identity;

+#[cfg(feature = "op_get_email_identity_policies")]
 pub(crate) mod shape_get_email_identity_policies;

+#[cfg(feature = "op_get_email_template")]
 pub(crate) mod shape_get_email_template;

+#[cfg(feature = "op_get_export_job")]
 pub(crate) mod shape_get_export_job;

+#[cfg(feature = "op_get_import_job")]
 pub(crate) mod shape_get_import_job;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_get_message_insights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_get_multi_region_endpoint;

+#[cfg(feature = "op_get_reputation_entity")]
 pub(crate) mod shape_get_reputation_entity;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_get_suppressed_destination;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_get_tenant;

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) mod shape_list_configuration_sets;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_list_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_list_custom_verification_email_templates;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) mod shape_list_dedicated_ip_pools;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) mod shape_list_deliverability_test_reports;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) mod shape_list_domain_deliverability_campaigns;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_list_email_identities;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_list_email_identity_certificates;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_list_email_templates;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_list_export_jobs;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_list_import_jobs;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_list_multi_region_endpoints;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_list_recommendations;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_list_reputation_entities;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_list_resource_tenants;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_list_suppressed_destinations;

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) mod shape_list_tags_for_resource;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_list_tenant_resources;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_list_tenants;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_account_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_account_details")]
 pub(crate) mod shape_put_account_details;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 pub(crate) mod shape_put_account_pricing_attributes;

+#[cfg(feature = "op_put_account_sending_attributes")]
 pub(crate) mod shape_put_account_sending_attributes;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 pub(crate) mod shape_put_account_suppression_attributes;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 pub(crate) mod shape_put_account_vdm_attributes;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 pub(crate) mod shape_put_configuration_set_archiving_options;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 pub(crate) mod shape_put_configuration_set_delivery_options;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 pub(crate) mod shape_put_configuration_set_reputation_options;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 pub(crate) mod shape_put_configuration_set_sending_options;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 pub(crate) mod shape_put_configuration_set_suppression_options;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 pub(crate) mod shape_put_configuration_set_tracking_options;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 pub(crate) mod shape_put_configuration_set_vdm_options;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 pub(crate) mod shape_put_dedicated_ip_in_pool;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 pub(crate) mod shape_put_dedicated_ip_pool_scaling_attributes;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_dedicated_ip_warmup_attributes;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 pub(crate) mod shape_put_deliverability_dashboard_option;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 pub(crate) mod shape_put_email_identity_configuration_set_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_attributes;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_signing_attributes;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 pub(crate) mod shape_put_email_identity_feedback_attributes;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 pub(crate) mod shape_put_email_identity_mail_from_attributes;

+#[cfg(feature = "op_put_suppressed_destination")]
 pub(crate) mod shape_put_suppressed_destination;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 pub(crate) mod shape_put_tenant_suppression_attributes;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_send_bulk_email;

+#[cfg(feature = "op_send_custom_verification_email")]
 pub(crate) mod shape_send_custom_verification_email;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_send_email;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource;

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) mod shape_test_render_email_template;

+#[cfg(feature = "op_untag_resource")]
 pub(crate) mod shape_untag_resource;

+#[cfg(feature = "op_update_configuration_set")]
 pub(crate) mod shape_update_configuration_set;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 pub(crate) mod shape_update_configuration_set_event_destination;

+#[cfg(feature = "op_update_contact")]
 pub(crate) mod shape_update_contact;

+#[cfg(feature = "op_update_contact_list")]
 pub(crate) mod shape_update_contact_list;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 pub(crate) mod shape_update_custom_verification_email_template;

+#[cfg(feature = "op_update_email_identity_policy")]
 pub(crate) mod shape_update_email_identity_policy;

+#[cfg(feature = "op_update_email_template")]
 pub(crate) mod shape_update_email_template;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 pub(crate) mod shape_update_reputation_entity_customer_managed_status;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 pub(crate) mod shape_update_reputation_entity_policy;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) fn or_empty_doc(data: &[u8]) -> &[u8] {
     if data.is_empty() {
         b"{}"
@@ -268,522 +738,1364 @@
     }
 }

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_account_suspended_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_already_exists_exception;

+#[cfg(feature = "op_associate_email_identity_certificate")]
 pub(crate) mod shape_associate_email_identity_certificate_input;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_bad_request_exception;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data_input;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub(crate) mod shape_concurrent_modification_exception;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_conflict_exception;

+#[cfg(feature = "op_create_configuration_set_event_destination")]
 pub(crate) mod shape_create_configuration_set_event_destination_input;

+#[cfg(feature = "op_create_configuration_set")]
 pub(crate) mod shape_create_configuration_set_input;

+#[cfg(feature = "op_create_contact")]
 pub(crate) mod shape_create_contact_input;

+#[cfg(feature = "op_create_contact_list")]
 pub(crate) mod shape_create_contact_list_input;

+#[cfg(feature = "op_create_custom_verification_email_template")]
 pub(crate) mod shape_create_custom_verification_email_template_input;

+#[cfg(feature = "op_create_dedicated_ip_pool")]
 pub(crate) mod shape_create_dedicated_ip_pool_input;

+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) mod shape_create_deliverability_test_report_input;

+#[cfg(feature = "op_create_email_identity")]
 pub(crate) mod shape_create_email_identity_input;

+#[cfg(feature = "op_create_email_identity_policy")]
 pub(crate) mod shape_create_email_identity_policy_input;

+#[cfg(feature = "op_create_email_template")]
 pub(crate) mod shape_create_email_template_input;

+#[cfg(feature = "op_create_export_job")]
 pub(crate) mod shape_create_export_job_input;

+#[cfg(feature = "op_create_import_job")]
 pub(crate) mod shape_create_import_job_input;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_create_multi_region_endpoint_input;

+#[cfg(feature = "op_create_tenant")]
 pub(crate) mod shape_create_tenant_input;

+#[cfg(feature = "op_create_tenant_resource_association")]
 pub(crate) mod shape_create_tenant_resource_association_input;

+#[cfg(feature = "op_delete_tenant")]
 pub(crate) mod shape_delete_tenant_input;

+#[cfg(feature = "op_delete_tenant_resource_association")]
 pub(crate) mod shape_delete_tenant_resource_association_input;

+#[cfg(feature = "op_disassociate_email_identity_certificate")]
 pub(crate) mod shape_disassociate_email_identity_certificate_input;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_get_email_address_insights_input;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_get_tenant_input;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_internal_service_error_exception;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_invalid_next_token_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_limit_exceeded_exception;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts_input;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_list_email_identity_certificates_input;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_list_export_jobs_input;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_list_import_jobs_input;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_list_recommendations_input;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_list_reputation_entities_input;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_list_resource_tenants_input;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_list_tenant_resources_input;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_list_tenants_input;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_mail_from_domain_not_verified_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_rejected;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub(crate) mod shape_not_found_exception;

+#[cfg(feature = "op_put_account_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_account_dedicated_ip_warmup_attributes_input;

+#[cfg(feature = "op_put_account_details")]
 pub(crate) mod shape_put_account_details_input;

+#[cfg(feature = "op_put_account_pricing_attributes")]
 pub(crate) mod shape_put_account_pricing_attributes_input;

+#[cfg(feature = "op_put_account_sending_attributes")]
 pub(crate) mod shape_put_account_sending_attributes_input;

+#[cfg(feature = "op_put_account_suppression_attributes")]
 pub(crate) mod shape_put_account_suppression_attributes_input;

+#[cfg(feature = "op_put_account_vdm_attributes")]
 pub(crate) mod shape_put_account_vdm_attributes_input;

+#[cfg(feature = "op_put_configuration_set_archiving_options")]
 pub(crate) mod shape_put_configuration_set_archiving_options_input;

+#[cfg(feature = "op_put_configuration_set_delivery_options")]
 pub(crate) mod shape_put_configuration_set_delivery_options_input;

+#[cfg(feature = "op_put_configuration_set_reputation_options")]
 pub(crate) mod shape_put_configuration_set_reputation_options_input;

+#[cfg(feature = "op_put_configuration_set_sending_options")]
 pub(crate) mod shape_put_configuration_set_sending_options_input;

+#[cfg(feature = "op_put_configuration_set_suppression_options")]
 pub(crate) mod shape_put_configuration_set_suppression_options_input;

+#[cfg(feature = "op_put_configuration_set_tracking_options")]
 pub(crate) mod shape_put_configuration_set_tracking_options_input;

+#[cfg(feature = "op_put_configuration_set_vdm_options")]
 pub(crate) mod shape_put_configuration_set_vdm_options_input;

+#[cfg(feature = "op_put_dedicated_ip_in_pool")]
 pub(crate) mod shape_put_dedicated_ip_in_pool_input;

+#[cfg(feature = "op_put_dedicated_ip_pool_scaling_attributes")]
 pub(crate) mod shape_put_dedicated_ip_pool_scaling_attributes_input;

+#[cfg(feature = "op_put_dedicated_ip_warmup_attributes")]
 pub(crate) mod shape_put_dedicated_ip_warmup_attributes_input;

+#[cfg(feature = "op_put_deliverability_dashboard_option")]
 pub(crate) mod shape_put_deliverability_dashboard_option_input;

+#[cfg(feature = "op_put_email_identity_configuration_set_attributes")]
 pub(crate) mod shape_put_email_identity_configuration_set_attributes_input;

+#[cfg(feature = "op_put_email_identity_dkim_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_attributes_input;

+#[cfg(feature = "op_put_email_identity_dkim_signing_attributes")]
 pub(crate) mod shape_put_email_identity_dkim_signing_attributes_input;

+#[cfg(feature = "op_put_email_identity_feedback_attributes")]
 pub(crate) mod shape_put_email_identity_feedback_attributes_input;

+#[cfg(feature = "op_put_email_identity_mail_from_attributes")]
 pub(crate) mod shape_put_email_identity_mail_from_attributes_input;

+#[cfg(feature = "op_put_suppressed_destination")]
 pub(crate) mod shape_put_suppressed_destination_input;

+#[cfg(feature = "op_put_tenant_suppression_attributes")]
 pub(crate) mod shape_put_tenant_suppression_attributes_input;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_send_bulk_email_input;

+#[cfg(feature = "op_send_custom_verification_email")]
 pub(crate) mod shape_send_custom_verification_email_input;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_send_email_input;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_sending_paused_exception;

+#[cfg(feature = "op_tag_resource")]
 pub(crate) mod shape_tag_resource_input;

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) mod shape_test_render_email_template_input;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub(crate) mod shape_too_many_requests_exception;

+#[cfg(feature = "op_update_configuration_set_event_destination")]
 pub(crate) mod shape_update_configuration_set_event_destination_input;

+#[cfg(feature = "op_update_configuration_set")]
 pub(crate) mod shape_update_configuration_set_input;

+#[cfg(feature = "op_update_contact")]
 pub(crate) mod shape_update_contact_input;

+#[cfg(feature = "op_update_contact_list")]
 pub(crate) mod shape_update_contact_list_input;

+#[cfg(feature = "op_update_custom_verification_email_template")]
 pub(crate) mod shape_update_custom_verification_email_template_input;

+#[cfg(feature = "op_update_email_identity_policy")]
 pub(crate) mod shape_update_email_identity_policy_input;

+#[cfg(feature = "op_update_email_template")]
 pub(crate) mod shape_update_email_template_input;

+#[cfg(feature = "op_update_reputation_entity_customer_managed_status")]
 pub(crate) mod shape_update_reputation_entity_customer_managed_status_input;

+#[cfg(feature = "op_update_reputation_entity_policy")]
 pub(crate) mod shape_update_reputation_entity_policy_input;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_account_details;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_archiving_options;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_batch_get_metric_data_query;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_report;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry_result_list;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_configuration_overrides;

+#[cfg(feature = "op_list_configuration_sets")]
 pub(crate) mod shape_configuration_set_name_list;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_custom_verification_email_templates_list;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_daily_volumes;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub(crate) mod shape_dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ips")]
 pub(crate) mod shape_dedicated_ip_list;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) mod shape_dedicated_ip_pool;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub(crate) mod shape_deliverability_test_report;

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) mod shape_deliverability_test_reports;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_delivery_options;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_destination;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_details;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub(crate) mod shape_dkim_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub(crate) mod shape_dkim_signing_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub(crate) mod shape_dns_token_list;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_domain_deliverability_campaign;

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) mod shape_domain_deliverability_campaign_list;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_domain_deliverability_tracking_option;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) mod shape_domain_deliverability_tracking_options;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_email_content;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_email_insights_list;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub(crate) mod shape_email_template_content;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_email_template_metadata_list;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_event_destination_definition;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_destinations;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_destination;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_export_job_summary_list;

+#[cfg(feature = "op_get_export_job")]
 pub(crate) mod shape_export_statistics;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub(crate) mod shape_failure_info;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_identity_certificate_list;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_identity_info_list;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub(crate) mod shape_import_data_source;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_import_destination;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_import_job_summary_list;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_isp_placements;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_contacts_filter;

+#[cfg(feature = "op_send_email")]
 pub(crate) mod shape_list_management_options;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_list_of_contact_lists;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_list_of_contacts;

+#[cfg(feature = "op_list_dedicated_ip_pools")]
 pub(crate) mod shape_list_of_dedicated_ip_pools;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_mail_from_attributes;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_mailbox_validation;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_message_security_options;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_tag;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_message_tag_list;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_error_list;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_result_list;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_multi_region_endpoints;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_overall_volume;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_placement_statistics;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_get_email_identity_policies"))]
 pub(crate) mod shape_policy_map;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_pricing_attributes;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_recommendations_list;

+#[cfg(feature = "op_list_reputation_entities")]
 pub(crate) mod shape_reputation_entities_list;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub(crate) mod shape_reputation_entity;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_reputation_options;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_resource_tenant_metadata_list;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_routes;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_send_quota;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_sending_options;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_suppressed_destination;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_suppressed_destination_summaries;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_suppression_attributes;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_suppression_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub(crate) mod shape_suppression_validation_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_validation_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) mod shape_tag;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource"
+))]
 pub(crate) mod shape_tag_list;

+#[cfg(feature = "op_get_tenant")]
 pub(crate) mod shape_tenant;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_tenant_info_list;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_tenant_resource_list;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub(crate) mod shape_tenant_suppression_attributes;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub(crate) mod shape_topic;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub(crate) mod shape_topic_preference;

+#[cfg(any(feature = "op_get_contact", feature = "op_list_contacts"))]
 pub(crate) mod shape_topic_preference_list;

+#[cfg(feature = "op_get_contact_list")]
 pub(crate) mod shape_topics;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) mod shape_tracking_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_vdm_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_vdm_options;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_verification_info;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_additional_contact_email_addresses;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_entries;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_bulk_email_entry_result;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_destination;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_contact;

+#[cfg(feature = "op_list_contact_lists")]
 pub(crate) mod shape_contact_list;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_contact_list_destination;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub(crate) mod shape_custom_verification_email_template_metadata;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_daily_volume;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_dashboard_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_dashboard_options;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_domain_isp_placements;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_email_address_insights_mailbox_evaluations;

+#[cfg(feature = "op_get_email_address_insights")]
 pub(crate) mod shape_email_address_insights_verdict;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_email_insights;

+#[cfg(feature = "op_list_email_templates")]
 pub(crate) mod shape_email_template_metadata;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_esps;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_event_bridge_destination;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_destination;

+#[cfg(feature = "op_list_export_jobs")]
 pub(crate) mod shape_export_job_summary;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) mod shape_guardian_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub(crate) mod shape_guardian_options;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub(crate) mod shape_identity_certificate;

+#[cfg(feature = "op_list_email_identities")]
 pub(crate) mod shape_identity_info;

+#[cfg(feature = "op_list_import_jobs")]
 pub(crate) mod shape_import_job_summary;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_inbox_placement_tracking_option;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub(crate) mod shape_ip_list;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) mod shape_isp_placement;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_kinesis_firehose_destination;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_message;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_message_header;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_message_insights_data_source;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_error;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_data_result;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_metrics_data_source;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_multi_region_endpoint;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_pinpoint_destination;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_raw_message;

+#[cfg(feature = "op_list_recommendations")]
 pub(crate) mod shape_recommendation;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_replacement_email_content;

+#[cfg(feature = "op_list_resource_tenants")]
 pub(crate) mod shape_resource_tenant_metadata;

+#[cfg(feature = "op_get_account")]
 pub(crate) mod shape_review_details;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) mod shape_route;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub(crate) mod shape_route_details;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_sns_destination;

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) mod shape_soa_record;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub(crate) mod shape_status_record;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) mod shape_suppressed_destination_attributes;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) mod shape_suppressed_destination_summary;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_condition_threshold;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) mod shape_suppression_list_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant"
+))]
 pub(crate) mod shape_suppression_list_reasons;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_template;

+#[cfg(feature = "op_list_tenants")]
 pub(crate) mod shape_tenant_info;

+#[cfg(feature = "op_list_tenant_resources")]
 pub(crate) mod shape_tenant_resource;

+#[cfg(feature = "op_list_contacts")]
 pub(crate) mod shape_topic_filter;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub(crate) mod shape_tracking_configuration_overrides;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_volume_statistics;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) mod shape_attachment;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) mod shape_blacklist_entry;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_body;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_dimension_configuration;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub(crate) mod shape_content;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_default_signing_scheme;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) mod shape_domain_isp_placement;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) mod shape_event_types;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_dimensions;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_metric;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_export_metrics;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_insights_events;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_message_insights_filters;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_metric_value_list;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub(crate) mod shape_regions;

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) mod shape_replacement_template;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub(crate) mod shape_smime_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) mod shape_suppression_confidence_threshold;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub(crate) mod shape_timestamp_list;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) mod shape_cloud_watch_dimension_configurations;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_email_address_filter_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_email_subject_filter_list;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub(crate) mod shape_export_dimension_value;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_insights_event;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_isp_filter_list;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub(crate) mod shape_isp_name_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_last_delivery_event_list;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) mod shape_last_engagement_event_list;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_event_details;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_bounce;

+#[cfg(feature = "op_get_message_insights")]
 pub(crate) mod shape_complaint;
diff --git a/src/serde_util.rs b/src/serde_util.rs
--- a/src/serde_util.rs
+++ b/src/serde_util.rs
@@ -1,4 +1,5 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(feature = "op_create_deliverability_test_report")]
 pub(crate) fn create_deliverability_test_report_output_output_correct_errors(
     mut builder: crate::operation::create_deliverability_test_report::builders::CreateDeliverabilityTestReportOutputBuilder,
 ) -> crate::operation::create_deliverability_test_report::builders::CreateDeliverabilityTestReportOutputBuilder {
@@ -13,6 +14,7 @@
     builder
 }

+#[cfg(feature = "op_get_blacklist_reports")]
 pub(crate) fn get_blacklist_reports_output_output_correct_errors(
     mut builder: crate::operation::get_blacklist_reports::builders::GetBlacklistReportsOutputBuilder,
 ) -> crate::operation::get_blacklist_reports::builders::GetBlacklistReportsOutputBuilder {
@@ -22,6 +24,7 @@
     builder
 }

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub(crate) fn get_deliverability_dashboard_options_output_output_correct_errors(
     mut builder: crate::operation::get_deliverability_dashboard_options::builders::GetDeliverabilityDashboardOptionsOutputBuilder,
 ) -> crate::operation::get_deliverability_dashboard_options::builders::GetDeliverabilityDashboardOptionsOutputBuilder {
@@ -31,6 +34,7 @@
     builder
 }

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub(crate) fn get_deliverability_test_report_output_output_correct_errors(
     mut builder: crate::operation::get_deliverability_test_report::builders::GetDeliverabilityTestReportOutputBuilder,
 ) -> crate::operation::get_deliverability_test_report::builders::GetDeliverabilityTestReportOutputBuilder {
@@ -52,6 +56,7 @@
     builder
 }

+#[cfg(feature = "op_get_domain_deliverability_campaign")]
 pub(crate) fn get_domain_deliverability_campaign_output_output_correct_errors(
     mut builder: crate::operation::get_domain_deliverability_campaign::builders::GetDomainDeliverabilityCampaignOutputBuilder,
 ) -> crate::operation::get_domain_deliverability_campaign::builders::GetDomainDeliverabilityCampaignOutputBuilder {
@@ -64,6 +69,7 @@
     builder
 }

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub(crate) fn get_domain_statistics_report_output_output_correct_errors(
     mut builder: crate::operation::get_domain_statistics_report::builders::GetDomainStatisticsReportOutputBuilder,
 ) -> crate::operation::get_domain_statistics_report::builders::GetDomainStatisticsReportOutputBuilder {
@@ -79,6 +85,7 @@
     builder
 }

+#[cfg(feature = "op_get_email_template")]
 pub(crate) fn get_email_template_output_output_correct_errors(
     mut builder: crate::operation::get_email_template::builders::GetEmailTemplateOutputBuilder,
 ) -> crate::operation::get_email_template::builders::GetEmailTemplateOutputBuilder {
@@ -94,6 +101,7 @@
     builder
 }

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) fn get_suppressed_destination_output_output_correct_errors(
     mut builder: crate::operation::get_suppressed_destination::builders::GetSuppressedDestinationOutputBuilder,
 ) -> crate::operation::get_suppressed_destination::builders::GetSuppressedDestinationOutputBuilder {
@@ -108,6 +116,7 @@
     builder
 }

+#[cfg(feature = "op_list_deliverability_test_reports")]
 pub(crate) fn list_deliverability_test_reports_output_output_correct_errors(
     mut builder: crate::operation::list_deliverability_test_reports::builders::ListDeliverabilityTestReportsOutputBuilder,
 ) -> crate::operation::list_deliverability_test_reports::builders::ListDeliverabilityTestReportsOutputBuilder {
@@ -117,6 +126,7 @@
     builder
 }

+#[cfg(feature = "op_list_domain_deliverability_campaigns")]
 pub(crate) fn list_domain_deliverability_campaigns_output_output_correct_errors(
     mut builder: crate::operation::list_domain_deliverability_campaigns::builders::ListDomainDeliverabilityCampaignsOutputBuilder,
 ) -> crate::operation::list_domain_deliverability_campaigns::builders::ListDomainDeliverabilityCampaignsOutputBuilder {
@@ -126,6 +136,7 @@
     builder
 }

+#[cfg(feature = "op_list_tags_for_resource")]
 pub(crate) fn list_tags_for_resource_output_output_correct_errors(
     mut builder: crate::operation::list_tags_for_resource::builders::ListTagsForResourceOutputBuilder,
 ) -> crate::operation::list_tags_for_resource::builders::ListTagsForResourceOutputBuilder {
@@ -135,6 +146,7 @@
     builder
 }

+#[cfg(feature = "op_send_bulk_email")]
 pub(crate) fn send_bulk_email_output_output_correct_errors(
     mut builder: crate::operation::send_bulk_email::builders::SendBulkEmailOutputBuilder,
 ) -> crate::operation::send_bulk_email::builders::SendBulkEmailOutputBuilder {
@@ -144,6 +156,7 @@
     builder
 }

+#[cfg(feature = "op_test_render_email_template")]
 pub(crate) fn test_render_email_template_output_output_correct_errors(
     mut builder: crate::operation::test_render_email_template::builders::TestRenderEmailTemplateOutputBuilder,
 ) -> crate::operation::test_render_email_template::builders::TestRenderEmailTemplateOutputBuilder {
@@ -153,6 +166,7 @@
     builder
 }

+#[cfg(feature = "op_get_suppressed_destination")]
 pub(crate) fn suppressed_destination_correct_errors(
     mut builder: crate::types::builders::SuppressedDestinationBuilder,
 ) -> crate::types::builders::SuppressedDestinationBuilder {
@@ -168,6 +182,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub(crate) fn dedicated_ip_correct_errors(
     mut builder: crate::types::builders::DedicatedIpBuilder,
 ) -> crate::types::builders::DedicatedIpBuilder {
@@ -183,6 +198,7 @@
     builder
 }

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub(crate) fn dedicated_ip_pool_correct_errors(
     mut builder: crate::types::builders::DedicatedIpPoolBuilder,
 ) -> crate::types::builders::DedicatedIpPoolBuilder {
@@ -195,6 +211,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn export_destination_correct_errors(
     mut builder: crate::types::builders::ExportDestinationBuilder,
 ) -> crate::types::builders::ExportDestinationBuilder {
@@ -204,6 +221,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub(crate) fn import_data_source_correct_errors(
     mut builder: crate::types::builders::ImportDataSourceBuilder,
 ) -> crate::types::builders::ImportDataSourceBuilder {
@@ -216,6 +234,7 @@
     builder
 }

+#[cfg(feature = "op_get_email_identity")]
 pub(crate) fn mail_from_attributes_correct_errors(
     mut builder: crate::types::builders::MailFromAttributesBuilder,
 ) -> crate::types::builders::MailFromAttributesBuilder {
@@ -231,6 +250,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub(crate) fn tracking_options_correct_errors(
     mut builder: crate::types::builders::TrackingOptionsBuilder,
 ) -> crate::types::builders::TrackingOptionsBuilder {
@@ -240,6 +260,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub(crate) fn vdm_attributes_correct_errors(
     mut builder: crate::types::builders::VdmAttributesBuilder,
 ) -> crate::types::builders::VdmAttributesBuilder {
@@ -249,6 +270,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) fn contact_list_destination_correct_errors(
     mut builder: crate::types::builders::ContactListDestinationBuilder,
 ) -> crate::types::builders::ContactListDestinationBuilder {
@@ -261,6 +287,7 @@
     builder
 }

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub(crate) fn event_destination_correct_errors(
     mut builder: crate::types::builders::EventDestinationBuilder,
 ) -> crate::types::builders::EventDestinationBuilder {
@@ -273,6 +300,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn message_insights_data_source_correct_errors(
     mut builder: crate::types::builders::MessageInsightsDataSourceBuilder,
 ) -> crate::types::builders::MessageInsightsDataSourceBuilder {
@@ -285,6 +313,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub(crate) fn message_tag_correct_errors(
     mut builder: crate::types::builders::MessageTagBuilder,
 ) -> crate::types::builders::MessageTagBuilder {
@@ -297,6 +330,7 @@
     builder
 }

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub(crate) fn metrics_data_source_correct_errors(
     mut builder: crate::types::builders::MetricsDataSourceBuilder,
 ) -> crate::types::builders::MetricsDataSourceBuilder {
@@ -318,6 +352,7 @@
     builder
 }

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub(crate) fn route_correct_errors(
     mut builder: crate::types::builders::RouteBuilder,
 ) -> crate::types::builders::RouteBuilder {
@@ -327,6 +362,7 @@
     builder
 }

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub(crate) fn suppressed_destination_summary_correct_errors(
     mut builder: crate::types::builders::SuppressedDestinationSummaryBuilder,
 ) -> crate::types::builders::SuppressedDestinationSummaryBuilder {
@@ -342,6 +378,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub(crate) fn suppression_list_destination_correct_errors(
     mut builder: crate::types::builders::SuppressionListDestinationBuilder,
 ) -> crate::types::builders::SuppressionListDestinationBuilder {
@@ -353,6 +394,7 @@
     builder
 }

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub(crate) fn suppression_validation_attributes_correct_errors(
     mut builder: crate::types::builders::SuppressionValidationAttributesBuilder,
 ) -> crate::types::builders::SuppressionValidationAttributesBuilder {
@@ -367,6 +409,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_validation_options_correct_errors(
     mut builder: crate::types::builders::SuppressionValidationOptionsBuilder,
 ) -> crate::types::builders::SuppressionValidationOptionsBuilder {
@@ -381,6 +428,26 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub(crate) fn tag_correct_errors(
     mut builder: crate::types::builders::TagBuilder,
 ) -> crate::types::builders::TagBuilder {
@@ -393,6 +460,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub(crate) fn topic_correct_errors(
     mut builder: crate::types::builders::TopicBuilder,
 ) -> crate::types::builders::TopicBuilder {
@@ -408,6 +480,12 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub(crate) fn topic_preference_correct_errors(
     mut builder: crate::types::builders::TopicPreferenceBuilder,
 ) -> crate::types::builders::TopicPreferenceBuilder {
@@ -420,6 +498,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn cloud_watch_destination_correct_errors(
     mut builder: crate::types::builders::CloudWatchDestinationBuilder,
 ) -> crate::types::builders::CloudWatchDestinationBuilder {
@@ -429,6 +512,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn event_bridge_destination_correct_errors(
     mut builder: crate::types::builders::EventBridgeDestinationBuilder,
 ) -> crate::types::builders::EventBridgeDestinationBuilder {
@@ -438,6 +526,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn kinesis_firehose_destination_correct_errors(
     mut builder: crate::types::builders::KinesisFirehoseDestinationBuilder,
 ) -> crate::types::builders::KinesisFirehoseDestinationBuilder {
@@ -450,6 +543,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn sns_destination_correct_errors(
     mut builder: crate::types::builders::SnsDestinationBuilder,
 ) -> crate::types::builders::SnsDestinationBuilder {
@@ -459,6 +557,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_condition_threshold_correct_errors(
     mut builder: crate::types::builders::SuppressionConditionThresholdBuilder,
 ) -> crate::types::builders::SuppressionConditionThresholdBuilder {
@@ -468,6 +573,13 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub(crate) fn suppression_confidence_threshold_correct_errors(
     mut builder: crate::types::builders::SuppressionConfidenceThresholdBuilder,
 ) -> crate::types::builders::SuppressionConfidenceThresholdBuilder {
@@ -479,6 +591,11 @@
     builder
 }

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub(crate) fn cloud_watch_dimension_configuration_correct_errors(
     mut builder: crate::types::builders::CloudWatchDimensionConfigurationBuilder,
 ) -> crate::types::builders::CloudWatchDimensionConfigurationBuilder {
diff --git a/src/types.rs b/src/types.rs
--- a/src/types.rs
+++ b/src/types.rs
@@ -1,706 +1,1654 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_tracking_options::TrackingOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_delivery_options::DeliveryOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_reputation_options::ReputationOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_sending_options::SendingOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_suppression_options::SuppressionOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_vdm_options::VdmOptions;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_archiving_options::ArchivingOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_message_security_options::MessageSecurityOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_destination_definition::EventDestinationDefinition;

+#[cfg(any(
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes"
+))]
 pub use crate::types::_scaling_mode::ScalingMode;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_email_content::EmailContent;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_status::DeliverabilityTestStatus;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes::DkimSigningAttributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_list_email_identities"
+))]
 pub use crate::types::_identity_type::IdentityType;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub use crate::types::_dkim_attributes::DkimAttributes;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::_email_template_content::EmailTemplateContent;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_data_source::ExportDataSource;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_destination::ExportDestination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_import_destination::ImportDestination;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub use crate::types::_import_data_source::ImportDataSource;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_details::Details;

+#[cfg(any(
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_list_multi_region_endpoints"
+))]
 pub use crate::types::_status::Status;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub use crate::types::_tenant_suppression_attributes::TenantSuppressionAttributes;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_tenant",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status"
+))]
 pub use crate::types::_sending_status::SendingStatus;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_send_quota::SendQuota;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_suppression_attributes::SuppressionAttributes;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_account_details::AccountDetails;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_vdm_attributes::VdmAttributes;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_pricing_attributes::PricingAttributes;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_dedicated_ip::DedicatedIp;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub use crate::types::_dedicated_ip_pool::DedicatedIpPool;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 pub use crate::types::_deliverability_dashboard_account_status::DeliverabilityDashboardAccountStatus;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_report::DeliverabilityTestReport;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_placement_statistics::PlacementStatistics;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub use crate::types::_domain_deliverability_campaign::DomainDeliverabilityCampaign;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_overall_volume::OverallVolume;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_mailbox_validation::MailboxValidation;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_attributes::MailFromAttributes;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_list_email_identities"))]
 pub use crate::types::_verification_status::VerificationStatus;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_info::VerificationInfo;

+#[cfg(any(feature = "op_get_export_job", feature = "op_list_export_jobs"))]
 pub use crate::types::_export_source_type::ExportSourceType;

+#[cfg(any(
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_job_status::JobStatus;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub use crate::types::_failure_info::FailureInfo;

+#[cfg(feature = "op_get_export_job")]
 pub use crate::types::_export_statistics::ExportStatistics;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::_reputation_entity_type::ReputationEntityType;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_reputation_entity::ReputationEntity;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination::SuppressedDestination;

+#[cfg(feature = "op_get_tenant")]
 pub use crate::types::_tenant::Tenant;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_list_contacts_filter::ListContactsFilter;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_destination_type::ImportDestinationType;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 pub use crate::types::_mail_type::MailType;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 pub use crate::types::_contact_language::ContactLanguage;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_pricing_attributes"))]
 pub use crate::types::_pricing_plan::PricingPlan;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub use crate::types::_suppression_validation_attributes::SuppressionValidationAttributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_delivery_options"
+))]
 pub use crate::types::_tls_policy::TlsPolicy;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 pub use crate::types::_suppression_list_scope::SuppressionListScope;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_validation_options::SuppressionValidationOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_tracking_options"
+))]
 pub use crate::types::_https_policy::HttpsPolicy;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes_origin::DkimSigningAttributesOrigin;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_status::DkimStatus;

+#[cfg(any(
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_mail_from_attributes"
+))]
 pub use crate::types::_behavior_on_mx_failure::BehaviorOnMxFailure;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 pub use crate::types::_suppression_list_reason::SuppressionListReason;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_content::BulkEmailContent;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_configuration_overrides::ConfigurationOverrides;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_destination::Destination;

+#[cfg(feature = "op_send_email")]
 pub use crate::types::_list_management_options::ListManagementOptions;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_batch_get_metric_data_query::BatchGetMetricDataQuery;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_result::MetricDataResult;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_error::MetricDataError;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::Tag;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_dashboard_options::DashboardOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_guardian_options::GuardianOptions;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_signing_scheme::SigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_kinesis_firehose_destination::KinesisFirehoseDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_destination::CloudWatchDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_sns_destination::SnsDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_bridge_destination::EventBridgeDestination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_pinpoint_destination::PinpointDestination;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub use crate::types::_topic_preference::TopicPreference;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_topic::Topic;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_message::Message;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_raw_message::RawMessage;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_template::Template;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_key_length::DkimSigningKeyLength;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metrics_data_source::MetricsDataSource;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_data_source::MessageInsightsDataSource;

+#[cfg(any(
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job"
+))]
 pub use crate::types::_data_format::DataFormat;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_destination::SuppressionListDestination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_destination::ContactListDestination;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_details::ReviewDetails;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_feature_status::FeatureStatus;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_dashboard_attributes::DashboardAttributes;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_guardian_attributes::GuardianAttributes;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub use crate::types::_event_destination::EventDestination;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_warmup_status::WarmupStatus;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_domain_deliverability_tracking_option::DomainDeliverabilityTrackingOption;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_isp_placement::IspPlacement;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_volume_statistics::VolumeStatistics;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_daily_volume::DailyVolume;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_verdict::EmailAddressInsightsVerdict;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_mailbox_evaluations::EmailAddressInsightsMailboxEvaluations;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_domain_status::MailFromDomainStatus;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_error::VerificationError;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_soa_record::SoaRecord;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_tag::MessageTag;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_email_insights::EmailInsights;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub use crate::types::_route::Route;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_status_record::StatusRecord;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities"
+))]
 pub use crate::types::_recommendation_impact::RecommendationImpact;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination_attributes::SuppressedDestinationAttributes;

+#[cfg(feature = "op_list_contact_lists")]
 pub use crate::types::_contact_list::ContactList;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_list_contacts",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_subscription_status::SubscriptionStatus;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_topic_filter::TopicFilter;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_contact::Contact;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub use crate::types::_custom_verification_email_template_metadata::CustomVerificationEmailTemplateMetadata;

+#[cfg(feature = "op_list_email_identities")]
 pub use crate::types::_identity_info::IdentityInfo;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate::IdentityCertificate;

+#[cfg(feature = "op_list_email_templates")]
 pub use crate::types::_email_template_metadata::EmailTemplateMetadata;

+#[cfg(feature = "op_list_export_jobs")]
 pub use crate::types::_export_job_summary::ExportJobSummary;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_job_summary::ImportJobSummary;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub use crate::types::_multi_region_endpoint::MultiRegionEndpoint;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_list_recommendations_filter_key::ListRecommendationsFilterKey;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation::Recommendation;

+#[cfg(feature = "op_list_reputation_entities")]
 pub use crate::types::_reputation_entity_filter_key::ReputationEntityFilterKey;

+#[cfg(feature = "op_list_resource_tenants")]
 pub use crate::types::_resource_tenant_metadata::ResourceTenantMetadata;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::_suppressed_destination_summary::SuppressedDestinationSummary;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_list_tenant_resources_filter_key::ListTenantResourcesFilterKey;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_tenant_resource::TenantResource;

+#[cfg(feature = "op_list_tenants")]
 pub use crate::types::_tenant_info::TenantInfo;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_condition_threshold::SuppressionConditionThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry::BulkEmailEntry;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_tracking_configuration_overrides::TrackingConfigurationOverrides;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry_result::BulkEmailEntryResult;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric_namespace::MetricNamespace;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric::Metric;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_query_error_code::QueryErrorCode;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_default_signing_scheme::DefaultSigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_smime_signing_scheme::SmimeSigningScheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_message_insights",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_type::EventType;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_content::Content;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_body::Body;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_filters::MessageInsightsFilters;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_import_action::SuppressionListImportAction;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_import_action::ContactListImportAction;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_route_details::RouteDetails;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_status::ReviewStatus;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub use crate::types::_blacklist_entry::BlacklistEntry;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_inbox_placement_tracking_option::InboxPlacementTrackingOption;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_domain_isp_placement::DomainIspPlacement;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_confidence_verdict::EmailAddressInsightsConfidenceVerdict;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate_status::IdentityCertificateStatus;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation_type::RecommendationType;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation_status::RecommendationStatus;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_resource_type::ResourceType;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_threshold::SuppressionConfidenceThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_email_content::ReplacementEmailContent;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_status::BulkEmailStatus;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 pub use crate::types::_metric_dimension_name::MetricDimensionName;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_signature_format::SignatureFormat;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_dimension_configuration::CloudWatchDimensionConfiguration;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_header::MessageHeader;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment::Attachment;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_metric::ExportMetric;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_insights_event::InsightsEvent;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_verdict_threshold::SuppressionConfidenceVerdictThreshold;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_template::ReplacementTemplate;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_dimension_value_source::DimensionValueSource;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment_content_disposition::AttachmentContentDisposition;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment_content_transfer_encoding::AttachmentContentTransferEncoding;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metric_aggregation::MetricAggregation;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_delivery_event_type::DeliveryEventType;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_engagement_event_type::EngagementEventType;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_event_details::EventDetails;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce::Bounce;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_complaint::Complaint;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce_type::BounceType;

+#[cfg(feature = "op_get_account")]
 mod _account_details;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _archiving_options;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment_content_disposition;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _attachment_content_transfer_encoding;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _batch_get_metric_data_query;

+#[cfg(any(
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_mail_from_attributes"
+))]
 mod _behavior_on_mx_failure;

+#[cfg(feature = "op_get_blacklist_reports")]
 mod _blacklist_entry;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _body;

+#[cfg(feature = "op_get_message_insights")]
 mod _bounce;

+#[cfg(feature = "op_get_message_insights")]
 mod _bounce_type;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_entry;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_entry_result;

+#[cfg(feature = "op_send_bulk_email")]
 mod _bulk_email_status;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _cloud_watch_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _cloud_watch_dimension_configuration;

+#[cfg(feature = "op_get_message_insights")]
 mod _complaint;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _configuration_overrides;

+#[cfg(feature = "op_list_contacts")]
 mod _contact;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 mod _contact_language;

+#[cfg(feature = "op_list_contact_lists")]
 mod _contact_list;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _contact_list_destination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _contact_list_import_action;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _content;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 mod _custom_verification_email_template_metadata;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _daily_volume;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _dashboard_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _dashboard_options;

+#[cfg(any(
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job"
+))]
 mod _data_format;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 mod _dedicated_ip;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 mod _dedicated_ip_pool;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _default_signing_scheme;

+#[cfg(feature = "op_get_deliverability_dashboard_options")]
 mod _deliverability_dashboard_account_status;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 mod _deliverability_test_report;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 mod _deliverability_test_status;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _delivery_event_type;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _delivery_options;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _destination;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod _details;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _dimension_value_source;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 mod _dkim_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_attributes;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_attributes_origin;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_signing_key_length;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 mod _dkim_status;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 mod _domain_deliverability_campaign;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _domain_deliverability_tracking_option;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _domain_isp_placement;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_confidence_verdict;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_mailbox_evaluations;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _email_address_insights_verdict;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _email_content;

+#[cfg(feature = "op_get_message_insights")]
 mod _email_insights;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 mod _email_template_content;

+#[cfg(feature = "op_list_email_templates")]
 mod _email_template_metadata;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _engagement_event_type;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_bridge_destination;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 mod _event_destination;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_destination_definition;

+#[cfg(feature = "op_get_message_insights")]
 mod _event_details;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_message_insights",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _event_type;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_destination;

+#[cfg(feature = "op_list_export_jobs")]
 mod _export_job_summary;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _export_metric;

+#[cfg(any(feature = "op_get_export_job", feature = "op_list_export_jobs"))]
 mod _export_source_type;

+#[cfg(feature = "op_get_export_job")]
 mod _export_statistics;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 mod _failure_info;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _feature_status;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _guardian_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _guardian_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_tracking_options"
+))]
 mod _https_policy;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod _identity_certificate;

+#[cfg(feature = "op_list_email_identity_certificates")]
 mod _identity_certificate_status;

+#[cfg(feature = "op_list_email_identities")]
 mod _identity_info;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_get_email_identity",
+    feature = "op_list_email_identities"
+))]
 mod _identity_type;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 mod _import_data_source;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _import_destination;

+#[cfg(feature = "op_list_import_jobs")]
 mod _import_destination_type;

+#[cfg(feature = "op_list_import_jobs")]
 mod _import_job_summary;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _inbox_placement_tracking_option;

+#[cfg(feature = "op_get_message_insights")]
 mod _insights_event;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod _isp_placement;

+#[cfg(any(
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs"
+))]
 mod _job_status;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _kinesis_firehose_destination;

+#[cfg(feature = "op_list_contacts")]
 mod _list_contacts_filter;

+#[cfg(feature = "op_send_email")]
 mod _list_management_options;

+#[cfg(feature = "op_list_recommendations")]
 mod _list_recommendations_filter_key;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _list_tenant_resources_filter_key;

+#[cfg(feature = "op_get_email_identity")]
 mod _mail_from_attributes;

+#[cfg(feature = "op_get_email_identity")]
 mod _mail_from_domain_status;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_details"))]
 mod _mail_type;

+#[cfg(feature = "op_get_email_address_insights")]
 mod _mailbox_validation;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _message;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _message_header;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _message_insights_data_source;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _message_insights_filters;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _message_security_options;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _message_tag;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _metric_aggregation;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _metric_data_error;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _metric_data_result;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric_dimension_name;

+#[cfg(any(
+    feature = "op_batch_get_metric_data",
+    feature = "op_create_export_job",
+    feature = "op_get_export_job"
+))]
 mod _metric_namespace;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 mod _metrics_data_source;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 mod _multi_region_endpoint;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _overall_volume;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _pinpoint_destination;

+#[cfg(feature = "op_get_deliverability_test_report")]
 mod _placement_statistics;

+#[cfg(feature = "op_get_account")]
 mod _pricing_attributes;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_pricing_attributes"))]
 mod _pricing_plan;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _query_error_code;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 mod _raw_message;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities"
+))]
 mod _recommendation_impact;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation_status;

+#[cfg(feature = "op_list_recommendations")]
 mod _recommendation_type;

+#[cfg(feature = "op_send_bulk_email")]
 mod _replacement_email_content;

+#[cfg(feature = "op_send_bulk_email")]
 mod _replacement_template;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 mod _reputation_entity;

+#[cfg(feature = "op_list_reputation_entities")]
 mod _reputation_entity_filter_key;

+#[cfg(any(
+    feature = "op_get_reputation_entity",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _reputation_entity_type;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _reputation_options;

+#[cfg(feature = "op_list_resource_tenants")]
 mod _resource_tenant_metadata;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _resource_type;

+#[cfg(feature = "op_get_account")]
 mod _review_details;

+#[cfg(feature = "op_get_account")]
 mod _review_status;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 mod _route;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 mod _route_details;

+#[cfg(any(
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes"
+))]
 mod _scaling_mode;

+#[cfg(feature = "op_get_account")]
 mod _send_quota;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _sending_options;

+#[cfg(any(
+    feature = "op_create_tenant",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_tenant",
+    feature = "op_list_reputation_entities",
+    feature = "op_update_reputation_entity_customer_managed_status"
+))]
 mod _sending_status;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _signature_format;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 mod _smime_signing_scheme;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 mod _sns_destination;

+#[cfg(feature = "op_get_email_identity")]
 mod _soa_record;

+#[cfg(any(
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_list_multi_region_endpoints"
+))]
 mod _status;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 mod _status_record;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_list_contacts",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 mod _subscription_status;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod _suppressed_destination;

+#[cfg(feature = "op_get_suppressed_destination")]
 mod _suppressed_destination_attributes;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod _suppressed_destination_summary;

+#[cfg(feature = "op_get_account")]
 mod _suppression_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_condition_threshold;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_confidence_threshold;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_confidence_verdict_threshold;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _suppression_list_destination;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 mod _suppression_list_import_action;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 mod _suppression_list_reason;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_tenant",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_tenant_suppression_attributes"
+))]
 mod _suppression_list_scope;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _suppression_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 mod _suppression_validation_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 mod _suppression_validation_options;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 mod _tag;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _template;

+#[cfg(feature = "op_get_tenant")]
 mod _tenant;

+#[cfg(feature = "op_list_tenants")]
 mod _tenant_info;

+#[cfg(feature = "op_list_tenant_resources")]
 mod _tenant_resource;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 mod _tenant_suppression_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_delivery_options"
+))]
 mod _tls_policy;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 mod _topic;

+#[cfg(feature = "op_list_contacts")]
 mod _topic_filter;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 mod _topic_preference;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 mod _tracking_configuration_overrides;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 mod _tracking_options;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 mod _vdm_attributes;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 mod _vdm_options;

+#[cfg(feature = "op_get_email_identity")]
 mod _verification_error;

+#[cfg(feature = "op_get_email_identity")]
 mod _verification_info;

+#[cfg(any(feature = "op_get_email_identity", feature = "op_list_email_identities"))]
 mod _verification_status;

+#[cfg(feature = "op_get_domain_statistics_report")]
 mod _volume_statistics;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 mod _warmup_status;

 /// Builders
diff --git a/src/types/builders.rs b/src/types/builders.rs
--- a/src/types/builders.rs
+++ b/src/types/builders.rs
@@ -1,240 +1,505 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_tracking_options::TrackingOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_delivery_options::DeliveryOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_reputation_options::ReputationOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_sending_options::SendingOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_suppression_options::SuppressionOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_vdm_options::VdmOptionsBuilder;

+#[cfg(any(feature = "op_create_configuration_set", feature = "op_get_configuration_set"))]
 pub use crate::types::_archiving_options::ArchivingOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_message_security_options::MessageSecurityOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_destination_definition::EventDestinationDefinitionBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_email_content::EmailContentBuilder;

+#[cfg(any(
+    feature = "op_create_email_identity",
+    feature = "op_put_email_identity_dkim_signing_attributes"
+))]
 pub use crate::types::_dkim_signing_attributes::DkimSigningAttributesBuilder;

+#[cfg(any(feature = "op_create_email_identity", feature = "op_get_email_identity"))]
 pub use crate::types::_dkim_attributes::DkimAttributesBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_template",
+    feature = "op_get_email_template",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::_email_template_content::EmailTemplateContentBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_data_source::ExportDataSourceBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_destination::ExportDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_import_destination::ImportDestinationBuilder;

+#[cfg(any(feature = "op_create_import_job", feature = "op_get_import_job"))]
 pub use crate::types::_import_data_source::ImportDataSourceBuilder;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_details::DetailsBuilder;

+#[cfg(any(feature = "op_create_tenant", feature = "op_get_tenant"))]
 pub use crate::types::_tenant_suppression_attributes::TenantSuppressionAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_send_quota::SendQuotaBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_suppression_attributes::SuppressionAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_account_details::AccountDetailsBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_vdm_attributes::VdmAttributesBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_pricing_attributes::PricingAttributesBuilder;

+#[cfg(any(feature = "op_get_dedicated_ip", feature = "op_get_dedicated_ips"))]
 pub use crate::types::_dedicated_ip::DedicatedIpBuilder;

+#[cfg(feature = "op_get_dedicated_ip_pool")]
 pub use crate::types::_dedicated_ip_pool::DedicatedIpPoolBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_test_report",
+    feature = "op_list_deliverability_test_reports"
+))]
 pub use crate::types::_deliverability_test_report::DeliverabilityTestReportBuilder;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_placement_statistics::PlacementStatisticsBuilder;

+#[cfg(any(
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_list_domain_deliverability_campaigns"
+))]
 pub use crate::types::_domain_deliverability_campaign::DomainDeliverabilityCampaignBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_overall_volume::OverallVolumeBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_mailbox_validation::MailboxValidationBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_mail_from_attributes::MailFromAttributesBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_verification_info::VerificationInfoBuilder;

+#[cfg(any(feature = "op_get_export_job", feature = "op_get_import_job"))]
 pub use crate::types::_failure_info::FailureInfoBuilder;

+#[cfg(feature = "op_get_export_job")]
 pub use crate::types::_export_statistics::ExportStatisticsBuilder;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_reputation_entity::ReputationEntityBuilder;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination::SuppressedDestinationBuilder;

+#[cfg(feature = "op_get_tenant")]
 pub use crate::types::_tenant::TenantBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_list_contacts_filter::ListContactsFilterBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_suppression_attributes"))]
 pub use crate::types::_suppression_validation_attributes::SuppressionValidationAttributesBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_validation_options::SuppressionValidationOptionsBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_content::BulkEmailContentBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_configuration_overrides::ConfigurationOverridesBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_destination::DestinationBuilder;

+#[cfg(feature = "op_send_email")]
 pub use crate::types::_list_management_options::ListManagementOptionsBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_batch_get_metric_data_query::BatchGetMetricDataQueryBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_result::MetricDataResultBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::_metric_data_error::MetricDataErrorBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_configuration_set",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_template",
+    feature = "op_get_tenant",
+    feature = "op_list_tags_for_resource",
+    feature = "op_tag_resource"
+))]
 pub use crate::types::_tag::TagBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_dashboard_options::DashboardOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_put_configuration_set_vdm_options"
+))]
 pub use crate::types::_guardian_options::GuardianOptionsBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_kinesis_firehose_destination::KinesisFirehoseDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_destination::CloudWatchDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_sns_destination::SnsDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_event_bridge_destination::EventBridgeDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_pinpoint_destination::PinpointDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_contact",
+    feature = "op_get_contact",
+    feature = "op_list_contacts",
+    feature = "op_update_contact"
+))]
 pub use crate::types::_topic_preference::TopicPreferenceBuilder;

+#[cfg(any(
+    feature = "op_create_contact_list",
+    feature = "op_get_contact_list",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::_topic::TopicBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_message::MessageBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_raw_message::RawMessageBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_template::TemplateBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_metrics_data_source::MetricsDataSourceBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_data_source::MessageInsightsDataSourceBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_suppression_list_destination::SuppressionListDestinationBuilder;

+#[cfg(any(
+    feature = "op_create_import_job",
+    feature = "op_get_import_job",
+    feature = "op_list_import_jobs"
+))]
 pub use crate::types::_contact_list_destination::ContactListDestinationBuilder;

+#[cfg(feature = "op_get_account")]
 pub use crate::types::_review_details::ReviewDetailsBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_dashboard_attributes::DashboardAttributesBuilder;

+#[cfg(any(feature = "op_get_account", feature = "op_put_account_vdm_attributes"))]
 pub use crate::types::_guardian_attributes::GuardianAttributesBuilder;

+#[cfg(feature = "op_get_configuration_set_event_destinations")]
 pub use crate::types::_event_destination::EventDestinationBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_domain_deliverability_tracking_option::DomainDeliverabilityTrackingOptionBuilder;

+#[cfg(feature = "op_get_deliverability_test_report")]
 pub use crate::types::_isp_placement::IspPlacementBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_volume_statistics::VolumeStatisticsBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_daily_volume::DailyVolumeBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_verdict::EmailAddressInsightsVerdictBuilder;

+#[cfg(feature = "op_get_email_address_insights")]
 pub use crate::types::_email_address_insights_mailbox_evaluations::EmailAddressInsightsMailboxEvaluationsBuilder;

+#[cfg(feature = "op_get_email_identity")]
 pub use crate::types::_soa_record::SoaRecordBuilder;

+#[cfg(any(
+    feature = "op_get_message_insights",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_tag::MessageTagBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_email_insights::EmailInsightsBuilder;

+#[cfg(feature = "op_get_multi_region_endpoint")]
 pub use crate::types::_route::RouteBuilder;

+#[cfg(any(feature = "op_get_reputation_entity", feature = "op_list_reputation_entities"))]
 pub use crate::types::_status_record::StatusRecordBuilder;

+#[cfg(feature = "op_get_suppressed_destination")]
 pub use crate::types::_suppressed_destination_attributes::SuppressedDestinationAttributesBuilder;

+#[cfg(feature = "op_list_contact_lists")]
 pub use crate::types::_contact_list::ContactListBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_topic_filter::TopicFilterBuilder;

+#[cfg(feature = "op_list_contacts")]
 pub use crate::types::_contact::ContactBuilder;

+#[cfg(feature = "op_list_custom_verification_email_templates")]
 pub use crate::types::_custom_verification_email_template_metadata::CustomVerificationEmailTemplateMetadataBuilder;

+#[cfg(feature = "op_list_email_identities")]
 pub use crate::types::_identity_info::IdentityInfoBuilder;

+#[cfg(feature = "op_list_email_identity_certificates")]
 pub use crate::types::_identity_certificate::IdentityCertificateBuilder;

+#[cfg(feature = "op_list_email_templates")]
 pub use crate::types::_email_template_metadata::EmailTemplateMetadataBuilder;

+#[cfg(feature = "op_list_export_jobs")]
 pub use crate::types::_export_job_summary::ExportJobSummaryBuilder;

+#[cfg(feature = "op_list_import_jobs")]
 pub use crate::types::_import_job_summary::ImportJobSummaryBuilder;

+#[cfg(feature = "op_list_multi_region_endpoints")]
 pub use crate::types::_multi_region_endpoint::MultiRegionEndpointBuilder;

+#[cfg(feature = "op_list_recommendations")]
 pub use crate::types::_recommendation::RecommendationBuilder;

+#[cfg(feature = "op_list_resource_tenants")]
 pub use crate::types::_resource_tenant_metadata::ResourceTenantMetadataBuilder;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::_suppressed_destination_summary::SuppressedDestinationSummaryBuilder;

+#[cfg(feature = "op_list_tenant_resources")]
 pub use crate::types::_tenant_resource::TenantResourceBuilder;

+#[cfg(feature = "op_list_tenants")]
 pub use crate::types::_tenant_info::TenantInfoBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_condition_threshold::SuppressionConditionThresholdBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry::BulkEmailEntryBuilder;

+#[cfg(any(feature = "op_send_bulk_email", feature = "op_send_email"))]
 pub use crate::types::_tracking_configuration_overrides::TrackingConfigurationOverridesBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_bulk_email_entry_result::BulkEmailEntryResultBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_default_signing_scheme::DefaultSigningSchemeBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_configuration_set",
+    feature = "op_update_configuration_set"
+))]
 pub use crate::types::_smime_signing_scheme::SmimeSigningSchemeBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_content::ContentBuilder;

+#[cfg(any(feature = "op_create_deliverability_test_report", feature = "op_send_email"))]
 pub use crate::types::_body::BodyBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_message_insights_filters::MessageInsightsFiltersBuilder;

+#[cfg(feature = "op_create_multi_region_endpoint")]
 pub use crate::types::_route_details::RouteDetailsBuilder;

+#[cfg(feature = "op_get_blacklist_reports")]
 pub use crate::types::_blacklist_entry::BlacklistEntryBuilder;

+#[cfg(any(
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::_inbox_placement_tracking_option::InboxPlacementTrackingOptionBuilder;

+#[cfg(feature = "op_get_domain_statistics_report")]
 pub use crate::types::_domain_isp_placement::DomainIspPlacementBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_get_account",
+    feature = "op_get_configuration_set",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_configuration_set_suppression_options"
+))]
 pub use crate::types::_suppression_confidence_threshold::SuppressionConfidenceThresholdBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_email_content::ReplacementEmailContentBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_update_configuration_set_event_destination"
+))]
 pub use crate::types::_cloud_watch_dimension_configuration::CloudWatchDimensionConfigurationBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_message_header::MessageHeaderBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::_attachment::AttachmentBuilder;

+#[cfg(any(feature = "op_create_export_job", feature = "op_get_export_job"))]
 pub use crate::types::_export_metric::ExportMetricBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_insights_event::InsightsEventBuilder;

+#[cfg(feature = "op_send_bulk_email")]
 pub use crate::types::_replacement_template::ReplacementTemplateBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_event_details::EventDetailsBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_bounce::BounceBuilder;

+#[cfg(feature = "op_get_message_insights")]
 pub use crate::types::_complaint::ComplaintBuilder;
diff --git a/src/types/error.rs b/src/types/error.rs
--- a/src/types/error.rs
+++ b/src/types/error.rs
@@ -1,54 +1,872 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_bad_request_exception::BadRequestException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundException;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsException;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::error::_internal_service_error_exception::InternalServiceErrorException;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::error::_concurrent_modification_exception::ConcurrentModificationException;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_account_suspended_exception::AccountSuspendedException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_mail_from_domain_not_verified_exception::MailFromDomainNotVerifiedException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_message_rejected::MessageRejected;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_sending_paused_exception::SendingPausedException;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::error::_invalid_next_token_exception::InvalidNextTokenException;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_conflict_exception::ConflictException;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 mod _account_suspended_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 mod _already_exists_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _bad_request_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 mod _concurrent_modification_exception;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _conflict_exception;

+#[cfg(feature = "op_batch_get_metric_data")]
 mod _internal_service_error_exception;

+#[cfg(feature = "op_list_suppressed_destinations")]
 mod _invalid_next_token_exception;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _limit_exceeded_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _mail_from_domain_not_verified_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _message_rejected;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 mod _not_found_exception;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 mod _sending_paused_exception;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 mod _too_many_requests_exception;

 /// Builders
diff --git a/src/types/error/builders.rs b/src/types/error/builders.rs
--- a/src/types/error/builders.rs
+++ b/src/types/error/builders.rs
@@ -1,26 +1,435 @@
 // Code generated by software.amazon.smithy.rust.codegen.smithy-rs. DO NOT EDIT.
+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_put_deliverability_dashboard_option"
+))]
 pub use crate::types::error::_already_exists_exception::AlreadyExistsExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_bad_request_exception::BadRequestExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_export_job",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_contacts",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_recommendations",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template"
+))]
 pub use crate::types::error::_not_found_exception::NotFoundExceptionBuilder;

+#[cfg(any(
+    feature = "op_associate_email_identity_certificate",
+    feature = "op_batch_get_metric_data",
+    feature = "op_cancel_export_job",
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_create_tenant_resource_association",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_configuration_set_event_destination",
+    feature = "op_delete_contact",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_custom_verification_email_template",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_email_identity_policy",
+    feature = "op_delete_email_template",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_delete_suppressed_destination",
+    feature = "op_delete_tenant",
+    feature = "op_delete_tenant_resource_association",
+    feature = "op_disassociate_email_identity_certificate",
+    feature = "op_get_account",
+    feature = "op_get_blacklist_reports",
+    feature = "op_get_configuration_set",
+    feature = "op_get_configuration_set_event_destinations",
+    feature = "op_get_contact",
+    feature = "op_get_contact_list",
+    feature = "op_get_custom_verification_email_template",
+    feature = "op_get_dedicated_ip",
+    feature = "op_get_dedicated_ip_pool",
+    feature = "op_get_dedicated_ips",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_get_deliverability_test_report",
+    feature = "op_get_domain_deliverability_campaign",
+    feature = "op_get_domain_statistics_report",
+    feature = "op_get_email_address_insights",
+    feature = "op_get_email_identity",
+    feature = "op_get_email_identity_policies",
+    feature = "op_get_email_template",
+    feature = "op_get_export_job",
+    feature = "op_get_import_job",
+    feature = "op_get_message_insights",
+    feature = "op_get_multi_region_endpoint",
+    feature = "op_get_reputation_entity",
+    feature = "op_get_suppressed_destination",
+    feature = "op_get_tenant",
+    feature = "op_list_configuration_sets",
+    feature = "op_list_contact_lists",
+    feature = "op_list_contacts",
+    feature = "op_list_custom_verification_email_templates",
+    feature = "op_list_dedicated_ip_pools",
+    feature = "op_list_deliverability_test_reports",
+    feature = "op_list_domain_deliverability_campaigns",
+    feature = "op_list_email_identities",
+    feature = "op_list_email_identity_certificates",
+    feature = "op_list_email_templates",
+    feature = "op_list_export_jobs",
+    feature = "op_list_import_jobs",
+    feature = "op_list_multi_region_endpoints",
+    feature = "op_list_recommendations",
+    feature = "op_list_reputation_entities",
+    feature = "op_list_resource_tenants",
+    feature = "op_list_suppressed_destinations",
+    feature = "op_list_tags_for_resource",
+    feature = "op_list_tenant_resources",
+    feature = "op_list_tenants",
+    feature = "op_put_account_dedicated_ip_warmup_attributes",
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_put_account_sending_attributes",
+    feature = "op_put_account_suppression_attributes",
+    feature = "op_put_account_vdm_attributes",
+    feature = "op_put_configuration_set_archiving_options",
+    feature = "op_put_configuration_set_delivery_options",
+    feature = "op_put_configuration_set_reputation_options",
+    feature = "op_put_configuration_set_sending_options",
+    feature = "op_put_configuration_set_suppression_options",
+    feature = "op_put_configuration_set_tracking_options",
+    feature = "op_put_configuration_set_vdm_options",
+    feature = "op_put_dedicated_ip_in_pool",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_put_dedicated_ip_warmup_attributes",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_put_email_identity_configuration_set_attributes",
+    feature = "op_put_email_identity_dkim_attributes",
+    feature = "op_put_email_identity_dkim_signing_attributes",
+    feature = "op_put_email_identity_feedback_attributes",
+    feature = "op_put_email_identity_mail_from_attributes",
+    feature = "op_put_suppressed_destination",
+    feature = "op_put_tenant_suppression_attributes",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email",
+    feature = "op_tag_resource",
+    feature = "op_test_render_email_template",
+    feature = "op_untag_resource",
+    feature = "op_update_configuration_set",
+    feature = "op_update_configuration_set_event_destination",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list",
+    feature = "op_update_custom_verification_email_template",
+    feature = "op_update_email_identity_policy",
+    feature = "op_update_email_template",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_too_many_requests_exception::TooManyRequestsExceptionBuilder;

+#[cfg(feature = "op_batch_get_metric_data")]
 pub use crate::types::error::_internal_service_error_exception::InternalServiceErrorExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_delete_configuration_set",
+    feature = "op_delete_contact_list",
+    feature = "op_delete_dedicated_ip_pool",
+    feature = "op_delete_email_identity",
+    feature = "op_delete_multi_region_endpoint",
+    feature = "op_put_dedicated_ip_pool_scaling_attributes",
+    feature = "op_tag_resource",
+    feature = "op_untag_resource",
+    feature = "op_update_contact",
+    feature = "op_update_contact_list"
+))]
 pub use crate::types::error::_concurrent_modification_exception::ConcurrentModificationExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_configuration_set",
+    feature = "op_create_configuration_set_event_destination",
+    feature = "op_create_contact_list",
+    feature = "op_create_custom_verification_email_template",
+    feature = "op_create_dedicated_ip_pool",
+    feature = "op_create_deliverability_test_report",
+    feature = "op_create_email_identity",
+    feature = "op_create_email_identity_policy",
+    feature = "op_create_email_template",
+    feature = "op_create_export_job",
+    feature = "op_create_import_job",
+    feature = "op_create_multi_region_endpoint",
+    feature = "op_create_tenant",
+    feature = "op_get_deliverability_dashboard_options",
+    feature = "op_put_deliverability_dashboard_option",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_limit_exceeded_exception::LimitExceededExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_account_suspended_exception::AccountSuspendedExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_mail_from_domain_not_verified_exception::MailFromDomainNotVerifiedExceptionBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_message_rejected::MessageRejectedBuilder;

+#[cfg(any(
+    feature = "op_create_deliverability_test_report",
+    feature = "op_send_bulk_email",
+    feature = "op_send_custom_verification_email",
+    feature = "op_send_email"
+))]
 pub use crate::types::error::_sending_paused_exception::SendingPausedExceptionBuilder;

+#[cfg(feature = "op_list_suppressed_destinations")]
 pub use crate::types::error::_invalid_next_token_exception::InvalidNextTokenExceptionBuilder;

+#[cfg(any(
+    feature = "op_put_account_details",
+    feature = "op_put_account_pricing_attributes",
+    feature = "op_update_reputation_entity_customer_managed_status",
+    feature = "op_update_reputation_entity_policy"
+))]
 pub use crate::types::error::_conflict_exception::ConflictExceptionBuilder;
```


## Customizations

- Add one non-default Cargo feature and matching cfg gates for each model operation.
- Derive the Cargo package/library names from the service key.
- Remove upstream `tests/` from generated output.

## Reproduction

```text
cargo run -p aws-sdk-modularizer -- --manifest services-manifest.json
```
